---
title: Node.ToString
linktitle: ToString
articleTitle: ToString
second_title: Aspose.Words для .NET
description: Откройте для себя метод Node ToString, легко преобразуйте содержимое узлов в строки с настраиваемыми форматами для улучшенной обработки данных. Оптимизируйте свое кодирование сегодня!
type: docs
weight: 160
url: /ru/net/aspose.words/node/tostring/
---
## ToString(*[SaveFormat](../../saveformat/)*) {#tostring_1}

Экспортирует содержимое узла в строку указанного формата.

```csharp
public string ToString(SaveFormat saveFormat)
```

### Возвращаемое значение

Содержимое узла в указанном формате.

## Примеры

Показывает разницу между вызовом методов GetText и ToString на узле.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText извлечет видимый текст, а также коды полей и специальные символы.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015", doc.GetText().Trim());

// ToString вернет нам внешний вид документа, сохраненного в переданном формате сохранения.
Assert.AreEqual("«Field»", doc.ToString(SaveFormat.Text).Trim());
```

Экспортирует содержимое узла в строку в формате HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// Когда мы вызываем метод ToString с использованием перегрузки html SaveFormat,
// он преобразует содержимое узла в его необработанное HTML-представление.
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

// Мы также можем изменить результат этого преобразования с помощью объекта SaveOptions.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ExportRelativeFontSize = true;

Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(saveOptions));
```

Показывает, как извлечь метки списка всех абзацев, являющихся элементами списка.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// Находим, есть ли у нас список абзацев. В нашем документе наш список использует простые арабские цифры,
// которые начинаются в три и заканчиваются в шесть.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem).ToList())
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // Это текст, который мы получаем при выводе этого узла в текстовый формат.
     // Этот текстовый вывод будет опускать списочные метки. Обрезайте любые символы форматирования абзаца.
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Это получает позицию абзаца на текущем уровне списка. Если у нас есть список с несколькими уровнями,
    // это скажет нам, в какой позиции он находится на этом уровне.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Объединяем их вместе, чтобы включить метку списка с текстом в вывод.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Смотрите также

* enum [SaveFormat](../../saveformat/)
* class [Node](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## ToString(*[SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#tostring_2}

Экспортирует содержимое узла в строку, используя указанные параметры сохранения.

```csharp
public string ToString(SaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| saveOptions | SaveOptions | Задает параметры, управляющие способом сохранения узла. |

### Возвращаемое значение

Содержимое узла в указанном формате.

## Примеры

Экспортирует содержимое узла в строку в формате HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// Когда мы вызываем метод ToString с использованием перегрузки html SaveFormat,
// он преобразует содержимое узла в его необработанное HTML-представление.
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

// Мы также можем изменить результат этого преобразования с помощью объекта SaveOptions.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ExportRelativeFontSize = true;

Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(saveOptions));
```

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Node](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
