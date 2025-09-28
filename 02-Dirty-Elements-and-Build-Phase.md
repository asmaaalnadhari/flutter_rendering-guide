# 02 — Dirty Elements & Build Phase

## لماذا "Dirty"؟
- `setState()` أو `Element.markNeedsBuild()` يوسم الـElement كـ dirty لإعادة البناء في الإطار القادم.

## كيف تُبنى؟
- `BuildOwner.buildScope()` يعيد بناء جميع العناصر dirty في نطاق واحد، ويطابق widgets الجديدة مع elements الموجودة (إعادة استخدام حيث أمكن).

## مثال
```dart
class Counter extends StatefulWidget { /* ... */ }
class _CounterState extends State<Counter> {
  int value = 0;
  void inc() => setState(() => value++); // يوسم العنصر dirty
  @override
  Widget build(BuildContext c) => Text('$value');
}
```

## تحسين الأداء
- استخدم `const` وقسّم الواجهات الكبيرة إلى Widgets أصغر.

## مراجع
- Element.markNeedsBuild/dirty: https://api.flutter.dev/flutter/widgets/Element/markNeedsBuild.html
- BuildOwner.buildScope: https://api.flutter.dev/flutter/widgets/BuildOwner/buildScope.html
