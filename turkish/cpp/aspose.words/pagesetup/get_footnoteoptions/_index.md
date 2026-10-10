---
title: "Aspose::Words::PageSetup::get_FootnoteOptions metodu"
linktitle: "get_FootnoteOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup::get_FootnoteOptions metodu. C++'ta bu bölümde dipnotların numaralandırmasını ve konumlandırmasını kontrol eden seçenekler sağlar."
type: docs
weight: 17000
url: /tr/cpp/aspose.words/pagesetup/get_footnoteoptions/
---
## PageSetup::get_FootnoteOptions method


Bu bölümde dipnotların numaralandırmasını ve konumlandırmasını kontrol eden seçenekler sağlar.

```cpp
System::SharedPtr<Aspose::Words::Notes::FootnoteOptions> Aspose::Words::PageSetup::get_FootnoteOptions()
```


## Örnekler



Bir bölümde dipnotları/son notları etkileyen seçeneklerin nasıl yapılandırılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote reference text.");

// İlk bölümdeki tüm dipnotların numaralandırmasını 1'den yeniden başlatacak şekilde yapılandırın
// her yeni sayfada ve her sayfada metnin hemen altında kendilerini gösterecek şekilde.
System::SharedPtr<Aspose::Words::Notes::FootnoteOptions> footnoteOptions = doc->get_Sections()->idx_get(0)->get_PageSetup()->get_FootnoteOptions();
footnoteOptions->set_Position(Aspose::Words::Notes::FootnotePosition::BeneathText);
footnoteOptions->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartPage);
footnoteOptions->set_StartNumber(1);

builder->Write(u" Hello again.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Endnote reference text.");

// İlk bölümdeki tüm son notların bölüm boyunca sürekli bir sayım sürdürmesi için yapılandırın,
// 1'den başlayarak. Ayrıca, hepsinin belge sonunda toplanmış olarak görünmesini ayarlayın.
System::SharedPtr<Aspose::Words::Notes::EndnoteOptions> endnoteOptions = doc->get_Sections()->idx_get(0)->get_PageSetup()->get_EndnoteOptions();
endnoteOptions->set_Position(Aspose::Words::Notes::EndnotePosition::EndOfDocument);
endnoteOptions->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::Continuous);
endnoteOptions->set_StartNumber(1);

doc->Save(get_ArtifactsDir() + u"PageSetup.FootnoteOptions.docx");
```

## Ayrıca Bakınız

* Class [FootnoteOptions](../../../aspose.words.notes/footnoteoptions/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
