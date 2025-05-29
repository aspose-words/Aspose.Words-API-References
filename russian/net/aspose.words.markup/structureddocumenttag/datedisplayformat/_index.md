---
title: StructuredDocumentTag.DateDisplayFormat
linktitle: DateDisplayFormat
articleTitle: DateDisplayFormat
second_title: Aspose.Words для .NET
description: Откройте для себя свойство StructuredDocumentTag DateDisplayFormat для легкой настройки форматов отображения даты. Повысьте ясность и привлекательность вашего документа!
type: docs
weight: 90
url: /ru/net/aspose.words.markup/structureddocumenttag/datedisplayformat/
---
## StructuredDocumentTag.DateDisplayFormat property

Строка, представляющая формат отображения дат.

```csharp
public string DateDisplayFormat { get; set; }
```

## Примечания

Не может быть`нулевой`.

Даты для английского языка (США) — «мм/дд/гггг».

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
