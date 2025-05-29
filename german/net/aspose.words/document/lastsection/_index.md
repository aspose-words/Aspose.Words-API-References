---
title: Document.LastSection
linktitle: LastSection
articleTitle: LastSection
second_title: Aspose.Words für .NET
description: Entdecken Sie die LastSection-Eigenschaft, um einfach auf den letzten Abschnitt Ihres Dokuments zuzugreifen und so die Navigation und die Effizienz der Inhaltsverwaltung zu verbessern.
type: docs
weight: 250
url: /de/net/aspose.words/document/lastsection/
---
## Document.LastSection property

Ruft den letzten Abschnitt im Dokument ab.

```csharp
public Section LastSection { get; }
```

## Bemerkungen

Rückgaben`null`wenn keine Abschnitte vorhanden sind.

## Beispiele

Zeigt, wie mit einem Dokumentgenerator ein neuer Abschnitt erstellt wird.

```csharp
Document doc = new Document();

// Ein leeres Dokument enthält standardmäßig einen Abschnitt,
// die untergeordnete Knoten enthalten, die wir bearbeiten können.
Assert.AreEqual(1, doc.Sections.Count);

// Verwenden Sie einen Dokumentgenerator, um dem ersten Abschnitt Text hinzuzufügen.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Erstellen Sie einen zweiten Abschnitt, indem Sie einen Abschnittsumbruch einfügen.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(2, doc.Sections.Count);

// Jeder Abschnitt hat seine eigenen Seiteneinrichtungseinstellungen.
// Wir können den Text im zweiten Abschnitt in zwei Spalten aufteilen.
// Dies hat keine Auswirkungen auf den Text im ersten Abschnitt.
doc.LastSection.PageSetup.TextColumns.SetCount(2);
builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

Assert.AreEqual(1, doc.FirstSection.PageSetup.TextColumns.Count);
Assert.AreEqual(2, doc.LastSection.PageSetup.TextColumns.Count);

doc.Save(ArtifactsDir + "Section.Create.docx");
```

### Siehe auch

* class [Section](../../section/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
