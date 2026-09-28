---
title: "Aspose::Words::LowCode::Watermarker::SetWatermarkToImages метод"
linktitle: "SetWatermarkToImages"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::LowCode::Watermarker::SetWatermarkToImages метод. Добавляет изображение‑водяной знак в документ с параметрами. Рендерит вывод в изображения в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.lowcode/watermarker/setwatermarktoimages/
---
## Watermarker::SetWatermarkToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Добавляет изображение водяного знака в документ с параметрами. Рендерит вывод в изображения.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Watermarker::SetWatermarkToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::SharedPtr<System::IO::Stream> &watermarkImageStream)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Поток изображения, отображаемый как водяной знак. |

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetWatermarkToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Добавляет изображение водяного знака в документ с параметрами. Рендерит вывод в изображения.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Watermarker::SetWatermarkToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::SharedPtr<System::IO::Stream> &watermarkImageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Поток изображения, отображаемый как водяной знак. |
| параметры | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Определяет дополнительные параметры для изображений водяного знака. |

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetWatermarkToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&) method


Добавляет текстовый водяной знак в документ с параметрами. Рендерит вывод в изображения.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Watermarker::SetWatermarkToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::String &watermarkText)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Поток входного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения. |
| watermarkText | const System::String\& | Текст, отображаемый в виде водяного знака. |

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetWatermarkToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Добавляет текстовый водяной знак в документ с параметрами. Рендерит вывод в изображения.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Watermarker::SetWatermarkToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Поток входного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения. |
| watermarkText | const System::String\& | Текст, отображаемый в виде водяного знака. |
| параметры | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Определяет дополнительные параметры для текстового водяного знака. |

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetWatermarkToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::ArrayPtr\<uint8_t\>\&) method


Добавляет изображение водяного знака в документ с параметрами. Рендерит вывод в изображения.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Watermarker::SetWatermarkToImages(const System::String &inputFileName, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::ArrayPtr<uint8_t> &watermarkImageBytes)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения. |
| watermarkImageBytes | const System::ArrayPtr\<uint8_t\>\& | Байты изображения, отображаемые как водяной знак. |

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetWatermarkToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Добавляет изображение водяного знака в документ с параметрами. Рендерит вывод в изображения.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Watermarker::SetWatermarkToImages(const System::String &inputFileName, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::ArrayPtr<uint8_t> &watermarkImageBytes, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения. |
| watermarkImageBytes | const System::ArrayPtr\<uint8_t\>\& | Байты изображения, отображаемые как водяной знак. |
| параметры | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Определяет дополнительные параметры для изображений водяного знака. |

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetWatermarkToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&) method


Добавляет текстовый водяной знак в документ с параметрами. Рендерит вывод в изображения.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Watermarker::SetWatermarkToImages(const System::String &inputFileName, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::String &watermarkText)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения. |
| watermarkText | const System::String\& | Текст, отображаемый в виде водяного знака. |

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetWatermarkToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Добавляет текстовый водяной знак в документ с параметрами. Рендерит вывод в изображения.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Watermarker::SetWatermarkToImages(const System::String &inputFileName, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения. |
| watermarkText | const System::String\& | Текст, отображаемый в виде водяного знака. |
| параметры | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Определяет дополнительные параметры для текстового водяного знака. |

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
