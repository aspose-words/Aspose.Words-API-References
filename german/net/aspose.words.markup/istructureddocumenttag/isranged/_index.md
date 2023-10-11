---
title: IStructuredDocumentTag.IsRanged
second_title: Aspose.Words für .NET-API-Referenz
description: IStructuredDocumentTag methode. Gibt true zurück wenn es sich bei dieser Instanz um ein strukturiertes DokumentTag im Bereich handelt.
type: docs
weight: 140
url: /de/net/aspose.words.markup/istructureddocumenttag/isranged/
---
## IStructuredDocumentTag.IsRanged method

Gibt „true“ zurück, wenn es sich bei dieser Instanz um ein strukturiertes Dokument-Tag im Bereich handelt.

```csharp
public bool IsRanged()
```

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

* interface [IStructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../istructureddocumenttag/)
* Montage [Aspose.Words](../../../)


