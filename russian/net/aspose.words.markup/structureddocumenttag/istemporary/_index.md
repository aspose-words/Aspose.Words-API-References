---
title: StructuredDocumentTag.IsTemporary
linktitle: IsTemporary
articleTitle: IsTemporary
second_title: Aspose.Words для .NET
description: Узнайте, как свойство StructuredDocumentTag IsTemporary определяет, удаляется ли ваш SDT из WordProcessingML при изменении контента. Оптимизируйте свои документы сегодня!
type: docs
weight: 160
url: /ru/net/aspose.words.markup/structureddocumenttag/istemporary/
---
## StructuredDocumentTag.IsTemporary property

Указывает, является ли это**СДТ** должны быть удалены из документа WordProcessingML при изменении его содержимого .

```csharp
public bool IsTemporary { get; set; }
```

## Примеры

Показывает, как изготавливать одноразовые элементы управления.

```csharp
Document doc = new Document();

// Вставьте структурированный тег документа в виде простого текста,
// которая будет действовать как простая текстовая форма, в которую пользователь может ввести текст.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Установите свойство "IsTemporary" в значение "true", чтобы тег структурированного документа исчез и
// ассимилировать его содержимое в документ после того, как пользователь отредактирует его один раз в Microsoft Word.
// Установите свойство "IsTemporary" в значение "false", чтобы разрешить пользователю редактировать содержимое
// структурированного тега документа любое количество раз.
tag.IsTemporary = isTemporary;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Please enter text: ");
builder.InsertNode(tag);

// Вставьте еще один структурированный тег документа в виде флажка и установите его состояние по умолчанию на «отмечено».
tag = new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline);
tag.Checked = true;

// Установите свойство "IsTemporary" в значение "true", чтобы флажок стал символом
// как только пользователь нажмет на него в Microsoft Word.
// Установите свойство «IsTemporary» в значение «false», чтобы разрешить пользователю нажимать на флажок любое количество раз.
tag.IsTemporary = isTemporary;

builder.Write("\nPlease click the check box: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IsTemporary.docx");
```

### Смотрите также

* class [StructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
