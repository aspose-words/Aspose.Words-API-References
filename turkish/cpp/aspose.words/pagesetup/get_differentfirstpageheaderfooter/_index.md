---
title: "Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter yöntemi"
linktitle: "get_DifferentFirstPageHeaderFooter"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter yöntemi. C++'ta ilk sayfada farklı bir üstbilgi veya altbilgi kullanılıyorsa doğru döner."
type: docs
weight: 13000
url: /tr/cpp/aspose.words/pagesetup/get_differentfirstpageheaderfooter/
---
## PageSetup::get_DifferentFirstPageHeaderFooter method


İlk sayfada farklı bir üst bilgi veya alt bilgi kullanılıyorsa doğru.

```cpp
bool Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter()
```


## Örnekler



Birincil üstbilgi/altbilgileri nasıl etkinleştirip devre dışı bırakacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aşağıda iki tür üstbilgi/altbilgi bulunmaktadır.
// 1 -  \"First\" üstbilgi/altbilgi, bölümün ilk sayfasında görünür.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderFirst);
builder->Writeln(u"First page header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterFirst);
builder->Writeln(u"First page footer.");

// 2 -  \"Primary\" üstbilgi/altbilgi, bölümdeki her sayfada görünür.
// İlk ve çift sayfa üstbilgi/altbilgisiyle birincil üstbilgi/altbilgiyi geçersiz kılabiliriz.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Primary header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"Primary footer.");

builder->MoveToSection(0);
builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Her bölüm, sayfa görünümüyle ilgili özellikleri belirten bir "PageSetup" nesnesine sahiptir
// örneğin yönlendirme, boyut ve kenarlıklar.
// \"DifferentFirstPageHeaderFooter\" özelliğini \"true\" olarak ayarlayın, böylece ilk üstbilgi/altbilgi ilk sayfaya uygulanır.
// \"DifferentFirstPageHeaderFooter\" özelliğini \"false\" olarak ayarlayın
// ilk sayfanın birincil üstbilgi/altbilgi göstermesi için.
builder->get_PageSetup()->set_DifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);

doc->Save(get_ArtifactsDir() + u"PageSetup.DifferentFirstPageHeaderFooter.docx");
```

## Ayrıca Bakınız

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
