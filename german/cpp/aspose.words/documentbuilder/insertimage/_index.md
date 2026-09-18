---
title: "Aspose::Words::DocumentBuilder::InsertImage Methode"
linktitle: "InsertImage"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::InsertImage Methode. Fügt ein Bild aus einem Byte-Array in das Dokument ein. Das Bild wird inline und mit 100 %iger Skalierung in C++ eingefügt."
type: docs
weight: 39000
url: /de/cpp/aspose.words/documentbuilder/insertimage/
---
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&) method


Fügt ein Bild aus einem Byte-Array in das Dokument ein. Das Bild wird inline und mit 100 % Skalierung eingefügt.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | Das Byte-Array, das das Bild enthält. |

### ReturnValue

Der Bildknoten, der gerade eingefügt wurde.
## Hinweise


Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem [Shape](../../../aspose.words.drawing/shape/) Objekt ändern, das von dieser Methode zurückgegeben wird.

## Beispiele



Zeigt, wie man ein Bild aus einem Byte-Array in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::ArrayPtr<uint8_t> imageByteArray = Aspose::Words::ApiExamples::TestUtil::ImageToByteArray(get_ImageDir() + u"Logo.jpg");

// Unten sind drei Möglichkeiten, ein Bild aus einem Byte-Array einzufügen.
// 1 -  Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
builder->InsertImage(imageByteArray);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Inline-Form mit benutzerdefinierten Abmessungen:
builder->InsertImage(imageByteArray, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Schwebende Form mit benutzerdefinierten Abmessungen:
builder->InsertImage(imageByteArray, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Fügt ein Bild aus einem Byte‑Array an der angegebenen Position und Größe ein.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | Das Byte-Array, das das Bild enthält. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| left | double | Abstand in Punkten vom Ursprung zur linken Seite des Bildes. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| top | double | Abstand in Punkten vom Ursprung zur oberen Seite des Bildes. |
| Breite | double | Die Breite des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |
| Höhe | double | Die Höhe des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |
| wrapType | Aspose::Words::Drawing::WrapType | Gibt an, wie der Text um das Bild herumfließt. |

### ReturnValue

Der Bildknoten, der gerade eingefügt wurde.
## Hinweise


Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem [Shape](../../../aspose.words.drawing/shape/) Objekt ändern, das von dieser Methode zurückgegeben wird.

## Beispiele



Zeigt, wie man ein Bild aus einem Byte-Array in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::ArrayPtr<uint8_t> imageByteArray = Aspose::Words::ApiExamples::TestUtil::ImageToByteArray(get_ImageDir() + u"Logo.jpg");

// Unten sind drei Möglichkeiten, ein Bild aus einem Byte-Array einzufügen.
// 1 -  Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
builder->InsertImage(imageByteArray);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Inline-Form mit benutzerdefinierten Abmessungen:
builder->InsertImage(imageByteArray, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Schwebende Form mit benutzerdefinierten Abmessungen:
builder->InsertImage(imageByteArray, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&, double, double) method


Fügt ein Inline‑Bild aus einem Byte‑Array in das Dokument ein und skaliert es auf die angegebene Größe.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes, double width, double height)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | Das Byte-Array, das das Bild enthält. |
| Breite | double | Die Breite des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |
| Höhe | double | Die Höhe des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |

### ReturnValue

Der Bildknoten, der gerade eingefügt wurde.
## Hinweise


Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem [Shape](../../../aspose.words.drawing/shape/) Objekt ändern, das von dieser Methode zurückgegeben wird.

## Beispiele



Zeigt, wie man ein Bild aus einem Byte-Array in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::ArrayPtr<uint8_t> imageByteArray = Aspose::Words::ApiExamples::TestUtil::ImageToByteArray(get_ImageDir() + u"Logo.jpg");

// Unten sind drei Möglichkeiten, ein Bild aus einem Byte-Array einzufügen.
// 1 -  Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
builder->InsertImage(imageByteArray);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Inline-Form mit benutzerdefinierten Abmessungen:
builder->InsertImage(imageByteArray, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Schwebende Form mit benutzerdefinierten Abmessungen:
builder->InsertImage(imageByteArray, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&) method


Fügt ein Bild aus einem **Image**-Objekt in das Dokument ein. Das Bild wird inline und mit 100 % Skalierung eingefügt.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Bild | const System::SharedPtr\<System::Drawing::Image\>\& | Das Bild, das in das Dokument eingefügt werden soll. |

### ReturnValue

Der Bildknoten, der gerade eingefügt wurde.
## Hinweise


Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem [Shape](../../../aspose.words.drawing/shape/) Objekt ändern, das von dieser Methode zurückgegeben wird.

## Beispiele



Zeigt, wie man ein Bild aus einem Objekt in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFile = get_ImageDir() + u"Logo.jpg";

// Unten sind drei Möglichkeiten, ein Bild aus einer Image-Objektinstanz einzufügen.
// 1 -  Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
builder->InsertImage(imageFile);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Inline-Form mit benutzerdefinierten Abmessungen:
builder->InsertImage(imageFile, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Schwebende Form mit benutzerdefinierten Abmessungen:
builder->InsertImage(imageFile, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Fügt ein Bild aus einem **Image**‑Objekt an der angegebenen Position und Größe ein.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Bild | const System::SharedPtr\<System::Drawing::Image\>\& | Das Bild, das in das Dokument eingefügt werden soll. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| left | double | Abstand in Punkten vom Ursprung zur linken Seite des Bildes. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| top | double | Abstand in Punkten vom Ursprung zur oberen Seite des Bildes. |
| Breite | double | Die Breite des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |
| Höhe | double | Die Höhe des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |
| wrapType | Aspose::Words::Drawing::WrapType | Gibt an, wie der Text um das Bild herumfließt. |

### ReturnValue

Der Bildknoten, der gerade eingefügt wurde.
## Hinweise


Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem [Shape](../../../aspose.words.drawing/shape/) Objekt ändern, das von dieser Methode zurückgegeben wird.

## Beispiele



Zeigt, wie man ein Bild aus einem Objekt in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFile = get_ImageDir() + u"Logo.jpg";

// Unten sind drei Möglichkeiten, ein Bild aus einer Image-Objektinstanz einzufügen.
// 1 -  Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
builder->InsertImage(imageFile);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Inline-Form mit benutzerdefinierten Abmessungen:
builder->InsertImage(imageFile, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Schwebende Form mit benutzerdefinierten Abmessungen:
builder->InsertImage(imageFile, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&, double, double) method


Fügt ein Inline‑Bild aus einem **Image**‑Objekt in das Dokument ein und skaliert es auf die angegebene Größe.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image, double width, double height)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Bild | const System::SharedPtr\<System::Drawing::Image\>\& | Das Bild, das in das Dokument eingefügt werden soll. |
| Breite | double | Die Breite des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |
| Höhe | double | Die Höhe des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |

### ReturnValue

Der Bildknoten, der gerade eingefügt wurde.
## Hinweise


Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem [Shape](../../../aspose.words.drawing/shape/) Objekt ändern, das von dieser Methode zurückgegeben wird.

## Beispiele



Zeigt, wie man ein Bild aus einem Objekt in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFile = get_ImageDir() + u"Logo.jpg";

// Unten sind drei Möglichkeiten, ein Bild aus einer Image-Objektinstanz einzufügen.
// 1 -  Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
builder->InsertImage(imageFile);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Inline-Form mit benutzerdefinierten Abmessungen:
builder->InsertImage(imageFile, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Schwebende Form mit benutzerdefinierten Abmessungen:
builder->InsertImage(imageFile, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&) method


Fügt ein Bild aus einem Stream in das Dokument ein. Das Bild wird inline und mit 100 % Skalierung eingefügt.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Datenstrom | const System::SharedPtr\<System::IO::Stream\>\& | Der Stream, der das Bild enthält. |

### ReturnValue

Der Bildknoten, der gerade eingefügt wurde.
## Hinweise


Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem [Shape](../../../aspose.words.drawing/shape/) Objekt ändern, das von dieser Methode zurückgegeben wird.

## Beispiele



Zeigt, wie man ein Bild aus einem Stream in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    // Unten sind drei Möglichkeiten, ein Bild aus einem Stream einzufügen.
    // 1 -  Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
    builder->InsertImage(stream);

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 2 -  Inline-Form mit benutzerdefinierten Abmessungen:
    builder->InsertImage(stream, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 3 -  Schwebende Form mit benutzerdefinierten Abmessungen:
    builder->InsertImage(stream, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromStream.docx");
```


Zeigt, wie man eine Form mit einem Bild aus einem Stream in ein Dokument einfügt.
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

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Fügt ein Bild aus einem Stream an der angegebenen Position und Größe ein.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Datenstrom | const System::SharedPtr\<System::IO::Stream\>\& | Der Stream, der das Bild enthält. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| left | double | Abstand in Punkten vom Ursprung zur linken Seite des Bildes. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| top | double | Abstand in Punkten vom Ursprung zur oberen Seite des Bildes. |
| Breite | double | Die Breite des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |
| Höhe | double | Die Höhe des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |
| wrapType | Aspose::Words::Drawing::WrapType | Gibt an, wie der Text um das Bild herumfließt. |

### ReturnValue

Der Bildknoten, der gerade eingefügt wurde.
## Hinweise


Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem [Shape](../../../aspose.words.drawing/shape/) Objekt ändern, das von dieser Methode zurückgegeben wird.

## Beispiele



Zeigt, wie man ein Bild aus einem Stream in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    // Unten sind drei Möglichkeiten, ein Bild aus einem Stream einzufügen.
    // 1 -  Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
    builder->InsertImage(stream);

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 2 -  Inline-Form mit benutzerdefinierten Abmessungen:
    builder->InsertImage(stream, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 3 -  Schwebende Form mit benutzerdefinierten Abmessungen:
    builder->InsertImage(stream, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromStream.docx");
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&, double, double) method


Fügt ein Inline‑Bild aus einem Stream in das Dokument ein und skaliert es auf die angegebene Größe.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream, double width, double height)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Datenstrom | const System::SharedPtr\<System::IO::Stream\>\& | Der Stream, der das Bild enthält. |
| Breite | double | Die Breite des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |
| Höhe | double | Die Höhe des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |

### ReturnValue

Der Bildknoten, der gerade eingefügt wurde.
## Hinweise


Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem [Shape](../../../aspose.words.drawing/shape/) Objekt ändern, das von dieser Methode zurückgegeben wird.

## Beispiele



Zeigt, wie man ein Bild aus einem Stream in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    // Unten sind drei Möglichkeiten, ein Bild aus einem Stream einzufügen.
    // 1 -  Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
    builder->InsertImage(stream);

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 2 -  Inline-Form mit benutzerdefinierten Abmessungen:
    builder->InsertImage(stream, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 3 -  Schwebende Form mit benutzerdefinierten Abmessungen:
    builder->InsertImage(stream, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromStream.docx");
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::String\&) method


Fügt ein Bild aus einer Datei oder URL in das Dokument ein. Das Bild wird inline und mit 100 % Skalierung eingefügt.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | const System::String\& | Die Datei mit dem Bild. Kann jede gültige lokale oder entfernte URI sein. |

### ReturnValue

Der Bildknoten, der gerade eingefügt wurde.
## Hinweise


Diese Überladung lädt das Bild automatisch herunter, bevor es in das Dokument eingefügt wird, wenn Sie eine entfernte URI angeben.

Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem [Shape](../../../aspose.words.drawing/shape/) Objekt ändern, das von dieser Methode zurückgegeben wird.

## Beispiele



Zeigt, wie man ein Bild aus dem lokalen Dateisystem in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Unten sind drei Möglichkeiten, ein Bild aus einem lokalen Dateinamen einzufügen.
// 1 -  Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Inline-Form mit benutzerdefinierten Abmessungen:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Schwebende Form mit benutzerdefinierten Abmessungen:
builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```


Zeigt, wie man bestimmt, welches Bild eingefügt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"Scalable Vector Graphics.svg");

// Aspose.Words fügt ein SVG-Bild in das Dokument als PNG mit der svgBlip-Erweiterung ein.
// die die ursprüngliche Vektor‑SVG-Bilddarstellung enthält.
doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

// Aspose.Words fügt ein SVG-Bild in das Dokument als PNG ein, genau wie Microsoft Word es für das alte Format tut.
doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertSvgImage.Svg.doc");

doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);

// Aspose.Words fügt ein SVG-Bild in das Dokument als EMF-Metadatei ein, um das Bild in Vektorrepräsentation zu behalten.
doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertSvgImage.Emf.docx");
```


Zeigt, wie man ein GIF-Bild in das Dokument einfügt.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// Wir können ein GIF-Bild über Pfad oder Byte‑Array einfügen.
// Es funktioniert nur, wenn DocumentBuilder auf Word‑Version 2010 oder höher optimiert ist.
// Hinweis: Der Zugriff auf die Bildbytes verursacht die Konvertierung von GIF zu PNG.
System::SharedPtr<Aspose::Words::Drawing::Shape> gifImage = builder->InsertImage(get_ImageDir() + u"Graphics Interchange Format.gif");

gifImage = builder->InsertImage(System::IO::File::ReadAllBytes(get_ImageDir() + u"Graphics Interchange Format.gif"));

builder->get_Document()->Save(get_ArtifactsDir() + u"InsertGif.docx");
```


Zeigt, wie man eine Form mit einem Bild in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Unten sind zwei Orte, an denen die "InsertShape"-Methode des DocumentBuilder
// kann das Bild bereitstellen, das die Form anzeigen wird.
// 1 -  Übergeben Sie einen lokalen Dateisystem-Dateinamen einer Bilddatei:
builder->Write(u"Image from local file: ");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->Writeln();

// 2 -  Übergeben Sie eine URL, die auf ein Bild verweist.
builder->Write(u"Image from a URL: ");
builder->InsertImage(get_ImageUrl());
builder->Writeln();

doc->Save(get_ArtifactsDir() + u"Image.FromUrl.docx");
```


Zeigt, wie man ein schwebendes Bild in die Mitte einer Seite einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie ein schwebendes Bild ein, das hinter dem überlappenden Text erscheint und es an der Seitenmitte ausrichtet.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```


Zeigt, wie man ein WebP‑Bild einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"WebP image.webp");

doc->Save(get_ArtifactsDir() + u"Image.InsertWebpImage.docx");
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Fügt ein Bild aus einer Datei oder URL an der angegebenen Position und Größe ein.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | const System::String\& | Die Datei, die das Bild enthält. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| left | double | Abstand in Punkten vom Ursprung zur linken Seite des Bildes. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| top | double | Abstand in Punkten vom Ursprung zur oberen Seite des Bildes. |
| Breite | double | Die Breite des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |
| Höhe | double | Die Höhe des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |
| wrapType | Aspose::Words::Drawing::WrapType | Gibt an, wie der Text um das Bild herumfließt. |

### ReturnValue

Der Bildknoten, der gerade eingefügt wurde.
## Hinweise


Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem [Shape](../../../aspose.words.drawing/shape/) Objekt ändern, das von dieser Methode zurückgegeben wird.

## Beispiele



Zeigt, wie man ein Bild einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Es gibt zwei Möglichkeiten, einen DocumentBuilder zu verwenden, um ein Bild bereitzustellen und es dann als schwebende Form einzufügen.
// 1 -  Aus einer Datei im lokalen Dateisystem:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 0.0, 200.0, 200.0, Aspose::Words::Drawing::WrapType::Square);

// 2 -  Aus einer URL:
builder->InsertImage(get_ImageUrl(), Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 250.0, 200.0, 200.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFloatingImage.docx");
```


Zeigt, wie man ein Bild aus dem lokalen Dateisystem in ein Dokument einfügt und dabei seine Abmessungen beibehält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Die InsertImage‑Methode erstellt eine schwebende Form mit dem übergebenen Bild in ihren Bilddaten.
// Wir können die Abmessungen der Form angeben, indem wir sie an diese Methode übergeben.
System::SharedPtr<Aspose::Words::Drawing::Shape> imageShape = builder->InsertImage(get_ImageDir() + u"Logo.jpg", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 0.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 0.0, -1.0, -1.0, Aspose::Words::Drawing::WrapType::Square);

// Das Übergeben negativer Werte als beabsichtigte Abmessungen definiert automatisch
// die Abmessungen der Form basierend auf den Abmessungen ihres Bildes.
ASPOSE_ASSERT_EQ(300.0, imageShape->get_Width());
ASPOSE_ASSERT_EQ(300.0, imageShape->get_Height());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertImageOriginalSize.docx");
```


Zeigt, wie man ein Bild aus dem lokalen Dateisystem in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Unten sind drei Möglichkeiten, ein Bild aus einem lokalen Dateinamen einzufügen.
// 1 -  Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Inline-Form mit benutzerdefinierten Abmessungen:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Schwebende Form mit benutzerdefinierten Abmessungen:
builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::String\&, double, double) method


Fügt ein Inline‑Bild aus einer Datei oder URL in das Dokument ein und skaliert es auf die angegebene Größe.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName, double width, double height)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | const System::String\& | Die Datei, die das Bild enthält. |
| Breite | double | Die Breite des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |
| Höhe | double | Die Höhe des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |

### ReturnValue

Der Bildknoten, der gerade eingefügt wurde.
## Hinweise


Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem [Shape](../../../aspose.words.drawing/shape/) Objekt ändern, das von dieser Methode zurückgegeben wird.

## Beispiele



Zeigt, wie man ein Bild aus dem lokalen Dateisystem in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Unten sind drei Möglichkeiten, ein Bild aus einem lokalen Dateinamen einzufügen.
// 1 -  Inline-Form mit einer Standardgröße basierend auf den Originalabmessungen des Bildes:
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Inline-Form mit benutzerdefinierten Abmessungen:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Schwebende Form mit benutzerdefinierten Abmessungen:
builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(std::basic_istream<CharType, Traits> &stream)
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(std::basic_istream\<CharType, Traits\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(std::basic_istream<CharType, Traits> &stream, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```

## Siehe auch

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

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
