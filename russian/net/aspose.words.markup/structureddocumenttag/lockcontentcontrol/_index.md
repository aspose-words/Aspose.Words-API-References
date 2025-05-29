---
title: StructuredDocumentTag.LockContentControl
linktitle: LockContentControl
articleTitle: LockContentControl
second_title: Aspose.Words для .NET
description: Узнайте, как свойство StructuredDocumentTag LockContentControl повышает безопасность документа, не давая пользователям удалять важный контент. Узнайте больше!
type: docs
weight: 190
url: /ru/net/aspose.words.markup/structureddocumenttag/lockcontentcontrol/
---
## StructuredDocumentTag.LockContentControl property

При установке на`истинный` , это свойство запретит пользователю удалять это**СДТ** .

```csharp
public bool LockContentControl { get; set; }
```

## Примеры

Показывает, как применять ограничения редактирования к структурированным тегам документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте структурированный тег документа с простым текстом, который действует как текстовое поле, предлагающее пользователю заполнить его.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Установите свойство «LockContents» в значение «true», чтобы запретить пользователю редактировать содержимое этого текстового поля.
tag.LockContents = true;
builder.Write("The contents of this structured document tag cannot be edited: ");
builder.InsertNode(tag);

tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Установите свойство "LockContentControl" в значение "true", чтобы запретить пользователю
// удаление этого структурированного тега документа вручную в Microsoft Word.
tag.LockContentControl = true;

builder.InsertParagraph();
builder.Write("This structured document tag cannot be deleted but its contents can be edited: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Lock.docx");
```

### Смотрите также

* class [StructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
