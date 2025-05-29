---
title: DocumentBuilder.InsertDocument
linktitle: InsertDocument
articleTitle: InsertDocument
second_title: Aspose.Words för .NET
description: Infoga enkelt dokument var som helst vid markören med DocumentBuilders InsertDocument-metod. Effektivisera ditt arbetsflöde och öka produktiviteten!
type: docs
weight: 310
url: /sv/net/aspose.words/documentbuilder/insertdocument/
---
## InsertDocument(*[Document](../../document/), [ImportFormatMode](../../importformatmode/)*) {#insertdocument}

Infogar ett dokument vid markörens position.

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcDoc | Document | Källdokument för infogning. |
| importFormatMode | ImportFormatMode | Anger hur formatering som krockar ska sammanfogas. |

### Returvärde

Första noden för det infogade innehållet.

## Anmärkningar

Den här metoden imiterar beteendet i MS Word, som om CTRL+'A' (markera allt innehåll) trycktes, sedan CTRL+'C' (kopiera markerat till bufferten) i ett dokument och sedan CTRL+'V' (infoga innehåll från bufferten) i ett annat dokument.

## Exempel

Visar hur man infogar ett dokument i ett annat dokument.

```csharp
Document doc = new Document(MyDir + "Document.docx");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.PageBreak);

Document docToInsert = new Document(MyDir + "Formatted elements.docx");

builder.InsertDocument(docToInsert, ImportFormatMode.KeepSourceFormatting);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.InsertDocument.docx");
```

### Se även

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertDocument(*[Document](../../document/), [ImportFormatMode](../../importformatmode/), [ImportFormatOptions](../../importformatoptions/)*) {#insertdocument_1}

Infogar ett dokument vid markörens position.

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode, 
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

## Exempel

Visar hur man åtgärdar dubbletter av format när man infogar dokument.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

Style myStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyStyle");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

// Klona dokumentet och redigera klonens "MyStyle"-stil så att den har en annan färg än originalets.
// Om vi infogar klonen i originaldokumentet kommer de två stilarna med samma namn att orsaka en kollision.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// När vi aktiverar SmartStyleBehavior och använder importformatläget KeepSourceFormatting,
// Aspose.Words löser stilkrockar genom att konvertera källdokumentets stilar.
// med samma namn som destinationsformat till direkta styckeattribut.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### Se även

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
