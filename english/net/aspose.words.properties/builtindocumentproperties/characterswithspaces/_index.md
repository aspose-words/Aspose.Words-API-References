---
title: BuiltInDocumentProperties.CharactersWithSpaces
linktitle: CharactersWithSpaces
articleTitle: CharactersWithSpaces
second_title: Aspose.Words for .NET
description: Discover the BuiltInDocumentProperties CharactersWithSpaces property, which estimates character count, including spaces, for efficient document management.
type: docs
weight: 50
url: /net/aspose.words.properties/builtindocumentproperties/characterswithspaces/
---
## BuiltInDocumentProperties.CharactersWithSpaces property

Represents an estimate of the number of characters (including spaces) in the document.

```csharp
public int CharactersWithSpaces { get; set; }
```

## Remarks

Aspose.Words updates this property when you call [`UpdateWordCount`](../../../aspose.words/document/updatewordcount/).

## Examples

Shows how to work with document properties in the "Content" category.

```csharp
public void Content()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");
    BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

    // By using built in properties,
    // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
    // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
    // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
    // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
    // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

    // The "Pages" property stores the page count of the document. 
    Assert.That(properties.Pages, Is.EqualTo(6));

    // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
    // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
    doc.UpdateWordCount();

    Assert.That(properties.Words, Is.EqualTo(1035));
    Assert.That(properties.Characters, Is.EqualTo(6026));
    Assert.That(properties.CharactersWithSpaces, Is.EqualTo(7041));

    // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
    LineCounter lineCounter = new LineCounter(doc);
    properties.Lines = lineCounter.GetLineCount();

    Assert.That(properties.Lines, Is.EqualTo(142));

    // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
    properties.Paragraphs = doc.GetChildNodes(NodeType.Paragraph, true).Count;
    Assert.That(properties.Paragraphs, Is.EqualTo(29));

    // Get an estimate of the file size of our document via the "Bytes" built-in property.
    Assert.That(properties.Bytes, Is.EqualTo(20310));

    // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
    doc.AttachedTemplate = MyDir + "Business brochure.dotx";

    Assert.That(properties.Template, Is.EqualTo("Normal"));

    properties.Template = doc.AttachedTemplate;

    // "ContentStatus" is a descriptive built-in property.
    properties.ContentStatus = "Draft";

    // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
    Assert.That(properties.ContentType, Is.EqualTo(string.Empty));

    // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
    Assert.That(properties.LinksUpToDate, Is.False);

    doc.Save(ArtifactsDir + "DocumentProperties.Content.docx");
}

/// <summary>
/// Counts the lines in a document.
/// Traverses the document's layout entities tree upon construction,
/// counting entities of the "Line" type that also contain real text.
/// </summary>
private class LineCounter
{
    public LineCounter(Document doc)
    {
        mLayoutEnumerator = new LayoutEnumerator(doc);

        CountLines();
    }

    public int GetLineCount()
    {
        return mLineCount;
    }

    private void CountLines()
    {
        do
        {
            if (mLayoutEnumerator.Type == LayoutEntityType.Line)
            {
                mScanningLineForRealText = true;
            }

            if (mLayoutEnumerator.MoveFirstChild())
            {
                if (mScanningLineForRealText && mLayoutEnumerator.Kind.StartsWith("TEXT"))
                {
                    mLineCount++;
                    mScanningLineForRealText = false;
                }
                CountLines();
                mLayoutEnumerator.MoveParent();
            }
        } while (mLayoutEnumerator.MoveNext());
    }

    private readonly LayoutEnumerator mLayoutEnumerator;
    private int mLineCount;
    private bool mScanningLineForRealText;
}
```

### See Also

* class [BuiltInDocumentProperties](../)
* namespace [Aspose.Words.Properties](../../../aspose.words.properties/)
* assembly [Aspose.Words](../../../)
