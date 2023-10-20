---
title: StructuredDocumentTag.IsTemporary
linktitle: IsTemporary
articleTitle: IsTemporary
second_title: Aspose.Words для .NET
description: StructuredDocumentTag IsTemporary свойство. Указывает является ли этоСДТ должен быть удален из документа WordProcessingML при изменении его содержимого  на С#.
type: docs
weight: 160
url: /ru/net/aspose.words.markup/structureddocumenttag/istemporary/
---
## StructuredDocumentTag.IsTemporary property

Указывает, является ли это**СДТ** должен быть удален из документа WordProcessingML при изменении его содержимого .

```csharp
public bool IsTemporary { get; set; }
```

## Примеры

Показывает, как сделать одноразовые элементы управления.

```csharp
Document doc = new Document();

// Вставляем тег структурированного документа в виде простого текста,
// который будет действовать как обычная текстовая форма, в которую пользователь может вводить текст.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Установите для свойства IsTemporary значение true, чтобы тег структурированного документа исчез и
// ассимилируем его содержимое в документ после того, как пользователь один раз отредактирует его в Microsoft Word.
// Установите для свойства IsTemporary значение «false», чтобы позволить пользователю редактировать содержимое
// тега структурированного документа любое количество раз.
tag.IsTemporary = isTemporary;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Please enter text: ");
builder.InsertNode(tag);

// Вставляем еще один тег структурированного документа в виде флажка и устанавливаем для него состояние по умолчанию «отмечено».
tag = new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline);
tag.Checked = true;

// Установите для свойства IsTemporary значение true, чтобы флажок стал символом
// как только пользователь нажмет на него в Microsoft Word.
// Установите для свойства IsTemporary значение false, чтобы пользователь мог щелкнуть флажок любое количество раз.
tag.IsTemporary = isTemporary;

builder.Write("\nPlease click the check box: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IsTemporary.docx");
```

### Смотрите также

* class [StructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
