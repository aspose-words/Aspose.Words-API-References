---
title: "Aspose::Words::LowCode::Replacer::Replace метод"
linktitle: "Replace"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::LowCode::Replacer::Replace метод. Заменяет все вхождения указанного строкового шаблона на строку замены во входном потоке с использованием регулярного выражения, с указанным форматом сохранения и дополнительными параметрами в C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.lowcode/replacer/replace/
---
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель во входном потоке, используя регулярное выражение, с указанным форматом сохранения и дополнительными параметрами.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. |
| шаблон | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Шаблон регулярного выражения, используемый для поиска совпадений. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |

### ReturnValue

Количество выполненных замен.
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель во входном потоке, используя регулярное выражение, с указанным форматом сохранения и дополнительными параметрами.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. |
| шаблон | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Шаблон регулярного выражения, используемый для поиска совпадений. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных параметров. |

### ReturnValue

Количество выполненных замен.
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) method


Заменяет все вхождения указанного строкового шаблона на строку‑замену во входном потоке, используя указанный формат сохранения и дополнительные параметры.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. |
| шаблон | const System::String\& | Строка, которую нужно заменить. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |

### ReturnValue

Количество выполненных замен.
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Заменяет все вхождения указанного строкового шаблона на строку‑замену во входном потоке, используя указанный формат сохранения и дополнительные параметры.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. |
| шаблон | const System::String\& | Строка, которую нужно заменить. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных параметров. |

### ReturnValue

Количество выполненных замен.
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель во входном потоке, используя регулярное выражение, с указанным форматом сохранения и дополнительными параметрами.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения. |
| шаблон | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Шаблон регулярного выражения, используемый для поиска совпадений. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |

### ReturnValue

Количество выполненных замен.
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель во входном потоке, используя регулярное выражение, с указанным форматом сохранения и дополнительными параметрами.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения. |
| шаблон | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Шаблон регулярного выражения, используемый для поиска совпадений. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных параметров. |

### ReturnValue

Количество выполненных замен.
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) method


Заменяет все вхождения указанного строкового шаблона на строку‑замену во входном потоке, используя указанный формат сохранения и дополнительные параметры.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения. |
| шаблон | const System::String\& | Строка, которую нужно заменить. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |

### ReturnValue

Количество выполненных замен.
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Заменяет все вхождения указанного строкового шаблона на строку‑замену во входном потоке, используя указанный формат сохранения и дополнительные параметры.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения. |
| шаблон | const System::String\& | Строка, которую нужно заменить. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных параметров. |

### ReturnValue

Количество выполненных замен.
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель во входном файле, используя регулярное выражение, с указанным форматом сохранения и дополнительными параметрами.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| outputFileName | const System::String\& | Имя выходного файла. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. |
| шаблон | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Шаблон регулярного выражения, используемый для поиска совпадений. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |

### ReturnValue

Количество выполненных замен.
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель во входном файле, используя регулярное выражение, с указанным форматом сохранения и дополнительными параметрами.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| outputFileName | const System::String\& | Имя выходного файла. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. |
| шаблон | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Шаблон регулярного выражения, используемый для поиска совпадений. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных параметров. |

### ReturnValue

Количество выполненных замен.
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) method


Заменяет все вхождения указанного строкового шаблона на строку‑замену во входном файле, используя указанный формат сохранения и дополнительные параметры.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| outputFileName | const System::String\& | Имя выходного файла. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. |
| шаблон | const System::String\& | Строка, которую нужно заменить. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |

### ReturnValue

Количество выполненных замен.
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Заменяет все вхождения указанного строкового шаблона на строку‑замену во входном файле, используя указанный формат сохранения и дополнительные параметры.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| outputFileName | const System::String\& | Имя выходного файла. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. |
| шаблон | const System::String\& | Строка, которую нужно заменить. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных параметров. |

### ReturnValue

Количество выполненных замен.
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель во входном файле, используя регулярное выражение, с указанным форматом сохранения и дополнительными параметрами.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| outputFileName | const System::String\& | Имя выходного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения. |
| шаблон | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Шаблон регулярного выражения, используемый для поиска совпадений. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |

### ReturnValue

Количество выполненных замен.
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель во входном файле, используя регулярное выражение, с указанным форматом сохранения и дополнительными параметрами.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| outputFileName | const System::String\& | Имя выходного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения. |
| шаблон | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Шаблон регулярного выражения, используемый для поиска совпадений. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных параметров. |

### ReturnValue

Количество выполненных замен.
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) method


Заменяет все вхождения указанного строкового шаблона на строку‑замену во входном файле, используя указанный формат сохранения и дополнительные параметры.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| outputFileName | const System::String\& | Имя выходного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения. |
| шаблон | const System::String\& | Строка, которую нужно заменить. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |

### ReturnValue

Количество выполненных замен.
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Заменяет все вхождения указанного строкового шаблона на строку‑замену во входном файле, используя указанный формат сохранения и дополнительные параметры.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| outputFileName | const System::String\& | Имя выходного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения. |
| шаблон | const System::String\& | Строка, которую нужно заменить. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных параметров. |

### ReturnValue

Количество выполненных замен.
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Заменяет все вхождения указанного строкового шаблона на строку‑замену во входном файле с использованием регулярного выражения.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| outputFileName | const System::String\& | Имя выходного файла. |
| шаблон | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Шаблон регулярного выражения, используемый для поиска совпадений. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |

### ReturnValue

Количество выполненных замен.
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::String\&, const System::String\&) method


Заменяет все вхождения указанного строкового шаблона на строку‑замену во входном файле.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::String &pattern, const System::String &replacement)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| outputFileName | const System::String\& | Имя выходного файла. |
| шаблон | const System::String\& | Строка, которую нужно заменить. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |

### ReturnValue

Количество выполненных замен.
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
