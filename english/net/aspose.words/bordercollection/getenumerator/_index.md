---
title: BorderCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words for .NET
description: BorderCollection GetEnumerator method. Returns an enumerator object that can be used to iterate over all borders in the collection in C#.
type: docs
weight: 160
url: /net/aspose.words/bordercollection/getenumerator/
---
## BorderCollection.GetEnumerator method

Returns an enumerator object that can be used to iterate over all borders in the collection.

```csharp
public IEnumerator<Border> GetEnumerator()
```

## Examples

Shows how to iterate over and edit all of the borders in a paragraph format object.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Configure the builder's paragraph format settings to create a green wave border on all sides.
BorderCollection borders = builder.ParagraphFormat.Borders;

using (IEnumerator<Border> enumerator = borders.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Border border = enumerator.Current;
        border.Color = Color.Green;
        border.LineStyle = LineStyle.Wave;
        border.LineWidth = 3;
    }
}

// Insert a paragraph. Our border settings will determine the appearance of its border.
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "BorderCollection.GetBordersEnumerator.docx");
```

### See Also

* class [Border](../../border/)
* class [BorderCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
