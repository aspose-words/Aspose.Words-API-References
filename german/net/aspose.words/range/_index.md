---
title: Range Class
linktitle: Range
articleTitle: Range
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.Range-Klasse, Ihren Schlüssel zur mühelosen Verwaltung von Dokumentabschnitten. Verbessern Sie Ihre Dokumentenverarbeitung mit nahtloser Kontrolle und Flexibilität.
type: docs
weight: 5250
url: /de/net/aspose.words/range/
---
## Range class

Stellt einen zusammenhängenden Bereich in einem Dokument dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Bereichen](https://docs.aspose.com/words/net/working-with-ranges/) Dokumentationsartikel.

```csharp
public class Range : IEnumerable<Node>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Bookmarks](../../aspose.words/range/bookmarks/) { get; } | Gibt einen[`Bookmarks`](./bookmarks/) Sammlung, die alle Lesezeichen im Bereich darstellt. |
| [Fields](../../aspose.words/range/fields/) { get; } | Gibt einen[`Fields`](./fields/) Sammlung, die alle Felder im Bereich darstellt. |
| [FormFields](../../aspose.words/range/formfields/) { get; } | Gibt einen[`FormFields`](./formfields/) Sammlung, die alle Formularfelder im Bereich darstellt. |
| [Revisions](../../aspose.words/range/revisions/) { get; } | Ruft eine Sammlung von Revisionen (nachverfolgten Änderungen) ab, die in diesem Bereich vorhanden sind. |
| [StructuredDocumentTags](../../aspose.words/range/structureddocumenttags/) { get; } | Gibt einen[`StructuredDocumentTags`](./structureddocumenttags/) Sammlung, die alle strukturierten Dokument-Tags im Bereich darstellt. |
| [Text](../../aspose.words/range/text/) { get; } | Ruft den Text des Bereichs ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Delete](../../aspose.words/range/delete/)() | Löscht alle Zeichen des Bereichs. |
| [GetEnumerator](../../aspose.words/range/getenumerator/)() |  |
| [NormalizeFieldTypes](../../aspose.words/range/normalizefieldtypes/)() | Ändert Feldtypwerte[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) von[`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) in diesem Bereich, sodass sie den in den Feldcodes enthaltenen Feldtypen entsprechen. |
| [Replace](../../aspose.words/range/replace/#replace_2)(*Regex, string*) | Ersetzt alle Vorkommen eines durch einen regulären Ausdruck angegebenen Zeichenmusters durch eine andere Zeichenfolge. |
| [Replace](../../aspose.words/range/replace/#replace)(*string, string*) | Ersetzt alle Vorkommen eines angegebenen Zeichenfolgenmusters durch eine Ersatzzeichenfolge. |
| [Replace](../../aspose.words/range/replace/#replace_3)(*Regex, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Ersetzt alle Vorkommen eines durch einen regulären Ausdruck angegebenen Zeichenmusters durch eine andere Zeichenfolge. |
| [Replace](../../aspose.words/range/replace/#replace_1)(*string, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Ersetzt alle Vorkommen eines angegebenen Zeichenfolgenmusters durch eine Ersatzzeichenfolge. |
| [ToDocument](../../aspose.words/range/todocument/)() | Erstellt ein neues, vollständig formatiertes Dokument, das den Bereich enthält. |
| [UnlinkFields](../../aspose.words/range/unlinkfields/)() | Hebt die Verknüpfung der Felder in diesem Bereich auf. |
| [UpdateFields](../../aspose.words/range/updatefields/)() | Aktualisiert die Werte der Dokumentfelder in diesem Bereich. |

## Bemerkungen

Das Dokument wird durch einen Knotenbaum dargestellt und die Knoten stellen Operationen bereit, um mit dem Baum zu arbeiten. Einige Operationen lassen sich jedoch leichter ausführen, wenn das Dokument als zusammenhängende Textsequenz behandelt wird.

`Range` ist eine „Fassaden“-Schnittstelle, die Methoden bereitstellt, die document oder Teile des Dokuments als „flachen“ Text behandeln, unabhängig von der Tatsache, dass die document -Knoten in einem baumartigen Objektmodell gespeichert sind.

`Range` enthält keinen Text oder Knoten, es ist lediglich eine Ansicht oder ein „Fenster“ über einem Dokumentfragment.

## Beispiele

Zeigt, wie der Textinhalt aller Knoten abgerufen wird, die ein Bereich abdeckt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### Siehe auch

* class [Node](../node/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
