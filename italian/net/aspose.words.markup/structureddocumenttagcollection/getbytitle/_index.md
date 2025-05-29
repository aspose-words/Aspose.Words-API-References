---
title: StructuredDocumentTagCollection.GetByTitle
linktitle: GetByTitle
articleTitle: GetByTitle
second_title: Aspose.Words per .NET
description: Scopri il metodo GetByTitle in StructuredDocumentTagCollection, che recupera in modo efficiente il primo tag del documento in base al titolo, per una gestione semplificata dei dati.
type: docs
weight: 50
url: /it/net/aspose.words.markup/structureddocumenttagcollection/getbytitle/
---
## StructuredDocumentTagCollection.GetByTitle method

Restituisce il primo tag di documento strutturato riscontrato nella raccolta con il titolo specificato.

```csharp
public IStructuredDocumentTag GetByTitle(string title)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| title | String | Il tag del titolo del documento strutturato. |

## Osservazioni

Restituisce null se non è possibile trovare il tag del documento strutturato con il titolo specificato.

## Esempi

Mostra come ottenere il tag del documento strutturato.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Ottieni il tag del documento strutturato tramite Id.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsMultiSection);
Console.WriteLine(sdt.Title);

// Ottieni il tag del documento strutturato o il tag con intervallo in base al titolo.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### Guarda anche

* interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* class [StructuredDocumentTagCollection](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
