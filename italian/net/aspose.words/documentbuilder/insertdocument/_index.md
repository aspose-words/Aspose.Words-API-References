---
title: DocumentBuilder.InsertDocument
second_title: Aspose.Words per .NET API Reference
description: DocumentBuilder metodo. Inserisce un documento nella posizione del cursore.
type: docs
weight: 290
url: /it/net/aspose.words/documentbuilder/insertdocument/
---
## InsertDocument(Document, ImportFormatMode) {#insertdocument}

Inserisce un documento nella posizione del cursore.

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcDoc | Document | Documento di origine per l'inserimento. |
| importFormatMode | ImportFormatMode | Specifica come unire la formattazione dello stile in conflitto. |

### Valore di ritorno

Primo nodo del contenuto inserito.

### Osservazioni

Questo metodo imita il comportamento di MS Word, come se fosse stato premuto CTRL+'A' (seleziona tutto il contenuto), poi CTRL+'C' (copia selezionato nel buffer) all'interno di un documento e poi CTRL+'V' (inserisci contenuto dal buffer) all'interno di un altro documento.

### Esempi

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
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)

---

## InsertDocument(Document, ImportFormatMode, ImportFormatOptions) {#insertdocument_1}

Inserisce un documento nella posizione del cursore.

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcDoc | Document | Documento di origine per l'inserimento. |
| importFormatMode | ImportFormatMode | Specifica come unire la formattazione dello stile in conflitto. |
| importFormatOptions | ImportFormatOptions | Consente di specificare le opzioni che influiscono sulla formattazione di un documento risultante. |

### Valore di ritorno

Primo nodo del contenuto inserito.

### Osservazioni

Questo metodo imita il comportamento di MS Word, come se fosse stato premuto CTRL+'A' (seleziona tutto il contenuto), poi CTRL+'C' (copia selezionato nel buffer) all'interno di un documento e poi CTRL+'V' (inserisci contenuto dal buffer) all'interno di un altro documento.

### Esempi

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

// Clona il documento e modifica lo stile "MyStyle" del clone, quindi è di un colore diverso da quello dell'originale.
// Se inseriamo il clone nel documento originale, i due stili con lo stesso nome causeranno uno scontro.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// Quando abilitiamo SmartStyleBehavior e utilizziamo la modalità di formato di importazione KeepSourceFormatting,
// Aspose.Words risolverà i conflitti di stile convertendo gli stili del documento sorgente.
// con gli stessi nomi degli stili di destinazione negli attributi di paragrafo diretto.
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
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)


