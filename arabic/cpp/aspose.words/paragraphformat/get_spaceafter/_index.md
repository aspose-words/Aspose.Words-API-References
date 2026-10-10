---
title: "Aspose::Words::ParagraphFormat::get_SpaceAfter طريقة"
linktitle: "get_SpaceAfter"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ParagraphFormat::get_SpaceAfter طريقة. يحصل أو يضبط مقدار التباعد (بالنقاط) بعد الفقرة في C++."
type: docs
weight: 31000
url: /ar/cpp/aspose.words/paragraphformat/get_spaceafter/
---
## ParagraphFormat::get_SpaceAfter method


يحصل أو يعيّن مقدار المسافة (بالنقاط) بعد الفقرة.

```cpp
double Aspose::Words::ParagraphFormat::get_SpaceAfter()
```

## ملاحظات


ليس له أي تأثير عندما يكون [SpaceAfterAuto](../get_spaceafterauto/) **true**.

القيم الصالحة تتراوح من 0 إلى 1584 شاملًا.

## أمثلة



يظهر كيفية ضبط التباعد التلقائي للفقرات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// تطبيق كمية كبيرة من المسافة قبل وبعد الفقرات التي سيُنشئها هذا المُنشئ.
builder->get_ParagraphFormat()->set_SpaceBefore(24);
builder->get_ParagraphFormat()->set_SpaceAfter(24);

// اضبط هذه العلامات إلى "true" لتطبيق التباعد التلقائي،
// مع تجاهل التباعد في الخصائص التي ضبطناها أعلاه بفعالية.
// تركها كـ "false" سيطبق التباعد المخصص للفقرات.
builder->get_ParagraphFormat()->set_SpaceAfterAuto(autoSpacing);
builder->get_ParagraphFormat()->set_SpaceBeforeAuto(autoSpacing);

// أدرج فقرتين سيكون لهما تباعد فوق وتحتهما واحفظ المستند.
builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphSpacingAuto.docx");
```


يوضح كيفية تطبيق عدم وجود مسافة بين الفقرات ذات النمط نفسه.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// تطبيق كمية كبيرة من المسافة قبل وبعد الفقرات التي سيُنشئها هذا المُنشئ.
builder->get_ParagraphFormat()->set_SpaceBefore(24);
builder->get_ParagraphFormat()->set_SpaceAfter(24);

// اضبط علامة "NoSpaceBetweenParagraphsOfSameStyle" إلى "true" لتطبيق
// عدم وجود مسافة بين الفقرات ذات النمط نفسه، مما سيُجَمّع الفقرات المتشابهة.
// اترك علامة "NoSpaceBetweenParagraphsOfSameStyle" كـ "false"
// لتطبيق المسافة بشكل متساوٍ على كل فقرة.
builder->get_ParagraphFormat()->set_NoSpaceBetweenParagraphsOfSameStyle(noSpaceBetweenParagraphsOfSameStyle);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Quote"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphSpacingSameStyle.docx");
```

## انظر أيضًا

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
