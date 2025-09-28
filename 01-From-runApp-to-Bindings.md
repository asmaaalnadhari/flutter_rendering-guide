# 01 — From runApp() to Bindings

## المسار العام
App code → runApp(MyApp) → WidgetsFlutterBinding (ensure/init)
→ attachRootWidget() → root Element → first build scope
→ SchedulerBinding (vsync) → onBeginFrame/onDrawFrame

### ماذا يحدث؟
1) **تهيئة الـBindings**: `WidgetsFlutterBinding` يجمع Mixins عدّة (`SchedulerBinding` + `RendererBinding` + …).
2) **زرع الجذر**: `attachRootWidget` يزرع جذر شجرة الـElements المرتبط بـ RenderView.
3) **دورة الإطار**: مع كل vsync: `onBeginFrame` ثم `onDrawFrame`؛ ثم build → layout → paint → compositing → raster.

## روابط مرجعية
- WidgetsBinding: https://api.flutter.dev/flutter/widgets/WidgetsBinding-class.html
- SchedulerBinding (onBeginFrame/onDrawFrame): https://api.flutter.dev/flutter/scheduler/SchedulerBinding-mixin.html
- Life of a Flutter Frame (flutter/engine wiki): https://github.com/flutter/flutter/wiki/Understanding-Flutter-Frame-Rendering
