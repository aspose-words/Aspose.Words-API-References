---
title: StructuredDocumentTagCollection.GetByTitle
second_title: Aspose.Words per .NET API Reference
description: StructuredDocumentTagCollection metodo. Restituisce il primo tag di documento strutturato riscontrato nella raccolta con il titolo specificato.
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
| title | String | Il titolo del tag del documento strutturato. |

### Osservazioni

Restituisce null se non è possibile trovare il tag del documento strutturato con il titolo specificato.

### Esempi

Mostra come ottenere il tag del documento strutturato.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Ottieni il tag del documento strutturato in base all'ID.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsRanged());
Console.WriteLine(sdt.Title);

// Ottieni il tag del documento strutturato o il tag con intervalli in base al titolo.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### Guarda anche

* interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* class [StructuredDocumentTagCollection](../)
* spazio dei nomi [Aspose.Words.Markup](../../structureddocumenttagcollection/)
* assemblea [Aspose.Words](../../../)


