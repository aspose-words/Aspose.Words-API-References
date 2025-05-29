---
title: HtmlSaveOptions.DocumentSplitHeadingLevel
linktitle: DocumentSplitHeadingLevel
articleTitle: DocumentSplitHeadingLevel
second_title: Aspose.Words для .NET
description: Оптимизируйте разделение документа с помощью DocumentSplitHeadingLevel в HtmlSaveOptions. Управляйте уровнями заголовков для лучшей организации. По умолчанию установлено значение 2.
type: docs
weight: 90
url: /ru/net/aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/
---
## HtmlSaveOptions.DocumentSplitHeadingLevel property

Указывает максимальный уровень заголовков, по которому следует разделить документ. Значение по умолчанию:`2` .

```csharp
public int DocumentSplitHeadingLevel { get; set; }
```

## Примечания

Когда[`DocumentSplitCriteria`](../documentsplitcriteria/) включает в себяHeadingParagraph и этому свойству присвоено значение от 1 до 9, документ будет разделен на абзацы, отформатированные с использованием **Заголовок 1** ,**Заголовок 2** ,**Заголовок 3**и т. д. стили до указанного уровня заголовка.

По умолчанию только**Заголовок 1** и**Заголовок 2** абзацы приводят к разделению документа. Установка этого свойства в ноль приведет к тому, что документ вообще не будет разделен на абзацы заголовков.

## Примеры

Показывает, как разделить выходной HTML-документ по заголовкам на несколько частей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Каждый абзац, который мы форматируем с использованием стиля «Заголовок», может служить заголовком.
// Каждый заголовок может также иметь уровень заголовка, определяемый номером его стиля заголовка.
// Заголовки ниже относятся к уровням 1-3.
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #1");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #2");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #3");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #4");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #5");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #6");

// Создайте объект HtmlSaveOptions и установите критерий разделения на «HeadingParagraph».
// Эти критерии разделят документ на абзацы со стилями «Заголовок» на несколько меньших документов,
// и сохранить каждый документ в отдельном HTML-файле в локальной файловой системе.
// Мы также установим максимальный уровень заголовка, который разделит документ на 2.
// При сохранении документа он будет разделен на заголовки уровней 1 и 2, но не на заголовки уровней 3–9.
HtmlSaveOptions options = new HtmlSaveOptions
{
    DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph,
    DocumentSplitHeadingLevel = 2
};

// Наш документ имеет четыре заголовка уровней 1 - 2. Один из этих заголовков не будет
// точка разделения, поскольку она находится в начале документа.
// Операция сохранения разделит наш документ в трех местах на четыре меньших документа.
doc.Save(ArtifactsDir + "HtmlSaveOptions.HeadingLevels.html", options);

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels.html");

Assert.AreEqual("Heading #1", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-01.html");

Assert.AreEqual("Heading #2\r" +
                "Heading #3", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-02.html");

Assert.AreEqual("Heading #4", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-03.html");

Assert.AreEqual("Heading #5\r" +
                "Heading #6", doc.GetText().Trim());
```

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
