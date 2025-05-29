---
title: StructuredDocumentTagCollection Class
linktitle: StructuredDocumentTagCollection
articleTitle: StructuredDocumentTagCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Markup.StructuredDocumentTagCollection für die effiziente Verwaltung strukturierter Dokument-Tags und verbessern Sie so Ihre Dokumentverarbeitungsfunktionen.
type: docs
weight: 4760
url: /de/net/aspose.words.markup/structureddocumenttagcollection/
---
## StructuredDocumentTagCollection class

Eine Sammlung von[`IStructuredDocumentTag`](../istructureddocumenttag/) Instanzen, die die strukturierten Dokument-Tags im angegebenen Bereich darstellen.

Um mehr zu erfahren, besuchen Sie die[Strukturierte Dokument-Tags oder Inhaltssteuerung](https://docs.aspose.com/words/net/working-with-content-control-sdt/) Dokumentationsartikel.

```csharp
public class StructuredDocumentTagCollection : IEnumerable<IStructuredDocumentTag>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.markup/structureddocumenttagcollection/count/) { get; } | Gibt die Anzahl der strukturierten Dokument-Tags in der Sammlung zurück. |
| [Item](../../aspose.words.markup/structureddocumenttagcollection/item/) { get; } | Gibt das strukturierte Dokument-Tag am angegebenen Index zurück. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetById](../../aspose.words.markup/structureddocumenttagcollection/getbyid/)(*int*) | Gibt das strukturierte Dokument-Tag nach Kennung zurück. |
| [GetByTag](../../aspose.words.markup/structureddocumenttagcollection/getbytag/)(*string*) | Gibt das erste strukturierte Dokument-Tag zurück, das in der Sammlung mit dem angegebenen Tag gefunden wurde. |
| [GetByTitle](../../aspose.words.markup/structureddocumenttagcollection/getbytitle/)(*string*) | Gibt das erste strukturierte Dokument-Tag zurück, das in der Sammlung mit dem angegebenen Titel gefunden wurde. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagcollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück. |
| [Remove](../../aspose.words.markup/structureddocumenttagcollection/remove/)(*int*) | Entfernt das strukturierte Dokument-Tag mit der angegebenen Kennung. |
| [RemoveAt](../../aspose.words.markup/structureddocumenttagcollection/removeat/)(*int*) | Entfernt ein strukturiertes Dokument-Tag am angegebenen Index. |

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

* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)
