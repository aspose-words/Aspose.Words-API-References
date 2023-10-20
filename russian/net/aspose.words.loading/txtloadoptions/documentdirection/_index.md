---
title: TxtLoadOptions.DocumentDirection
linktitle: DocumentDirection
articleTitle: DocumentDirection
second_title: Aspose.Words для .NET
description: TxtLoadOptions DocumentDirection свойство. Получает или задает направление документа. Значение по умолчаниюLeftToRight  на С#.
type: docs
weight: 40
url: /ru/net/aspose.words.loading/txtloadoptions/documentdirection/
---
## TxtLoadOptions.DocumentDirection property

Получает или задает направление документа. Значение по умолчанию:LeftToRight .

```csharp
public DocumentDirection DocumentDirection { get; set; }
```

## Примеры

Показывает, как определить направление текста документа в виде открытого текста.

```csharp
// Создаем объект «TxtLoadOptions», который мы можем передать конструктору документа
// чтобы изменить способ загрузки открытого текстового документа.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Установите для свойства «DocumentDirection» значение «DocumentDirection.Auto», автоматически обнаруживает
// направление каждого абзаца текста, который Aspose.Words загружает из открытого текста.
// Свойство Bidi каждого абзаца сохранит направление.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// Обнаружить текст на иврите как написанный справа налево.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// Обнаружение текста на английском языке как справа налево.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

### Смотрите также

* enum [DocumentDirection](../../documentdirection/)
* class [TxtLoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
