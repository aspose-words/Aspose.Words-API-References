---
title: ImportFormatOptions.ForceCopyStyles
second_title: Aspose.Words för .NET API Referens
description: ImportFormatOptions fast egendom. Hämtar eller ställer in ett booleskt värde som anger antingen att kopiera motstridiga stilar inKeepSourceFormatting mode. Standardvärdet ärfalsk .
type: docs
weight: 30
url: /sv/net/aspose.words/importformatoptions/forcecopystyles/
---
## ImportFormatOptions.ForceCopyStyles property

Hämtar eller ställer in ett booleskt värde som anger antingen att kopiera motstridiga stilar inKeepSourceFormatting mode. Standardvärdet är`falsk` .

```csharp
public bool ForceCopyStyles { get; set; }
```

### Anmärkningar

Som standard, om en matchande stil redan finns i ett måldokument, utökas källformatet formatting till direkta nodattribut och stilen för denna nod återställs till en standard.

När detta alternativ är inställt på`Sann`, kommer källformatet att tvångskopieras till måldokument med unikt namn och tillämpas på den importerade noden.

Observera, i det här fallet är det inte garanterat att formateringen av den importerade noden i destination document kommer att bevaras.

### Exempel

Visar hur man kopierar källstilar med unika namn med tvång.

```csharp
// Båda dokumenten innehåller MyStyle1 och MyStyle2, MyStyle3 finns bara i ett källdokument.
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
* namnutrymme [Aspose.Words](../../importformatoptions/)
* hopsättning [Aspose.Words](../../../)


