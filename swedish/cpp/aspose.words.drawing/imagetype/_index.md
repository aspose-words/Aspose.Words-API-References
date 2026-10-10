---
title: "Aspose::Words::Drawing::ImageType enum"
linktitle: "ImageType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ImageType enum. Anger typen (formatet) på en bild i ett Microsoft Word-dokument i C++."
type: docs
weight: 28000
url: /sv/cpp/aspose.words.drawing/imagetype/
---
## ImageType enum


Anger typen (formatet) av en bild i ett Microsoft Word-dokument.

```cpp
enum class ImageType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| NoImage | 0 | Det finns ingen bilddata. |
| Okänd | 1 | En okänd bildtyp eller bildtyp som inte kan lagras direkt i ett Microsoft Word-dokument. |
| Emf | 2 | Windows Enhanced Metafile. |
| Wmf | 3 | Windows Metafile. |
| Pict | 4 | Macintosh PICT. En befintlig bild kommer att bevaras i ett dokument, men att infoga nya PICT‑bilder i ett dokument stöds inte. |
| Jpeg | 5 | JPEG JFIF. |
| Png | 6 | Portable Network Graphics. |
| Bmp | 7 | Windows Bitmap. |
| Eps | 8 | Encapsulated PostScript. |
| WebP | 9 | WebP. |
| Gif | 10 | GIF. |


## Exempel



Visar hur man lägger till en bild i en form och kontrollerar dess typ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> imgShape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, imgShape->get_ImageData()->get_ImageType());
```

## Se även

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
