---
title: "Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter yöntemi"
linktitle: "get_OddAndEvenPagesHeaderFooter"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter yöntemi. C++'ta belge tek sayılı ve çift sayılı sayfalar için farklı üstbilgi ve altbilgi içeriyorsa doğru."
type: docs
weight: 30000
url: /tr/cpp/aspose.words/pagesetup/get_oddandevenpagesheaderfooter/
---
## PageSetup::get_OddAndEvenPagesHeaderFooter method


Belgenin tek ve çift numaralı sayfalar için farklı üst ve alt bilgilere sahip olması durumunda doğru.

```cpp
bool Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter() const
```


## Örnekler



Çift sayfa üstbilgi/altbilgilerini nasıl etkinleştireceğinizi veya devre dışı bırakacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aşağıda iki tür üstbilgi/altbilgi bulunmaktadır.
// 1 -  "Primary" üstbilgi/altbilgi, bölümdeki her sayfada görünür.
// İlk ve çift sayfa üstbilgi/altbilgisiyle birincil üstbilgi/altbilgiyi geçersiz kılabiliriz.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Primary header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"Primary footer.");

// 2 -  "Even" üstbilgi/altbilgi, bu bölümün her çift sayfasında görünür.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderEven);
builder->Writeln(u"Even page header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterEven);
builder->Writeln(u"Even page footer.");

builder->MoveToSection(0);
builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Her bölüm, sayfa görünümüyle ilgili özellikleri belirten bir "PageSetup" nesnesine sahiptir
// örneğin yönlendirme, boyut ve kenarlıklar.
// "OddAndEvenPagesHeaderFooter" özelliğini "true" olarak ayarlayın
// çift sayfa üstbilgi/altbilgisini çift sayfalarda göstermek için.
// "OddAndEvenPagesHeaderFooter" özelliğini "false" olarak ayarlayın
// çift sayfalarda birincil üstbilgi/altbilgiyi göstermek için.
builder->get_PageSetup()->set_OddAndEvenPagesHeaderFooter(oddAndEvenPagesHeaderFooter);

doc->Save(get_ArtifactsDir() + u"PageSetup.OddAndEvenPagesHeaderFooter.docx");
```

## Ayrıca Bakınız

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
