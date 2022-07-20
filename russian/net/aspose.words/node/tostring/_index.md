---
title: ToString
second_title: Справочник по API Aspose.Words для .NET
description: Экспортирует содержимое узла в строку в указанном формате.
type: docs
weight: 160
url: /ru/net/aspose.words/node/tostring/
---
## ToString(SaveFormat) {#tostring_1}

Экспортирует содержимое узла в строку в указанном формате.

```csharp
public string ToString(SaveFormat saveFormat)
```

### Возвращаемое значение

Содержимое узла в указанном формате.

### Примеры

Показывает разницу между вызовом методов GetText и ToString на узле.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText извлечет видимый текст, а также коды полей и специальные символы.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015\u000c", doc.GetText());

// ToString даст нам внешний вид документа, если он будет сохранен в переданном формате сохранения.
Assert.AreEqual("«Field»\r\n", doc.ToString(SaveFormat.Text));
```

Экспортирует содержимое узла в строку в формате HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// Когда мы вызываем метод ToString, используя перегрузку html SaveFormat,
// он преобразует содержимое узла в их необработанное html-представление.
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

// Мы также можем изменить результат этого преобразования, используя объект SaveOptions.
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

// Определяем, есть ли у нас список абзацев. В нашем документе в нашем списке используются простые арабские цифры,
// которые начинаются с трех и заканчиваются на шести.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // Это текст, который мы получаем при получении, когда мы выводим этот узел в текстовый формат.
    // В этом текстовом выводе метки списка будут пропущены. Обрежьте все символы форматирования абзаца. 
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Получаем позицию абзаца на текущем уровне списка. Если у нас есть список с несколькими уровнями,
    // это скажет нам, какая позиция находится на этом уровне.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Объедините их вместе, чтобы включить в вывод метку списка с текстом.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Смотрите также

* enum [SaveFormat](../../saveformat)
* class [Node](../../node)
* пространство имен [Aspose.Words](../../node)
* сборка [Aspose.Words](../../../)

---

## ToString(SaveOptions) {#tostring_2}

Экспортирует содержимое узла в строку, используя указанные параметры сохранения.

```csharp
public string ToString(SaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| saveOptions | SaveOptions | Указывает параметры, управляющие способом сохранения узла. |

### Возвращаемое значение

Содержимое узла в указанном формате.

### Примеры

Экспортирует содержимое узла в строку в формате HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// Когда мы вызываем метод ToString, используя перегрузку html SaveFormat,
// он преобразует содержимое узла в их необработанное html-представление.
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

// Мы также можем изменить результат этого преобразования, используя объект SaveOptions.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ExportRelativeFontSize = true;

Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(saveOptions));
```

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions)
* class [Node](../../node)
* пространство имен [Aspose.Words](../../node)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
