# 05 — Layer Tree, Compositing & SceneBuilder

## لماذا طبقات؟
- `TransformLayer`, `OpacityLayer`, `Clip*Layer` تسمح بتحريك أجزاء كاملة دون إعادة تسجيل الرسم.

## من الطبقات إلى المشهد
- `RenderView.compositeFrame()` يبني `Scene` بواسطة `SceneBuilder`, ثم `FlutterView.render(scene)`.

## تحسين الأداء
- تجنّب `Opacity` على عناصر كبيرة متحركة؛ استخدم `AnimatedOpacity`/`FadeTransition` أو رسوم مركّبة (translate/scale).

## مراجع
- SceneBuilder (dart:ui): https://api.flutter.dev/flutter/dart-ui/SceneBuilder-class.html
- Opacity caveats: https://docs.flutter.dev/perf/rendering/best-practices#avoid-opacity-unless-necessary
- Compositing: https://docs.flutter.dev/perf/rendering
