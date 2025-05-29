---
title: Splitter.RemoveBlankPages
linktitle: RemoveBlankPages
articleTitle: RemoveBlankPages
second_title: Aspose.Words для .NET
description: Без усилий удаляйте пустые страницы из ваших документов с помощью метода Splitter RemoveBlankPages. Экономьте время и улучшайте свой рабочий процесс уже сегодня!
type: docs
weight: 30
url: /ru/net/aspose.words.lowcode/splitter/removeblankpages/
---
## RemoveBlankPages(*string, string*) {#removeblankpages_2}

Удаляет пустые страницы из документа и сохраняет вывод. Возвращает список номеров страниц, которые были удалены.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |

### Возвращаемое значение

Список номеров страниц был признан пустым и удален.

## Примеры

Показывает, как удалить пустые страницы из документа.

```csharp
// Удалить пустые страницы из документа можно несколькими способами:
string doc = MyDir + "Blank pages.docx";

Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.1.docx");
Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.2.docx", SaveFormat.Docx);
```

### Смотрите также

* class [Splitter](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## RemoveBlankPages(*string, string, [SaveFormat](../../../aspose.words/saveformat/)*) {#removeblankpages_3}

Удаляет пустые страницы из документа и сохраняет вывод в указанном формате. Возвращает список номеров страниц, которые были удалены.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName, 
    SaveFormat saveFormat)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |
| saveFormat | SaveFormat | Формат сохранения. |

### Возвращаемое значение

Список номеров страниц был признан пустым и удален.

## Примеры

Показывает, как удалить пустые страницы из документа.

```csharp
// Удалить пустые страницы из документа можно несколькими способами:
string doc = MyDir + "Blank pages.docx";

Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.1.docx");
Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.2.docx", SaveFormat.Docx);
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## RemoveBlankPages(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#removeblankpages_4}

Удаляет пустые страницы из документа и сохраняет вывод в указанном формате. Возвращает список номеров страниц, которые были удалены.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName, 
    SaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |
| saveOptions | SaveOptions | Параметры сохранения. |

### Возвращаемое значение

Список номеров страниц был признан пустым и удален.

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## RemoveBlankPages(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#removeblankpages}

Удаляет пустые страницы из документа, предоставленного во входном потоке, и сохраняет обновленный документ в выходном потоке в указанном формате сохранения. Возвращает список номеров страниц, которые были удалены.

```csharp
public static List<int> RemoveBlankPages(Stream inputStream, Stream outputStream, 
    SaveFormat saveFormat)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной поток. |
| outputStream | Stream | Выходной поток. |
| saveFormat | SaveFormat | Формат сохранения. |

### Возвращаемое значение

Список номеров страниц был признан пустым и удален.

## Примеры

Показывает, как удалить пустые страницы из документа из потока.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Blank pages.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.RemoveBlankPagesStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Splitter.RemoveBlankPages(streamIn, streamOut, SaveFormat.Docx);
}
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## RemoveBlankPages(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#removeblankpages_1}

Удаляет пустые страницы из документа, предоставленного во входном потоке, и сохраняет обновленный документ в выходном потоке в указанном формате сохранения. Возвращает список номеров страниц, которые были удалены.

```csharp
public static List<int> RemoveBlankPages(Stream inputStream, Stream outputStream, 
    SaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной поток. |
| outputStream | Stream | Выходной поток. |
| saveOptions | SaveOptions | Параметры сохранения. |

### Возвращаемое значение

Список номеров страниц был признан пустым и удален.

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
