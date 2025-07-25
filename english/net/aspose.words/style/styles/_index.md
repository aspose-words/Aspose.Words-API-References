---
title: Style.Styles
linktitle: Styles
articleTitle: Styles
second_title: Aspose.Words for .NET
description: Discover the Style Styles property to access a curated collection of styles, enhancing your design with unique, cohesive aesthetics.
type: docs
weight: 190
url: /net/aspose.words/style/styles/
---
## Style.Styles property

Gets the collection of styles this style belongs to.

```csharp
public StyleCollection Styles { get; }
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

* class [StyleCollection](../../stylecollection/)
* class [Style](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
