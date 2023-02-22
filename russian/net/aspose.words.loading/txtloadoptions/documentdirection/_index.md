---
title: TxtLoadOptions.DocumentDirection
second_title: Справочник по API Aspose.Words для .NET
description: TxtLoadOptions свойство. Получает или задает направление документа. Значение по умолчаниюLeftToRight .
type: docs
weight: 30
url: /ru/net/aspose.words.loading/txtloadoptions/documentdirection/
---
## TxtLoadOptions.DocumentDirection property

Получает или задает направление документа. Значение по умолчанию:LeftToRight .

```csharp
public DocumentDirection DocumentDirection { get; set; }
```

### Примеры

Показывает, как определить направление текста в текстовом документе.

```csharp
// Создаем объект "TxtLoadOptions", который мы можем передать конструктору документа
// чтобы изменить способ загрузки документа с открытым текстом.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Установите для свойства "DocumentDirection" значение "DocumentDirection.Auto", чтобы автоматически обнаруживать
// направление каждого абзаца текста, который Aspose.Words загружает из открытого текста.
// Свойство "Bidi" каждого абзаца будет хранить его направление.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// Определить текст на иврите как написанный справа налево.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// Определить английский текст как написанный справа налево.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

### Смотрите также

* enum [DocumentDirection](../../documentdirection/)
* class [TxtLoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../txtloadoptions/)
* сборка [Aspose.Words](../../../)


