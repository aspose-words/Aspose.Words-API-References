---
title: "Aspose::Words::DocumentBuilder::InsertImage method"
linktitle: "InsertImage"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::DocumentBuilder::InsertImage. Вставляет изображение из массива байтов в документ. Изображение вставляется встроенно и в масштабе 100 % в C++."
type: docs
weight: 39000
url: /ru/cpp/aspose.words/documentbuilder/insertimage/
---
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&) method


Вставляет изображение из массива байтов в документ. Изображение вставляется встроенно и с масштабом 100%.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | Массив байтов, содержащий изображение. |

### ReturnValue

Узел изображения, который только что был вставлен.
## Примечания


Вы можете изменить размер изображения, его расположение, способ позиционирования и другие параметры, используя объект [Shape](../../../aspose.words.drawing/shape/), возвращаемый этим методом.

## Примеры



Показывает, как вставить изображение из массива байтов в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::ArrayPtr<uint8_t> imageByteArray = Aspose::Words::ApiExamples::TestUtil::ImageToByteArray(get_ImageDir() + u"Logo.jpg");

// Ниже представлены три способа вставки изображения из массива байтов.
// 1 - Встроенная фигура с размером по умолчанию, основанным на оригинальных размерах изображения:
builder->InsertImage(imageByteArray);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Встроенная фигура с пользовательскими размерами:
builder->InsertImage(imageByteArray, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Плавающая фигура с пользовательскими размерами:
builder->InsertImage(imageByteArray, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Вставляет изображение из массива байтов в указанную позицию и размер.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | Массив байтов, содержащий изображение. |
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



Показывает, как вставить изображение из массива байтов в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::ArrayPtr<uint8_t> imageByteArray = Aspose::Words::ApiExamples::TestUtil::ImageToByteArray(get_ImageDir() + u"Logo.jpg");

// Ниже представлены три способа вставки изображения из массива байтов.
// 1 - Встроенная фигура с размером по умолчанию, основанным на оригинальных размерах изображения:
builder->InsertImage(imageByteArray);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Встроенная фигура с пользовательскими размерами:
builder->InsertImage(imageByteArray, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Плавающая фигура с пользовательскими размерами:
builder->InsertImage(imageByteArray, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&, double, double) method


Вставляет встроенное изображение из массива байтов в документ и масштабирует его до указанного размера.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes, double width, double height)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | Массив байтов, содержащий изображение. |
| width | double | Ширина изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |

### ReturnValue

Узел изображения, который только что был вставлен.
## Примечания


Вы можете изменить размер изображения, его расположение, способ позиционирования и другие параметры, используя объект [Shape](../../../aspose.words.drawing/shape/), возвращаемый этим методом.

## Примеры



Показывает, как вставить изображение из массива байтов в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::ArrayPtr<uint8_t> imageByteArray = Aspose::Words::ApiExamples::TestUtil::ImageToByteArray(get_ImageDir() + u"Logo.jpg");

// Ниже представлены три способа вставки изображения из массива байтов.
// 1 - Встроенная фигура с размером по умолчанию, основанным на оригинальных размерах изображения:
builder->InsertImage(imageByteArray);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Встроенная фигура с пользовательскими размерами:
builder->InsertImage(imageByteArray, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Плавающая фигура с пользовательскими размерами:
builder->InsertImage(imageByteArray, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&) method


Вставляет изображение из объекта **Image** в документ. Изображение вставляется встроенно и с масштабом 100%.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| изображение | const System::SharedPtr\<System::Drawing::Image\>\& | Изображение, которое будет вставлено в документ. |

### ReturnValue

Узел изображения, который только что был вставлен.
## Примечания


Вы можете изменить размер изображения, его расположение, способ позиционирования и другие параметры, используя объект [Shape](../../../aspose.words.drawing/shape/), возвращаемый этим методом.

## Примеры



Показывает, как вставить изображение из объекта в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFile = get_ImageDir() + u"Logo.jpg";

// Ниже представлены три способа вставки изображения из экземпляра объекта Image.
// 1 - Встроенная фигура с размером по умолчанию, основанным на оригинальных размерах изображения:
builder->InsertImage(imageFile);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Встроенная фигура с пользовательскими размерами:
builder->InsertImage(imageFile, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Плавающая фигура с пользовательскими размерами:
builder->InsertImage(imageFile, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Вставляет изображение из объекта **Image** в указанную позицию и размер.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| изображение | const System::SharedPtr\<System::Drawing::Image\>\& | Изображение, которое будет вставлено в документ. |
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



Показывает, как вставить изображение из объекта в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFile = get_ImageDir() + u"Logo.jpg";

// Ниже представлены три способа вставки изображения из экземпляра объекта Image.
// 1 - Встроенная фигура с размером по умолчанию, основанным на оригинальных размерах изображения:
builder->InsertImage(imageFile);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Встроенная фигура с пользовательскими размерами:
builder->InsertImage(imageFile, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Плавающая фигура с пользовательскими размерами:
builder->InsertImage(imageFile, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&, double, double) method


Вставляет встроенное изображение из объекта **Image** в документ и масштабирует его до указанного размера.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image, double width, double height)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| изображение | const System::SharedPtr\<System::Drawing::Image\>\& | Изображение, которое будет вставлено в документ. |
| width | double | Ширина изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |

### ReturnValue

Узел изображения, который только что был вставлен.
## Примечания


Вы можете изменить размер изображения, его расположение, способ позиционирования и другие параметры, используя объект [Shape](../../../aspose.words.drawing/shape/), возвращаемый этим методом.

## Примеры



Показывает, как вставить изображение из объекта в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFile = get_ImageDir() + u"Logo.jpg";

// Ниже представлены три способа вставки изображения из экземпляра объекта Image.
// 1 - Встроенная фигура с размером по умолчанию, основанным на оригинальных размерах изображения:
builder->InsertImage(imageFile);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Встроенная фигура с пользовательскими размерами:
builder->InsertImage(imageFile, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Плавающая фигура с пользовательскими размерами:
builder->InsertImage(imageFile, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&) method


Вставляет изображение из потока в документ. Изображение вставляется встроенно и с масштабом 100%.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | Поток, содержащий изображение. |

### ReturnValue

Узел изображения, который только что был вставлен.
## Примечания


Вы можете изменить размер изображения, его расположение, способ позиционирования и другие параметры, используя объект [Shape](../../../aspose.words.drawing/shape/), возвращаемый этим методом.

## Примеры



Показывает, как вставить изображение из потока в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    // Ниже представлены три способа вставки изображения из потока.
    // 1 - Встроенная фигура с размером по умолчанию, основанным на оригинальных размерах изображения:
    builder->InsertImage(stream);

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 2 - Встроенная фигура с пользовательскими размерами:
    builder->InsertImage(stream, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 3 - Плавающая фигура с пользовательскими размерами:
    builder->InsertImage(stream, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromStream.docx");
```


Показывает, как вставить фигуру с изображением из потока в документ.
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

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Вставляет изображение из потока в указанную позицию и размер.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | Поток, содержащий изображение. |
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



Показывает, как вставить изображение из потока в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    // Ниже представлены три способа вставки изображения из потока.
    // 1 - Встроенная фигура с размером по умолчанию, основанным на оригинальных размерах изображения:
    builder->InsertImage(stream);

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 2 - Встроенная фигура с пользовательскими размерами:
    builder->InsertImage(stream, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 3 - Плавающая фигура с пользовательскими размерами:
    builder->InsertImage(stream, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromStream.docx");
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&, double, double) method


Вставляет встроенное изображение из потока в документ и масштабирует его до указанного размера.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream, double width, double height)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | Поток, содержащий изображение. |
| width | double | Ширина изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |

### ReturnValue

Узел изображения, который только что был вставлен.
## Примечания


Вы можете изменить размер изображения, его расположение, способ позиционирования и другие параметры, используя объект [Shape](../../../aspose.words.drawing/shape/), возвращаемый этим методом.

## Примеры



Показывает, как вставить изображение из потока в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    // Ниже представлены три способа вставки изображения из потока.
    // 1 - Встроенная фигура с размером по умолчанию, основанным на оригинальных размерах изображения:
    builder->InsertImage(stream);

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 2 - Встроенная фигура с пользовательскими размерами:
    builder->InsertImage(stream, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 3 - Плавающая фигура с пользовательскими размерами:
    builder->InsertImage(stream, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromStream.docx");
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::String\&) method


Вставляет изображение из файла или URL в документ. Изображение вставляется встроенно и с масштабом 100%.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | const System::String\& | Файл с изображением. Может быть любой действительный локальный или удалённый URI. |

### ReturnValue

Узел изображения, который только что был вставлен.
## Примечания


Эта перегрузка автоматически загрузит изображение перед вставкой в документ, если указать удалённый URI.

Вы можете изменить размер изображения, его расположение, способ позиционирования и другие параметры, используя объект [Shape](../../../aspose.words.drawing/shape/), возвращаемый этим методом.

## Примеры



Показывает, как вставить изображение из локальной файловой системы в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ниже представлены три способа вставки изображения из имени файла локальной системы.
// 1 - Встроенная фигура с размером по умолчанию, основанным на оригинальных размерах изображения:
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Встроенная фигура с пользовательскими размерами:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Плавающая фигура с пользовательскими размерами:
builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```


Показывает, как определить, какое изображение будет вставлено.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"Scalable Vector Graphics.svg");

// Aspose.Words вставляет SVG‑изображение в документ как PNG с расширением svgBlip
// который содержит оригинальное векторное представление SVG‑изображения.
doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

// Aspose.Words вставляет SVG‑изображение в документ как PNG, так же как Microsoft Word делает это для старого формата.
doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertSvgImage.Svg.doc");

doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);

// Aspose.Words вставляет SVG‑изображение в документ в виде EMF‑метафайла, чтобы сохранить изображение в векторном представлении.
doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertSvgImage.Emf.docx");
```


Показывает, как вставить GIF‑изображение в документ.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// Мы можем вставить GIF‑изображение, используя путь или массив байтов.
// Это работает только если DocumentBuilder оптимизирован для версии Word 2010 или выше.
// Обратите внимание, что доступ к байтам изображения приводит к конвертации GIF в PNG.
System::SharedPtr<Aspose::Words::Drawing::Shape> gifImage = builder->InsertImage(get_ImageDir() + u"Graphics Interchange Format.gif");

gifImage = builder->InsertImage(System::IO::File::ReadAllBytes(get_ImageDir() + u"Graphics Interchange Format.gif"));

builder->get_Document()->Save(get_ArtifactsDir() + u"InsertGif.docx");
```


Показывает, как вставить форму с изображением в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ниже приведены два места, откуда метод "InsertShape" построителя документов
// может получать изображение, которое будет отображать форма.
// 1 -  Передайте имя файла изображения из локальной файловой системы:
builder->Write(u"Image from local file: ");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->Writeln();

// 2 -  Передайте URL, указывающий на изображение.
builder->Write(u"Image from a URL: ");
builder->InsertImage(get_ImageUrl());
builder->Writeln();

doc->Save(get_ArtifactsDir() + u"Image.FromUrl.docx");
```


Показывает, как вставить плавающее изображение в центр страницы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте плавающее изображение, которое будет находиться позади перекрывающего текста, и выровняйте его по центру страницы.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```


Показывает, как вставить изображение WebP.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"WebP image.webp");

doc->Save(get_ArtifactsDir() + u"Image.InsertWebpImage.docx");
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Вставляет изображение из файла или URL в указанную позицию и размер.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | const System::String\& | Файл, содержащий изображение. |
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



Показывает, как вставить изображение.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Существует два способа использования построителя документов для получения изображения и последующей вставки его в виде плавающей формы.
// 1 -  Из файла в локальной файловой системе:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 0.0, 200.0, 200.0, Aspose::Words::Drawing::WrapType::Square);

// 2 -  Из URL:
builder->InsertImage(get_ImageUrl(), Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 250.0, 200.0, 200.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFloatingImage.docx");
```


Показывает, как вставить изображение из локальной файловой системы в документ, сохраняя его размеры.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Метод InsertImage создает плавающую форму с переданным изображением в её данных изображения.
// Мы можем указать размеры формы, передав их этому методу.
System::SharedPtr<Aspose::Words::Drawing::Shape> imageShape = builder->InsertImage(get_ImageDir() + u"Logo.jpg", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 0.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 0.0, -1.0, -1.0, Aspose::Words::Drawing::WrapType::Square);

// Передача отрицательных значений в качестве желаемых размеров автоматически определит
// размеры формы на основе размеров её изображения.
ASPOSE_ASSERT_EQ(300.0, imageShape->get_Width());
ASPOSE_ASSERT_EQ(300.0, imageShape->get_Height());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertImageOriginalSize.docx");
```


Показывает, как вставить изображение из локальной файловой системы в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ниже представлены три способа вставки изображения из имени файла локальной системы.
// 1 - Встроенная фигура с размером по умолчанию, основанным на оригинальных размерах изображения:
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Встроенная фигура с пользовательскими размерами:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Плавающая фигура с пользовательскими размерами:
builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::String\&, double, double) method


Вставляет встроенное изображение из файла или URL в документ и масштабирует его до указанного размера.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName, double width, double height)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | const System::String\& | Файл, содержащий изображение. |
| width | double | Ширина изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |

### ReturnValue

Узел изображения, который только что был вставлен.
## Примечания


Вы можете изменить размер изображения, его расположение, способ позиционирования и другие параметры, используя объект [Shape](../../../aspose.words.drawing/shape/), возвращаемый этим методом.

## Примеры



Показывает, как вставить изображение из локальной файловой системы в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ниже представлены три способа вставки изображения из имени файла локальной системы.
// 1 - Встроенная фигура с размером по умолчанию, основанным на оригинальных размерах изображения:
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Встроенная фигура с пользовательскими размерами:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Плавающая фигура с пользовательскими размерами:
builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(std::basic_istream<CharType, Traits> &stream)
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(std::basic_istream\<CharType, Traits\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(std::basic_istream<CharType, Traits> &stream, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```

## См. также

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

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
