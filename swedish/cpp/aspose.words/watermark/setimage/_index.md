---
title: "Aspose::Words::Watermark::SetImage metod"
linktitle: "SetImage"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Watermark::SetImage metod. Lägger till en bildvattenstämpel i dokumentet i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words/watermark/setimage/
---
## Watermark::SetImage(const System::SharedPtr\<System::Drawing::Image\>\&) method


Lägger till bildvattenstämpel i dokumentet.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::Drawing::Image> &image)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | Bild som visas som en vattenstämpel. |

## Exempel



Visar hur man skapar en vattenstämpel från en bild i det lokala filsystemet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ändra bildvattenstämpelns utseende med ett ImageWatermarkOptions-objekt,
// och skicka sedan med den när du skapar en vattenstämpel från en bildfil.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// Vi har olika alternativ för att infoga en bild.
// Använd någon av följande metoder för att lägga till bildvattenstämpel.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## Se även

* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Lägger till bildvattenstämpel i dokumentet.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::Drawing::Image> &image, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | Bild som visas som en vattenstämpel. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definierar ytterligare alternativ för bildvattenstämpeln. |

## Exempel



Visar hur man skapar en vattenstämpel från en bild i det lokala filsystemet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ändra bildvattenstämpelns utseende med ett ImageWatermarkOptions-objekt,
// och skicka sedan med den när du skapar en vattenstämpel från en bildfil.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// Vi har olika alternativ för att infoga en bild.
// Använd någon av följande metoder för att lägga till bildvattenstämpel.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## Se även

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Lägger till bildvattenstämpel i dokumentet.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::IO::Stream> &imageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| imageStream | const System::SharedPtr\<System::IO::Stream\>\& | Strömmen som innehåller bilddata som visas som en vattenstämpel. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definierar ytterligare alternativ för bildvattenstämpeln. |

## Exempel



Visar hur man skapar en vattenstämpel från en bildström.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ändra bildvattenstämpelns utseende med ett ImageWatermarkOptions-objekt,
// och skicka sedan med den när du skapar en vattenstämpel från en bildfil.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);

{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open, System::IO::FileAccess::Read);
    doc->get_Watermark()->SetImage(imageStream, imageWatermarkOptions);
}

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermarkStream.docx");
```

## Se även

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Lägger till bildvattenstämpel i dokumentet.

```cpp
void Aspose::Words::Watermark::SetImage(const System::String &imagePath, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| imagePath | const System::String\& | Sökväg till bildfilen som visas som en vattenstämpel. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definierar ytterligare alternativ för bildvattenstämpeln. |

## Exempel



Visar hur man skapar en vattenstämpel från en bild i det lokala filsystemet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ändra bildvattenstämpelns utseende med ett ImageWatermarkOptions-objekt,
// och skicka sedan med den när du skapar en vattenstämpel från en bildfil.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// Vi har olika alternativ för att infoga en bild.
// Använd någon av följande metoder för att lägga till bildvattenstämpel.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## Se även

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
