---
title: Replacer.ReplaceToImages
linktitle: ReplaceToImages
articleTitle: ReplaceToImages
second_title: Aspose.Words для .NET
description: С легкостью преобразуйте входные файлы, заменяя шаблоны символов пользовательскими строками и создавая потрясающие изображения с помощью нашего метода ReplaceToImages.
type: docs
weight: 30
url: /ru/net/aspose.words.lowcode/replacer/replacetoimages/
---
## ReplaceToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages_2}

Заменяет все вхождения указанного шаблона строки символов на строку замены во входном файле. Преобразует вывод в изображения.

```csharp
public static Stream[] ReplaceToImages(string inputFileName, ImageSaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| saveOptions | ImageSaveOptions | Параметры сохранения. |
| pattern | String | Строка, подлежащая замене. |
| replacement | String | Строка для замены всех вхождений шаблона. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных опций. |

## Примеры

Показывает, как заменить строку в документе и сохранить результат в виде изображения.

```csharp
// Существует несколько способов заменить строку в документе:
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

Stream[] images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);

FindReplaceOptions options = new FindReplaceOptions();
options.FindWholeWordsOnly = false;
images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, options);
```

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## ReplaceToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages}

Заменяет все вхождения указанного шаблона строки символов на строку замены во входном файле. Преобразует вывод в изображения.

```csharp
public static Stream[] ReplaceToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной файловый поток. |
| saveOptions | ImageSaveOptions | Параметры сохранения. |
| pattern | String | Строка, подлежащая замене. |
| replacement | String | Строка для замены всех вхождений шаблона. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных опций. |

## Примеры

Показывает, как заменить строку в документе, используя документы из потока, и сохранить результат в виде изображений.

```csharp
// Существует несколько способов заменить строку в документе, используя документы из потока:
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

using (FileStream streamIn = new FileStream(MyDir + "Footer.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);

    FindReplaceOptions options = new FindReplaceOptions();
    options.FindWholeWordsOnly = false;
    images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, options);
}
```

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## ReplaceToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages_3}

Заменяет все вхождения указанного шаблона регулярного выражения на строку замены во входном файле. Преобразует вывод в изображения.

```csharp
public static Stream[] ReplaceToImages(string inputFileName, ImageSaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| saveOptions | ImageSaveOptions | Параметры сохранения. |
| pattern | Regex | Шаблон регулярного выражения, используемый для поиска совпадений. |
| replacement | String | Строка для замены всех вхождений шаблона. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных опций. |

## Примеры

Показывает, как заменить строку регулярным выражением в документе и сохранить результат в виде изображения.

```csharp
// Существует несколько способов заменить строку регулярным выражением в документе:
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

Stream[] images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);
images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
```

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## ReplaceToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages_1}

Заменяет все вхождения указанного шаблона регулярного выражения на строку замены во входном файле. Преобразует вывод в изображения.

```csharp
public static Stream[] ReplaceToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной файловый поток. |
| saveOptions | ImageSaveOptions | Параметры сохранения. |
| pattern | Regex | Шаблон регулярного выражения, используемый для поиска совпадений. |
| replacement | String | Строка для замены всех вхождений шаблона. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных опций. |

## Примеры

Показывает, как заменить строку регулярным выражением в документе, используя документы из потока, и сохранить результат в виде изображений.

```csharp
// Существует несколько способов заменить строку регулярным выражением в документе, используя документы из потока:
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

using (FileStream streamIn = new FileStream(MyDir + "Replace regex.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);
    images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
}
```

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
