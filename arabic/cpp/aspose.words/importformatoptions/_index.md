---
title: "فئة Aspose::Words::ImportFormatOptions"
linktitle: "ImportFormatOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::ImportFormatOptions. يسمح بتحديد خيارات استيراد مختلفة لتنسيق المخرجات. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 35000
url: /ar/cpp/aspose.words/importformatoptions/
---
## ImportFormatOptions class


يسمح بتحديد خيارات استيراد مختلفة لتنسيق المخرجات. لمعرفة المزيد، زر مقالة الوثائق [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/)

```cpp
class ImportFormatOptions : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_AdjustSentenceAndWordSpacing](./get_adjustsentenceandwordspacing/)() const | يحصل أو يضبط قيمة منطقية تحدد ما إذا كان يجب تعديل تباعد الجمل والكلمات تلقائيًا. القيمة الافتراضية هي **false**. |
| [get_AppendDocumentWithNewPage](./get_appenddocumentwithnewpage/)() const | يحصل أو يضبط قيمة منطقية تشير إلى ما إذا كان يجب تغيير نوع القسم الأول المستورد إلى [NewPage](../sectionstart/) بالقوة عند استدعاء [AppendDocument()](../). القيمة الافتراضية هي **true**. |
| [get_ForceCopyStyles](./get_forcecopystyles/)() const | يحصل أو يضبط قيمة منطقية تشير إلى ما إذا كان يجب نسخ الأنماط المتضاربة في وضع [KeepSourceFormatting](../importformatmode/). القيمة الافتراضية هي **false**. |
| [get_IgnoreHeaderFooter](./get_ignoreheaderfooter/)() const | يحصل أو يضبط قيمة منطقية تحدد أن تنسيق المصدر لمحتوى رؤوس/تذييلات الصفحات يتم تجاهله إذا تم استخدام وضع [KeepSourceFormatting](../importformatmode/). القيمة الافتراضية هي **true**. |
| [get_IgnoreTextBoxes](./get_ignoretextboxes/)() const | يحصل أو يضبط قيمة منطقية تحدد أن تنسيق المصدر لمحتوى صناديق النص يتم تجاهله إذا تم استخدام وضع [KeepSourceFormatting](../importformatmode/). القيمة الافتراضية هي **true**. |
| [get_KeepSourceNumbering](./get_keepsourcenumbering/)() const | يحصل أو يضبط قيمة منطقية تحدد كيفية استيراد الترقيم عندما يتصادم في مستندات المصدر والوجهة. القيمة الافتراضية هي **false**. |
| [get_MergePastedLists](./get_mergepastedlists/)() const | يحصل أو يضبط قيمة منطقية تحدد ما إذا كانت القوائم الملصوقة ستدمج مع القوائم المحيطة. القيمة الافتراضية هي **false**. |
| [get_ResolveThemeColors](./get_resolvethemecolors/)() const | يحصل أو يضبط قيمة منطقية تحدد ما إذا كان يجب حل ألوان السمة للأشكال بالقوة. القيمة الافتراضية هي **false**. |
| [get_SmartStyleBehavior](./get_smartstylebehavior/)() const | يحصل أو يضبط قيمة منطقية تحدد كيفية استيراد الأنماط عندما تكون لها أسماء متساوية في مستندات المصدر والوجهة. القيمة الافتراضية هي **false**. |
| [GetType](./gettype/)() const override |  |
| [ImportFormatOptions](./importformatoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AdjustSentenceAndWordSpacing](./set_adjustsentenceandwordspacing/)(bool) | مُعيّن لـ [Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing](./get_adjustsentenceandwordspacing/). |
| [set_AppendDocumentWithNewPage](./set_appenddocumentwithnewpage/)(bool) | مُعيّن لـ [Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage](./get_appenddocumentwithnewpage/). |
| [set_ForceCopyStyles](./set_forcecopystyles/)(bool) | مُعيّن لـ [Aspose::Words::ImportFormatOptions::get_ForceCopyStyles](./get_forcecopystyles/). |
| [set_IgnoreHeaderFooter](./set_ignoreheaderfooter/)(bool) | مُعيّن لـ [Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter](./get_ignoreheaderfooter/). |
| [set_IgnoreTextBoxes](./set_ignoretextboxes/)(bool) | مُعيّن لـ [Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes](./get_ignoretextboxes/). |
| [set_KeepSourceNumbering](./set_keepsourcenumbering/)(bool) | مُعيّن لـ [Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering](./get_keepsourcenumbering/). |
| [set_MergePastedLists](./set_mergepastedlists/)(bool) | مُعيّن لـ [Aspose::Words::ImportFormatOptions::get_MergePastedLists](./get_mergepastedlists/). |
| [set_ResolveThemeColors](./set_resolvethemecolors/)(bool) | مُعيّن لـ [Aspose::Words::ImportFormatOptions::get_ResolveThemeColors](./get_resolvethemecolors/). |
| [set_SmartStyleBehavior](./set_smartstylebehavior/)(bool) | المُعيّن لـ [Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior](./get_smartstylebehavior/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
