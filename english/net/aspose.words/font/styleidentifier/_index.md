---
title: Font.StyleIdentifier
linktitle: StyleIdentifier
articleTitle: StyleIdentifier
second_title: Aspose.Words for .NET
description: Discover the Font StyleIdentifier property to easily manage character styles in your formatting. Enhance your design with locale-independent solutions!
type: docs
weight: 420
url: /net/aspose.words/font/styleidentifier/
---
## Font.StyleIdentifier property

Gets or sets the locale independent style identifier of the character style applied to this formatting.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

## Examples

Shows how to change the style of existing text.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Below are two ways of referencing styles.
// 1 -  Using the style name:
builder.Font.StyleName = "Emphasis";
builder.Writeln("Text originally in \"Emphasis\" style");

// 2 -  Using a built-in style identifier:
builder.Font.StyleIdentifier = StyleIdentifier.IntenseEmphasis;
builder.Writeln("Text originally in \"Intense Emphasis\" style");

// Convert all uses of one style to another,
// using the above methods to reference old and new styles.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true))
{
    if (run.Font.StyleName == "Emphasis")
        run.Font.StyleName = "Strong";

    if (run.Font.StyleIdentifier == StyleIdentifier.IntenseEmphasis)
        run.Font.StyleIdentifier = StyleIdentifier.Strong;
}

doc.Save(ArtifactsDir + "Font.ChangeStyle.docx");
```

### See Also

* enum [StyleIdentifier](../../styleidentifier/)
* class [Font](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
