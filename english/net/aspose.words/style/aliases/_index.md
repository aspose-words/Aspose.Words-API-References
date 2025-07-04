---
title: Style.Aliases
linktitle: Aliases
articleTitle: Aliases
second_title: Aspose.Words for .NET
description: Discover all style aliases effortlessly with the Style Aliases property. If none exist, receive an empty string array. Simplify your style management!
type: docs
weight: 10
url: /net/aspose.words/style/aliases/
---
## Style.Aliases property

Gets all aliases of this style. If style has no aliases then empty array of string is returned.

```csharp
public string[] Aliases { get; }
```

## Examples

Shows how to use style aliases.

```csharp
Document doc = new Document(MyDir + "Style with alias.docx");

// This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
// If a style's name has multiple values separated by commas, each clause is a separate alias.
Style style = doc.Styles["MyStyle"];
Assert.That(style.Aliases, Is.EqualTo(new [] { "MyStyle Alias 1", "MyStyle Alias 2" }));
Assert.That(style.BaseStyleName, Is.EqualTo("Title"));
Assert.That(style.LinkedStyleName, Is.EqualTo("MyStyle Char"));

// We can reference a style using its alias, as well as its name.
Assert.That(doc.Styles["MyStyle Alias 2"], Is.EqualTo(doc.Styles["MyStyle Alias 1"]));

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.ParagraphFormat.Style = doc.Styles["MyStyle Alias 1"];
builder.Writeln("Hello world!");
builder.ParagraphFormat.Style = doc.Styles["MyStyle Alias 2"];
builder.Write("Hello again!");

Assert.That(doc.FirstSection.Body.Paragraphs[1].ParagraphFormat.Style, Is.EqualTo(doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.Style));
```

### See Also

* class [Style](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
