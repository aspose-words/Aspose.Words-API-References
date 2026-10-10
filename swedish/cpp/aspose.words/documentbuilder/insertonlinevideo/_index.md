---
title: "Aspose::Words::DocumentBuilder::InsertOnlineVideo metod"
linktitle: "InsertOnlineVideo"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::InsertOnlineVideo metod. Infogar ett onlinevideobjekt i dokumentet och skalar det till den angivna storleken i C++."
type: docs
weight: 43000
url: /sv/cpp/aspose.words/documentbuilder/insertonlinevideo/
---
## DocumentBuilder::InsertOnlineVideo(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Infogar ett online-videobjekt i dokumentet och skalar det till den angivna storleken.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| videoUrl | const System::String\& | URL:en till videon. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Anger var avståndet till bilden mäts från. |
| left | double | Avstånd i punkter från ursprunget till bildens vänstra sida. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Anger var avståndet till bilden mäts från. |
| top | double | Avstånd i punkter från ursprunget till bildens övre sida. |
| bredd | double | Bredden på bilden i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| höjd | double | Höjden på bilden i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| wrapType | Aspose::Words::Drawing::WrapType | Anger hur text ska omslutas runt bilden. |

### ReturnValue

Bildnod som just har infogats.
## Anmärkningar


Du kan ändra bildens storlek, plats, placeringsmetod och andra inställningar med hjälp av objektet [Shape](../../../aspose.words.drawing/shape/) som returneras av denna metod.

Infogning av online‑video från följande resurser stöds:

* [https://www.youtube.com/](https://www.youtube.com/)
* [https://vimeo.com/](https://vimeo.com/)



Om din online‑video inte visas korrekt, använd [InsertOnlineVideo()](../), som accepterar anpassad inbäddad HTML‑kod.

Koden för att bädda in video kan variera mellan leverantörer, konsultera den leverantör du valt för detaljer.

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Infogar ett online-videobjekt i dokumentet och skalar det till den angivna storleken.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, const System::String &videoEmbedCode, const System::ArrayPtr<uint8_t> &thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| videoUrl | const System::String\& | URL:en till videon. |
| videoEmbedCode | const System::String\& | Inbäddningskoden för videon. |
| thumbnailImageBytes | const System::ArrayPtr\<uint8_t\>\& | Miniatyrbildens byte. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Anger var avståndet till bilden mäts från. |
| left | double | Avstånd i punkter från ursprunget till bildens vänstra sida. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Anger var avståndet till bilden mäts från. |
| top | double | Avstånd i punkter från ursprunget till bildens övre sida. |
| bredd | double | Bredden på bilden i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| höjd | double | Höjden på bilden i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| wrapType | Aspose::Words::Drawing::WrapType | Anger hur text ska omslutas runt bilden. |

### ReturnValue

Bildnod som just har infogats.
## Anmärkningar


Du kan ändra bildens storlek, plats, placeringsmetod och andra inställningar med hjälp av objektet [Shape](../../../aspose.words.drawing/shape/) som returneras av denna metod.

## Exempel



Visar hur man infogar en online‑video i ett dokument med en anpassad miniatyrbild.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String videoUrl = u"https://vimeo.com/52477838";
System::String videoEmbedCode = System::String(u"<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" ") + u"title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

System::ArrayPtr<uint8_t> thumbnailImageBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");

{
    auto stream = System::MakeObject<System::IO::MemoryStream>(thumbnailImageBytes);
    {
        System::SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromStream(stream);
        // Nedan följer två sätt att skapa en form med en anpassad miniatyrbild, som länkar till en online‑video
        // som spelas upp när vi klickar på formen i Microsoft Word.
        // 1 -  Infoga en inline‑form vid byggarens nodinfogningsmarkör:
        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image->get_Width(), image->get_Height());

        builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

        // 2 -  Infoga en flytande form:
        double left = builder->get_PageSetup()->get_RightMargin() - image->get_Width();
        double top = builder->get_PageSetup()->get_BottomMargin() - image->get_Height();

        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, left, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, top, image->get_Width(), image->get_Height(), Aspose::Words::Drawing::WrapType::Square);
    }
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, double, double) method


Infogar ett online-videobjekt i dokumentet och skalar det till den angivna storleken.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, const System::String &videoEmbedCode, const System::ArrayPtr<uint8_t> &thumbnailImageBytes, double width, double height)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| videoUrl | const System::String\& | URL:en till videon. |
| videoEmbedCode | const System::String\& | Inbäddningskoden för videon. |
| thumbnailImageBytes | const System::ArrayPtr\<uint8_t\>\& | Miniatyrbildens byte. |
| bredd | double | Bredden på bilden i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| höjd | double | Höjden på bilden i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |

### ReturnValue

Bildnod som just har infogats.
## Anmärkningar


Du kan ändra bildens storlek, plats, placeringsmetod och andra inställningar med hjälp av objektet [Shape](../../../aspose.words.drawing/shape/) som returneras av denna metod.

## Exempel



Visar hur man infogar en online‑video i ett dokument med en anpassad miniatyrbild.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String videoUrl = u"https://vimeo.com/52477838";
System::String videoEmbedCode = System::String(u"<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" ") + u"title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

System::ArrayPtr<uint8_t> thumbnailImageBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");

{
    auto stream = System::MakeObject<System::IO::MemoryStream>(thumbnailImageBytes);
    {
        System::SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromStream(stream);
        // Nedan följer två sätt att skapa en form med en anpassad miniatyrbild, som länkar till en online‑video
        // som spelas upp när vi klickar på formen i Microsoft Word.
        // 1 -  Infoga en inline‑form vid byggarens nodinfogningsmarkör:
        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image->get_Width(), image->get_Height());

        builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

        // 2 -  Infoga en flytande form:
        double left = builder->get_PageSetup()->get_RightMargin() - image->get_Width();
        double top = builder->get_PageSetup()->get_BottomMargin() - image->get_Height();

        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, left, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, top, image->get_Width(), image->get_Height(), Aspose::Words::Drawing::WrapType::Square);
    }
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, double, double) method


Infogar ett online-videobjekt i dokumentet och skalar det till den angivna storleken.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, double width, double height)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| videoUrl | const System::String\& | URL:en till videon. |
| bredd | double | Bredden på bilden i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| höjd | double | Höjden på bilden i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |

### ReturnValue

Bildnod som just har infogats.
## Anmärkningar


Du kan ändra bildens storlek, plats, placeringsmetod och andra inställningar med hjälp av objektet [Shape](../../../aspose.words.drawing/shape/) som returneras av denna metod.

Infogning av online‑video från följande resurser stöds:

* [https://www.youtube.com/](https://www.youtube.com/)
* [https://vimeo.com/](https://vimeo.com/)



Om din online‑video inte visas korrekt, använd [InsertOnlineVideo()](../), som accepterar anpassad inbäddad HTML‑kod.

Koden för att bädda in video kan variera mellan leverantörer, konsultera den leverantör du valt för detaljer.

## Exempel



Visar hur man infogar en online‑video i ett dokument med en URL.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertOnlineVideo(u"https://youtu.be/g1N9ke8Prmk", 360, 270);

// Vi kan titta på videon i Microsoft Word genom att klicka på formen.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertVideoWithUrl.docx");
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
