---
title: "Aspose::Words::Drawing::ImageType enum"
linktitle: "ImageType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ImageType enum. Bir Microsoft Word belgesindeki bir görüntünün türünü (formatını) C++'da belirtir."
type: docs
weight: 28000
url: /tr/cpp/aspose.words.drawing/imagetype/
---
## ImageType enum


Microsoft Word belgesindeki bir görüntünün tipini (formatını) belirtir.

```cpp
enum class ImageType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| NoImage | 0 | Görüntü verisi yok. |
| Bilinmiyor | 1 | Bilinmeyen bir görüntü türü veya doğrudan bir Microsoft Word belgesi içinde depolanamayan bir görüntü türü. |
| Emf | 2 | Windows Gelişmiş Metadoğası. |
| Wmf | 3 | Windows Metafile. |
| Pict | 4 | Macintosh PICT. Mevcut bir görüntü bir belgede korunur, ancak yeni PICT görüntülerinin bir belgeye eklenmesi desteklenmez. |
| Jpeg | 5 | JPEG JFIF. |
| Png | 6 | Taşınabilir Ağ Grafikleri. |
| Bmp | 7 | Windows Bitmap. |
| Eps | 8 | Encapsulated PostScript. |
| WebP | 9 | WebP. |
| Gif | 10 | GIF. |


## Örnekler



Bir şekle görüntü eklemeyi ve türünü kontrol etmeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> imgShape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, imgShape->get_ImageData()->get_ImageType());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
