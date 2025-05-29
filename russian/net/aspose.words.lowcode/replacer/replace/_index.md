---
title: Replacer.Replace
linktitle: Replace
articleTitle: Replace
second_title: Aspose.Words для .NET
description: Легко замените все экземпляры определенной строки в вашем входном файле с помощью метода Replacer Replace. Оптимизируйте редактирование текста сегодня!
type: docs
weight: 20
url: /ru/net/aspose.words.lowcode/replacer/replace/
---
## Replace(*string, string, string, string*) {#replace_8}

Заменяет все вхождения указанного шаблона строки символов на заменяющую строку во входном файле.

```csharp
public static int Replace(string inputFileName, string outputFileName, string pattern, 
    string replacement)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |
| pattern | String | Строка, подлежащая замене. |
| replacement | String | Строка для замены всех вхождений шаблона. |

### Возвращаемое значение

Количество произведенных замен.

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

## Примеры

Показывает, как заменить строку в документе.

```csharp
// Существует несколько способов заменить строку в документе:
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

FindReplaceOptions options = new FindReplaceOptions();
options.FindWholeWordsOnly = false;
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.1.docx", pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.2.docx", SaveFormat.Docx, pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.3.docx", SaveFormat.Docx, pattern, replacement, options);
```

### Смотрите также

* class [Replacer](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## Replace(*string, string, [SaveFormat](../../../aspose.words/saveformat/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_4}

Заменяет все вхождения указанного шаблона строки символов заменяющей строкой во входном файле с указанным форматом сохранения и дополнительными параметрами.

```csharp
public static int Replace(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |
| saveFormat | SaveFormat | Формат сохранения. |
| pattern | String | Строка, подлежащая замене. |
| replacement | String | Строка для замены всех вхождений шаблона. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных опций. |

### Возвращаемое значение

Количество произведенных замен.

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

## Примеры

Показывает, как заменить строку в документе.

```csharp
// Существует несколько способов заменить строку в документе:
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

FindReplaceOptions options = new FindReplaceOptions();
options.FindWholeWordsOnly = false;
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.1.docx", pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.2.docx", SaveFormat.Docx, pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.3.docx", SaveFormat.Docx, pattern, replacement, options);
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## Replace(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_6}

Заменяет все вхождения указанного шаблона строки символов заменяющей строкой во входном файле с указанным форматом сохранения и дополнительными параметрами.

```csharp
public static int Replace(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |
| saveOptions | SaveOptions | Параметры сохранения. |
| pattern | String | Строка, подлежащая замене. |
| replacement | String | Строка для замены всех вхождений шаблона. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных опций. |

### Возвращаемое значение

Количество произведенных замен.

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## Replace(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace}

Заменяет все вхождения указанного шаблона строки символов на заменяющую строку во входном потоке с указанным форматом сохранения и дополнительными параметрами.

```csharp
public static int Replace(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной поток. |
| outputStream | Stream | Выходной поток. |
| saveFormat | SaveFormat | Формат сохранения. |
| pattern | String | Строка, подлежащая замене. |
| replacement | String | Строка для замены всех вхождений шаблона. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных опций. |

### Возвращаемое значение

Количество произведенных замен.

## Примечания

Если выходной формат представляет собой изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), в указанном потоке будет сохранена только первая страница вывода.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый TIFF в указанном потоке.

## Примеры

Показывает, как заменить строку в документе, используя документы из потока.

```csharp
// Существует несколько способов заменить строку в документе, используя документы из потока:
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

using (FileStream streamIn = new FileStream(MyDir + "Footer.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Replace(streamIn, streamOut, SaveFormat.Docx, pattern, replacement);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
    {
        FindReplaceOptions options = new FindReplaceOptions();
        options.FindWholeWordsOnly = false;
        Replacer.Replace(streamIn, streamOut, SaveFormat.Docx, pattern, replacement, options);
    }
}
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## Replace(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_2}

Заменяет все вхождения указанного шаблона строки символов на заменяющую строку во входном потоке с указанным форматом сохранения и дополнительными параметрами.

```csharp
public static int Replace(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной поток. |
| outputStream | Stream | Выходной поток. |
| saveOptions | SaveOptions | Параметры сохранения. |
| pattern | String | Строка, подлежащая замене. |
| replacement | String | Строка для замены всех вхождений шаблона. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных опций. |

### Возвращаемое значение

Количество произведенных замен.

## Примечания

Если выходной формат представляет собой изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), в указанном потоке будет сохранена только первая страница вывода.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый TIFF в указанном потоке.

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## Replace(*string, string, Regex, string*) {#replace_9}

Заменяет все вхождения указанного шаблона строки символов на строку замены во входном файле с использованием регулярного выражения.

```csharp
public static int Replace(string inputFileName, string outputFileName, Regex pattern, 
    string replacement)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |
| pattern | Regex | Шаблон регулярного выражения, используемый для поиска совпадений. |
| replacement | String | Строка для замены всех вхождений шаблона. |

### Возвращаемое значение

Количество произведенных замен.

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

## Примеры

Показывает, как заменить строку регулярным выражением в документе.

```csharp
// Существует несколько способов заменить строку регулярным выражением в документе:
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.1.docx", pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.2.docx", SaveFormat.Docx, pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.3.docx", SaveFormat.Docx, pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
```

### Смотрите также

* class [Replacer](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## Replace(*string, string, [SaveFormat](../../../aspose.words/saveformat/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_5}

Заменяет все вхождения указанного шаблона строки символов на строку замены во входном файле, используя регулярное выражение, с указанным форматом сохранения и дополнительными параметрами.

```csharp
public static int Replace(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |
| saveFormat | SaveFormat | Формат сохранения. |
| pattern | Regex | Шаблон регулярного выражения, используемый для поиска совпадений. |
| replacement | String | Строка для замены всех вхождений шаблона. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных опций. |

### Возвращаемое значение

Количество произведенных замен.

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

## Примеры

Показывает, как заменить строку регулярным выражением в документе.

```csharp
// Существует несколько способов заменить строку регулярным выражением в документе:
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.1.docx", pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.2.docx", SaveFormat.Docx, pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.3.docx", SaveFormat.Docx, pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## Replace(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_7}

Заменяет все вхождения указанного шаблона строки символов на строку замены во входном файле, используя регулярное выражение, с указанным форматом сохранения и дополнительными параметрами.

```csharp
public static int Replace(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |
| saveOptions | SaveOptions | Параметры сохранения. |
| pattern | Regex | Шаблон регулярного выражения, используемый для поиска совпадений. |
| replacement | String | Строка для замены всех вхождений шаблона. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных опций. |

### Возвращаемое значение

Количество произведенных замен.

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## Replace(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_1}

Заменяет все вхождения указанного шаблона строки символов на строку замены во входном потоке, используя регулярное выражение, с указанным форматом сохранения и дополнительными параметрами.

```csharp
public static int Replace(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной поток. |
| outputStream | Stream | Выходной поток. |
| saveFormat | SaveFormat | Формат сохранения. |
| pattern | Regex | Шаблон регулярного выражения, используемый для поиска совпадений. |
| replacement | String | Строка для замены всех вхождений шаблона. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных опций. |

### Возвращаемое значение

Количество произведенных замен.

## Примечания

Если выходной формат представляет собой изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), в указанном потоке будет сохранена только первая страница вывода.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый TIFF в указанном потоке.

## Примеры

Показывает, как заменить строку регулярным выражением в документе, используя документы из потока.

```csharp
// Существует несколько способов заменить строку регулярным выражением в документе, используя документы из потока:
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

using (FileStream streamIn = new FileStream(MyDir + "Replace regex.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceStreamRegex.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Replace(streamIn, streamOut, SaveFormat.Docx, pattern, replacement);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceStreamRegex.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Replace(streamIn, streamOut, SaveFormat.Docx, pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
}
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## Replace(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_3}

Заменяет все вхождения указанного шаблона строки символов на строку замены во входном потоке, используя регулярное выражение, с указанным форматом сохранения и дополнительными параметрами.

```csharp
public static int Replace(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной поток. |
| outputStream | Stream | Выходной поток. |
| saveOptions | SaveOptions | Параметры сохранения. |
| pattern | Regex | Шаблон регулярного выражения, используемый для поиска совпадений. |
| replacement | String | Строка для замены всех вхождений шаблона. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных опций. |

### Возвращаемое значение

Количество произведенных замен.

## Примечания

Если выходной формат представляет собой изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), в указанном потоке будет сохранена только первая страница вывода.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый TIFF в указанном потоке.

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
