---
title: PaperSize
second_title: Справочник по API Aspose.Words для .NET
description: Определяет размер бумаги.
type: docs
weight: 4140
url: /ru/net/aspose.words/papersize/
---
## PaperSize enumeration

Определяет размер бумаги.

```csharp
public enum PaperSize
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| A3 | `0` | 297 x 420 мм. |
| A4 | `1` | 210 х 297 мм. |
| A5 | `2` | 148 x 210 мм. |
| B4 | `3` | 250 х 353 мм. |
| B5 | `4` | 176 x 250 мм. |
| Executive | `5` | 7,25 x 10,5 дюймов. |
| Folio | `6` | 8,5 х 13 дюймов. |
| Ledger | `7` | 17 х 11 дюймов. |
| Legal | `8` | 8,5 х 14 дюймов. |
| Letter | `9` | 8,5 х 11 дюймов. |
| EnvelopeDL | `10` | 110 х 220 мм. |
| Quarto | `11` | 8,47 x 10,83 дюйма. |
| Statement | `12` | 8,5 x 5,5 дюймов. |
| Tabloid | `13` | 11 х 17 дюймов. |
| Paper10x14 | `14` | 10 х 14 дюймов. |
| Paper11x17 | `15` | 11 х 17 дюймов. |
| Number10Envelope | `16` | 4,125 x 9,5 дюйма. |
| Custom | `17` | Пользовательский размер бумаги. |

### Примеры

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

Показывает, как установить размеры страницы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Мы можем изменить размер текущей страницы на предопределенный размер
// с помощью свойства "PaperSize" объекта PageSetup этого раздела.
builder.PageSetup.PaperSize = PaperSize.Tabloid;

Assert.AreEqual(792.0d, builder.PageSetup.PageWidth);
Assert.AreEqual(1224.0d, builder.PageSetup.PageHeight);

builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

// Каждый раздел имеет свой собственный объект PageSetup. Когда мы используем конструктор документов для создания нового раздела,
// объект PageSetup этого раздела наследует все значения объекта PageSetup предыдущего раздела.
builder.InsertBreak(BreakType.SectionBreakEvenPage);

Assert.AreEqual(PaperSize.Tabloid, builder.PageSetup.PaperSize);

builder.PageSetup.PaperSize = PaperSize.A5;
builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

Assert.AreEqual(419.55d, builder.PageSetup.PageWidth);
Assert.AreEqual(595.30d, builder.PageSetup.PageHeight);

builder.InsertBreak(BreakType.SectionBreakEvenPage);

// Установить произвольный размер для страниц этого раздела.
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
// Вызовите метод "RemoveAllChildren", чтобы удалить все эти узлы,
// и получаем узел документа без дочерних элементов.
doc.RemoveAllChildren();

// Этот документ теперь не имеет составных дочерних узлов, к которым мы можем добавить содержимое.
// Если мы хотим отредактировать его, нам нужно будет повторно заполнить его коллекцию узлов.
// Сначала создайте новый раздел, а затем добавьте его как дочерний к корневому узлу документа.
Section section = new Section(doc);
doc.AppendChild(section);

// Установите некоторые свойства настройки страницы для раздела.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Разделу нужно тело, которое будет содержать и отображать все его содержимое
// на странице между шапкой и нижним колонтитулом раздела.
Body body = new Body(doc);
section.AppendChild(body);

// Создать абзац, установить некоторые свойства форматирования, а затем добавить его в тело как дочерний элемент.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Наконец, добавьте содержимое для создания документа. Создать прогон,
// установить его внешний вид и содержимое, а затем добавить его как дочерний элемент к абзацу.
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
