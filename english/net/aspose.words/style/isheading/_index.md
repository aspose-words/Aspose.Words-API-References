---
title: Style.IsHeading
linktitle: IsHeading
articleTitle: IsHeading
second_title: Aspose.Words for .NET
description: Discover the IsHeading property. Easily identify if a style is a built-in Heading style, enhancing your document's structure and readability.
type: docs
weight: 70
url: /net/aspose.words/style/isheading/
---
## Style.IsHeading property

True when the style is one of the built-in Heading styles.

```csharp
public bool IsHeading { get; }
```

## Examples

Shows how to access a document's style collection.

```csharp
Document doc = new Document();

Assert.That(doc.Styles.Count, Is.EqualTo(4));

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

        Assert.That(curStyle.Document, Is.EqualTo(doc));
    }
}
```

### See Also

* class [Style](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
