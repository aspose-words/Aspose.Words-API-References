---
title: ImportFormatOptions.ForceCopyStyles
linktitle: ForceCopyStyles
articleTitle: ForceCopyStyles
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ImportFormatOptions ForceCopyStyles och styr enkelt kopiering av stilar i KeepSourceFormatting-läget. Standardvärdet är falskt för optimala resultat.
type: docs
weight: 30
url: /sv/net/aspose.words/importformatoptions/forcecopystyles/
---
## ImportFormatOptions.ForceCopyStyles property

Hämtar eller anger ett booleskt värde som anger att antingen motstridiga stilar ska kopieras inKeepSourceFormatting läge. Standardvärdet är`falsk` .

```csharp
public bool ForceCopyStyles { get; set; }
```

## Anmärkningar

Som standard, om ett matchande format redan finns i ett måldokument, expanderas källformatet formatering till direkta nodattribut och formatet för denna nod återställs till standardinställningen.

När det här alternativet är inställt på`sann`, källstilen kommer att tvångskopieras till destinationsdokumentet med ett unikt namn och tillämpas på den importerade noden.

Observera att det i det här fallet inte garanteras att formateringen av den importerade noden i destinationsdokumentet document kommer att bevaras.

## Exempel

Visar hur man tvångskopierar källformat med unika namn.

```csharp
// Båda dokumenten innehåller MinStil1 och MinStil2, MinStil3 finns bara i ett källdokument.
Document srcDoc = new Document(MyDir + "Styles source.docx");
Document dstDoc = new Document(MyDir + "Styles destination.docx");

ImportFormatOptions options = new ImportFormatOptions { ForceCopyStyles = true };
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

ParagraphCollection paras = dstDoc.Sections[1].Body.Paragraphs;

Assert.AreEqual(paras[0].ParagraphFormat.Style.Name, "MyStyle1_0");
Assert.AreEqual(paras[1].ParagraphFormat.Style.Name, "MyStyle2_0");
Assert.AreEqual(paras[2].ParagraphFormat.Style.Name, "MyStyle3");
```

### Se även

* class [ImportFormatOptions](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
