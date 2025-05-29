---
title: ImportFormatOptions.IgnoreTextBoxes
linktitle: IgnoreTextBoxes
articleTitle: IgnoreTextBoxes
second_title: Aspose.Words для .NET
description: Узнайте, как свойство ImportFormatOptions IgnoreTextBoxes улучшает форматирование документа, управляя содержимым текстовых полей. Оптимизируйте с легкостью сегодня!
type: docs
weight: 50
url: /ru/net/aspose.words/importformatoptions/ignoretextboxes/
---
## ImportFormatOptions.IgnoreTextBoxes property

Возвращает или задает логическое значение, указывающее, что исходное форматирование содержимого текстовых полей игнорируется , еслиKeepSourceFormatting используется режим . Значение по умолчанию:`истинный` .

```csharp
public bool IgnoreTextBoxes { get; set; }
```

## Примеры

Показывает, как управлять форматированием текстового поля при добавлении документа.

```csharp
// Создаем документ, в который будут вставлены узлы из другого документа.
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

builder.Writeln("Hello world!");

// Создаем еще один документ с текстовым полем, который импортируем в первый документ.
Document srcDoc = new Document();
builder = new DocumentBuilder(srcDoc);

Shape textBox = builder.InsertShape(ShapeType.TextBox, 300, 100);
builder.MoveTo(textBox.FirstParagraph);
builder.ParagraphFormat.Style.Font.Name = "Courier New";
builder.ParagraphFormat.Style.Font.Size = 24;
builder.Write("Textbox contents");

// Установите флаг, чтобы указать, следует ли очистить или сохранить форматирование текстового поля
// при импорте их в другие документы.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreTextBoxes = ignoreTextBoxes;

// Импортируем текстовое поле из исходного документа в целевой документ,
// а затем проверяем, сохранили ли мы стиль его текстового содержимого.
NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);
Shape importedTextBox = (Shape)importer.ImportNode(textBox, true);
dstDoc.FirstSection.Body.Paragraphs[1].AppendChild(importedTextBox);

if (ignoreTextBoxes)
{
    Assert.AreEqual(12.0d, importedTextBox.FirstParagraph.Runs[0].Font.Size);
    Assert.AreEqual("Times New Roman", importedTextBox.FirstParagraph.Runs[0].Font.Name);
}
else
{
    Assert.AreEqual(24.0d, importedTextBox.FirstParagraph.Runs[0].Font.Size);
    Assert.AreEqual("Courier New", importedTextBox.FirstParagraph.Runs[0].Font.Name);
}

dstDoc.Save(ArtifactsDir + "DocumentBuilder.IgnoreTextBoxes.docx");
```

### Смотрите также

* class [ImportFormatOptions](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
