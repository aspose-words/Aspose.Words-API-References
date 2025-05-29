---
title: Section.Body
linktitle: Body
articleTitle: Body
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Abschnittstext“, die den untergeordneten Knoten „Text“ abruft und Ihre Webentwicklung durch optimiertes Inhaltsmanagement verbessert.
type: docs
weight: 20
url: /de/net/aspose.words/section/body/
---
## Section.Body property

Gibt die[`Body`](../../body/) untergeordneter Knoten des Abschnitts.

```csharp
public Body Body { get; }
```

## Bemerkungen

[`Body`](../../body/) enthält den Haupttext des Abschnitts.

Rückgaben`null` wenn der Abschnitt keine[`Body`](../../body/) Knoten unter seinen Kindern.

## Beispiele

Löscht den Haupttext aus allen Abschnitten des Dokuments, wobei die Abschnitte selbst erhalten bleiben.

```csharp
Document doc = new Document();

// Ein leeres Dokument enthält einen Abschnitt, einen Hauptteil und einen Absatz.
// Rufen Sie die Methode „RemoveAllChildren“ auf, um alle diese Knoten zu entfernen.
// und am Ende einen Dokumentknoten ohne untergeordnete Elemente erhalten.
doc.RemoveAllChildren();

// Dieses Dokument hat jetzt keine zusammengesetzten untergeordneten Knoten, denen wir Inhalte hinzufügen können.
// Wenn wir es bearbeiten möchten, müssen wir seine Knotensammlung neu füllen.
// Erstellen Sie zuerst einen neuen Abschnitt und hängen Sie ihn dann als untergeordnetes Element an den Stammdokumentknoten an.
Section section = new Section(doc);
doc.AppendChild(section);

// Ein Abschnitt benötigt einen Hauptteil, der seinen gesamten Inhalt enthält und anzeigt
// auf der Seite zwischen Kopf- und Fußzeile des Abschnitts.
Body body = new Body(doc);
section.AppendChild(body);

// Dieser Body hat keine untergeordneten Elemente, daher können wir ihm noch keine Läufe hinzufügen.
Assert.AreEqual(0, doc.FirstSection.Body.GetChildNodes(NodeType.Any, true).Count);

    // Rufen Sie „EnsureMinimum“ auf, um sicherzustellen, dass dieser Textkörper mindestens einen leeren Absatz enthält.
body.EnsureMinimum();

// Jetzt können wir dem Textkörper Läufe hinzufügen und das Dokument dazu bringen, sie anzuzeigen.
body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Siehe auch

* class [Body](../../body/)
* class [Section](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
