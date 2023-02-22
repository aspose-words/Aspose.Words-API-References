---
title: StructuredDocumentTag.IsTemporary
second_title: Справочник по API Aspose.Words для .NET
description: StructuredDocumentTag свойство. Указывает является ли это СДТ должен быть удален из документа WordProcessingML при изменении его содержимого .
type: docs
weight: 160
url: /ru/net/aspose.words.markup/structureddocumenttag/istemporary/
---
## StructuredDocumentTag.IsTemporary property

Указывает, является ли это **СДТ** должен быть удален из документа WordProcessingML при изменении его содержимого .

```csharp
public bool IsTemporary { get; set; }
```

### Примеры

Показывает, как сделать одноразовые элементы управления.

```csharp
Document doc = new Document();

// Вставляем простой текстовый структурированный тег документа,
// который будет действовать как простая текстовая форма, в которую пользователь может вводить текст.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Установите для свойства "IsTemporary" значение "true", чтобы тег структурированного документа исчез и
// ассимилировать его содержимое в документ после того, как пользователь отредактирует его один раз в Microsoft Word.
// Установите для свойства "IsTemporary" значение "false", чтобы позволить пользователю редактировать содержимое
// тега структурированного документа любое количество раз.
tag.IsTemporary = isTemporary;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Please enter text: ");
builder.InsertNode(tag);

// Вставьте еще один тег структурированного документа в виде флажка и установите для него состояние по умолчанию «отмечено».
tag = new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline);
tag.Checked = true;

// Установите для свойства "IsTemporary" значение "true", чтобы флажок стал символом
// как только пользователь щелкнет по нему в Microsoft Word.
// Установите для свойства "IsTemporary" значение "false", чтобы разрешить пользователю щелкать по флажку любое количество раз.
tag.IsTemporary = isTemporary;

builder.Write("\nPlease click the check box: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IsTemporary.docx");
```

### Смотрите также

* class [StructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../structureddocumenttag/)
* сборка [Aspose.Words](../../../)


