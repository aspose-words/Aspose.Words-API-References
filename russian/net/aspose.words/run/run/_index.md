---
title: Run
linktitle: Run
articleTitle: Run
second_title: Aspose.Words для .NET
description: Создавайте и настраивайте свой экземпляр класса Run без усилий. Разблокируйте мощные функции для оптимизированной производительности и улучшенной функциональности.
type: docs
weight: 10
url: /ru/net/aspose.words/run/run/
---
## Run(*[DocumentBase](../../documentbase/)*) {#constructor}

Инициализирует новый экземпляр[`Run`](../) класс.

```csharp
public Run(DocumentBase doc)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | DocumentBase | Документ владельца. |

## Примечания

Когда[`Run`](../) создан, он принадлежит указанному документу, но еще не является частью документа и[`ParentNode`](../../node/parentnode/) является`нулевой`.

Чтобы добавить[`Run`](../) к использованию документа[`InsertAfter`](../../compositenode/insertafter/) или[`InsertBefore`](../../compositenode/insertbefore/) в абзаце, куда вы хотите вставить строку.

## Примеры

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

* class [DocumentBase](../../documentbase/)
* class [Run](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## Run(*[DocumentBase](../../documentbase/), string*) {#constructor_1}

Инициализирует новый экземпляр**Бегать** класс.

```csharp
public Run(DocumentBase doc, string text)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | DocumentBase | Документ владельца. |
| text | String | Текст тиража. |

## Примечания

Когда[`Run`](../) создан, он принадлежит указанному документу, но еще не является частью документа и[`ParentNode`](../../node/parentnode/) является`нулевой`.

Чтобы добавить[`Run`](../) к использованию документа[`InsertAfter`](../../compositenode/insertafter/) или[`InsertBefore`](../../compositenode/insertbefore/) в абзаце, куда вы хотите вставить строку.

## Примеры

Показывает, как отформатировать фрагмент текста, используя его свойство шрифта.

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
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
