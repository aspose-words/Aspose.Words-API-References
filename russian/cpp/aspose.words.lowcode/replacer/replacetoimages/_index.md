---
title: "Aspose::Words::LowCode::Replacer::ReplaceToImages метод"
linktitle: "ReplaceToImages"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::LowCode::Replacer::ReplaceToImages метод. Заменяет все вхождения указанного шаблона регулярного выражения на строку замены во входном файле. Выводит результат в виде изображений в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.lowcode/replacer/replacetoimages/
---
## Replacer::ReplaceToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Заменяет все вхождения указанного шаблона регулярного выражения на строку‑заменитель во входном файле. Выводит результат в виде изображений.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Replacer::ReplaceToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Поток входного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения. |
| шаблон | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Шаблон регулярного выражения, используемый для поиска совпадений. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::ReplaceToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Заменяет все вхождения указанного шаблона регулярного выражения на строку‑заменитель во входном файле. Выводит результат в виде изображений.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Replacer::ReplaceToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Поток входного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения. |
| шаблон | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Шаблон регулярного выражения, используемый для поиска совпадений. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных параметров. |

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::ReplaceToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&) method


Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель во входном файле. Выводит результат в виде изображений.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Replacer::ReplaceToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Поток входного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения. |
| шаблон | const System::String\& | Строка, которую нужно заменить. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::ReplaceToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель во входном файле. Выводит результат в виде изображений.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Replacer::ReplaceToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Поток входного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения. |
| шаблон | const System::String\& | Строка, которую нужно заменить. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных параметров. |

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::ReplaceToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Заменяет все вхождения указанного шаблона регулярного выражения на строку‑заменитель во входном файле. Выводит результат в виде изображений.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Replacer::ReplaceToImages(const System::String &inputFileName, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения. |
| шаблон | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Шаблон регулярного выражения, используемый для поиска совпадений. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::ReplaceToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Заменяет все вхождения указанного шаблона регулярного выражения на строку‑заменитель во входном файле. Выводит результат в виде изображений.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Replacer::ReplaceToImages(const System::String &inputFileName, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения. |
| шаблон | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Шаблон регулярного выражения, используемый для поиска совпадений. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных параметров. |

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::ReplaceToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&) method


Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель во входном файле. Выводит результат в виде изображений.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Replacer::ReplaceToImages(const System::String &inputFileName, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения. |
| шаблон | const System::String\& | Строка, которую нужно заменить. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::ReplaceToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель во входном файле. Выводит результат в виде изображений.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Replacer::ReplaceToImages(const System::String &inputFileName, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения. |
| шаблон | const System::String\& | Строка, которую нужно заменить. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных параметров. |

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
