# 03 — Layout: Constraints → Size → Position

## نموذج القيود الصندوقي
- Parent يمرّر `BoxConstraints` → child يحسب حجمَه عبر `performLayout()` → ثم parent يضعه.

## أين يحدث ذلك؟
- داخل `RenderObject` (غالبًا `RenderBox`) وتدار عبر `PipelineOwner.flushLayout()`.

## تحسين الأداء
- تجنّب القياسات المتداخلة المكلفة (`Intrinsic*`).
- راقب تبويب Layout في DevTools.

## مراجع
- RenderBox: https://api.flutter.dev/flutter/rendering/RenderBox-class.html
- PipelineOwner.flushLayout: https://api.flutter.dev/flutter/rendering/PipelineOwner/flushLayout.html
- Performance best practices (Layout): https://docs.flutter.dev/perf/rendering/best-practices
