---
title: IStructuredDocumentTag.IsMultiSection
linktitle: IsMultiSection
articleTitle: IsMultiSection
second_title: Aspose.Words per .NET
description: Scopri la proprietà IsMultiSection di IStructuredDocumentTag, che identifica se il tag è una multisezione con intervallo, migliorando l'organizzazione e la funzionalità del documento.
type: docs
weight: 40
url: /it/net/aspose.words.markup/istructureddocumenttag/ismultisection/
---
## IStructuredDocumentTag.IsMultiSection property

Restituisce true se questa istanza è un tag di documento strutturato con intervallo (multi-sezione).

```csharp
public bool IsMultiSection { get; }
```

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

* interface [IStructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
