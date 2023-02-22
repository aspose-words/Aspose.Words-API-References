---
title: Run.Run
second_title: Справочник по API Aspose.Words для .NET
description: Run строитель. Инициализирует новый экземпляр Бежать класс.
type: docs
weight: 10
url: /ru/net/aspose.words/run/run/
---
## Run(DocumentBase) {#constructor}

Инициализирует новый экземпляр **Бежать** класс.

```csharp
public Run(DocumentBase doc)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | DocumentBase | Документ владельца. |

### Примечания

Когда **Бежать** создан, он принадлежит указанному документу, но не является частью документа и **Родительский узел** нулевой.

Чтобы добавить **Бежать** к документу используйте InsertAfter или InsertBefore в абзаце, куда вы хотите вставить прогон.

### Примеры

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

* class [DocumentBase](../../documentbase/)
* class [Run](../)
* пространство имен [Aspose.Words](../../run/)
* сборка [Aspose.Words](../../../)

---

## Run(DocumentBase, string) {#constructor_1}

Инициализирует новый экземпляр **Бежать** класс.

```csharp
public Run(DocumentBase doc, string text)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | DocumentBase | Документ владельца. |
| text | String | Текст пробега. |

### Примечания

Когда **Бежать** создан, он принадлежит указанному документу, но не является частью документа и **Родительский узел** нулевой.

Чтобы добавить **Бежать** к документу используйте InsertAfter или InsertBefore в абзаце, куда вы хотите вставить прогон.

### Примеры

Показывает, как отформатировать набор текста, используя его свойство шрифта.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

### Смотрите также

* class [DocumentBase](../../documentbase/)
* class [Run](../)
* пространство имен [Aspose.Words](../../run/)
* сборка [Aspose.Words](../../../)


