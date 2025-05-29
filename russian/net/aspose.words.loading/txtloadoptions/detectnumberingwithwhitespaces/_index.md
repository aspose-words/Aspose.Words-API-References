---
title: TxtLoadOptions.DetectNumberingWithWhitespaces
linktitle: DetectNumberingWithWhitespaces
articleTitle: DetectNumberingWithWhitespaces
second_title: Aspose.Words для .NET
description: Оптимизируйте импорт документов с помощью функции DetectNumberingWithWhitespaces в TxtLoadOptions, которая обеспечивает точное распознавание нумерованных списков из обычного текста.
type: docs
weight: 40
url: /ru/net/aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/
---
## TxtLoadOptions.DetectNumberingWithWhitespaces property

Позволяет указать, как распознаются элементы нумерованного списка при импорте документа из обычного текстового формата. Значение по умолчанию:`истинный`.

```csharp
public bool DetectNumberingWithWhitespaces { get; set; }
```

## Примечания

Если эта опция установлена на`ЛОЖЬ`, алгоритм распознавания списков обнаруживает абзацы списка, когда номера списков заканчиваются на либо на точку, закрывающую скобку или символы маркера (например, «•», «*», «-» или «o»).

Если эта опция установлена на`истинный`В качестве разделителей номеров списков также используются пробелы: алгоритм распознавания списков для арабской нумерации (1., 1.1.2.) использует как пробелы, так и символы точек («.»).

## Примеры

Показывает, как обнаруживать списки при загрузке текстовых документов.

```csharp
// Создаем текстовый документ в строке с четырьмя отдельными частями, которые мы можем интерпретировать как списки,
// с разными разделителями. При загрузке открытого текстового документа в объект "Документ",
// Aspose.Words всегда обнаружит первые три списка и добавит объект «Список»
// для каждого свойства "Списки" документа.
const string textDoc = "Full stop delimiters:\n" +
                       "1. First list item 1\n" +
                       "2. First list item 2\n" +
                       "3. First list item 3\n\n" +
                       "Right bracket delimiters:\n" +
                       "1) Second list item 1\n" +
                       "2) Second list item 2\n" +
                       "3) Second list item 3\n\n" +
                       "Bullet delimiters:\n" +
                       "• Third list item 1\n" +
                       "• Third list item 2\n" +
                       "• Third list item 3\n\n" +
                       "Whitespace delimiters:\n" +
                       "1 Fourth list item 1\n" +
                       "2 Fourth list item 2\n" +
                       "3 Fourth list item 3";

// Создаем объект "TxtLoadOptions", который можно передать конструктору документа
// чтобы изменить способ загрузки текстового документа.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Установите свойство "DetectNumberingWithWhitespaces" в значение "true" для обнаружения пронумерованных элементов
// с разделителями-пробелами, такими как четвертый список в нашем документе, как списки.
// Это также может привести к ложному определению абзацев, начинающихся с цифр, как списков.
// Установите свойство "DetectNumberingWithWhitespaces" в значение "false"
// чтобы не создавать списки из пронумерованных элементов с разделителями-пробелами.
loadOptions.DetectNumberingWithWhitespaces = detectNumberingWithWhitespaces;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(textDoc)), loadOptions);

if (detectNumberingWithWhitespaces)
{
    Assert.AreEqual(4, doc.Lists.Count);
    Assert.True(doc.FirstSection.Body.Paragraphs.Any(p => p.GetText().Contains("Fourth list") && ((Paragraph)p).IsListItem));
}
else
{
    Assert.AreEqual(3, doc.Lists.Count);
    Assert.False(doc.FirstSection.Body.Paragraphs.Any(p => p.GetText().Contains("Fourth list") && ((Paragraph)p).IsListItem));
}
```

### Смотрите также

* class [TxtLoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
