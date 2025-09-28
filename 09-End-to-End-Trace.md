# 09 — End‑to‑End Trace (من النقر للبكسلات)

## سيناريو: المستخدم يضغط زر "Like"
1) Tap → `setState` → `Element.markNeedsBuild()` (dirty)

2) الإطار التالي (`WidgetsBinding.drawFrame`):

   - BuildOwner.buildScope() → يعيد بناء subtree الخاص بالزر فقط

   - RendererBinding.flushLayout() → يعيد القياس إن لزم

   - RendererBinding.flushCompositingBits() → يحدّث معلومات الطبقات

   - RendererBinding.flushPaint() → يسجّل الأوامر إلى Pictures

   - SceneBuilder يبني `Scene` → `FlutterView.render(Scene)`

3) Raster thread (Impeller) يحوّل المشهد إلى بكسلات

4) النتيجة: انتقال/تلوين سلس عند 60/120fps


## نقاط تحسين مرتبطة

- صمّم الشجرة بمكوّنات صغيرة لتقليل إعادة البناء.

- فضّل انتقالات compositor-friendly.

- راقب DevTools لتحديد ما إذا كان التأخير على UI أم Raster.


## مراجع

- drawFrame/Bindings: https://api.flutter.dev/flutter/widgets/WidgetsBinding/drawFrame.html

- Rendering pipeline overview: https://docs.flutter.dev/resources/architectural-overview
