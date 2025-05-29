---
title: Range.StructuredDocumentTags
linktitle: StructuredDocumentTags
articleTitle: StructuredDocumentTags
second_title: Aspose.Words per .NET
description: Scopri la proprietà Range StructuredDocumentTags, che fornisce una raccolta completa di tag di documenti strutturati, migliorando l'organizzazione e la funzionalità del tuo documento.
type: docs
weight: 50
url: /it/net/aspose.words/range/structureddocumenttags/
---
## Range.StructuredDocumentTags property

Restituisce un`StructuredDocumentTags` raccolta che rappresenta tutti i tag di documenti strutturati nell'intervallo.

```csharp
public StructuredDocumentTagCollection StructuredDocumentTags { get; }
```

## Esempi

Mostra come rimuovere il tag del documento strutturato.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

StructuredDocumentTagCollection structuredDocumentTags = doc.Range.StructuredDocumentTags;
IStructuredDocumentTag sdt;
for (int i = 0; i < structuredDocumentTags.Count; i++)
{
    sdt = structuredDocumentTags[i];
    Console.WriteLine(sdt.Title);
}

sdt = structuredDocumentTags.GetById(1691867797);
Assert.AreEqual(1691867797, sdt.Id);

Assert.AreEqual(5, structuredDocumentTags.Count);
// Rimuovi il tag del documento strutturato tramite Id.
structuredDocumentTags.Remove(1691867797);
// Rimuovi il tag del documento strutturato dalla posizione 0.
structuredDocumentTags.RemoveAt(0);
Assert.AreEqual(3, structuredDocumentTags.Count);
```

### Guarda anche

* class [StructuredDocumentTagCollection](../../../aspose.words.markup/structureddocumenttagcollection/)
* class [Range](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
