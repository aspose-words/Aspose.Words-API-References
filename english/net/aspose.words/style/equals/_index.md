---
title: Style.Equals
linktitle: Equals
articleTitle: Equals
second_title: Aspose.Words for .NET
description: Discover the Style Equals method for comparing built-in styles. Understand linked and next paragraph styles for enhanced formatting and design efficiency.
type: docs
weight: 220
url: /net/aspose.words/style/equals/
---
## Style.Equals method

Compares with the specified style. Styles Istds are compared for built-in styles only. Styles defaults are not included in comparison. Base style, linked style and next paragraph style are recursively compared.

```csharp
public bool Equals(Style style)
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
