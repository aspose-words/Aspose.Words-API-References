---
title: Style.BuiltIn
linktitle: BuiltIn
articleTitle: BuiltIn
second_title: Aspose.Words for .NET
description: Style BuiltIn property. True if this style is one of the builtin styles in MS Word in C#.
type: docs
weight: 40
url: /net/aspose.words/style/builtin/
---
## Style.BuiltIn property

True if this style is one of the built-in styles in MS Word.

```csharp
public bool BuiltIn { get; }
```

## Examples

Shows how to differentiate custom styles from built-in styles.

```csharp
Document doc = new Document();

// When we create a document using Microsoft Word, or programmatically using Aspose.Words,
// the document will come with a collection of styles to apply to its text to modify its appearance.
// We can access these built-in styles via the document's "Styles" collection.
// These styles will all have the "BuiltIn" flag set to "true".
Style style = doc.Styles["Emphasis"];

Assert.True(style.BuiltIn);

// Create a custom style and add it to the collection.
// Custom styles such as this will have the "BuiltIn" flag set to "false". 
style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Navy;
style.Font.Name = "Courier New";

Assert.False(style.BuiltIn);
```

### See Also

* class [Style](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
