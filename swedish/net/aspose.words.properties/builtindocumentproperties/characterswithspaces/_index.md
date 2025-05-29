---
title: BuiltInDocumentProperties.CharactersWithSpaces
linktitle: CharactersWithSpaces
articleTitle: CharactersWithSpaces
second_title: Aspose.Words för .NET
description: Upptäck egenskapen BuiltInDocumentProperties CharactersWithSpaces, som uppskattar antalet tecken, inklusive mellanslag, för effektiv dokumenthantering.
type: docs
weight: 50
url: /sv/net/aspose.words.properties/builtindocumentproperties/characterswithspaces/
---
## BuiltInDocumentProperties.CharactersWithSpaces property

Representerar en uppskattning av antalet tecken (inklusive mellanslag) i dokumentet.

```csharp
public int CharactersWithSpaces { get; set; }
```

## Anmärkningar

Aspose.Words uppdaterar den här egenskapen när du anropar[`UpdateWordCount`](../../../aspose.words/document/updatewordcount/).

## Exempel

Visar hur man arbetar med dokumentegenskaper i kategorin "Innehåll".

```csharp
public void Content()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");
    BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

    // Genom att använda inbyggda egenskaper,
    // vi kan behandla dokumentstatistik som ord-/sid-/teckenantal som metadata som kan granskas utan att öppna dokumentet
    // Dessa egenskaper nås genom att högerklicka på filen i Utforskaren och navigera till Egenskaper > Detaljer > Innehåll
    // Om vi vill visa denna data inuti dokumentet kan vi använda fält som NUMPAGES, NUMWORDS, NUMCHARS etc.
    // Dessa värden kan också visas i Microsoft Word genom att navigera Arkiv > Egenskaper > Avancerade egenskaper > Statistik
    // Sidantal: Egenskapen PageCount visar antalet sidor i realtid och dess värde kan tilldelas egenskapen Pages

     // Egenskapen "Sidor" lagrar dokumentets sidantal.
    Assert.AreEqual(6, properties.Pages);

    // De inbyggda egenskaperna "Words", "Characters" och "CharactersWithSpaces" visar också olika dokumentstatistik,
    // men vi måste anropa metoden "UpdateWordCount" på hela dokumentet innan vi kan förvänta oss att de innehåller korrekta värden.
    doc.UpdateWordCount();

    Assert.AreEqual(1035, properties.Words);
    Assert.AreEqual(6026, properties.Characters);
    Assert.AreEqual(7041, properties.CharactersWithSpaces);

    // Räkna antalet rader i dokumentet och tilldela sedan resultatet till den inbyggda egenskapen "Lines".
    LineCounter lineCounter = new LineCounter(doc);
    properties.Lines = lineCounter.GetLineCount();

    Assert.AreEqual(142, properties.Lines);

    // Tilldela antalet styckenoder i dokumentet till den inbyggda egenskapen "Stycken".
    properties.Paragraphs = doc.GetChildNodes(NodeType.Paragraph, true).Count;
    Assert.AreEqual(29, properties.Paragraphs);

    // Få en uppskattning av filstorleken på vårt dokument via den inbyggda egenskapen "Bytes".
    Assert.AreEqual(20310, properties.Bytes);

    // Ställ in en annan mall för vårt dokument och uppdatera sedan den inbyggda egenskapen "Mall" manuellt för att återspegla denna ändring.
    doc.AttachedTemplate = MyDir + "Business brochure.dotx";

    Assert.AreEqual("Normal", properties.Template);

    properties.Template = doc.AttachedTemplate;

    // "ContentStatus" är en beskrivande inbyggd egenskap.
    properties.ContentStatus = "Draft";

    // Vid sparning kommer den inbyggda egenskapen "ContentType" att innehålla MIME-typen för utdataformatet för sparning.
    Assert.AreEqual(string.Empty, properties.ContentType);

    // Om dokumentet innehåller länkar, och alla är uppdaterade, kan vi ställa in egenskapen "LinksUpToDate" till "true".
    Assert.False(properties.LinksUpToDate);

    doc.Save(ArtifactsDir + "DocumentProperties.Content.docx");
}

/// <summary>
/// Räknar raderna i ett dokument.
/// Går igenom dokumentets layoutentitetsträd vid konstruktion,
/// räknar enheter av typen "Linje" som också innehåller riktig text.
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

### Se även

* class [BuiltInDocumentProperties](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)
