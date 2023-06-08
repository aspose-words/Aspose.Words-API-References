---
title: Style.BaseStyleName
linktitle: BaseStyleName
articleTitle: BaseStyleName
second_title: Aspose.Words for .NET
description: Style BaseStyleName property. Gets/sets the name of the style this style is based on in C#.
type: docs
weight: 30
url: /net/aspose.words/style/basestylename/
---
## Style.BaseStyleName property

Gets/sets the name of the style this style is based on.

```csharp
public string BaseStyleName { get; set; }
```

## Remarks

This will be an empty string if the style is not based on any other style and it can be set to an empty string.

## Examples

Shows how to use style aliases.

```csharp
Document doc = new Document(MyDir + "Style with alias.docx");

// This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
// If a style's name has multiple values separated by commas, each clause is a separate alias.
Style style = doc.Styles["MyStyle"];
Assert.AreEqual(new [] { "MyStyle Alias 1", "MyStyle Alias 2" }, style.Aliases);
Assert.AreEqual("Title", style.BaseStyleName);
Assert.AreEqual("MyStyle Char", style.LinkedStyleName);

// We can reference a style using its alias, as well as its name.
Assert.AreEqual(doc.Styles["MyStyle Alias 1"], doc.Styles["MyStyle Alias 2"]);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.ParagraphFormat.Style = doc.Styles["MyStyle Alias 1"];
builder.Writeln("Hello world!");
builder.ParagraphFormat.Style = doc.Styles["MyStyle Alias 2"];
builder.Write("Hello again!");

Assert.AreEqual(doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.Style, 
    doc.FirstSection.Body.Paragraphs[1].ParagraphFormat.Style);
```

### See Also

* class [Style](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
