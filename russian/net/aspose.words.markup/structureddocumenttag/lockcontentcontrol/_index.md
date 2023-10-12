---
title: StructuredDocumentTag.LockContentControl
second_title: Справочник по API Aspose.Words для .NET
description: StructuredDocumentTag свойство. Если установлено значениеистинный  это свойство запретит пользователю удалять это СДТ .
type: docs
weight: 190
url: /ru/net/aspose.words.markup/structureddocumenttag/lockcontentcontrol/
---
## StructuredDocumentTag.LockContentControl property

Если установлено значение`истинный` , это свойство запретит пользователю удалять это **СДТ** .

```csharp
public bool LockContentControl { get; set; }
```

### Примеры

Показывает, как применить ограничения редактирования к тегам структурированного документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте тег структурированного документа в виде простого текста, который действует как текстовое поле, предлагающее пользователю его заполнить.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Установите для свойства «LockContents» значение «true», чтобы запретить пользователю редактировать содержимое этого текстового поля.
tag.LockContents = true;
builder.Write("The contents of this structured document tag cannot be edited: ");
builder.InsertNode(tag);

tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Установите для свойства «LockContentControl» значение «true», чтобы запретить пользователю
// удаление этого тега структурированного документа вручную в Microsoft Word.
tag.LockContentControl = true;

builder.InsertParagraph();
builder.Write("This structured document tag cannot be deleted but its contents can be edited: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Lock.docx");
```

### Смотрите также

* class [StructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../structureddocumenttag/)
* сборка [Aspose.Words](../../../)


