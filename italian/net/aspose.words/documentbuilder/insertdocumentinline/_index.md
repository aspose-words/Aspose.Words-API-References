---
title: DocumentBuilder.InsertDocumentInline
linktitle: InsertDocumentInline
articleTitle: InsertDocumentInline
second_title: Aspose.Words per .NET
description: Inserisci documenti in linea senza sforzo con il metodo InsertDocumentInline di DocumentBuilder, migliorando il flusso di lavoro e l'esperienza di modifica dei documenti.
type: docs
weight: 320
url: /it/net/aspose.words/documentbuilder/insertdocumentinline/
---
## DocumentBuilder.InsertDocumentInline method

Inserisce un documento in linea nella posizione del cursore.

```csharp
public Node InsertDocumentInline(Document srcDoc, ImportFormatMode importFormatMode, 
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

A differenza di[`InsertDocument`](../insertdocument/) questo metodo sposta il contenuto del paragrafo del documento di destinazione, prima del quale è inserito il documento sorgente, nell'ultimo paragrafo del documento sorgente inserito. In pratica, questo significa che l'interruzione di paragrafo dell'ultimo paragrafo inserito viene rimossa.

Nota: se l'ultimo nodo del documento sorgente non è un paragrafo, non verrà fatto nulla.

## Esempi

Mostra come inserire un documento in linea nella posizione del cursore.

```csharp
DocumentBuilder srcDoc = new DocumentBuilder();
srcDoc.Write("[src content]");

// Crea il documento di destinazione.
DocumentBuilder dstDoc = new DocumentBuilder();
dstDoc.Write("Before ");
dstDoc.InsertNode(new BookmarkStart(dstDoc.Document, "src_place"));
dstDoc.InsertNode(new BookmarkEnd(dstDoc.Document, "src_place"));
dstDoc.Write(" after");

Assert.AreEqual("Before  after", dstDoc.Document.GetText().TrimEnd());

// Inserisce il documento sorgente nella destinazione in linea.
dstDoc.MoveToBookmark("src_place");
dstDoc.InsertDocumentInline(srcDoc.Document, ImportFormatMode.UseDestinationStyles, new ImportFormatOptions());

Assert.AreEqual("Before [src content] after", dstDoc.Document.GetText().TrimEnd());
```

### Guarda anche

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
