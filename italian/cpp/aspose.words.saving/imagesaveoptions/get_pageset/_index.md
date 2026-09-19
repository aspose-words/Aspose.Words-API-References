---
title: "Aspose::Words::Saving::ImageSaveOptions::get_PageSet metodo"
linktitle: "get_PageSet"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_PageSet metodo. Ottiene o imposta le pagine da renderizzare. Il valore predefinito è tutte le pagine del documento in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.saving/imagesaveoptions/get_pageset/
---
## ImageSaveOptions::get_PageSet method


Ottiene o imposta le pagine da renderizzare. Il valore predefinito è tutte le pagine del documento.

```cpp
System::SharedPtr<Aspose::Words::Saving::PageSet> Aspose::Words::Saving::ImageSaveOptions::get_PageSet()
```

## Note


Questa proprietà ha effetto solo durante il rendering delle pagine del documento. Questa proprietà è ignorata quando si renderizzano forme in immagini.

## Esempi



Mostra come rendere una pagina da un documento in un'immagine JPEG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo rende il documento in un'immagine.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Imposta "PageSet" a "1" per selezionare la seconda pagina tramite
// l'indice basato su zero da cui iniziare a rendere il documento.
options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(1));

// Quando salviamo il documento nel formato JPEG, Aspose.Words rende solo una pagina.
// Questa immagine conterrà una pagina a partire dalla pagina due,
// che sarà semplicemente la seconda pagina del documento originale.
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.OnePage.jpg", options);
```


Mostra come specificare quale pagina di un documento renderizzare come immagine.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world! This is page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"This is page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"This is page 3.");

ASSERT_EQ(3, doc->get_PageCount());

// Quando salviamo il documento come immagine, Aspose.Words renderizza solo la prima pagina per impostazione predefinita.
// Possiamo passare un oggetto SaveOptions per specificare una pagina diversa da renderizzare.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Gif);
// Renderizza ogni pagina del documento in un file immagine separato.
for (int32_t i = 1; i <= doc->get_PageCount(); i++)
{
    saveOptions->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(1));

    doc->Save(get_ArtifactsDir() + System::String::Format(u"ImageSaveOptions.PageIndex.Page {0}.gif", i), saveOptions);
}
```


Mostra come rendere ogni pagina di un documento in un'immagine TIFF separata.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo rende il documento in un'immagine.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);

for (int32_t i = 0; i < doc->get_PageCount(); i++)
{
    // Imposta la proprietà "PageSet" al numero della prima pagina da
    // da cui iniziare a renderizzare il documento.
    options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(i));
    // Esporta la pagina a 2325x5325 pixel e 600 dpi.
    options->set_Resolution(600.0f);
    options->set_ImageSize(System::Drawing::Size(2325, 5325));

    doc->Save(get_ArtifactsDir() + System::String::Format(u"ImageSaveOptions.PageByPage.{0}.tiff", i + 1), options);
}
```


Mostra come estrarre pagine basate su intervalli di pagine esatti.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
auto pageSet = System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<System::SharedPtr<Aspose::Words::Saving::PageRange>>({System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 4), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1)}));

imageOptions->set_PageSet(pageSet);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

## Vedi anche

* Class [PageSet](../../pageset/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
