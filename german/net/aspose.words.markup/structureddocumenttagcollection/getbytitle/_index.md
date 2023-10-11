---
title: StructuredDocumentTagCollection.GetByTitle
second_title: Aspose.Words für .NET-API-Referenz
description: StructuredDocumentTagCollection methode. Gibt das erste strukturierte DokumentTag zurück das in der Sammlung mit dem angegebenen Titel gefunden wird.
type: docs
weight: 50
url: /de/net/aspose.words.markup/structureddocumenttagcollection/getbytitle/
---
## StructuredDocumentTagCollection.GetByTitle method

Gibt das erste strukturierte Dokument-Tag zurück, das in der Sammlung mit dem angegebenen Titel gefunden wird.

```csharp
public IStructuredDocumentTag GetByTitle(string title)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| title | String | Der Titel des strukturierten Dokument-Tags. |

### Bemerkungen

Gibt null zurück, wenn das strukturierte Dokument-Tag mit dem angegebenen Titel nicht gefunden werden kann.

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


