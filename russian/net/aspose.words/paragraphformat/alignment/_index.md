---
title: ParagraphFormat.Alignment
second_title: Справочник по API Aspose.Words для .NET
description: ParagraphFormat свойство. Получает или задает выравнивание текста для абзаца.
type: docs
weight: 30
url: /ru/net/aspose.words/paragraphformat/alignment/
---
## ParagraphFormat.Alignment property

Получает или задает выравнивание текста для абзаца.

```csharp
public ParagraphAlignment Alignment { get; set; }
```

### Примеры

Показывает, как вставить абзац в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Arial";
font.Underline = Underline.Dash;

ParagraphFormat paragraphFormat = builder.ParagraphFormat;
paragraphFormat.FirstLineIndent = 8;
paragraphFormat.Alignment = ParagraphAlignment.Justify;
paragraphFormat.AddSpaceBetweenFarEastAndAlpha = true;
paragraphFormat.AddSpaceBetweenFarEastAndDigit = true;
paragraphFormat.KeepTogether = true;

// Метод Writeln завершает абзац после добавления текста
// и затем начинает новую строку, добавляя новый абзац.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
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

* enum [ParagraphAlignment](../../paragraphalignment/)
* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../paragraphformat/)
* сборка [Aspose.Words](../../../)


