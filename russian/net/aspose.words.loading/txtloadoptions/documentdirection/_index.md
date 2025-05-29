---
title: TxtLoadOptions.DocumentDirection
linktitle: DocumentDirection
articleTitle: DocumentDirection
second_title: Aspose.Words для .NET
description: Откройте для себя свойство TxtLoadOptions DocumentDirection, чтобы легко задать направление документа. Оптимизируйте свой макет с помощью настройки LeftToRight по умолчанию!
type: docs
weight: 50
url: /ru/net/aspose.words.loading/txtloadoptions/documentdirection/
---
## TxtLoadOptions.DocumentDirection property

Возвращает или задает направление документа. Значение по умолчанию:LeftToRight .

```csharp
public DocumentDirection DocumentDirection { get; set; }
```

## Примеры

Показывает, как определить направление текста в текстовом документе.

```csharp
// Создаем объект "TxtLoadOptions", который можно передать конструктору документа
// чтобы изменить способ загрузки текстового документа.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Установите свойство "DocumentDirection" на "DocumentDirection.Auto", чтобы автоматически определить
// направление каждого абзаца текста, который Aspose.Words загружает из открытого текста.
// Свойство «Bidi» каждого абзаца будет хранить его направление.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// Определить, что текст на иврите написан справа налево.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// Определить английский текст как написанный справа налево.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

### Смотрите также

* enum [DocumentDirection](../../documentdirection/)
* class [TxtLoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
