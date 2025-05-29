---
title: Comparer.CompareToImages
linktitle: CompareToImages
articleTitle: CompareToImages
second_title: Aspose.Words для .NET
description: С легкостью сравнивайте документы с помощью CompareToImages, сохраняя различия в виде изображений для каждой страницы, что повышает ясность и визуальный анализ.
type: docs
weight: 30
url: /ru/net/aspose.words.lowcode/comparer/comparetoimages/
---
## CompareToImages(*string, string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#comparetoimages_1}

Сравнивает два документа и сохраняет различия в виде изображений. Каждый элемент в возвращаемом массиве представляет собой одну страницу вывода, представленную в виде изображения.

```csharp
public static Stream[] CompareToImages(string v1, string v2, ImageSaveOptions imageSaveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| v1 | String | Оригинальный документ. |
| v2 | String | Измененный документ. |
| imageSaveOptions | ImageSaveOptions | Параметры сохранения выходного изображения. |
| author | String | Инициалы автора для использования при исправлениях. |
| dateTime | DateTime | Дата и время, которые следует использовать для внесения изменений. |
| compareOptions | CompareOptions | Параметры сравнения документов. |

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## CompareToImages(*Stream, Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#comparetoimages}

Сравнивает два документа и сохраняет различия в виде изображений. Каждый элемент в возвращаемом массиве представляет собой одну страницу вывода, представленную в виде изображения.

```csharp
public static Stream[] CompareToImages(Stream v1, Stream v2, ImageSaveOptions imageSaveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| v1 | Stream | Оригинальный документ. |
| v2 | Stream | Измененный документ. |
| imageSaveOptions | ImageSaveOptions | Параметры сохранения выходного изображения. |
| author | String | Инициалы автора для использования при исправлениях. |
| dateTime | DateTime | Дата и время, которые следует использовать для внесения изменений. |
| compareOptions | CompareOptions | Параметры сравнения документов. |

## Примеры

Показывает, как сравнивать документы и сохранять результаты в виде изображений.

```csharp
// Существует несколько способов сравнения документов:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Stream[] pages = Comparer.CompareToImages(firstDoc, secondDoc, new ImageSaveOptions(SaveFormat.Png), "Author", new DateTime());

using (FileStream firstStreamIn = new FileStream(firstDoc, FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(secondDoc, FileMode.Open, FileAccess.Read))
    {
        CompareOptions compareOptions = new CompareOptions();
        compareOptions.IgnoreCaseChanges = true;
        pages = Comparer.CompareToImages(firstStreamIn, secondStreamIn, new ImageSaveOptions(SaveFormat.Png), "Author", new DateTime(), compareOptions);
    }
}
```

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
