# 06 — Rasterization: Impeller & Skia

## ما الذي يحدث؟
- يأخذ المحرّك الـScene ويحوّلها إلى بكسلات على خيط الرستر.
- Impeller (افتراضي على iOS، ومفعّل افتراضيًا على Android API 29+ في الإصدارات الحديثة) يسبق تجميع الشادر لتقليل jank.

## Raster Cache
- قد يحوّل المحرّك رسومات معقّدة وثابتة إلى texture لإعادة الاستخدام لاحقًا.

## تحسين الأداء
- لا تعتمد على الكاش لعناصر ضخمة تتغير رسومها كل إطار؛ راقب Memory/Raster Cache في DevTools.

## مراجع
- Impeller overview: https://docs.flutter.dev/perf/impeller
- Engine wiki (Impeller): https://github.com/flutter/engine/wiki/Impeller
- DevTools (memory/raster cache): https://docs.flutter.dev/tools/devtools/memory
