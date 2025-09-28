# 07 — Threads & Frame Timeline

```
UI Thread (Dart): build → layout → paint → build Scene
Raster Thread    : rasterize(scene) → pixels
IO/Decode        : تحميل الصور/الخطوط
```

- أي عمل ثقيل على UI thread يؤدي إلى jank.
- استخدم Isolates للمهام الثقيلة، وخفف حسابات build/layout.

## مراجع
- Frame rendering timeline: https://github.com/flutter/flutter/wiki/Understanding-Flutter-Frame-Rendering
- DevTools Performance: https://docs.flutter.dev/tools/devtools/performance
- Isolates: https://api.dart.dev/stable/dart-isolate/dart-isolate-library.html
