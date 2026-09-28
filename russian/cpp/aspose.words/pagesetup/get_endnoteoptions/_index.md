---
title: "Aspose::Words::PageSetup::get_EndnoteOptions метод"
linktitle: "get_EndnoteOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::PageSetup::get_EndnoteOptions метод. Предоставляет параметры, управляющие нумерацией и расположением концевых сносок в этом разделе в C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words/pagesetup/get_endnoteoptions/
---
## PageSetup::get_EndnoteOptions method


Предоставляет параметры, которые управляют нумерацией и расположением концевых сносок в этом разделе.

```cpp
System::SharedPtr<Aspose::Words::Notes::EndnoteOptions> Aspose::Words::PageSetup::get_EndnoteOptions()
```


## Примеры



Показывает, как настроить параметры, влияющие на сноски/концевые сноски в разделе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote reference text.");

// Настройте все сноски в первом разделе так, чтобы нумерация начиналась с 1
// на каждой новой странице и отображаются непосредственно под текстом на каждой странице.
System::SharedPtr<Aspose::Words::Notes::FootnoteOptions> footnoteOptions = doc->get_Sections()->idx_get(0)->get_PageSetup()->get_FootnoteOptions();
footnoteOptions->set_Position(Aspose::Words::Notes::FootnotePosition::BeneathText);
footnoteOptions->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartPage);
footnoteOptions->set_StartNumber(1);

builder->Write(u" Hello again.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Endnote reference text.");

// Настройте все концевые сноски в первом разделе так, чтобы сохранялся непрерывный счет по всему разделу,
// начиная с 1. Также установите их все так, чтобы они отображались собранными в конце документа.
System::SharedPtr<Aspose::Words::Notes::EndnoteOptions> endnoteOptions = doc->get_Sections()->idx_get(0)->get_PageSetup()->get_EndnoteOptions();
endnoteOptions->set_Position(Aspose::Words::Notes::EndnotePosition::EndOfDocument);
endnoteOptions->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::Continuous);
endnoteOptions->set_StartNumber(1);

doc->Save(get_ArtifactsDir() + u"PageSetup.FootnoteOptions.docx");
```

## См. также

* Class [EndnoteOptions](../../../aspose.words.notes/endnoteoptions/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
