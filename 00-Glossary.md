# 00 — Glossary (المعجم السريع)

- **Widget**: وصف declarative للشكل/السلوك؛ غير قابل للتغيير.
- **Element**: الجسر الحيّ بين الـWidget والتنفيذ؛ يدير دورة الحياة ويحدد متى يُعاد `build()`.
- **RenderObject / RenderBox**: طبقة التنفيذ الرسومي: layout/paint/hit-test.
- **Binding**: المُنسّق العام لدورة الإطار (Widgets/Scheduler/Renderer).
- **Dirty Element**: عنصر موسوم لإعادة البناء في الإطار القادم (بعد `setState()` أو `markNeedsBuild()`).
- **Pictures**: سجلات أوامر رسم متجهية، تُركَّب لاحقًا في مشهد.
- **Layer Tree**: طبقات مركّبة (`Transform/Opacity/Clip…`) لإعادة الاستخدام والحركة دون إعادة الرسم.
- **Scene / SceneBuilder**: تمثيل المشهد النهائي قبل تسليمه للمحرّك.
- **Rasterization**: تحويل المشهد إلى بكسلات (Impeller/Skia).

## مصادر موثوقة
- Flutter Architectural Overview: https://docs.flutter.dev/resources/architectural-overview
- Inside Flutter (widgets/elements/render objects): https://docs.flutter.dev/resources/inside-flutter
