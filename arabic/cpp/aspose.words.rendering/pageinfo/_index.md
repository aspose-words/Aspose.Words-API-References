---
title: "فئة Aspose::Words::Rendering::PageInfo"
linktitle: "PageInfo"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Rendering::PageInfo. تمثل معلومات حول صفحة مستند معينة. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.rendering/pageinfo/
---
## PageInfo class


يمثل معلومات حول صفحة مستند معينة. لمعرفة المزيد، زر مقالة الوثائق [Rendering](https://docs.aspose.com/words/cpp/rendering/).

```cpp
class PageInfo : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Colored](./get_colored/)() | ترجع **true** إذا كانت الصفحة تحتوي على محتوى ملون. |
| [get_HeightInPoints](./get_heightinpoints/)() | يحصل على ارتفاع الصفحة بالنقاط. |
| [get_Landscape](./get_landscape/)() const | ترجع **true** إذا كان اتجاه الصفحة المحدد في المستند لهذه الصفحة هو أفقي. |
| [get_PaperSize](./get_papersize/)() | يحصل على حجم الورق كقائمة تعداد. |
| [get_PaperTray](./get_papertray/)() const | يحصل على صينية الورق (حاوية) لهذه الصفحة كما هو محدد في المستند. القيمة خاصة بالتنفيذ (الطابعة). |
| [get_SizeInPoints](./get_sizeinpoints/)() const | يحصل على حجم الصفحة بالنقاط. |
| [get_WidthInPoints](./get_widthinpoints/)() | يحصل على عرض الصفحة بالنقاط. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float) | يحسب حجم الصفحة بالبكسل لعامل تكبير ودقة محددين. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float, float) | يحسب حجم الصفحة بالبكسل لعامل تكبير ودقة محددين. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## ملاحظات


عرض وارتفاع الصفحة التي تُرجعها هذه الكائن تمثل الحجم "النهائي" للصفحة، أي أنها تم تدويرها بالفعل إلى الاتجاه الصحيح.

## انظر أيضًا

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
