---
title: IStructuredDocumentTag.IsShowingPlaceholderText
linktitle: IsShowingPlaceholderText
articleTitle: IsShowingPlaceholderText
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „IStructuredDocumentTag IsShowingPlaceholderText“, um Platzhaltertext in Ihrem SDT einfach zu identifizieren und so die Übersichtlichkeit und Verwaltung des Inhalts zu verbessern.
type: docs
weight: 50
url: /de/net/aspose.words.markup/istructureddocumenttag/isshowingplaceholdertext/
---
## IStructuredDocumentTag.IsShowingPlaceholderText property

Gibt an, ob der Inhalt dieser**SDT** muss so interpretiert werden, dass es Platzhaltertext enthält (im Gegensatz zu regulärem Textinhalt innerhalb des SDT).

Wenn auf „true“ gesetzt, wird dieser Status beim Öffnen dieses Dokuments wiederhergestellt (Platzhaltertext wird angezeigt).

```csharp
public bool IsShowingPlaceholderText { get; set; }
```

## Beispiele

Zeigt, wie der Inhalt eines Bausteins als benutzerdefinierter Platzhaltertext für ein strukturiertes Dokument-Tag verwendet wird.

```csharp
Document doc = new Document();

// Fügen Sie ein strukturiertes Dokument-Tag vom Typ „PlainText“ mit reinem Text ein, das als Textfeld fungiert.
// Der standardmäßig angezeigte Inhalt ist die Eingabeaufforderung „Klicken Sie hier, um Text einzugeben.“
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Wir können das Tag so einstellen, dass es den Inhalt eines Bausteins anstelle des Standardtextes anzeigt.
// Fügen Sie zunächst dem Glossardokument einen Baustein mit Inhalt hinzu.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;

BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "Custom Placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.AppendChild(new Body(glossaryDoc));
substituteBlock.FirstSection.Body.AppendParagraph("Custom placeholder text.");

glossaryDoc.AppendChild(substituteBlock);

// Verwenden Sie dann die Eigenschaft „PlaceholderName“ des strukturierten Dokument-Tags, um diesen Baustein nach Namen zu referenzieren.
tag.PlaceholderName = "Custom Placeholder";

// Wenn sich „PlaceholderName“ auf einen vorhandenen Block im Glossardokument des übergeordneten Dokuments bezieht,
// Wir können den Baustein über die Eigenschaft „Platzhalter“ überprüfen.
Assert.AreEqual(substituteBlock, tag.Placeholder);

// Setzen Sie die Eigenschaft "IsShowingPlaceholderText" auf "true", um die
// Aktueller Inhalt des strukturierten Dokument-Tags als Platzhaltertext.
// Das bedeutet, dass durch Klicken auf das Textfeld in Microsoft Word sofort der gesamte Inhalt des Tags hervorgehoben wird.
// Setzen Sie die Eigenschaft "IsShowingPlaceholderText" auf "false", um die
// strukturiertes Dokument-Tag, um seinen Inhalt als Text zu behandeln, den ein Benutzer bereits eingegeben hat.
// Wenn Sie in Microsoft Word auf diesen Text klicken, wird der blinkende Cursor an der angeklickten Stelle platziert.
tag.IsShowingPlaceholderText = isShowingPlaceholderText;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

### Siehe auch

* interface [IStructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
