---
title: "Aspose::Words::DocumentBuilder::InsertOnlineVideo-Methode"
linktitle: "InsertOnlineVideo"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::InsertOnlineVideo-Methode. Fügt ein Online‑Video‑Objekt in das Dokument ein und skaliert es auf die angegebene Größe in C++."
type: docs
weight: 43000
url: /de/cpp/aspose.words/documentbuilder/insertonlinevideo/
---
## DocumentBuilder::InsertOnlineVideo(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Fügt ein Online‑Video‑Objekt in das Dokument ein und skaliert es auf die angegebene Größe.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| videoUrl | const System::String\& | Die URL zum Video. |
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

Das Einfügen von Online‑Video aus den folgenden Quellen wird unterstützt:

* [https://www.youtube.com/](https://www.youtube.com/)
* [https://vimeo.com/](https://vimeo.com/)



Wenn Ihr Online‑Video nicht korrekt angezeigt wird, verwenden Sie [InsertOnlineVideo()](../), das benutzerdefinierten eingebetteten HTML‑Code akzeptiert.

Der Code zum Einbetten von Videos kann je nach Anbieter variieren; konsultieren Sie Ihren jeweiligen Anbieter für Details.

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Fügt ein Online‑Video‑Objekt in das Dokument ein und skaliert es auf die angegebene Größe.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, const System::String &videoEmbedCode, const System::ArrayPtr<uint8_t> &thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| videoUrl | const System::String\& | Die URL zum Video. |
| videoEmbedCode | const System::String\& | Der Einbettungscode für das Video. |
| thumbnailImageBytes | const System::ArrayPtr\<uint8_t\>\& | Die Bytes des Miniaturbildes. |
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



Zeigt, wie man ein Online‑Video in ein Dokument mit einer benutzerdefinierten Miniatur einfügt.
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
        // Unten sind zwei Möglichkeiten, eine Form mit einer benutzerdefinierten Miniatur zu erstellen, die zu einem Online‑Video verlinkt
        // die abgespielt wird, wenn wir in Microsoft Word auf die Form klicken.
        // 1 - Fügen Sie eine Inline‑Form an der Einfügeposition des Builders ein:
        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image->get_Width(), image->get_Height());

        builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

        // 2 - Fügen Sie eine schwebende Form ein:
        double left = builder->get_PageSetup()->get_RightMargin() - image->get_Width();
        double top = builder->get_PageSetup()->get_BottomMargin() - image->get_Height();

        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, left, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, top, image->get_Width(), image->get_Height(), Aspose::Words::Drawing::WrapType::Square);
    }
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, double, double) method


Fügt ein Online‑Video‑Objekt in das Dokument ein und skaliert es auf die angegebene Größe.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, const System::String &videoEmbedCode, const System::ArrayPtr<uint8_t> &thumbnailImageBytes, double width, double height)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| videoUrl | const System::String\& | Die URL zum Video. |
| videoEmbedCode | const System::String\& | Der Einbettungscode für das Video. |
| thumbnailImageBytes | const System::ArrayPtr\<uint8_t\>\& | Die Bytes des Miniaturbildes. |
| Breite | double | Die Breite des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |
| Höhe | double | Die Höhe des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |

### ReturnValue

Der Bildknoten, der gerade eingefügt wurde.
## Hinweise


Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem [Shape](../../../aspose.words.drawing/shape/) Objekt ändern, das von dieser Methode zurückgegeben wird.

## Beispiele



Zeigt, wie man ein Online‑Video in ein Dokument mit einer benutzerdefinierten Miniatur einfügt.
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
        // Unten sind zwei Möglichkeiten, eine Form mit einer benutzerdefinierten Miniatur zu erstellen, die zu einem Online‑Video verlinkt
        // die abgespielt wird, wenn wir in Microsoft Word auf die Form klicken.
        // 1 - Fügen Sie eine Inline‑Form an der Einfügeposition des Builders ein:
        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image->get_Width(), image->get_Height());

        builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

        // 2 - Fügen Sie eine schwebende Form ein:
        double left = builder->get_PageSetup()->get_RightMargin() - image->get_Width();
        double top = builder->get_PageSetup()->get_BottomMargin() - image->get_Height();

        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, left, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, top, image->get_Width(), image->get_Height(), Aspose::Words::Drawing::WrapType::Square);
    }
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, double, double) method


Fügt ein Online‑Video‑Objekt in das Dokument ein und skaliert es auf die angegebene Größe.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, double width, double height)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| videoUrl | const System::String\& | Die URL zum Video. |
| Breite | double | Die Breite des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |
| Höhe | double | Die Höhe des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |

### ReturnValue

Der Bildknoten, der gerade eingefügt wurde.
## Hinweise


Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem [Shape](../../../aspose.words.drawing/shape/) Objekt ändern, das von dieser Methode zurückgegeben wird.

Das Einfügen von Online‑Video aus den folgenden Quellen wird unterstützt:

* [https://www.youtube.com/](https://www.youtube.com/)
* [https://vimeo.com/](https://vimeo.com/)



Wenn Ihr Online‑Video nicht korrekt angezeigt wird, verwenden Sie [InsertOnlineVideo()](../), das benutzerdefinierten eingebetteten HTML‑Code akzeptiert.

Der Code zum Einbetten von Videos kann je nach Anbieter variieren; konsultieren Sie Ihren jeweiligen Anbieter für Details.

## Beispiele



Zeigt, wie man ein Online‑Video in ein Dokument über eine URL einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertOnlineVideo(u"https://youtu.be/g1N9ke8Prmk", 360, 270);

// Wir können das Video in Microsoft Word ansehen, indem wir auf die Form klicken.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertVideoWithUrl.docx");
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
