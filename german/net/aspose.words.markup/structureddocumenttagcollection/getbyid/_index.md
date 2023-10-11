---
title: StructuredDocumentTagCollection.GetById
second_title: Aspose.Words für .NET-API-Referenz
description: StructuredDocumentTagCollection methode. Gibt das strukturierte DokumentTag nach Kennung zurück.
type: docs
weight: 30
url: /de/net/aspose.words.markup/structureddocumenttagcollection/getbyid/
---
## StructuredDocumentTagCollection.GetById method

Gibt das strukturierte Dokument-Tag nach Kennung zurück.

```csharp
public IStructuredDocumentTag GetById(int id)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| id | Int32 | Die Tag-ID des strukturierten Dokuments. |

### Bemerkungen

Gibt null zurück, wenn das strukturierte Dokument-Tag mit der angegebenen Kennung nicht gefunden werden kann.

### Beispiele

Zeigt, wie man ein strukturiertes Dokument-Tag erhält.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Holen Sie sich das Tag des strukturierten Dokuments anhand der ID.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsRanged());
Console.WriteLine(sdt.Title);

// Holen Sie sich das strukturierte Dokument-Tag oder das Bereichs-Tag nach Titel.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### Siehe auch

* interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* class [StructuredDocumentTagCollection](../)
* namensraum [Aspose.Words.Markup](../../structureddocumenttagcollection/)
* Montage [Aspose.Words](../../../)


