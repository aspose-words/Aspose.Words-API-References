---
title: "Aspose::Words::DocumentBuilder::InsertImage‑metod"
linktitle: "InsertImage"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::InsertImage‑metod. Infogar en bild från en byte‑array i dokumentet. Bilden infogas inline och med 100 % skala i C++."
type: docs
weight: 39000
url: /sv/cpp/aspose.words/documentbuilder/insertimage/
---
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&) method


Infogar en bild från en byte-array i dokumentet. Bilden infogas inline och med 100 % skala.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | Byte‑arrayen som innehåller bilden. |

### ReturnValue

Bildnod som just har infogats.
## Anmärkningar


Du kan ändra bildens storlek, plats, placeringsmetod och andra inställningar med hjälp av objektet [Shape](../../../aspose.words.drawing/shape/) som returneras av denna metod.

## Exempel



Visar hur man infogar en bild från en byte‑array i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::ArrayPtr<uint8_t> imageByteArray = Aspose::Words::ApiExamples::TestUtil::ImageToByteArray(get_ImageDir() + u"Logo.jpg");

// Nedan följer tre sätt att infoga en bild från en byte‑array.
// 1 -  Inline‑form med standardstorlek baserad på bildens ursprungliga dimensioner:
builder->InsertImage(imageByteArray);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Inline‑form med anpassade dimensioner:
builder->InsertImage(imageByteArray, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Flytande form med anpassade dimensioner:
builder->InsertImage(imageByteArray, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Infogar en bild från en byte-array på den angivna positionen och storleken.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | Byte‑arrayen som innehåller bilden. |
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



Visar hur man infogar en bild från en byte‑array i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::ArrayPtr<uint8_t> imageByteArray = Aspose::Words::ApiExamples::TestUtil::ImageToByteArray(get_ImageDir() + u"Logo.jpg");

// Nedan följer tre sätt att infoga en bild från en byte‑array.
// 1 -  Inline‑form med standardstorlek baserad på bildens ursprungliga dimensioner:
builder->InsertImage(imageByteArray);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Inline‑form med anpassade dimensioner:
builder->InsertImage(imageByteArray, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Flytande form med anpassade dimensioner:
builder->InsertImage(imageByteArray, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&, double, double) method


Infogar en inline-bild från en byte-array i dokumentet och skalar den till den angivna storleken.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes, double width, double height)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | Byte‑arrayen som innehåller bilden. |
| bredd | double | Bredden på bilden i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| höjd | double | Höjden på bilden i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |

### ReturnValue

Bildnod som just har infogats.
## Anmärkningar


Du kan ändra bildens storlek, plats, placeringsmetod och andra inställningar med hjälp av objektet [Shape](../../../aspose.words.drawing/shape/) som returneras av denna metod.

## Exempel



Visar hur man infogar en bild från en byte‑array i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::ArrayPtr<uint8_t> imageByteArray = Aspose::Words::ApiExamples::TestUtil::ImageToByteArray(get_ImageDir() + u"Logo.jpg");

// Nedan följer tre sätt att infoga en bild från en byte‑array.
// 1 -  Inline‑form med standardstorlek baserad på bildens ursprungliga dimensioner:
builder->InsertImage(imageByteArray);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Inline‑form med anpassade dimensioner:
builder->InsertImage(imageByteArray, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Flytande form med anpassade dimensioner:
builder->InsertImage(imageByteArray, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&) method


Infogar en bild från ett **Image**-objekt i dokumentet. Bilden infogas inline och med 100 % skala.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | Bilden som ska infogas i dokumentet. |

### ReturnValue

Bildnod som just har infogats.
## Anmärkningar


Du kan ändra bildens storlek, plats, placeringsmetod och andra inställningar med hjälp av objektet [Shape](../../../aspose.words.drawing/shape/) som returneras av denna metod.

## Exempel



Visar hur man infogar en bild från ett objekt i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFile = get_ImageDir() + u"Logo.jpg";

// Nedan följer tre sätt att infoga en bild från en Image‑objektinstans.
// 1 -  Inline‑form med standardstorlek baserad på bildens ursprungliga dimensioner:
builder->InsertImage(imageFile);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Inline‑form med anpassade dimensioner:
builder->InsertImage(imageFile, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Flytande form med anpassade dimensioner:
builder->InsertImage(imageFile, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Infogar en bild från ett **Image**-objekt på den angivna positionen och storleken.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | Bilden som ska infogas i dokumentet. |
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



Visar hur man infogar en bild från ett objekt i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFile = get_ImageDir() + u"Logo.jpg";

// Nedan följer tre sätt att infoga en bild från en Image‑objektinstans.
// 1 -  Inline‑form med standardstorlek baserad på bildens ursprungliga dimensioner:
builder->InsertImage(imageFile);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Inline‑form med anpassade dimensioner:
builder->InsertImage(imageFile, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Flytande form med anpassade dimensioner:
builder->InsertImage(imageFile, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&, double, double) method


Infogar en inline-bild från ett **Image**-objekt i dokumentet och skalar den till den angivna storleken.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image, double width, double height)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | Bilden som ska infogas i dokumentet. |
| bredd | double | Bredden på bilden i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| höjd | double | Höjden på bilden i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |

### ReturnValue

Bildnod som just har infogats.
## Anmärkningar


Du kan ändra bildens storlek, plats, placeringsmetod och andra inställningar med hjälp av objektet [Shape](../../../aspose.words.drawing/shape/) som returneras av denna metod.

## Exempel



Visar hur man infogar en bild från ett objekt i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFile = get_ImageDir() + u"Logo.jpg";

// Nedan följer tre sätt att infoga en bild från en Image‑objektinstans.
// 1 -  Inline‑form med standardstorlek baserad på bildens ursprungliga dimensioner:
builder->InsertImage(imageFile);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Inline‑form med anpassade dimensioner:
builder->InsertImage(imageFile, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Flytande form med anpassade dimensioner:
builder->InsertImage(imageFile, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&) method


Infogar en bild från en ström i dokumentet. Bilden infogas inline och med 100 % skala.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| ström | const System::SharedPtr\<System::IO::Stream\>\& | Strömmen som innehåller bilden. |

### ReturnValue

Bildnod som just har infogats.
## Anmärkningar


Du kan ändra bildens storlek, plats, placeringsmetod och andra inställningar med hjälp av objektet [Shape](../../../aspose.words.drawing/shape/) som returneras av denna metod.

## Exempel



Visar hur man infogar en bild från en ström i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    // Nedan följer tre sätt att infoga en bild från en ström.
    // 1 -  Inline‑form med standardstorlek baserad på bildens ursprungliga dimensioner:
    builder->InsertImage(stream);

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 2 -  Inline‑form med anpassade dimensioner:
    builder->InsertImage(stream, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 3 -  Flytande form med anpassade dimensioner:
    builder->InsertImage(stream, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromStream.docx");
```


Visar hur man infogar en form med en bild från en ström i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    builder->Write(u"Image from stream: ");
    builder->InsertImage(stream);
}

doc->Save(get_ArtifactsDir() + u"Image.FromStream.docx");
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Infogar en bild från en ström på den angivna positionen och storleken.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| ström | const System::SharedPtr\<System::IO::Stream\>\& | Strömmen som innehåller bilden. |
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



Visar hur man infogar en bild från en ström i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    // Nedan följer tre sätt att infoga en bild från en ström.
    // 1 -  Inline‑form med standardstorlek baserad på bildens ursprungliga dimensioner:
    builder->InsertImage(stream);

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 2 -  Inline‑form med anpassade dimensioner:
    builder->InsertImage(stream, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 3 -  Flytande form med anpassade dimensioner:
    builder->InsertImage(stream, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromStream.docx");
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&, double, double) method


Infogar en inline-bild från en ström i dokumentet och skalar den till den angivna storleken.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream, double width, double height)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| ström | const System::SharedPtr\<System::IO::Stream\>\& | Strömmen som innehåller bilden. |
| bredd | double | Bredden på bilden i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| höjd | double | Höjden på bilden i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |

### ReturnValue

Bildnod som just har infogats.
## Anmärkningar


Du kan ändra bildens storlek, plats, placeringsmetod och andra inställningar med hjälp av objektet [Shape](../../../aspose.words.drawing/shape/) som returneras av denna metod.

## Exempel



Visar hur man infogar en bild från en ström i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    // Nedan följer tre sätt att infoga en bild från en ström.
    // 1 -  Inline‑form med standardstorlek baserad på bildens ursprungliga dimensioner:
    builder->InsertImage(stream);

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 2 -  Inline‑form med anpassade dimensioner:
    builder->InsertImage(stream, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 3 -  Flytande form med anpassade dimensioner:
    builder->InsertImage(stream, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromStream.docx");
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::String\&) method


Infogar en bild från en fil eller URL i dokumentet. Bilden infogas inline och med 100 % skala.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | const System::String\& | Filen med bilden. Kan vara någon giltig lokal eller fjärr-URI. |

### ReturnValue

Bildnod som just har infogats.
## Anmärkningar


Denna överlagring laddar automatiskt ner bilden innan den infogas i dokumentet om du anger en fjärr-URI.

Du kan ändra bildens storlek, plats, placeringsmetod och andra inställningar med hjälp av objektet [Shape](../../../aspose.words.drawing/shape/) som returneras av denna metod.

## Exempel



Visar hur man infogar en bild från det lokala filsystemet i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nedan följer tre sätt att infoga en bild från ett lokalt filnamn.
// 1 -  Inline‑form med standardstorlek baserad på bildens ursprungliga dimensioner:
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Inline‑form med anpassade dimensioner:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Flytande form med anpassade dimensioner:
builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```


Visar hur man bestämmer vilken bild som kommer att infogas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"Scalable Vector Graphics.svg");

// Aspose.Words infogar SVG-bild i dokumentet som PNG med svgBlip-tillägg
// som innehåller den ursprungliga vektor‑SVG‑bildrepresentationen.
doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

// Aspose.Words infogar SVG-bild i dokumentet som PNG, precis som Microsoft Word gör för gammalt format.
doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertSvgImage.Svg.doc");

doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);

// Aspose.Words infogar SVG-bild i dokumentet som EMF‑metafil för att behålla bilden i vektorrepresentation.
doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertSvgImage.Emf.docx");
```


Visar hur man infogar en gif‑bild i dokumentet.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// Vi kan infoga en gif‑bild med sökväg eller byte‑array.
// Det fungerar endast om DocumentBuilder är optimerad för Word‑version 2010 eller högre.
// Observera att åtkomst till bildens byte‑data orsakar konvertering från Gif till Png.
System::SharedPtr<Aspose::Words::Drawing::Shape> gifImage = builder->InsertImage(get_ImageDir() + u"Graphics Interchange Format.gif");

gifImage = builder->InsertImage(System::IO::File::ReadAllBytes(get_ImageDir() + u"Graphics Interchange Format.gif"));

builder->get_Document()->Save(get_ArtifactsDir() + u"InsertGif.docx");
```


Visar hur man infogar en form med en bild i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nedan följer två platser där dokumentbyggarens "InsertShape"‑metod
// kan hämta bilden som formen ska visa.
// 1 -  Skicka ett lokalt filsystem‑filnamn för en bildfil:
builder->Write(u"Image from local file: ");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->Writeln();

// 2 -  Skicka en URL som pekar på en bild.
builder->Write(u"Image from a URL: ");
builder->InsertImage(get_ImageUrl());
builder->Writeln();

doc->Save(get_ArtifactsDir() + u"Image.FromUrl.docx");
```


Visar hur man infogar en flytande bild i sidans centrum.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en flytande bild som visas bakom den överlappande texten och justera den till sidans centrum.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```


Visar hur man infogar en WebP‑bild.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"WebP image.webp");

doc->Save(get_ArtifactsDir() + u"Image.InsertWebpImage.docx");
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Infogar en bild från en fil eller URL på den angivna positionen och storleken.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | const System::String\& | Filen som innehåller bilden. |
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



Visar hur man infogar en bild.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Det finns två sätt att använda en dokumentbyggare för att hämta en bild och sedan infoga den som en flytande form.
// 1 -  Från en fil i det lokala filsystemet:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 0.0, 200.0, 200.0, Aspose::Words::Drawing::WrapType::Square);

// 2 -  Från en URL:
builder->InsertImage(get_ImageUrl(), Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 250.0, 200.0, 200.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFloatingImage.docx");
```


Visar hur man infogar en bild från det lokala filsystemet i ett dokument samtidigt som dess dimensioner bevaras.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Metoden InsertImage skapar en flytande form med den överförda bilden i dess bilddata.
// Vi kan ange formens dimensioner genom att skicka dem till den här metoden.
System::SharedPtr<Aspose::Words::Drawing::Shape> imageShape = builder->InsertImage(get_ImageDir() + u"Logo.jpg", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 0.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 0.0, -1.0, -1.0, Aspose::Words::Drawing::WrapType::Square);

// Att skicka negativa värden som avsedda dimensioner kommer automatiskt att definiera
// formens dimensioner baserat på bildens dimensioner.
ASPOSE_ASSERT_EQ(300.0, imageShape->get_Width());
ASPOSE_ASSERT_EQ(300.0, imageShape->get_Height());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertImageOriginalSize.docx");
```


Visar hur man infogar en bild från det lokala filsystemet i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nedan följer tre sätt att infoga en bild från ett lokalt filnamn.
// 1 -  Inline‑form med standardstorlek baserad på bildens ursprungliga dimensioner:
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Inline‑form med anpassade dimensioner:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Flytande form med anpassade dimensioner:
builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::String\&, double, double) method


Infogar en inline-bild från en fil eller URL i dokumentet och skalar den till den angivna storleken.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName, double width, double height)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | const System::String\& | Filen som innehåller bilden. |
| bredd | double | Bredden på bilden i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| höjd | double | Höjden på bilden i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |

### ReturnValue

Bildnod som just har infogats.
## Anmärkningar


Du kan ändra bildens storlek, plats, placeringsmetod och andra inställningar med hjälp av objektet [Shape](../../../aspose.words.drawing/shape/) som returneras av denna metod.

## Exempel



Visar hur man infogar en bild från det lokala filsystemet i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nedan följer tre sätt att infoga en bild från ett lokalt filnamn.
// 1 -  Inline‑form med standardstorlek baserad på bildens ursprungliga dimensioner:
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Inline‑form med anpassade dimensioner:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Flytande form med anpassade dimensioner:
builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(std::basic_istream<CharType, Traits> &stream)
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(std::basic_istream\<CharType, Traits\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(std::basic_istream<CharType, Traits> &stream, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(std::basic_istream\<CharType, Traits\>\&, double, double) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(std::basic_istream<CharType, Traits> &stream, double width, double height)
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
