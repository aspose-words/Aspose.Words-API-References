---
title: StructuredDocumentTag.FullDate
linktitle: FullDate
articleTitle: FullDate
second_title: Aspose.Words для .NET
description: Откройте для себя свойство StructuredDocumentTag FullDate, которое фиксирует полную дату и время для повышения точности и отслеживания документа.
type: docs
weight: 130
url: /ru/net/aspose.words.markup/structureddocumenttag/fulldate/
---
## StructuredDocumentTag.FullDate property

Указывает полную дату и время последнего ввода в этот**СДТ** .

```csharp
public DateTime FullDate { get; set; }
```

## Примечания

Доступ к этому свойству будет возможен только дляDate Тип СДТ.

Для всех остальных типов SDT возникнет исключение.

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

* class [StructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
