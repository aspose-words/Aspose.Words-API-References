---
title: ITextShaperFactory.GetTextShaper
linktitle: GetTextShaper
articleTitle: GetTextShaper
second_title: Aspose.Words для .NET
description: ITextShaperFactory GetTextShaper метод. Возвращает новый экземпляр формирователя текста для шрифта указанногоfontPath иfaceIndex  на С#.
type: docs
weight: 10
url: /ru/net/aspose.words.shaping/itextshaperfactory/gettextshaper/
---
## GetTextShaper(*string, int*) {#gettextshaper_1}

Возвращает новый экземпляр формирователя текста для шрифта, указанного*fontPath* и*faceIndex* .

```csharp
public ITextShaper GetTextShaper(string fontPath, int faceIndex)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fontPath | String | Абсолютный путь к файлу шрифта. |
| faceIndex | Int32 | Индекс шрифта в коллекции шрифтов TrueType, или 0, если указанный файл шрифта не является коллекцией шрифтов TrueType. |

### Смотрите также

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* пространство имен [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* сборка [Aspose.Words](../../../)

---

## GetTextShaper(*string, byte[], int*) {#gettextshaper}

Возвращает новый экземпляр формирователя текста для шрифта, представленного*fontBlob* и*faceIndex* .

```csharp
public ITextShaper GetTextShaper(string fontId, byte[] fontBlob, int faceIndex)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fontId | String | Уникальный идентификатор, который может быть однозначно связан с предоставленным шрифтом.*fontBlob* . |
| fontBlob | Byte[] | Байтовый массив с данными шрифта. |
| faceIndex | Int32 | Индекс шрифта в коллекции шрифтов TrueType, или 0, если*fontBlob* не является коллекцией шрифтов TrueType. |

### Смотрите также

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* пространство имен [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* сборка [Aspose.Words](../../../)
