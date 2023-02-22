---
title: StructuredDocumentTag.Clear
second_title: Aspose.Words für .NET-API-Referenz
description: StructuredDocumentTag methode. Löscht den Inhalt dieses strukturierten DokumentTags und zeigt einen Platzhalter an falls definiert.
type: docs
weight: 330
url: /de/net/aspose.words.markup/structureddocumenttag/clear/
---
## StructuredDocumentTag.Clear method

Löscht den Inhalt dieses strukturierten Dokument-Tags und zeigt einen Platzhalter an, falls definiert.

```csharp
public void Clear()
```

### Bemerkungen

Es ist nicht möglich, den Inhalt eines strukturierten Dokument-Tags zu löschen, wenn es Revisionen hat.

Wenn dieses strukturierte Dokument-Tag benutzerdefiniertem XML zugeordnet wird (unter Verwendung von[`XmlMapping`](../xmlmapping/) -Eigenschaft), wird der referenzierte XML-Knoten gelöscht.

### Beispiele

Zeigt, wie der Inhalt strukturierter Dokument-Tag-Elemente gelöscht wird.

```csharp
Document doc = new Document();

// Erstellen Sie ein strukturiertes Klartext-Dokument-Tag und hängen Sie es dann an das Dokument an.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// Dieses strukturierte Dokument-Tag in Form eines Textfeldes zeigt bereits Platzhaltertext an.
Assert.AreEqual("Click here to enter text.", tag.GetText().Trim());
Assert.True(tag.IsShowingPlaceholderText);

// Erstellen Sie einen Baustein mit Textinhalten.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;
BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "My placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.EnsureMinimum();
substituteBlock.FirstSection.Body.FirstParagraph.AppendChild(new Run(glossaryDoc, "Custom placeholder text."));
glossaryDoc.AppendChild(substituteBlock);

// Legen Sie die "PlaceholderName"-Eigenschaft des strukturierten Dokument-Tags auf den Namen unseres Bausteins fest, um zu erhalten
// das strukturierte Dokument-Tag, um den Inhalt des Bausteins anstelle des ursprünglichen Standardtexts anzuzeigen.
tag.PlaceholderName = "My placeholder";

Assert.AreEqual("Custom placeholder text.", tag.GetText().Trim());
Assert.True(tag.IsShowingPlaceholderText);

// Bearbeiten Sie den Text des strukturierten Dokument-Tags und blenden Sie den Platzhaltertext aus.
Run run = (Run)tag.GetChild(NodeType.Run, 0, true);
run.Text = "New text.";
tag.IsShowingPlaceholderText = false;

Assert.AreEqual("New text.", tag.GetText().Trim());

// Verwenden Sie die Methode "Clear", um den Inhalt dieses strukturierten Dokument-Tags zu löschen und den Platzhalter erneut anzuzeigen.
tag.Clear();

Assert.True(tag.IsShowingPlaceholderText);
Assert.AreEqual("Custom placeholder text.", tag.GetText().Trim());
```

### Siehe auch

* class [StructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../structureddocumenttag/)
* Montage [Aspose.Words](../../../)


