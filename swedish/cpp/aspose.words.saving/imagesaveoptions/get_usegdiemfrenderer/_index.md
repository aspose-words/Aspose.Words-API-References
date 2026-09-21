---
title: "Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer metod"
linktitle: "get_UseGdiEmfRenderer"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer metod. Hämtar eller anger ett värde som bestämmer om GDI+ eller Aspose.Words metafilrenderare ska användas vid sparande till EMF i C++."
type: docs
weight: 18000
url: /sv/cpp/aspose.words.saving/imagesaveoptions/get_usegdiemfrenderer/
---
## ImageSaveOptions::get_UseGdiEmfRenderer method


Hämtar eller anger ett värde som bestämmer om GDI+ eller Aspose.Words‑metafilrenderare ska användas vid sparande till EMF.

```cpp
bool Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer() const
```

## Anmärkningar


Om den är satt till **true** används GDI+ metafilrenderare. Dvs. innehållet skrivs till ett GDI+ grafikobjekt och sparas till metafilen.

Om den är satt till **false** används Aspose.Words metafilrenderare. Dvs. innehållet skrivs direkt till metafilformatet med Aspose.Words.

Har effekt endast vid sparande till EMF.

GDI+ sparande fungerar endast på .NET.

Standardvärdet är **true**.

## Exempel



Visar hur man väljer en renderare när man konverterar ett dokument till .emf.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// När vi sparar dokumentet som en EMF-bild kan vi skicka ett SaveOptions‑objekt för att välja en renderare för bilden.
// Om vi sätter flaggan "UseGdiEmfRenderer" till "true" kommer Aspose.Words att använda GDI+ renderaren.
// Om vi sätter flaggan "UseGdiEmfRenderer" till "false" kommer Aspose.Words att använda sin egen metafilrenderare.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Emf);
saveOptions->set_UseGdiEmfRenderer(useGdiEmfRenderer);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Renderer.emf", saveOptions);
```

## Se även

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
