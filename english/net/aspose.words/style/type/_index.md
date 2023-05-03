---
title: Style.Type
linktitle: Type
second_title: Aspose.Words for .NET API Reference
description: Style Type property. Gets the style type paragraph or character in C#.
type: docs
weight: 170
url: /net/aspose.words/style/type/
---
## Style.Type property

Gets the style type (paragraph or character).

```csharp
public StyleType Type { get; }
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

* enum [StyleType](../../styletype/)
* class [Style](../)
* namespace [Aspose.Words](../../style/)
* assembly [Aspose.Words](../../../)
