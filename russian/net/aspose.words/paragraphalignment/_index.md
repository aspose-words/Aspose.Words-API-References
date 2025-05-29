---
title: ParagraphAlignment Enum
linktitle: ParagraphAlignment
articleTitle: ParagraphAlignment
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.ParagraphAlignment для точного выравнивания текста в ваших документах. Улучшите читаемость и форматирование с легкостью!
type: docs
weight: 5130
url: /ru/net/aspose.words/paragraphalignment/
---
## ParagraphAlignment enumeration

Задает выравнивание текста в абзаце.

```csharp
public enum ParagraphAlignment
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Left | `0` | Текст выровнен по левому краю. |
| Center | `1` | Текст выравнивается по центру по горизонтали. |
| Right | `2` | Текст выровнен по правому краю. |
| Justify | `3` | Текст выровнен по левому и правому краю. |
| Distributed | `4` | Текст распределен равномерно. |
| ArabicMediumKashida | `5` | Только арабский. Длина кашиды для текста увеличивается до средней длины, определяемой потребителем. |
| ArabicHighKashida | `7` | Только арабский. Длина кашиды для текста увеличивается до максимально возможной длины. |
| ArabicLowKashida | `8` | Только арабский. Длина кашиды для текста увеличена до немного большей длины. |
| ThaiDistributed | `9` | Только тайский. Текст выровнен с оптимизацией для тайского языка. |
| MathElementCenterAsGroup | `10` | Единственный элемент Math в строке, выровненный по принципу «По центру группы». |

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
