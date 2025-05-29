---
title: StructuredDocumentTagCollection.GetByTitle
linktitle: GetByTitle
articleTitle: GetByTitle
second_title: Aspose.Words für .NET
description: Entdecken Sie die Methode GetByTitle in StructuredDocumentTagCollection, die effizient das erste Dokument-Tag nach Titel abruft und so die Datenverwaltung optimiert.
type: docs
weight: 50
url: /de/net/aspose.words.markup/structureddocumenttagcollection/getbytitle/
---
## StructuredDocumentTagCollection.GetByTitle method

Gibt das erste strukturierte Dokument-Tag zurück, das in der Sammlung mit dem angegebenen Titel gefunden wurde.

```csharp
public IStructuredDocumentTag GetByTitle(string title)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| title | String | Der Titel des strukturierten Dokument-Tags. |

## Bemerkungen

Gibt null zurück, wenn das strukturierte Dokument-Tag mit dem angegebenen Titel nicht gefunden werden kann.

## Beispiele

Zeigt, wie man strukturierte Dokument-Tags erhält.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Holen Sie sich das strukturierte Dokument-Tag nach ID.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsMultiSection);
Console.WriteLine(sdt.Title);

// Holen Sie sich das strukturierte Dokument-Tag oder das Bereichs-Tag nach Titel.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### Siehe auch

* interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* class [StructuredDocumentTagCollection](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
