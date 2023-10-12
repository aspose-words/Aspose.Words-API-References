---
title: Run.Run
second_title: Справочник по API Aspose.Words для .NET
description: Run строитель. Инициализирует новый экземплярRun класс.
type: docs
weight: 10
url: /ru/net/aspose.words/run/run/
---
## Run(DocumentBase) {#constructor}

Инициализирует новый экземпляр[`Run`](../) класс.

```csharp
public Run(DocumentBase doc)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | DocumentBase | Документ владельца. |

### Примечания

Когда[`Run`](../) создан, он принадлежит указанному документу, но еще не является частью документа и[`ParentNode`](../../node/parentnode/) является`нулевой`.

Чтобы добавить[`Run`](../) к использованию документаNode) илиNode) в абзаце, в который вы хотите вставить фрагмент.

### Примеры

Показывает, как вручную создать документ Aspose.Words.

```csharp
Document doc = new Document();

// Пустой документ содержит один раздел, одно тело и один абзац.
// Вызов метода «RemoveAllChildren», чтобы удалить все эти узлы,
// и в итоге получим узел документа без дочерних элементов.
doc.RemoveAllChildren();

// В этом документе теперь нет составных дочерних узлов, к которым мы можем добавлять контент.
// Если мы хотим его отредактировать, нам нужно будет заново заполнить его коллекцию узлов.
// Сначала создаем новый раздел, а затем добавляем его как дочерний к корневому узлу документа.
Section section = new Section(doc);
doc.AppendChild(section);

// Установите некоторые свойства настройки страницы для раздела.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Разделу необходимо тело, которое будет содержать и отображать все его содержимое
// на странице между заголовком и подвалом раздела.
Body body = new Body(doc);
section.AppendChild(body);

// Создайте абзац, установите некоторые свойства форматирования, а затем добавьте его как дочерний элемент к телу.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Наконец, добавим некоторый контент для оформления документа. Создать пробег,
// устанавливаем его внешний вид и содержимое, а затем добавляем его в качестве дочернего элемента к абзацу.
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

Инициализирует новый экземпляр **Бегать** класс.

```csharp
public Run(DocumentBase doc, string text)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | DocumentBase | Документ владельца. |
| text | String | Текст пробега. |

### Примечания

Когда[`Run`](../) создан, он принадлежит указанному документу, но еще не является частью документа и[`ParentNode`](../../node/parentnode/) является`нулевой`.

Чтобы добавить[`Run`](../) к использованию документаNode) илиNode) в абзаце, в который вы хотите вставить фрагмент.

### Примеры

Показывает, как форматировать фрагмент текста, используя его свойство шрифта.

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


