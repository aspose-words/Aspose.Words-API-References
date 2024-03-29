---
title: StructuredDocumentTag.Placeholder
linktitle: Placeholder
articleTitle: Placeholder
second_title: Aspose.Words für .NET
description: StructuredDocumentTag Placeholder eigendom. Ruft die abBuildingBlockenthält Platzhaltertext der angezeigt werden soll wenn der Inhalt dieses SDTLaufs leer ist das zugehörige zugeordnete XMLElement ist leer wie über angegebenXmlMapping element oder dieIsShowingPlaceholderText Element istWAHR  in C#.
type: docs
weight: 230
url: /de/net/aspose.words.markup/structureddocumenttag/placeholder/
---
## StructuredDocumentTag.Placeholder property

Ruft die ab[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/)enthält Platzhaltertext, der angezeigt werden soll, wenn der Inhalt dieses SDT-Laufs leer ist, das zugehörige zugeordnete XML-Element ist leer, wie über angegeben[`XmlMapping`](../xmlmapping/) element oder die[`IsShowingPlaceholderText`](../isshowingplaceholdertext/) Element ist`WAHR` .

```csharp
public BuildingBlock Placeholder { get; }
```

## Bemerkungen

Kann sein`Null`, was bedeutet, dass der Platzhalter für diesen Sdt nicht anwendbar ist.

## Beispiele

Zeigt, wie der Inhalt eines Bausteins als benutzerdefinierter Platzhaltertext für ein strukturiertes Dokument-Tag verwendet wird.

```csharp
Document doc = new Document();

// Fügen Sie ein strukturiertes Nur-Text-Dokument-Tag vom Typ „PlainText“ ein, das als Textfeld fungiert.
// Der Inhalt, der standardmäßig angezeigt wird, ist „Klicken Sie hier, um Text einzugeben.“ prompt.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Wir können das Tag dazu bringen, den Inhalt eines Bausteins anstelle des Standardtextes anzuzeigen.
// Fügen Sie zunächst einen Baustein mit Inhalt zum Glossardokument hinzu.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;

BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "Custom Placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.AppendChild(new Body(glossaryDoc));
substituteBlock.FirstSection.Body.AppendParagraph("Custom placeholder text.");

glossaryDoc.AppendChild(substituteBlock);

// Verwenden Sie dann die Eigenschaft „PlaceholderName“ des strukturierten Dokument-Tags, um diesen Baustein namentlich zu referenzieren.
tag.PlaceholderName = "Custom Placeholder";

// Wenn „PlaceholderName“ auf einen vorhandenen Block im Glossardokument des übergeordneten Dokuments verweist,
// Wir können den Baustein über die Eigenschaft „Platzhalter“ überprüfen.
Assert.AreEqual(substituteBlock, tag.Placeholder);

// Setzen Sie die Eigenschaft „IsShowingPlaceholderText“ auf „true“, um das zu behandeln
// Strukturierter Dokument-Tag des aktuellen Inhalts als Platzhaltertext.
// Das bedeutet, dass durch Klicken auf das Textfeld in Microsoft Word sofort der gesamte Inhalt des Tags hervorgehoben wird.
// Setzen Sie die Eigenschaft „IsShowingPlaceholderText“ auf „false“, um die zu erhalten
// strukturiertes Dokument-Tag, um seinen Inhalt als Text zu behandeln, den ein Benutzer bereits eingegeben hat.
// Wenn Sie in Microsoft Word auf diesen Text klicken, wird der blinkende Cursor an der angeklickten Stelle platziert.
tag.IsShowingPlaceholderText = isShowingPlaceholderText;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

### Siehe auch

* class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* class [StructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
