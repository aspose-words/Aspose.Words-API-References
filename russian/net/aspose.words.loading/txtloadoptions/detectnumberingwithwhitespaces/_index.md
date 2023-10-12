---
title: TxtLoadOptions.DetectNumberingWithWhitespaces
second_title: Справочник по API Aspose.Words для .NET
description: TxtLoadOptions свойство. Позволяет указать как распознаются нумерованные элементы списка когда документ импортируется из обычного текстового формата. Значение по умолчаниюистинный.
type: docs
weight: 40
url: /ru/net/aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/
---
## TxtLoadOptions.DetectNumberingWithWhitespaces property

Позволяет указать, как распознаются нумерованные элементы списка, когда документ импортируется из обычного текстового формата. Значение по умолчанию:`истинный`.

```csharp
public bool DetectNumberingWithWhitespaces { get; set; }
```

### Примечания

Если для этой опции установлено значение`ЛОЖЬ`, алгоритм распознавания списков обнаруживает абзацы списка, когда номера списка заканчиваются на либо точкой, правой скобкой, либо символами маркера (например, «•», «*», «-» или «o»).

Если для этой опции установлено значение`истинный`пробелы также используются в качестве разделителей номеров списков: Алгоритм распознавания списков для нумерации в арабском стиле (1., 1.1.2.) использует как пробелы, так и символы точки ("".").

### Примеры

Показывает, как обнаружить списки при загрузке документов в виде открытого текста.

```csharp
// Создаем текстовый документ в виде строки, состоящей из четырех отдельных частей, которые мы можем интерпретировать как списки,
// с разными разделителями. При загрузке открытого текстового документа в объект «Документ»
// Aspose.Words всегда обнаружит первые три списка и добавит объект «Список»
// для каждого свойства «Списки» документа.
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

// Создаем объект «TxtLoadOptions», который мы можем передать конструктору документа
// чтобы изменить способ загрузки открытого текстового документа.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Установите для свойства «DetectNumberingWithWhitespaces» значение «true», чтобы обнаруживать пронумерованные элементы
// с пробелами-разделителями, такими как четвертый список в нашем документе, как lists.
// Это также может ошибочно определить абзацы, начинающиеся с цифр, как списки.
// Установите для свойства «DetectNumberingWithWhitespaces» значение «false»
// чтобы не создавать списки из пронумерованных элементов с пробелами-разделителями.
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
* пространство имен [Aspose.Words.Loading](../../txtloadoptions/)
* сборка [Aspose.Words](../../../)


