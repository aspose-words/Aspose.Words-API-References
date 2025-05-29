---
title: SdtDateStorageFormat Enum
linktitle: SdtDateStorageFormat
articleTitle: SdtDateStorageFormat
second_title: Aspose.Words для .NET
description: Узнайте, как Aspose.Words.Markup.SdtDateStorageFormat улучшает обработку дат в SDT, обеспечивая бесперебойную интеграцию XML-данных в ваши документы.
type: docs
weight: 4700
url: /ru/net/aspose.words.markup/sdtdatestorageformat/
---
## SdtDateStorageFormat enumeration

Указывает, как дата для SDT даты сохраняется/извлекается, когда SDT привязан к узлу XML в хранилище данных документа.

```csharp
public enum SdtDateStorageFormat
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Date | `0` | Значение даты для даты SDT хранится как дата в стандартном формате даты XML Schema. |
| DateTime | `1` | Значение даты для даты SDT хранится как дата в стандартном формате XML Schema DateTime. |
| Text | `2` | Значение даты для даты SDT хранится в виде текста. |
| Default | `1` | По умолчаниюDateTime |

## Примеры

Показывает, как предложить пользователю ввести дату с помощью структурированного тега документа.

```csharp
Document doc = new Document();

// Вставьте структурированный тег документа, который предлагает пользователю ввести дату.
// В Microsoft Word этот элемент известен как «Элемент управления содержимым выбора даты».
// Когда мы нажимаем на стрелку в правом конце этого тега в Microsoft Word,
// мы увидим всплывающее окно в виде кликабельного календаря.
// Мы можем использовать это всплывающее окно для выбора даты, которую будет отображать тег.
StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.Date, MarkupLevel.Inline);

// Отображает дату в соответствии с региональным арабским языком Саудовской Аравии.
sdtDate.DateDisplayLocale = CultureInfo.GetCultureInfo("ar-SA").LCID;

// Задайте формат отображения даты.
sdtDate.DateDisplayFormat = "dd MMMM, yyyy";
sdtDate.DateStorageFormat = SdtDateStorageFormat.DateTime;

// Отображение даты по календарю Хиджры.
sdtDate.CalendarType = SdtCalendarType.Hijri;

// Прежде чем пользователь выберет дату в Microsoft Word, тег отобразит текст «Нажмите здесь, чтобы ввести дату».
// В соответствии с календарем тега установите свойство «FullDate», чтобы тег отображал дату по умолчанию.
sdtDate.FullDate = new DateTime(1440, 10, 20);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(sdtDate);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Date.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Markup](../../aspose.words.markup/)
* сборка [Aspose.Words](../../)
