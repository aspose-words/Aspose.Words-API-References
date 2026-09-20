---
title: "Aspose::Words::Drawing::ImageType enum"
linktitle: "ImageType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ImageType enum. Указывает тип (формат) изображения в документе Microsoft Word на C++."
type: docs
weight: 28000
url: /ru/cpp/aspose.words.drawing/imagetype/
---
## ImageType enum


Указывает тип (формат) изображения в документе Microsoft Word.

```cpp
enum class ImageType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| NoImage | 0 | Нет данных изображения. |
| Неизвестно | 1 | Неизвестный тип изображения или тип изображения, который нельзя напрямую сохранить в документе Microsoft Word. |
| Emf | 2 | Windows Enhanced Metafile. |
| Wmf | 3 | Windows Metafile. |
| Pict | 4 | Macintosh PICT. Существующее изображение будет сохранено в документе, но вставка новых изображений PICT в документ не поддерживается. |
| Jpeg | 5 | JPEG JFIF. |
| Png | 6 | Portable Network Graphics. |
| Bmp | 7 | Windows Bitmap. |
| Eps | 8 | Encapsulated PostScript. |
| WebP | 9 | WebP. |
| Gif | 10 | GIF. |


## Примеры



Показывает, как добавить изображение в форму и проверить её тип.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> imgShape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, imgShape->get_ImageData()->get_ImageType());
```

## См. также

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
