---
title: Enum ParagraphAlignment
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.ParagraphAlignment перечисление. Задает выравнивание текста в абзаце.
type: docs
weight: 4400
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
| Left | `0` | Текст выравнивается по левому краю. |
| Center | `1` | Текст центрируется по горизонтали. |
| Right | `2` | Текст выравнивается по правому краю. |
| Justify | `3` | Текст выравнивается по левому и правому краю. |
| Distributed | `4` | Текст распределен равномерно. |
| ArabicMediumKashida | `5` | Только на арабском языке. Длина текста Кашида увеличивается до средней длины, определяемой потребителем. |
| ArabicHighKashida | `7` | Только на арабском языке. Длина кашида для текста увеличена до максимально возможной длины. |
| ArabicLowKashida | `8` | Только на арабском языке. Длина текста кашида увеличена до немного большей длины. |
| ThaiDistributed | `9` | Только тайский. Текст выровнен по ширине с оптимизацией для тайского языка. |
| MathElementCenterAsGroup | `10` | Единственный математический элемент в строке, выровненный по принципу «Центрировано как группа». |

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


