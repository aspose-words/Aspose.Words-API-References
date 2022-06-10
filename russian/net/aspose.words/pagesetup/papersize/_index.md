---
title: PaperSize
second_title: Справочник по API Aspose.Words для .NET
description: Возвращает или задает размер бумаги.
type: docs
weight: 340
url: /ru/net/aspose.words/pagesetup/papersize/
---
## PageSetup.PaperSize property

Возвращает или задает размер бумаги.

```csharp
public PaperSize PaperSize { get; set; }
```

### Примечания

Установка этого свойства обновляет[`PageWidth`](../pagewidth)и[`PageHeight`](../pageheight)значения. Установка этого значения наCustomне изменяет существующие значения.

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

* enum [PaperSize](../../papersize)
* class [PageSetup](../../pagesetup)
* namespace [Aspose.Words](../../pagesetup)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
