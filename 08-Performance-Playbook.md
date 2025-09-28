# 08 — Performance Playbook (حسب المرحلة)

## Build
- `const` + تجزئة الواجهات + لا تحديث حالة داخل `build()`.

## Layout
- تقليل `Intrinsic*` والتداخلات؛ قياس أقل = أسرع.

## Paint/Compositing
- `RepaintBoundary` بحكمة.
- تجنّب `Opacity` على عناصر ضخمة متحركة؛ فضّل انتقالات compositor-friendly.

## Raster/Impeller
- راقب Raster Cache؛ اضبط أحجام الصور و`precacheImage` عند اللزوم.

## أدوات
- DevTools → Performance/Memory/Flutter frames.
- Performance Overlay: https://docs.flutter.dev/tools/devtools/performance#flutter-performance-overlay

## مراجع عامة
- Rendering best practices: https://docs.flutter.dev/perf/rendering/best-practices
- Performance docs hub: https://docs.flutter.dev/perf
