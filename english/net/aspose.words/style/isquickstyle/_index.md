---
title: Style.IsQuickStyle
linktitle: IsQuickStyle
articleTitle: IsQuickStyle
second_title: Aspose.Words for .NET API Reference
description: Style IsQuickStyle property. Specifies whether this style is shown in the Quick Style gallery inside MS Word UI in C#.
type: docs
weight: 80
url: /net/aspose.words/style/isquickstyle/
---
## Style.IsQuickStyle property

Specifies whether this style is shown in the Quick Style gallery inside MS Word UI.

```csharp
public bool IsQuickStyle { get; set; }
```

## Examples

Shows how to access a document's style collection.

```csharp
Document doc = new Document();

Assert.AreEqual(4, doc.Styles.Count);

// Enumerate and list all the styles that a document created using Aspose.Words contains by default.
using (IEnumerator<Style> stylesEnum = doc.Styles.GetEnumerator())
{
    while (stylesEnum.MoveNext())
    {
        Style curStyle = stylesEnum.Current;
        Console.WriteLine($"Style name:\t\"{curStyle.Name}\", of type \"{curStyle.Type}\"");
        Console.WriteLine($"\tSubsequent style:\t{curStyle.NextParagraphStyleName}");
        Console.WriteLine($"\tIs heading:\t\t\t{curStyle.IsHeading}");
        Console.WriteLine($"\tIs QuickStyle:\t\t{curStyle.IsQuickStyle}");

        Assert.AreEqual(doc, curStyle.Document);
    }
}
```

### See Also

* class [Style](../)
* namespace [Aspose.Words](../../style/)
* assembly [Aspose.Words](../../../)
