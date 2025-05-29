---
title: DocumentDirection Enum
linktitle: DocumentDirection
articleTitle: DocumentDirection
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.DocumentDirection, чтобы легко контролировать поток текста в ваших документах. Улучшите читаемость и форматирование с помощью этой мощной функции!
type: docs
weight: 4030
url: /ru/net/aspose.words.loading/documentdirection/
---
## DocumentDirection enumeration

Позволяет указать направление потока текста в документе.

```csharp
public enum DocumentDirection
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| LeftToRight | `0` | Направление слева направо. |
| RightToLeft | `1` | Направление справа налево. |
| Auto | `2` | Автоматическое определение направления. |

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

* пространство имен [Aspose.Words.Loading](../../aspose.words.loading/)
* сборка [Aspose.Words](../../)
