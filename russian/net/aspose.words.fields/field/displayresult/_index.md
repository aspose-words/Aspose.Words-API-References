---
title: Field.DisplayResult
linktitle: DisplayResult
articleTitle: DisplayResult
second_title: Aspose.Words для .NET
description: Field DisplayResult свойство. Получает текст представляющий результат отображаемого поля на С#.
type: docs
weight: 10
url: /ru/net/aspose.words.fields/field/displayresult/
---
## Field.DisplayResult property

Получает текст, представляющий результат отображаемого поля.

```csharp
public string DisplayResult { get; }
```

## Примечания

[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) необходимо вызвать метод, чтобы получить правильное значение для the [`FieldListNum`](../../fieldlistnum/) ,[`FieldAutoNum`](../../fieldautonum/) ,[`FieldAutoNumOut`](../../fieldautonumout/) и[`FieldAutoNumLgl`](../../fieldautonumlgl/) поля.

## Примеры

Показывает, как получить реальный текст, отображаемый в поле документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This document was written by ");
FieldAuthor fieldAuthor = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
fieldAuthor.AuthorName = "John Doe";

// Мы можем использовать свойство DisplayResult, чтобы проверить, какой именно текст
// поле будет отображаться на своем месте в документе.
Assert.AreEqual(string.Empty, fieldAuthor.DisplayResult);

 // Поля не поддерживают точные значения результатов в режиме реального времени.
// Чтобы наши поля отображали точные результаты в любой момент времени,
// например, прямо перед операцией сохранения, нам нужно обновить их вручную.
fieldAuthor.Update();

Assert.AreEqual("John Doe", fieldAuthor.DisplayResult);

doc.Save(ArtifactsDir + "Field.DisplayResult.docx");
```

### Смотрите также

* class [Field](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
