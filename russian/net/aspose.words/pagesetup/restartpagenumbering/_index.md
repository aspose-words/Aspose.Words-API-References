---
title: PageSetup.RestartPageNumbering
linktitle: RestartPageNumbering
articleTitle: RestartPageNumbering
second_title: Aspose.Words для .NET
description: Узнайте, как свойство RestartPageNumbering улучшает форматирование документа, позволяя нумеровать страницы по разделам. Оптимизируйте свой макет без усилий!
type: docs
weight: 360
url: /ru/net/aspose.words/pagesetup/restartpagenumbering/
---
## PageSetup.RestartPageNumbering property

Истина, если нумерация страниц начинается заново с начала раздела.

```csharp
public bool RestartPageNumbering { get; set; }
```

## Примечания

Если установлено значение`ЛОЖЬ` ,`RestartPageNumbering` свойство переопределит the [`PageStartingNumber`](../pagestartingnumber/) свойство, чтобы нумерация страниц могла продолжаться с предыдущего раздела.

## Примеры

Показывает, как настроить нумерацию страниц в разделе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 3.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("Section 2, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 3.");

// Перемещаем конструктор документа в основной заголовок первого раздела,
// который будет отображаться на каждой странице этого раздела.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// Вставьте поле СТРАНИЦА, в котором будет отображаться номер текущей страницы.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// Настройте раздел так, чтобы количество страниц, отображаемых в полях PAGE, начиналось с 5.
// Также настройте все поля PAGE для отображения номеров страниц с использованием заглавных римских цифр.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// Создаем еще один основной заголовок для второго раздела с другим полем PAGE.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// Настройте раздел так, чтобы количество страниц, отображаемых в полях PAGE, начиналось с 10.
// Также настройте все поля PAGE для отображения номеров страниц с использованием арабских цифр.
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### Смотрите также

* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
