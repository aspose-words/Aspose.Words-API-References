---
title: DocumentBuilder.InsertDocumentInline
linktitle: InsertDocumentInline
articleTitle: InsertDocumentInline
second_title: Aspose.Words för .NET
description: Infoga enkelt dokument i linje med DocumentBuilder InsertDocumentInline-metoden, vilket förbättrar ditt arbetsflöde och din dokumentredigeringsupplevelse.
type: docs
weight: 320
url: /sv/net/aspose.words/documentbuilder/insertdocumentinline/
---
## DocumentBuilder.InsertDocumentInline method

Infogar ett dokument inbäddat vid markörens position.

```csharp
public Node InsertDocumentInline(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcDoc | Document | Källdokument för infogning. |
| importFormatMode | ImportFormatMode | Anger hur formatering som krockar ska sammanfogas. |
| importFormatOptions | ImportFormatOptions | Gör det möjligt att ange alternativ som påverkar formateringen av ett resultatdokument. |

### Returvärde

Första noden för det infogade innehållet.

## Anmärkningar

Den här metoden imiterar beteendet i MS Word, som om CTRL+'A' (markera allt innehåll) trycktes, sedan CTRL+'C' (kopiera markerat till bufferten) i ett dokument och sedan CTRL+'V' (infoga innehåll från bufferten) i ett annat dokument.

Som en skillnad från[`InsertDocument`](../insertdocument/) den här metoden flyttar innehållet i stycket i destinationsdokumentet, före vilket källdokumentet infogas, till det sista stycket i det infogade källdokumentet. Detta innebär i själva verket att styckebrytningen i det senast infogade stycket tas bort.

Observera att om den sista noden i källdokumentet inte är ett stycke, kommer ingenting att göras.

## Exempel

Visar hur man infogar ett dokument inbäddat vid markörens position.

```csharp
DocumentBuilder srcDoc = new DocumentBuilder();
srcDoc.Write("[src content]");

// Skapa måldokument.
DocumentBuilder dstDoc = new DocumentBuilder();
dstDoc.Write("Before ");
dstDoc.InsertNode(new BookmarkStart(dstDoc.Document, "src_place"));
dstDoc.InsertNode(new BookmarkEnd(dstDoc.Document, "src_place"));
dstDoc.Write(" after");

Assert.AreEqual("Before  after", dstDoc.Document.GetText().TrimEnd());

// Infoga källdokument i destinationstexten.
dstDoc.MoveToBookmark("src_place");
dstDoc.InsertDocumentInline(srcDoc.Document, ImportFormatMode.UseDestinationStyles, new ImportFormatOptions());

Assert.AreEqual("Before [src content] after", dstDoc.Document.GetText().TrimEnd());
```

### Se även

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
