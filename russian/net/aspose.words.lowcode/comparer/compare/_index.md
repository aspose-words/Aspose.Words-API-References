---
title: Comparer.Compare
linktitle: Compare
articleTitle: Compare
second_title: Aspose.Words для .NET
description: Легко сравнивайте два документа с помощью нашего метода сравнения. Сохраняйте различия и отслеживайте изменения и редакции формата в одном выходном файле.
type: docs
weight: 20
url: /ru/net/aspose.words.lowcode/comparer/compare/
---
## Compare(*string, string, string, string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_4}

Сравнивает два документа с дополнительными параметрами и сохраняет различия в указанном выходном файле, создавая изменения в виде ряда редакций и редакций формата.

```csharp
public static void Compare(string v1, string v2, string outputFileName, string author, 
    DateTime dateTime, CompareOptions compareOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| v1 | String | Оригинальный документ. |
| v2 | String | Измененный документ. |
| outputFileName | String | Имя выходного файла. |
| author | String | Инициалы автора для использования при исправлениях. |
| dateTime | DateTime | Дата и время, которые следует использовать для внесения изменений. |
| compareOptions | CompareOptions | Параметры сравнения документов. |

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

## Примеры

Показывает, как просто сравнивать документы.

```csharp
// Существует несколько способов сравнения документов:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.1.docx", "Author", new DateTime());
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.2.docx", SaveFormat.Docx, "Author", new DateTime());

CompareOptions compareOptions = new CompareOptions();
compareOptions.IgnoreCaseChanges = true;
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.3.docx", "Author", new DateTime(), compareOptions);
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.4.docx", SaveFormat.Docx, "Author", new DateTime(), compareOptions);
```

### Смотрите также

* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## Compare(*string, string, string, [SaveFormat](../../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_2}

Сравнивает два документа с дополнительными параметрами и сохраняет различия в указанном выходном файле в предоставленном формате сохранения, создавая изменения в виде ряда редакций и редакций формата.

```csharp
public static void Compare(string v1, string v2, string outputFileName, SaveFormat saveFormat, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| v1 | String | Оригинальный документ. |
| v2 | String | Измененный документ. |
| outputFileName | String | Имя выходного файла. |
| saveFormat | SaveFormat | Формат сохранения выходных данных. |
| author | String | Инициалы автора для использования при исправлениях. |
| dateTime | DateTime | Дата и время, которые следует использовать для внесения изменений. |
| compareOptions | CompareOptions | Параметры сравнения документов. |

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

## Примеры

Показывает, как просто сравнивать документы.

```csharp
// Существует несколько способов сравнения документов:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.1.docx", "Author", new DateTime());
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.2.docx", SaveFormat.Docx, "Author", new DateTime());

CompareOptions compareOptions = new CompareOptions();
compareOptions.IgnoreCaseChanges = true;
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.3.docx", "Author", new DateTime(), compareOptions);
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.4.docx", SaveFormat.Docx, "Author", new DateTime(), compareOptions);
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## Compare(*string, string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_3}

Сравнивает два документа с дополнительными параметрами и сохраняет различия в указанном выходном файле в предоставленном формате сохранения, создавая изменения в виде ряда редакций и редакций формата.

```csharp
public static void Compare(string v1, string v2, string outputFileName, SaveOptions saveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| v1 | String | Оригинальный документ. |
| v2 | String | Измененный документ. |
| outputFileName | String | Имя выходного файла. |
| saveOptions | SaveOptions | Параметры сохранения выходных данных. |
| author | String | Инициалы автора для использования при исправлениях. |
| dateTime | DateTime | Дата и время, которые следует использовать для внесения изменений. |
| compareOptions | CompareOptions | Параметры сравнения документов. |

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## Compare(*Stream, Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare}

Сравнивает два документа, загруженных из потоков с дополнительными параметрами, и сохраняет различия в предоставленном выходном потоке в указанном формате сохранения, создавая изменения в виде ряда редакций и редакций формата.

```csharp
public static void Compare(Stream v1, Stream v2, Stream outputStream, SaveFormat saveFormat, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| v1 | Stream | Оригинальный документ. |
| v2 | Stream | Измененный документ. |
| outputStream | Stream | Выходной поток. |
| saveFormat | SaveFormat | Формат сохранения выходных данных. |
| author | String | Инициалы автора для использования при исправлениях. |
| dateTime | DateTime | Дата и время, которые следует использовать для внесения изменений. |
| compareOptions | CompareOptions | Параметры сравнения документов. |

## Примечания

Если выходной формат представляет собой изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), в указанном потоке будет сохранена только первая страница вывода.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый TIFF в указанном потоке.

## Примеры

Показывает, как сравнивать документы из потока.

```csharp
// Существует несколько способов сравнения документов из потока:
using (FileStream firstStreamIn = new FileStream(MyDir + "Table column bookmarks.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Table column bookmarks.doc", FileMode.Open, FileAccess.Read))
    {
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareStreamDocuments.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Comparer.Compare(firstStreamIn, secondStreamIn, streamOut, SaveFormat.Docx, "Author", new DateTime());

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareStreamDocuments.2.docx", FileMode.Create, FileAccess.ReadWrite))
        {
            CompareOptions compareOptions = new CompareOptions();
            compareOptions.IgnoreCaseChanges = true;
            Comparer.Compare(firstStreamIn, secondStreamIn, streamOut, SaveFormat.Docx, "Author", new DateTime(), compareOptions);
        }
    }
}
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## Compare(*Stream, Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_1}

Сравнивает два документа, загруженных из потоков с дополнительными параметрами, и сохраняет различия в предоставленном выходном потоке в указанном формате сохранения, создавая изменения в виде ряда редакций и редакций формата.

```csharp
public static void Compare(Stream v1, Stream v2, Stream outputStream, SaveOptions saveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| v1 | Stream | Оригинальный документ. |
| v2 | Stream | Измененный документ. |
| outputStream | Stream | Выходной поток. |
| saveOptions | SaveOptions | Параметры сохранения выходных данных. |
| author | String | Инициалы автора для использования при исправлениях. |
| dateTime | DateTime | Дата и время, которые следует использовать для внесения изменений. |
| compareOptions | CompareOptions | Параметры сравнения документов. |

## Примечания

Если выходной формат представляет собой изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), в указанном потоке будет сохранена только первая страница вывода.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый TIFF в указанном потоке.

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
