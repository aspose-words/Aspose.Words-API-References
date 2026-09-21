---
title: "Aspose::Words::Saving::ImageSaveOptions::get_Scale metod"
linktitle: "get_Scale"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::ImageSaveOptions::get_Scale‑metoden. Hämtar eller anger zoomfaktorn för de genererade bilderna i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words.saving/imagesaveoptions/get_scale/
---
## ImageSaveOptions::get_Scale method


Hämtar eller anger zoomfaktorn för de genererade bilderna.

```cpp
float Aspose::Words::Saving::ImageSaveOptions::get_Scale() const
```


## Exempel



Visar hur man redigerar bilden medan Aspose.Words konverterar ett dokument till en sådan.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// När vi sparar dokumentet som en bild kan vi skicka ett SaveOptions‑objekt till
// redigera bilden medan sparningsoperationen renderar den.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// Vi kan justera dessa egenskaper för att ändra bildens ljusstyrka och kontrast.
// Båda är på en 0‑1 skala och har standardvärdet 0,5.
options->set_ImageBrightness(0.3f);
options->set_ImageContrast(0.7f);
// Vi kan justera horisontell och vertikal upplösning med dessa egenskaper.
// Detta kommer att påverka bildens dimensioner.
// Standardvärdet för dessa egenskaper är 96,0, för en upplösning på 96 dpi.
options->set_HorizontalResolution(72.f);
options->set_VerticalResolution(72.f);
// Vi kan skala bilden med denna egenskap. Standardvärdet är 1,0, för en skalning på 100 %.
// Vi kan använda denna egenskap för att motverka eventuella förändringar i bildens dimensioner som en förändring av upplösningen skulle orsaka.
options->set_Scale(96.f / 72.f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.EditImage.png", options);
```


Visar hur man renderar ett Office‑objekt [Math](../../../aspose.words.math/) till en bildfil i det lokala filsystemet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// Skapa ett "ImageSaveOptions"-objekt för att skicka till nodrenderarens "Save"-metod för att modifiera
// hur den renderar OfficeMath-noden till en bild.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// Ställ in egenskapen "Scale" till 5 för att rendera objektet till fem gånger dess ursprungliga storlek.
saveOptions->set_Scale(5.0f);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"Shape.RenderOfficeMath.png", saveOptions);
```

## Se även

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
