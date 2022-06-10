---
title: PaperSize
second_title: Справочник по API Aspose.Words для .NET
description: Указывает размер бумаги.
type: docs
weight: 4090
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
| Number10Envelope | `16` | 4,125 x 9,5 дюйма. |
| Custom | `17` | Нестандартный размер бумаги. |

### Примеры

Показывает, как настроить размер бумаги, ориентацию, поля и другие параметры раздела.

```csharp
Document doc = new Document();

 // Пустой документ содержит один раздел, одно тело и один абзац.
 // Вызовите метод "RemoveAllChildren", чтобы удалить все эти узлы, 
 // и получаем узел документа без дочерних элементов.
doc.RemoveAllChildren();

 // У этого документа теперь нет составных дочерних узлов, к которым мы можем добавить содержимое.
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

 // Создаем абзац, устанавливаем некоторые свойства форматирования, а затем добавляем его как дочерний элемент к телу.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

 // Наконец, добавьте содержимое для создания документа. Создайте прогон, 
 // установить его внешний вид и содержимое, а затем добавить его как дочерний элемент к абзацу.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

Показывает, как установить размеры страницы.

```csharp
Document doc = new Document();

 // Пустой документ содержит один раздел, одно тело и один абзац.
 // Вызовите метод "RemoveAllChildren", чтобы удалить все эти узлы, 
 // и получаем узел документа без дочерних элементов.
doc.RemoveAllChildren();

 // У этого документа теперь нет составных дочерних узлов, к которым мы можем добавить содержимое.
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

 // Создаем абзац, устанавливаем некоторые свойства форматирования, а затем добавляем его как дочерний элемент к телу.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

 // Наконец, добавьте содержимое для создания документа. Создайте прогон, 
 // установить его внешний вид и содержимое, а затем добавить его как дочерний элемент к абзацу.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

Показывает, как создать документ Aspose.Words вручную.

```csharp
Document doc = new Document();

 // Пустой документ содержит один раздел, одно тело и один абзац.
 // Вызовите метод "RemoveAllChildren", чтобы удалить все эти узлы, 
 // и получаем узел документа без дочерних элементов.
doc.RemoveAllChildren();

 // У этого документа теперь нет составных дочерних узлов, к которым мы можем добавить содержимое.
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

 // Создаем абзац, устанавливаем некоторые свойства форматирования, а затем добавляем его как дочерний элемент к телу.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

 // Наконец, добавьте содержимое для создания документа. Создайте прогон, 
 // установить его внешний вид и содержимое, а затем добавить его как дочерний элемент к абзацу.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Смотрите также

* namespace [Aspose.Words](../../aspose.words)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
