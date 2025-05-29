---
title: StructuredDocumentTag.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words für .NET
description: Löschen Sie mühelos den Inhalt Ihres strukturierten Dokument-Tags mit der Clear-Methode und zeigen Sie einen definierten Platzhalter für eine verbesserte Dokumentenverwaltung an.
type: docs
weight: 360
url: /de/net/aspose.words.markup/structureddocumenttag/clear/
---
## StructuredDocumentTag.Clear method

Löscht den Inhalt dieses strukturierten Dokument-Tags und zeigt einen Platzhalter an, falls dieser definiert ist.

```csharp
public void Clear()
```

## Bemerkungen

Es ist nicht möglich, den Inhalt eines strukturierten Dokument-Tags zu löschen, wenn dieser Revisionen enthält.

Wenn dieses strukturierte Dokument-Tag auf benutzerdefiniertes XML abgebildet wird (mithilfe des[`XmlMapping`](../xmlmapping/) -Eigenschaft) wird der referenzierte XML-Knoten gelöscht.

## Beispiele

Zeigt, wie Inhalte strukturierter Dokument-Tag-Elemente gelöscht werden.

```csharp
Document doc = new Document();

// Erstellen Sie ein Dokument-Tag mit einfacher Textstruktur und hängen Sie es dann an das Dokument an.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// Dieses strukturierte Dokument-Tag in Form eines Textfelds zeigt bereits Platzhaltertext an.
Assert.AreEqual("Click here to enter text.", tag.GetText().Trim());
Assert.True(tag.IsShowingPlaceholderText);

// Erstellen Sie einen Baustein mit Textinhalt.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;
BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "My placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.EnsureMinimum();
substituteBlock.FirstSection.Body.FirstParagraph.AppendChild(new Run(glossaryDoc, "Custom placeholder text."));
glossaryDoc.AppendChild(substituteBlock);

// Setzen Sie die Eigenschaft "PlaceholderName" des strukturierten Dokument-Tags auf den Namen unseres Bausteins, um
// das strukturierte Dokument-Tag, um den Inhalt des Bausteins anstelle des ursprünglichen Standardtextes anzuzeigen.
tag.PlaceholderName = "My placeholder";

Assert.AreEqual("Custom placeholder text.", tag.GetText().Trim());
Assert.True(tag.IsShowingPlaceholderText);

// Bearbeiten Sie den Text des strukturierten Dokument-Tags und verbergen Sie den Platzhaltertext.
Run run = (Run)tag.GetChild(NodeType.Run, 0, true);
run.Text = "New text.";
tag.IsShowingPlaceholderText = false;

Assert.AreEqual("New text.", tag.GetText().Trim());

// Verwenden Sie die Methode „Clear“, um den Inhalt dieses strukturierten Dokument-Tags zu löschen und den Platzhalter erneut anzuzeigen.
tag.Clear();

Assert.True(tag.IsShowingPlaceholderText);
Assert.AreEqual("Custom placeholder text.", tag.GetText().Trim());
```

### Siehe auch

* class [StructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
