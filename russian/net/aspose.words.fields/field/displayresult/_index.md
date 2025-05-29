---
title: Field.DisplayResult
linktitle: DisplayResult
articleTitle: DisplayResult
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Field DisplayResult, которое предоставляет текст для отображаемых результатов поля, повышая ясность и удобство использования.
type: docs
weight: 10
url: /ru/net/aspose.words.fields/field/displayresult/
---
## Field.DisplayResult property

Получает текст, представляющий отображаемый результат поля.

```csharp
public string DisplayResult { get; }
```

## Примечания

[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) необходимо вызвать метод для получения правильного значения для the [`FieldListNum`](../../fieldlistnum/) ,[`FieldAutoNum`](../../fieldautonum/) ,[`FieldAutoNumOut`](../../fieldautonumout/) и[`FieldAutoNumLgl`](../../fieldautonumlgl/) поля.

## Примеры

Показывает, как получить реальный текст, отображаемый полем в документе.

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
// Чтобы убедиться, что наши поля отображают точные результаты в любой момент времени,
// например, прямо перед операцией сохранения, нам необходимо обновить их вручную.
fieldAuthor.Update();

Assert.AreEqual("John Doe", fieldAuthor.DisplayResult);

doc.Save(ArtifactsDir + "Field.DisplayResult.docx");
```

### Смотрите также

* class [Field](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
