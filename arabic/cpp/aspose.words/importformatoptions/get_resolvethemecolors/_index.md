---
title: "طريقة Aspose::Words::ImportFormatOptions::get_ResolveThemeColors"
linktitle: "get_ResolveThemeColors"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::ImportFormatOptions::get_ResolveThemeColors. يحصل أو يضبط قيمة منطقية تحدد ما إذا كان يجب حل ألوان السمة للأشكال بالقوة. القيمة الافتراضية هي false في C++."
type: docs
weight: 8500
url: /ar/cpp/aspose.words/importformatoptions/get_resolvethemecolors/
---
## ImportFormatOptions::get_ResolveThemeColors method


يحصل أو يضبط قيمة منطقية تحدد ما إذا كان يجب حل ألوان السمة للأشكال بالقوة. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_ResolveThemeColors() const
```

## ملاحظات


يرجى ملاحظة أن هذا الخيار ذو صلة فقط بوضع [KeepSourceFormatting](../../importformatmode/).

عادةً، لا يقوم Aspose.Words بحل ألوان سمة المصدر عند استيراد الأنماط التي يمكن الحفاظ عليها دون توسيع سمات التنسيق إلى سمات مباشرة. ومع ذلك، في هذه الحالة قد تختلف الألوان الفعلية للأشكال المستوردة عن تلك التي كانت في المستند الأصلي. السبب في ذلك هو اختلاف ألوان السمة بين مستندات المصدر والوجهة. ضبط هذا الخيار إلى **true** يجبر على حل ألوان سمة الشكل المصدر وبالتالي الحفاظ على اللون الفعلي للأشكال كما هو في مستند المصدر.

## أمثلة



يوضح كيفية استيراد عقدة مع حل ألوان سمة المصدر للأشكال.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

// انتقل إلى التذييل الأساسي وأدرج شكلاً يستخدم ألوان السمة.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 50);
shape->get_Stroke()->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
// استورد تذييل المصدر إلى المستند الوجهة مع حل ألوان السمة،
// بحيث يحتفظ الشكل لونه الفعلي من المستند المصدر.
System::SharedPtr<Aspose::Words::HeaderFooter> footer = srcDoc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ResolveThemeColors(true);
auto importedFooter = System::ExplicitCast<Aspose::Words::HeaderFooter>(dstDoc->ImportNode(footer, true, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options));

dstDoc->get_FirstSection()->get_HeadersFooters()->Add(importedFooter);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBase.ImportNodeWithResolveThemeColors.docx");
```

## انظر أيضًا

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
