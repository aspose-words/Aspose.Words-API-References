---
title: Style.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words for .NET
description: Discover the Style Name property, easily manage and customize your styles for enhanced design flexibility and user experience.
type: docs
weight: 130
url: /net/aspose.words/style/name/
---
## Style.Name property

Gets or sets the name of the style.

```csharp
public string Name { get; set; }
```

## Remarks

Can not be empty string.

If there already is a style with such name in the collection, then this style will override it. All affected nodes will reference new style.

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

Shows how to clone a document's style.

```csharp
Document doc = new Document();

// The AddCopy method creates a copy of the specified style and
// automatically generates a new name for the style, such as "Heading 1_0".
Style newStyle = doc.Styles.AddCopy(doc.Styles["Heading 1"]);

// Use the style's "Name" property to change the style's identifying name.
newStyle.Name = "My Heading 1";

// Our document now has two identical looking styles with different names.
// Changing settings of one of the styles do not affect the other.
newStyle.Font.Color = Color.Red;

Assert.That(newStyle.Name, Is.EqualTo("My Heading 1"));
Assert.That(doc.Styles["Heading 1"].Name, Is.EqualTo("Heading 1"));

Assert.That(newStyle.Type, Is.EqualTo(doc.Styles["Heading 1"].Type));
Assert.That(newStyle.Font.Name, Is.EqualTo(doc.Styles["Heading 1"].Font.Name));
Assert.That(newStyle.Font.Size, Is.EqualTo(doc.Styles["Heading 1"].Font.Size));
Assert.That(newStyle.Font.Color, Is.Not.EqualTo(doc.Styles["Heading 1"].Font.Color));
```

### See Also

* class [Style](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
