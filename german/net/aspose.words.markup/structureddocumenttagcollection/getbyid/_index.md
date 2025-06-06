---
title: StructuredDocumentTagCollection.GetById
linktitle: GetById
articleTitle: GetById
second_title: Aspose.Words für .NET
description: Rufen Sie strukturierte Dokument-Tags mühelos mit der GetById-Methode ab. Greifen Sie schnell auf Ihre Daten zu und steigern Sie die Effizienz Ihres Dokumentenmanagements.
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
| id | Int32 | Die strukturierte Dokument-Tag-Kennung. |

## Bemerkungen

Gibt null zurück, wenn das strukturierte Dokument-Tag mit der angegebenen Kennung nicht gefunden werden kann.

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
