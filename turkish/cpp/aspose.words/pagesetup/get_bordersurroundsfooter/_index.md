---
title: "Aspose::Words::PageSetup::get_BorderSurroundsFooter yöntemi"
linktitle: "get_BorderSurroundsFooter"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup::get_BorderSurroundsFooter yöntemi. Sayfa kenarlığının altbilgiyi içerip içermediğini C++'da belirtir."
type: docs
weight: 8000
url: /tr/cpp/aspose.words/pagesetup/get_bordersurroundsfooter/
---
## PageSetup::get_BorderSurroundsFooter method


Sayfa kenarlığının alt bilgiyi içerip içermediğini belirtir.

```cpp
bool Aspose::Words::PageSetup::get_BorderSurroundsFooter()
```


## Örnekler



Sayfaya ve üstbilgi/altbilgiye kenarlık uygulamanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world! This is the main body text.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer.");
builder->MoveToDocumentEnd();

// Mavi çift çizgili bir kenarlık ekleyin.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Double);
pageSetup->get_Borders()->set_Color(System::Drawing::Color::get_Blue());

// Bir bölümün PageSetup nesnesi, belirleyen "BorderSurroundsHeader" ve "BorderSurroundsFooter" bayraklarına sahiptir
// sayfa kenarlığının ana metni çevreleyip çevrelemediğini, ayrıca üstbilgi veya altbilgiyi sırasıyla içerip içermediğini.
// "BorderSurroundsHeader" bayrağını "true" olarak ayarlayarak üstbilgiyi kenarlığımızla çevreleyin,
// ve ardından "BorderSurroundsFooter" bayrağını ayarlayarak altbilgiyi kenarlığın dışına bırakın.
pageSetup->set_BorderSurroundsHeader(true);
pageSetup->set_BorderSurroundsFooter(false);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorder.docx");
```

## Ayrıca Bakınız

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
