---
title: IStructuredDocumentTag.IsMultiSection
linktitle: IsMultiSection
articleTitle: IsMultiSection
second_title: Aspose.Words für .NET
description: Entdecken Sie die IsMultiSection-Eigenschaft des IStructuredDocumentTag, die erkennt, ob es sich bei Ihrem Tag um einen Bereichs-Multisection handelt, und so die Dokumentorganisation und -funktionalität verbessert.
type: docs
weight: 40
url: /de/net/aspose.words.markup/istructureddocumenttag/ismultisection/
---
## IStructuredDocumentTag.IsMultiSection property

Gibt „true“ zurück, wenn diese Instanz ein strukturierter Dokumenttag mit mehreren Abschnitten ist.

```csharp
public bool IsMultiSection { get; }
```

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

* interface [IStructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
