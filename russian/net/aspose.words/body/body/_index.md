---
title: Body
linktitle: Body
articleTitle: Body
second_title: Aspose.Words для .NET
description: Создавайте и настраивайте новый экземпляр Body без усилий с помощью нашего интуитивно понятного конструктора. Испытайте бесшовную интеграцию для своих проектов уже сегодня!
type: docs
weight: 10
url: /ru/net/aspose.words/body/body/
---
## Body constructor

Инициализирует новый экземпляр[`Body`](../) класс.

```csharp
public Body(DocumentBase doc)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | DocumentBase | Документ владельца. |

## Примечания

Когда[`Body`](../) создан, он принадлежит указанному документу, но еще не является частью документа и[`ParentNode`](../../node/parentnode/) является`нулевой`.

Чтобы добавить[`Body`](../)к[`Section`](../../section/) использовать[`Добавитьдочерний`](../../compositenode/appendchild/)[`ВставитьПосле`](../../compositenode/insertafter/) или[`ВставитьПеред`](../../compositenode/insertbefore/) методы.

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
* class [Body](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
