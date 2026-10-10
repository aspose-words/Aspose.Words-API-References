---
title: "طريقة Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior"
linktitle: "get_SmartStyleBehavior"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior. يحصل على أو يعيّن قيمة منطقية تحدد كيفية استيراد الأنماط عندما يكون لها أسماء متساوية في المستندات المصدر والوجهة. القيمة الافتراضية هي false في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words/importformatoptions/get_smartstylebehavior/
---
## ImportFormatOptions::get_SmartStyleBehavior method


يحصل أو يضبط قيمة منطقية تحدد كيفية استيراد الأنماط عندما تكون لها أسماء متساوية في مستندات المصدر والوجهة. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior() const
```

## ملاحظات


عند تفعيل هذا الخيار **enabled**, سيتم توسيع النمط المصدر إلى سمات مباشرة داخل مستند الوجهة، إذا تم استخدام وضع الاستيراد [KeepSourceFormatting](../../importformatmode/).

عند تعطيل هذا الخيار **disabled**, سيتم توسيع النمط المصدر فقط إذا كان مرقمًا. لن يتم استبدال السمات الموجودة في الوجهة، بما في ذلك القوائم.

## أمثلة



يظهر كيفية حل الأنماط المكررة أثناء إدراج المستندات.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);

System::SharedPtr<Aspose::Words::Style> myStyle = builder->get_Document()->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
myStyle->get_Font()->set_Size(14);
myStyle->get_Font()->set_Name(u"Courier New");
myStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

builder->get_ParagraphFormat()->set_StyleName(myStyle->get_Name());
builder->Writeln(u"Hello world!");

// استنسخ المستند وقم بتحرير نمط \"MyStyle\" للنسخة المستنسخة، بحيث يكون بلون مختلف عن اللون الأصلي.
// إذا أدخلنا النسخة المستنسخة في المستند الأصلي، فإن النمطين ذي الاسم نفسه سيتسببان في تعارض.
System::SharedPtr<Aspose::Words::Document> srcDoc = dstDoc->Clone();
srcDoc->get_Styles()->idx_get(u"MyStyle")->get_Font()->set_Color(System::Drawing::Color::get_Red());

// عند تمكين SmartStyleBehavior واستخدام وضع استيراد KeepSourceFormatting،
// ستقوم Aspose.Words بحل تعارض الأنماط عن طريق تحويل أنماط المستند المصدر.
// مع نفس الأسماء كأنماط الوجهة إلى سمات الفقرة المباشرة.
auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_SmartStyleBehavior(true);

builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.SmartStyleBehavior.docx");
```

## انظر أيضًا

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
