---
title: "طريقة Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags"
linktitle: "get_IgnoreStructuredDocumentTags"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags. يحصل على أو يضبط قيمة منطقية تشير إلى ما إذا كان يجب تجاهل محتوى StructuredDocumentTag. القيمة الافتراضية هي false في C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words.replacing/findreplaceoptions/get_ignorestructureddocumenttags/
---
## FindReplaceOptions::get_IgnoreStructuredDocumentTags method


يحصل على أو يضبط قيمة منطقية تشير إلى ما إذا كان يجب تجاهل محتوى [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/). القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags() const
```

## ملاحظات


عند ضبط هذا الخيار على **true**، سيتم التعامل مع محتوى [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) كنص بسيط.

إلا، سيتم معالجة [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) كقصة مستقلة [Story](../../../aspose.words/story/) وسيتم البحث عن نمط الاستبدال بشكل منفصل لكل [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)، بحيث إذا كان النمط يعبر [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)، فلن يتم تنفيذ الاستبدال لهذا النمط.

## أمثلة



يوضح كيفية تجاهل محتوى العلامات أثناء الاستبدال.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// هذه الفقرة تحتوي على SDT.
auto p = System::ExplicitCast<Aspose::Words::Paragraph>(doc->get_FirstSection()->get_Body()->GetChild(Aspose::Words::NodeType::Paragraph, 2, true));
System::String textToSearch = p->ToString(Aspose::Words::SaveFormat::Text).Trim();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreStructuredDocumentTags(true);
doc->get_Range()->Replace(textToSearch, u"replacement", options);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
```

## انظر أيضًا

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
