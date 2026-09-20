---
title: "Aspose::Words::DocumentBuilder::InsertOnlineVideo метод"
linktitle: "InsertOnlineVideo"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilder::InsertOnlineVideo метод. Вставляет объект онлайн‑видео в документ и масштабирует его до указанного размера в C++."
type: docs
weight: 43000
url: /ru/cpp/aspose.words/documentbuilder/insertonlinevideo/
---
## DocumentBuilder::InsertOnlineVideo(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Вставляет онлайн‑видео объект в документ и масштабирует его до указанного размера.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| videoUrl | const System::String\& | URL видео. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Указывает, откуда измеряется расстояние до изображения. |
| left | double | Расстояние в пунктах от начала координат до левой стороны изображения. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Указывает, откуда измеряется расстояние до изображения. |
| top | double | Расстояние в пунктах от начала координат до верхней стороны изображения. |
| width | double | Ширина изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| wrapType | Aspose::Words::Drawing::WrapType | Указывает, как обтекать текст вокруг изображения. |

### ReturnValue

Узел изображения, который только что был вставлен.
## Примечания


Вы можете изменить размер изображения, его расположение, способ позиционирования и другие параметры, используя объект [Shape](../../../aspose.words.drawing/shape/), возвращаемый этим методом.

Поддерживается вставка онлайн‑видео из следующих ресурсов:

* [https://www.youtube.com/](https://www.youtube.com/)
* [https://vimeo.com/](https://vimeo.com/)



Если ваше онлайн‑видео отображается некорректно, используйте [InsertOnlineVideo()](../), который принимает пользовательский встроенный HTML‑код.

Код для встраивания видео может различаться у разных провайдеров; обратитесь к выбранному провайдеру за подробностями.

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Вставляет онлайн‑видео объект в документ и масштабирует его до указанного размера.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, const System::String &videoEmbedCode, const System::ArrayPtr<uint8_t> &thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| videoUrl | const System::String\& | URL видео. |
| videoEmbedCode | const System::String\& | Код встраивания видео. |
| thumbnailImageBytes | const System::ArrayPtr\<uint8_t\>\& | Байты изображения миниатюры. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Указывает, откуда измеряется расстояние до изображения. |
| left | double | Расстояние в пунктах от начала координат до левой стороны изображения. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Указывает, откуда измеряется расстояние до изображения. |
| top | double | Расстояние в пунктах от начала координат до верхней стороны изображения. |
| width | double | Ширина изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| wrapType | Aspose::Words::Drawing::WrapType | Указывает, как обтекать текст вокруг изображения. |

### ReturnValue

Узел изображения, который только что был вставлен.
## Примечания


Вы можете изменить размер изображения, его расположение, способ позиционирования и другие параметры, используя объект [Shape](../../../aspose.words.drawing/shape/), возвращаемый этим методом.

## Примеры



Показывает, как вставить онлайн‑видео в документ с пользовательской миниатюрой.
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
        // Ниже представлены два способа создания фигуры с пользовательской миниатюрой, которая ссылается на онлайн‑видео
        // которая будет воспроизводиться, когда мы щёлкнем по фигуре в Microsoft Word.
        // 1 -  Вставьте встроенную фигуру в позицию курсора вставки узла построителя:
        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image->get_Width(), image->get_Height());

        builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

        // 2 -  Вставьте плавающую фигуру:
        double left = builder->get_PageSetup()->get_RightMargin() - image->get_Width();
        double top = builder->get_PageSetup()->get_BottomMargin() - image->get_Height();

        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, left, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, top, image->get_Width(), image->get_Height(), Aspose::Words::Drawing::WrapType::Square);
    }
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, double, double) method


Вставляет онлайн‑видео объект в документ и масштабирует его до указанного размера.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, const System::String &videoEmbedCode, const System::ArrayPtr<uint8_t> &thumbnailImageBytes, double width, double height)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| videoUrl | const System::String\& | URL видео. |
| videoEmbedCode | const System::String\& | Код встраивания видео. |
| thumbnailImageBytes | const System::ArrayPtr\<uint8_t\>\& | Байты изображения миниатюры. |
| width | double | Ширина изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |

### ReturnValue

Узел изображения, который только что был вставлен.
## Примечания


Вы можете изменить размер изображения, его расположение, способ позиционирования и другие параметры, используя объект [Shape](../../../aspose.words.drawing/shape/), возвращаемый этим методом.

## Примеры



Показывает, как вставить онлайн‑видео в документ с пользовательской миниатюрой.
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
        // Ниже представлены два способа создания фигуры с пользовательской миниатюрой, которая ссылается на онлайн‑видео
        // которая будет воспроизводиться, когда мы щёлкнем по фигуре в Microsoft Word.
        // 1 -  Вставьте встроенную фигуру в позицию курсора вставки узла построителя:
        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image->get_Width(), image->get_Height());

        builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

        // 2 -  Вставьте плавающую фигуру:
        double left = builder->get_PageSetup()->get_RightMargin() - image->get_Width();
        double top = builder->get_PageSetup()->get_BottomMargin() - image->get_Height();

        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, left, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, top, image->get_Width(), image->get_Height(), Aspose::Words::Drawing::WrapType::Square);
    }
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, double, double) method


Вставляет онлайн‑видео объект в документ и масштабирует его до указанного размера.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, double width, double height)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| videoUrl | const System::String\& | URL видео. |
| width | double | Ширина изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |

### ReturnValue

Узел изображения, который только что был вставлен.
## Примечания


Вы можете изменить размер изображения, его расположение, способ позиционирования и другие параметры, используя объект [Shape](../../../aspose.words.drawing/shape/), возвращаемый этим методом.

Поддерживается вставка онлайн‑видео из следующих ресурсов:

* [https://www.youtube.com/](https://www.youtube.com/)
* [https://vimeo.com/](https://vimeo.com/)



Если ваше онлайн‑видео отображается некорректно, используйте [InsertOnlineVideo()](../), который принимает пользовательский встроенный HTML‑код.

Код для встраивания видео может различаться у разных провайдеров; обратитесь к выбранному провайдеру за подробностями.

## Примеры



Показывает, как вставить онлайн‑видео в документ, используя URL.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertOnlineVideo(u"https://youtu.be/g1N9ke8Prmk", 360, 270);

// Мы можем просмотреть видео из Microsoft Word, щёлкнув по фигуре.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertVideoWithUrl.docx");
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
