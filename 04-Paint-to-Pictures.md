# 04 — Paint: From RenderObjects to Pictures

## ماذا يحدث؟
- `paint(Canvas)` يسجل أوامر الرسم (متجهية) داخل `Picture`، وليس بكسلات بعد.

## أين يُدار؟
- عبر `PipelineOwner.flushPaint()` بعد إنهاء Layout.

## تحسين الأداء
- اجعل `CustomPainter.shouldRepaint` دقيقًا.
- استخدم `RepaintBoundary` بحكمة لتقليل انتشار إعادة الرسم.

## مراجع
- PipelineOwner.flushPaint: https://api.flutter.dev/flutter/rendering/PipelineOwner/flushPaint.html
- CustomPainter: https://api.flutter.dev/flutter/rendering/CustomPainter-class.html
- Rendering performance: https://docs.flutter.dev/perf/rendering
