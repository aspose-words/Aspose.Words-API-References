---
title: "Aspose::Words::LowCode::Converter::ConvertToImages метод"
linktitle: "ConvertToImages"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::LowCode::Converter::ConvertToImages метод. Преобразует страницы указанного документа в изображения в заданном формате и возвращает массив потоков, содержащих изображения, в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.lowcode/converter/converttoimages/
---
## Converter::ConvertToImages(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::SaveFormat) method


Преобразует страницы указанного документа в изображения в заданном формате и возвращает массив потоков, содержащих изображения.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<Aspose::Words::Document> &doc, Aspose::Words::SaveFormat saveFormat)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| док | const System::SharedPtr\<Aspose::Words::Document\>\& | Входной документ. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. Разрешены только форматы сохранения изображений. |

### ReturnValue

Возвращает массив потоков изображений. Потоки должны быть освобождены конечным пользователем.

## См. также

* Class [Document](../../../aspose.words/document/)
* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Преобразует страницы указанного документа в изображения, используя заданные параметры сохранения, и возвращает массив потоков, содержащих изображения.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<Aspose::Words::Document> &doc, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| док | const System::SharedPtr\<Aspose::Words::Document\>\& | Входной документ. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения изображения. |

### ReturnValue

Возвращает массив потоков изображений. Потоки должны быть освобождены конечным пользователем.

## См. также

* Class [Document](../../../aspose.words/document/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


Преобразует страницы указанного входного потока в изображения в заданном формате и возвращает массив потоков, содержащих изображения.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, Aspose::Words::SaveFormat saveFormat)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. Разрешены только форматы сохранения изображений. |

### ReturnValue

Возвращает массив потоков изображений. Потоки должны быть освобождены конечным пользователем.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Преобразует страницы указанного входного потока в изображения, используя предоставленные параметры загрузки и сохранения, и возвращает массив потоков, содержащих изображения.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Параметры загрузки входного документа. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения изображения. |

### ReturnValue

Возвращает массив потоков изображений. Потоки должны быть освобождены конечным пользователем.

## См. также

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Преобразует страницы указанного входного потока в изображения, используя заданные параметры сохранения, и возвращает массив потоков, содержащих изображения.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения изображения. |

### ReturnValue

Возвращает массив потоков изображений. Потоки должны быть освобождены конечным пользователем.

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, Aspose::Words::SaveFormat) method


Преобразует страницы указанного входного файла в изображения в заданном формате и возвращает массив потоков, содержащих изображения.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, Aspose::Words::SaveFormat saveFormat)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | const System::String\& | Имя входного файла. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. Разрешены только форматы сохранения изображений. |

### ReturnValue

Возвращает массив потоков изображений. Потоки должны быть освобождены конечным пользователем.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Преобразует страницы указанного входного файла в файлы изображений, используя предоставленные параметры загрузки и сохранения.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | const System::String\& | Имя входного файла. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Параметры загрузки входного документа. |
| outputFile | const System::String\& | Имя выходного файла, используемое для генерации имени файла страниц изображений по правилу "outputFile_pageIndex.extension" |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения изображения. |

## См. также

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Преобразует страницы указанного входного файла в изображения, используя заданные параметры сохранения, и возвращает массив потоков, содержащих изображения.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | const System::String\& | Имя входного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения изображения. |

### ReturnValue

Возвращает массив потоков изображений. Потоки должны быть освобождены конечным пользователем.

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&) method


Преобразует страницы указанного входного файла в файлы изображений.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | const System::String\& | Имя входного файла. |
| outputFile | const System::String\& | Имя выходного файла, используемое для генерации имени файла страниц изображений по правилу "outputFile_pageIndex.extension" |

## См. также

* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) method


Преобразует страницы указанного входного файла в файлы изображений в заданном формате.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile, Aspose::Words::SaveFormat saveFormat)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | const System::String\& | Имя входного файла. |
| outputFile | const System::String\& | Имя выходного файла, используемое для генерации имени файла страниц изображений по правилу "outputFile_pageIndex.extension" |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. Разрешены только форматы сохранения изображений. |

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Преобразует страницы указанного входного файла в файлы изображений, используя заданные параметры сохранения.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | const System::String\& | Имя входного файла. |
| outputFile | const System::String\& | Имя выходного файла, используемое для генерации имени файла страниц изображений по правилу "outputFile_pageIndex.extension" |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения изображения. |

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
