---
title: "Aspose::Words::Drawing::ImageType enum"
linktitle: "ImageType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ImageType enum. Gibt den Typ (Format) eines Bildes in einem Microsoft Word-Dokument in C++ an."
type: docs
weight: 28000
url: /de/cpp/aspose.words.drawing/imagetype/
---
## ImageType enum


Gibt den Typ (das Format) eines Bildes in einem Microsoft‑Word-Dokument an.

```cpp
enum class ImageType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| NoImage | 0 | Es gibt keine Bilddaten. |
| Unbekannt | 1 | Ein unbekannter Bildtyp oder ein Bildtyp, der nicht direkt in einem Microsoft Word-Dokument gespeichert werden kann. |
| Emf | 2 | Windows Enhanced Metafile. |
| Wmf | 3 | Windows Metafile. |
| Pict | 4 | Macintosh PICT. Ein vorhandenes Bild wird in einem Dokument erhalten bleiben, aber das Einfügen neuer PICT-Bilder in ein Dokument wird nicht unterstützt. |
| Jpeg | 5 | JPEG JFIF. |
| Png | 6 | Portable Network Graphics. |
| Bmp | 7 | Windows Bitmap. |
| Eps | 8 | Encapsulated PostScript. |
| WebP | 9 | WebP. |
| Gif | 10 | GIF. |


## Beispiele



Zeigt, wie man ein Bild zu einer Form hinzufügt und dessen Typ überprüft.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> imgShape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, imgShape->get_ImageData()->get_ImageType());
```

## Siehe auch

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
