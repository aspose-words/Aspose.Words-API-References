---
title: Style.LinkedStyleName
linktitle: LinkedStyleName
articleTitle: LinkedStyleName
second_title: Aspose.Words for .NET
description: Discover how to style the LinkedStyleName property, easily manage linked styles, and enhance your design workflow with seamless integration.
type: docs
weight: 90
url: /net/aspose.words/style/linkedstylename/
---
## Style.LinkedStyleName property

Gets/sets the name of the [`Style`](../) linked to this one. Returns empty string if no styles are linked.

```csharp
public string LinkedStyleName { get; set; }
```

## Remarks

It is only allowed to link the paragraph style to the character style and vice versa.

Setting LinkedStyleName for the current style automatically leads to setting LinkedStyleName for the linked style.

Assigning the empty string is equivalent to unlinking the previously linked style.

## Examples

Shows how to link styles among themselves.

```csharp
Document doc = new Document();

Style styleHeading1 = doc.Styles[StyleIdentifier.Heading1];

Style styleHeading1Char = doc.Styles.Add(StyleType.Character, "Heading 1 Char");
styleHeading1Char.Font.Name = "Verdana";
styleHeading1Char.Font.Bold = true;
styleHeading1Char.Font.Border.LineStyle = LineStyle.Dot;
styleHeading1Char.Font.Border.LineWidth = 15;

styleHeading1.LinkedStyleName = "Heading 1 Char";

Assert.AreEqual("Heading 1 Char", styleHeading1.LinkedStyleName);
Assert.AreEqual("Heading 1", styleHeading1Char.LinkedStyleName);
```

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
