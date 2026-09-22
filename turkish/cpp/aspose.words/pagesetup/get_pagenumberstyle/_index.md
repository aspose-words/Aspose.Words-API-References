---
title: "Aspose::Words::PageSetup::get_PageNumberStyle metodu"
linktitle: "get_PageNumberStyle"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup::get_PageNumberStyle metodu. C++'ta sayfa numarası biçimini alır veya ayarlar."
type: docs
weight: 34000
url: /tr/cpp/aspose.words/pagesetup/get_pagenumberstyle/
---
## PageSetup::get_PageNumberStyle method


Sayfa numarası biçimini alır veya ayarlar.

```cpp
Aspose::Words::NumberStyle Aspose::Words::PageSetup::get_PageNumberStyle()
```


## Örnekler



Bir bölümde sayfa numaralandırmasını nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Section 1, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 3.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"Section 2, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 3.");

// Belge oluşturucuyu ilk bölümün birincil üstbilgi kısmına taşıyın,
// bu bölümdeki her sayfa bunu görüntüleyecek.
builder->MoveToSection(0);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);

// Bir PAGE alanı ekleyin, bu alan geçerli sayfanın numarasını gösterecektir.
builder->Write(u"Page ");
builder->InsertField(u"PAGE", u"");

// Bölümü, PAGE alanlarının gösterdiği sayfa sayısının 5'ten başlaması için yapılandırın.
// Ayrıca, tüm PAGE alanlarını sayfa numaralarını büyük harf Roma rakamlarıyla göstermeleri için yapılandırın.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageStartingNumber(5);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);

// İkinci bölüm için başka bir birincil üstbilgi oluşturun, içinde başka bir PAGE alanı olsun.
builder->MoveToSection(1);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u" - ");
builder->InsertField(u"PAGE", u"");
builder->Write(u" - ");

// Bölümü, PAGE alanlarının gösterdiği sayfa sayısının 10'dan başlaması için yapılandırın.
// Ayrıca, tüm PAGE alanlarını sayfa numaralarını Arap rakamlarıyla göstermeleri için yapılandırın.
pageSetup = doc->get_Sections()->idx_get(1)->get_PageSetup();
pageSetup->set_PageStartingNumber(10);
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::Arabic);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageNumbering.docx");
```

## Ayrıca Bakınız

* Enum [NumberStyle](../../numberstyle/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
