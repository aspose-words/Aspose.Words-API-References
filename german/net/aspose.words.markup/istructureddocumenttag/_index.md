---
title: IStructuredDocumentTag Interface
linktitle: IStructuredDocumentTag
articleTitle: IStructuredDocumentTag
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.Markup.IStructuredDocumentTag-Schnittstelle für die effiziente Verwaltung strukturierter Dokument-Tags und verbessern Sie noch heute Ihre Dokumentverarbeitung!
type: docs
weight: 4660
url: /de/net/aspose.words.markup/istructureddocumenttag/
---
## IStructuredDocumentTag interface

Schnittstelle zur Definition gemeinsamer Daten für[`StructuredDocumentTag`](../structureddocumenttag/) Und[`StructuredDocumentTagRangeStart`](../structureddocumenttagrangestart/) .

```csharp
public interface IStructuredDocumentTag
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Appearance](../../aspose.words.markup/istructureddocumenttag/appearance/) { get; set; } | Ruft das Erscheinungsbild des strukturierten Dokumenttags ab oder legt es fest. |
| [Color](../../aspose.words.markup/istructureddocumenttag/color/) { get; set; } | Ruft die Farbe des strukturierten Dokument-Tags ab oder legt sie fest. |
| [Id](../../aspose.words.markup/istructureddocumenttag/id/) { get; } | Gibt eine eindeutige, schreibgeschützte, persistente numerische ID für dieses**SDT**. |
| [IsMultiSection](../../aspose.words.markup/istructureddocumenttag/ismultisection/) { get; } | Gibt „true“ zurück, wenn diese Instanz ein strukturierter Dokumenttag mit mehreren Abschnitten ist. |
| [IsShowingPlaceholderText](../../aspose.words.markup/istructureddocumenttag/isshowingplaceholdertext/) { get; set; } | Gibt an, ob der Inhalt dieser**SDT** muss so interpretiert werden, dass es Platzhaltertext enthält (im Gegensatz zu regulärem Textinhalt innerhalb des SDT). |
| [Level](../../aspose.words.markup/istructureddocumenttag/level/) { get; } | Ruft die Ebene ab, auf der dieses**SDT** tritt im Dokumentbaum auf. |
| [LockContentControl](../../aspose.words.markup/istructureddocumenttag/lockcontentcontrol/) { get; set; } | Wenn diese Eigenschaft auf „true“ gesetzt ist, verhindert sie, dass ein Benutzer diese**SDT** . |
| [LockContents](../../aspose.words.markup/istructureddocumenttag/lockcontents/) { get; set; } | Wenn diese Eigenschaft auf „true“ gesetzt ist, wird ein Benutzer daran gehindert, den Inhalt dieser**SDT** . |
| [Node](../../aspose.words.markup/istructureddocumenttag/node/) { get; } | Gibt das Node-Objekt zurück, das diese Schnittstelle implementiert. |
| [Placeholder](../../aspose.words.markup/istructureddocumenttag/placeholder/) { get; } | Ruft die[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) Enthält Platzhaltertext, der angezeigt werden soll, wenn der Inhalt dieses SDT-Laufs leer ist, das zugehörige zugeordnete XML-Element ist leer, wie über die[`XmlMapping`](./xmlmapping/) element oder das[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) Element ist wahr. |
| [PlaceholderName](../../aspose.words.markup/istructureddocumenttag/placeholdername/) { get; set; } | Ruft den Namen des[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) mit Platzhaltertext. |
| [SdtType](../../aspose.words.markup/istructureddocumenttag/sdttype/) { get; } | Ruft den Typ dieses**Strukturiertes Dokument-Tag** . |
| [Tag](../../aspose.words.markup/istructureddocumenttag/tag/) { get; set; } | Gibt ein Tag an, das mit dem aktuellen SDT-Knoten verknüpft ist. Darf nicht null sein. |
| [Title](../../aspose.words.markup/istructureddocumenttag/title/) { get; set; } | Gibt den Anzeigenamen an, der mit diesem**SDT** . Darf nicht null sein. |
| [WordOpenXML](../../aspose.words.markup/istructureddocumenttag/wordopenxml/) { get; } | Ruft eine Zeichenfolge ab, die das XML darstellt, das im Knoten imFlatOpc format. |
| [XmlMapping](../../aspose.words.markup/istructureddocumenttag/xmlmapping/) { get; } | Ruft ein Objekt ab, das die Zuordnung dieses strukturierten Dokumenttags zu XML-Daten in einem benutzerdefinierten XML-Teil des aktuellen Dokuments darstellt. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetChildNodes](../../aspose.words.markup/istructureddocumenttag/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die den angegebenen Typen entsprechen. |
| [RemoveSelfOnly](../../aspose.words.markup/istructureddocumenttag/removeselfonly/)() | Entfernt nur diesen SDT-Knoten selbst, behält aber seinen Inhalt im Dokumentbaum. |

## Beispiele

Zeigt, wie strukturierte Dokument-Tags entfernt werden, der Inhalt jedoch erhalten bleibt.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

    // Diese Sammlung bietet eine einheitliche Schnittstelle für den Zugriff auf strukturierte Tags mit und ohne Bereich.
IEnumerable<IStructuredDocumentTag> sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(5, sdts.Count());

// Hier können wir untergeordnete Knoten aus der gemeinsamen Schnittstelle strukturierter Tags mit und ohne Bereich abrufen.
foreach (IStructuredDocumentTag sdt in sdts)
    if (sdt.GetChildNodes(NodeType.Any, false).Count > 0)
        sdt.RemoveSelfOnly();

sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(0, sdts.Count());
```

### Siehe auch

* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)
