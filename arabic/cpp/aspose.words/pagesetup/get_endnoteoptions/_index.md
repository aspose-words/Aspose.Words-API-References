---
title: "طريقة Aspose::Words::PageSetup::get_EndnoteOptions"
linktitle: "get_EndnoteOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::PageSetup::get_EndnoteOptions. يوفر خيارات تتحكم في ترقيم وتحديد موضع الهوامش الختامية في هذا القسم في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words/pagesetup/get_endnoteoptions/
---
## PageSetup::get_EndnoteOptions method


يوفر خيارات تتحكم في ترقيم وتحديد موضع الحواشي السفلية في هذا القسم.

```cpp
System::SharedPtr<Aspose::Words::Notes::EndnoteOptions> Aspose::Words::PageSetup::get_EndnoteOptions()
```


## أمثلة



يعرض كيفية تكوين الخيارات التي تؤثر على الحواشي السفلية/الختامية في قسم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote reference text.");

// قم بتكوين جميع الحواشي السفلية في القسم الأول لإعادة بدء الترقيم من 1
// في كل صفحة جديدة وعرضها مباشرةً أسفل النص في كل صفحة.
System::SharedPtr<Aspose::Words::Notes::FootnoteOptions> footnoteOptions = doc->get_Sections()->idx_get(0)->get_PageSetup()->get_FootnoteOptions();
footnoteOptions->set_Position(Aspose::Words::Notes::FootnotePosition::BeneathText);
footnoteOptions->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartPage);
footnoteOptions->set_StartNumber(1);

builder->Write(u" Hello again.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Endnote reference text.");

// قم بتكوين جميع الهوامش الختامية في القسم الأول للحفاظ على عدّ مستمر طوال القسم،
// بدءًا من 1. أيضًا، اضبطهم جميعًا لتظهر مجمَّعة في نهاية المستند.
System::SharedPtr<Aspose::Words::Notes::EndnoteOptions> endnoteOptions = doc->get_Sections()->idx_get(0)->get_PageSetup()->get_EndnoteOptions();
endnoteOptions->set_Position(Aspose::Words::Notes::EndnotePosition::EndOfDocument);
endnoteOptions->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::Continuous);
endnoteOptions->set_StartNumber(1);

doc->Save(get_ArtifactsDir() + u"PageSetup.FootnoteOptions.docx");
```

## انظر أيضًا

* Class [EndnoteOptions](../../../aspose.words.notes/endnoteoptions/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
