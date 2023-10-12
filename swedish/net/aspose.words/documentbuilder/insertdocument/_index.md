---
title: DocumentBuilder.InsertDocument
second_title: Aspose.Words för .NET API Referens
description: DocumentBuilder metod. Infogar ett dokument vid markörens position.
type: docs
weight: 310
url: /sv/net/aspose.words/documentbuilder/insertdocument/
---
## InsertDocument(Document, ImportFormatMode) {#insertdocument}

Infogar ett dokument vid markörens position.

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcDoc | Document | Källdokument för insättning. |
| importFormatMode | ImportFormatMode | Anger hur stilformatering som krockar sammanfogas. |

### Returvärde

Första noden av det infogade innehållet.

### Anmärkningar

Den här metoden efterliknar MS Word-beteendet, som om CTRL+'A' (välj allt innehåll) trycktes, sedan CTRL+'C' (kopiera vald i bufferten) i ett document och sedan CTRL+'V' (infoga innehåll från buffert) inuti ett annat dokument.

### Exempel

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
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)

---

## InsertDocument(Document, ImportFormatMode, ImportFormatOptions) {#insertdocument_1}

Infogar ett dokument vid markörens position.

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcDoc | Document | Källdokument för insättning. |
| importFormatMode | ImportFormatMode | Anger hur stilformatering som krockar sammanfogas. |
| importFormatOptions | ImportFormatOptions | Tillåter att ange alternativ som påverkar formateringen av ett resultatdokument. |

### Returvärde

Första noden av det infogade innehållet.

### Anmärkningar

Den här metoden efterliknar MS Word-beteendet, som om CTRL+'A' (välj allt innehåll) trycktes, sedan CTRL+'C' (kopiera vald i bufferten) i ett document och sedan CTRL+'V' (infoga innehåll från buffert) inuti ett annat dokument.

### Exempel

Visar hur du löser dubbletter av stilar när du infogar dokument.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

Style myStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyStyle");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

// Klona dokumentet och redigera klonens "MyStyle"-stil, så det är en annan färg än originalets.
// Om vi infogar klonen i originaldokumentet kommer de två stilarna med samma namn att orsaka en konflikt.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// När vi aktiverar SmartStyleBehavior och använder importformatläget KeepSourceFormatting,
// Aspose.Words kommer att lösa stilkrockar genom att konvertera källdokumentstilar.
// med samma namn som målstilar till direkta styckeattribut.
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
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)


