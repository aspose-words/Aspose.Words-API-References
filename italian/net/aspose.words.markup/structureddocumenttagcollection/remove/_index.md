---
title: StructuredDocumentTagCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words per .NET
description: Rimuovi senza sforzo specifici tag di documenti strutturati utilizzando il metodo Remove di StructuredDocumentTagCollection per una gestione semplificata dei documenti.
type: docs
weight: 70
url: /it/net/aspose.words.markup/structureddocumenttagcollection/remove/
---
## StructuredDocumentTagCollection.Remove method

Rimuove il tag del documento strutturato con l'identificatore specificato.

```csharp
public void Remove(int id)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| id | Int32 | Identificatore del tag del documento strutturato. |

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

* class [StructuredDocumentTagCollection](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
