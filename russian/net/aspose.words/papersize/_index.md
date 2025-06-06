---
title: PaperSize Enum
linktitle: PaperSize
articleTitle: PaperSize
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.PaperSize для определения пользовательских размеров бумаги в ваших документах. Улучшите форматирование ваших документов с легкостью!
type: docs
weight: 5110
url: /ru/net/aspose.words/papersize/
---
## PaperSize enumeration

Указывает размер бумаги.

```csharp
public enum PaperSize
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| A3 | `0` | 297 x 420 мм. |
| A4 | `1` | 210 x 297 мм. |
| A5 | `2` | 148 x 210 мм. |
| B4 | `3` | 250 x 353 мм. |
| B5 | `4` | 176 x 250 мм. |
| Executive | `5` | 7,25 x 10,5 дюймов. |
| Folio | `6` | 8,5 x 13 дюймов. |
| Ledger | `7` | 17 x 11 дюймов. |
| Legal | `8` | 8,5 x 14 дюймов. |
| Letter | `9` | 8,5 x 11 дюймов. |
| EnvelopeDL | `10` | 110 x 220 мм. |
| Quarto | `11` | 8,47 x 10,83 дюйма. |
| Statement | `12` | 8,5 x 5,5 дюймов. |
| Tabloid | `13` | 11 x 17 дюймов. |
| Paper10x14 | `14` | 10 x 14 дюймов. |
| Paper11x17 | `15` | 11 x 17 дюймов. |
| Number10Envelope | `16` | 4,125 x 9,5 дюймов. |
| JisB4 | `17` | 257 x 364 мм. |
| JisB5 | `18` | 182 x 257 мм. |
| Custom | `19` | Пользовательский размер бумаги. |

## Примеры

Показывает, как настроить размер бумаги, ориентацию, поля, а также другие параметры раздела.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.PageSetup.PaperSize = PaperSize.Legal;
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.BottomMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.LeftMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.HeaderDistance = ConvertUtil.InchToPoint(0.2);
builder.PageSetup.FooterDistance = ConvertUtil.InchToPoint(0.2);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PageSetup.PageMargins.docx");
```

Показывает, как устанавливать размеры страниц.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Мы можем изменить размер текущей страницы на предопределенный размер
// с помощью свойства "PaperSize" объекта PageSetup этого раздела.
builder.PageSetup.PaperSize = PaperSize.Tabloid;

Assert.AreEqual(792.0d, builder.PageSetup.PageWidth);
Assert.AreEqual(1224.0d, builder.PageSetup.PageHeight);

builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

// Каждый раздел имеет свой объект PageSetup. Когда мы используем конструктор документов для создания нового раздела,
// объект PageSetup этого раздела наследует все значения объекта PageSetup предыдущего раздела.
builder.InsertBreak(BreakType.SectionBreakEvenPage);

Assert.AreEqual(PaperSize.Tabloid, builder.PageSetup.PaperSize);

builder.PageSetup.PaperSize = PaperSize.A5;
builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

Assert.AreEqual(419.55d, builder.PageSetup.PageWidth);
Assert.AreEqual(595.30d, builder.PageSetup.PageHeight);

builder.InsertBreak(BreakType.SectionBreakEvenPage);

// Установите индивидуальный размер для страниц этого раздела.
builder.PageSetup.PageWidth = 620;
builder.PageSetup.PageHeight = 480;

Assert.AreEqual(PaperSize.Custom, builder.PageSetup.PaperSize);

builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

doc.Save(ArtifactsDir + "PageSetup.PaperSizes.docx");
```

Показывает, как создать документ Aspose.Words вручную.

```csharp
Document doc = new Document();

// Пустой документ содержит один раздел, одно тело и один абзац.
// Вызываем метод "RemoveAllChildren", чтобы удалить все эти узлы,
// и в итоге получаем узел документа без дочерних элементов.
doc.RemoveAllChildren();

// В этом документе теперь нет составных дочерних узлов, в которые мы можем добавлять контент.
// Если мы хотим его отредактировать, нам нужно будет заново заполнить его коллекцию узлов.
// Сначала создадим новый раздел, а затем добавим его как дочерний элемент к корневому узлу документа.
Section section = new Section(doc);
doc.AppendChild(section);

// Задайте некоторые свойства настройки страницы для раздела.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Разделу необходимо тело, которое будет содержать и отображать все его содержимое
// на странице между верхним и нижним колонтитулами раздела.
Body body = new Body(doc);
section.AppendChild(body);

// Создаем абзац, задаем некоторые свойства форматирования, а затем добавляем его в качестве дочернего элемента к телу.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Наконец, добавьте немного контента для документа. Создайте запуск,
// задаем его внешний вид и содержимое, а затем добавляем его как дочерний элемент к абзацу.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
