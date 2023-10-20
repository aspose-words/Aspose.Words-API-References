---
title: IStructuredDocumentTag Interface
linktitle: IStructuredDocumentTag
articleTitle: IStructuredDocumentTag
second_title: Aspose.Words für .NET
description: Aspose.Words.Markup.IStructuredDocumentTag koppel. Schnittstelle zum Definieren gemeinsamer Daten fürStructuredDocumentTag UndStructuredDocumentTagRangeStart  in C#.
type: docs
weight: 3970
url: /de/net/aspose.words.markup/istructureddocumenttag/
---
## IStructuredDocumentTag interface

Schnittstelle zum Definieren gemeinsamer Daten für[`StructuredDocumentTag`](../structureddocumenttag/) Und[`StructuredDocumentTagRangeStart`](../structureddocumenttagrangestart/) .

```csharp
public interface IStructuredDocumentTag
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Color](../../aspose.words.markup/istructureddocumenttag/color/) { get; set; } | Ruft die Farbe des strukturierten Dokument-Tags ab oder legt diese fest. |
| [Id](../../aspose.words.markup/istructureddocumenttag/id/) { get; } | Gibt hierfür eine eindeutige, schreibgeschützte, persistente numerische ID an**SDT**. |
| [IsShowingPlaceholderText](../../aspose.words.markup/istructureddocumenttag/isshowingplaceholdertext/) { get; set; } | Gibt an, ob der Inhalt davon**SDT** soll so interpretiert werden, dass es den Platzhalter text enthält (im Gegensatz zu regulären Textinhalten innerhalb des SDT). |
| [Level](../../aspose.words.markup/istructureddocumenttag/level/) { get; } | Ruft die Ebene ab, auf der dies geschieht**SDT** kommt im Dokumentenbaum vor. |
| [LockContentControl](../../aspose.words.markup/istructureddocumenttag/lockcontentcontrol/) { get; set; } | Wenn diese Eigenschaft auf „true“ gesetzt ist, verhindert sie, dass ein Benutzer dies löscht**SDT** . |
| [LockContents](../../aspose.words.markup/istructureddocumenttag/lockcontents/) { get; set; } | Wenn diese Eigenschaft auf „true“ gesetzt ist, verhindert sie, dass ein Benutzer den Inhalt dieser Eigenschaft bearbeitet**SDT** . |
| [Placeholder](../../aspose.words.markup/istructureddocumenttag/placeholder/) { get; } | Ruft die ab[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)enthält Platzhaltertext, der angezeigt werden soll, wenn der Inhalt dieses SDT-Laufs leer ist, das zugehörige zugeordnete XML-Element ist leer, wie über angegeben[`XmlMapping`](./xmlmapping/) element oder die[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) Element ist wahr. |
| [PlaceholderName](../../aspose.words.markup/istructureddocumenttag/placeholdername/) { get; set; } | Ruft den Namen ab oder legt ihn fest[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) enthält Platzhaltertext. |
| [SdtType](../../aspose.words.markup/istructureddocumenttag/sdttype/) { get; } | Ruft den Typ davon ab**Strukturiertes Dokument-Tag** . |
| [Tag](../../aspose.words.markup/istructureddocumenttag/tag/) { get; set; } | Gibt ein Tag an, das dem aktuellen SDT-Knoten zugeordnet ist. Kann nicht null sein. |
| [Title](../../aspose.words.markup/istructureddocumenttag/title/) { get; set; } | Gibt den damit verbundenen Anzeigenamen an**SDT** . Kann nicht null sein. |
| [WordOpenXML](../../aspose.words.markup/istructureddocumenttag/wordopenxml/) { get; } | Ruft eine Zeichenfolge ab, die das im Knoten im enthaltene XML darstelltFlatOpc format. |
| [XmlMapping](../../aspose.words.markup/istructureddocumenttag/xmlmapping/) { get; } | Ruft ein Objekt ab, das die Zuordnung dieses strukturierten Dokument-Tags zu XML-Daten in einem benutzerdefinierten XML-Teil des aktuellen Dokuments darstellt. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [IsRanged](../../aspose.words.markup/istructureddocumenttag/isranged/)() | Gibt „true“ zurück, wenn es sich bei dieser Instanz um ein strukturiertes Dokument-Tag im Bereich handelt. |
| [StructuredDocumentTagNode](../../aspose.words.markup/istructureddocumenttag/structureddocumenttagnode/)() | Gibt ein Knotenobjekt zurück, das diese Schnittstelle implementiert. |

### Siehe auch

* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)
