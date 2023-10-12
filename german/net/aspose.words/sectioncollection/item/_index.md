---
title: SectionCollection.Item
second_title: Aspose.Words für .NET-API-Referenz
description: SectionCollection eigendom. Ruft einen Abschnitt am angegebenen Index ab.
type: docs
weight: 10
url: /de/net/aspose.words/sectioncollection/item/
---
## SectionCollection indexer

Ruft einen Abschnitt am angegebenen Index ab.

```csharp
public Section this[int index] { get; }
```

| Parameter | Beschreibung |
| --- | --- |
| index | Ein Index in der Liste der Abschnitte. |

### Bemerkungen

Der Index ist nullbasiert.

Negative Indizes sind zulässig und zeigen den Zugriff von der Rückseite der Sammlung an. Beispielsweise bedeutet -1 das letzte Element, -2 das vorletzte und so weiter.

Wenn der Index größer oder gleich der Anzahl der Elemente in der Liste ist, wird ein Nullverweis zurückgegeben.

Wenn der Index negativ ist und sein absoluter Wert größer als die Anzahl der Elemente in der Liste ist, wird ein Nullverweis zurückgegeben.

### Beispiele

Zeigt an, wann das Seitenlayout des Dokuments neu berechnet werden soll.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Das Speichern eines Dokuments als PDF, ein Bild oder das erstmalige Drucken erfolgt automatisch
// Das Layout des Dokuments innerhalb seiner Seiten zwischenspeichern.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Das Dokument auf irgendeine Weise ändern.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

 // In der aktuellen Version von Aspose.Words wird das Dokument beim Ändern nicht automatisch neu erstellt
// das zwischengespeicherte Seitenlayout. Wenn wir das zwischengespeicherte Layout wünschen
// Um auf dem neuesten Stand zu bleiben, müssen wir es manuell aktualisieren.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

Zeigt, wie ein neuer Abschnittsknoten für die Bearbeitung vorbereitet wird.

```csharp
Document doc = new Document();

// Ein leeres Dokument besteht aus einem Abschnitt, der einen Hauptteil hat, der wiederum einen Absatz enthält.
// Wir können diesem Dokument Inhalte hinzufügen, indem wir diesem Absatz Elemente wie Textläufe, Formen oder Tabellen hinzufügen.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// Wenn wir einen neuen Abschnitt wie diesen hinzufügen, hat er weder einen Hauptteil noch andere untergeordnete Knoten.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Führen Sie die Methode „EnsureMinimum“ aus, um diesem Abschnitt einen Hauptteil und einen Absatz hinzuzufügen und mit der Bearbeitung zu beginnen.
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Siehe auch

* class [Section](../../section/)
* class [SectionCollection](../)
* namensraum [Aspose.Words](../../sectioncollection/)
* Montage [Aspose.Words](../../../)


