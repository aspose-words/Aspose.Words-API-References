---
title: Document.LastSection
second_title: Aspose.Words für .NET-API-Referenz
description: Document eigendom. Ruft den letzten Abschnitt im Dokument ab.
type: docs
weight: 220
url: /de/net/aspose.words/document/lastsection/
---
## Document.LastSection property

Ruft den letzten Abschnitt im Dokument ab.

```csharp
public Section LastSection { get; }
```

### Bemerkungen

gibt zurück`Null` wenn es keine Abschnitte gibt.

### Beispiele

Zeigt, wie Sie mit einem Document Builder einen neuen Abschnitt erstellen.

```csharp
Document doc = new Document();

// Ein leeres Dokument enthält standardmäßig einen Abschnitt,
// die untergeordnete Knoten enthält, die wir bearbeiten können.
Assert.AreEqual(1, doc.Sections.Count);

// Verwenden Sie einen Dokumentenersteller, um Text zum ersten Abschnitt hinzuzufügen.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Erstellen Sie einen zweiten Abschnitt, indem Sie einen Abschnittsumbruch einfügen.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(2, doc.Sections.Count);

// Jeder Abschnitt hat seine eigenen Seiteneinrichtungseinstellungen.
// Wir können den Text im zweiten Abschnitt in zwei Spalten aufteilen.
// Dies wirkt sich nicht auf den Text im ersten Abschnitt aus.
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
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)


