---
title: Paragraphs
second_title: Aspose.Words för .NET API Referens
description: Representerar en uppskattning av antalet stycken i dokumentet.
type: docs
weight: 230
url: /sv/net/aspose.words.properties/builtindocumentproperties/paragraphs/
---
## BuiltInDocumentProperties.Paragraphs property

Representerar en uppskattning av antalet stycken i dokumentet.

```csharp
public int Paragraphs { get; set; }
```

### Anmärkningar

Aspose.Words uppdaterar den här egenskapen när du ringer[`UpdateWordCount`](../../../aspose.words/document/updatewordcount).

### Exempel

Visar hur du uppdaterar alla listetiketter i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words spårar inte dokumentmått som dessa i realtid.
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// För att få korrekta värden för tre av dessa egenskaper måste vi uppdatera dem manuellt.
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// För radräkningen måste vi anropa en specifik överbelastning av uppdateringsmetoden.
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

Visar hur man arbetar med dokumentegenskaper i kategorin "Innehåll".

```csharp
public void Content()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");
    BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

    // Genom att använda inbyggda egenskaper,
    // vi kan behandla dokumentstatistik som ord/sida/teckenantal som metadata som man kan titta på utan att öppna dokumentet
    // Dessa egenskaper nås genom att högerklicka på filen i Utforskaren och navigera till Egenskaper > Detaljer > Innehåll
    // Om vi vill visa dessa data inuti dokumentet kan vi använda fält som NUMPAGES, NUMWORDS, NUMCHARS etc.
    // Dessa värden kan också ses i Microsoft Word genom att navigera i Arkiv > Egenskaper > Avancerade egenskaper > Statistik
    // Antal sidor: Egenskapen PageCount visar antalet sidor i realtid och dess värde kan tilldelas egenskapen Sidor

    // Egenskapen "Sidor" lagrar antalet sidor i dokumentet. 
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

    // Tilldela antalet paragrafnoder i dokumentet till den inbyggda egenskapen "Paragraphs".
    properties.Paragraphs = doc.GetChildNodes(NodeType.Paragraph, true).Count;
    Assert.AreEqual(29, properties.Paragraphs);

    // Få en uppskattning av filstorleken på vårt dokument via den inbyggda "Bytes"-egenskapen.
    Assert.AreEqual(20310, properties.Bytes);

    // Ställ in en annan mall för vårt dokument och uppdatera sedan den inbyggda egenskapen "Mall" manuellt för att återspegla denna ändring.
    doc.AttachedTemplate = MyDir + "Business brochure.dotx";

    Assert.AreEqual("Normal", properties.Template);    

    properties.Template = doc.AttachedTemplate;

    // "ContentStatus" är en beskrivande inbyggd egenskap.
    properties.ContentStatus = "Draft";

    // När du har sparat kommer den inbyggda "ContentType"-egenskapen att innehålla MIME-typen för utdatasparformatet.
    Assert.AreEqual(string.Empty, properties.ContentType);

    // Om dokumentet innehåller länkar, och alla är uppdaterade, kan vi ställa in egenskapen "LinksUpToDate" till "true".
    Assert.False(properties.LinksUpToDate);

    doc.Save(ArtifactsDir + "DocumentProperties.Content.docx");
}

/// <summary>
/// Räknar raderna i ett dokument.
/// Går igenom dokumentets layoutentitetsträd vid konstruktion,
/// räknande enheter av typen "Linje" som också innehåller riktig text.
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

* class [BuiltInDocumentProperties](../../builtindocumentproperties)
* namnutrymme [Aspose.Words.Properties](../../builtindocumentproperties)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
