---
title: DocumentBuilder.InsertDocument
linktitle: InsertDocument
articleTitle: InsertDocument
second_title: Aspose.Words per .NET
description: Inserisci documenti senza sforzo in qualsiasi posizione del cursore con il metodo InsertDocument di DocumentBuilder. Semplifica il tuo flusso di lavoro e aumenta la produttività!
type: docs
weight: 310
url: /it/net/aspose.words/documentbuilder/insertdocument/
---
## InsertDocument(*[Document](../../document/), [ImportFormatMode](../../importformatmode/)*) {#insertdocument}

Inserisce un documento nella posizione del cursore.

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcDoc | Document | Documento sorgente da inserire. |
| importFormatMode | ImportFormatMode | Specifica come unire la formattazione di stile in conflitto. |

### Valore di ritorno

Primo nodo del contenuto inserito.

## Osservazioni

Questo metodo imita il comportamento di MS Word, come se venisse premuto CTRL+'A' (seleziona tutto il contenuto), quindi CTRL+'C' (copia la selezione nel buffer) all'interno di un documento e quindi CTRL+'V' (inserisci il contenuto dal buffer) all'interno di un altro documento.

## Esempi

Mostra come inserire un documento in un altro documento.

```csharp
Document doc = new Document(MyDir + "Document.docx");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.PageBreak);

Document docToInsert = new Document(MyDir + "Formatted elements.docx");

builder.InsertDocument(docToInsert, ImportFormatMode.KeepSourceFormatting);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.InsertDocument.docx");
```

### Guarda anche

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertDocument(*[Document](../../document/), [ImportFormatMode](../../importformatmode/), [ImportFormatOptions](../../importformatoptions/)*) {#insertdocument_1}

Inserisce un documento nella posizione del cursore.

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcDoc | Document | Documento sorgente da inserire. |
| importFormatMode | ImportFormatMode | Specifica come unire la formattazione di stile in conflitto. |
| importFormatOptions | ImportFormatOptions | Consente di specificare le opzioni che influiscono sulla formattazione di un documento risultante. |

### Valore di ritorno

Primo nodo del contenuto inserito.

## Osservazioni

Questo metodo imita il comportamento di MS Word, come se venisse premuto CTRL+'A' (seleziona tutto il contenuto), quindi CTRL+'C' (copia la selezione nel buffer) all'interno di un documento e quindi CTRL+'V' (inserisci il contenuto dal buffer) all'interno di un altro documento.

## Esempi

Mostra come risolvere gli stili duplicati durante l'inserimento di documenti.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

Style myStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyStyle");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

// Clona il documento e modifica lo stile "MyStyle" del clone, in modo che abbia un colore diverso da quello dell'originale.
// Se inseriamo il clone nel documento originale, i due stili con lo stesso nome causeranno un conflitto.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// Quando abilitiamo SmartStyleBehavior e utilizziamo la modalità di formato di importazione KeepSourceFormatting,
// Aspose.Words risolverà i conflitti di stile convertendo gli stili del documento sorgente.
// con gli stessi nomi degli stili di destinazione in attributi di paragrafo diretti.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### Guarda anche

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
