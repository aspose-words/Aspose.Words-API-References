---
title: Document.LastSection
linktitle: LastSection
articleTitle: LastSection
second_title: Aspose.Words für .NET
description: Document LastSection eigendom. Ruft den letzten Abschnitt im Dokument ab in C#.
type: docs
weight: 240
url: /de/net/aspose.words/document/lastsection/
---
## Document.LastSection property

Ruft den letzten Abschnitt im Dokument ab.

```csharp
public Section LastSection { get; }
```

## Bemerkungen

Gibt zurück`Null` wenn keine Abschnitte vorhanden sind.

## Beispiele

Zeigt, wie man mit einem Document Builder einen neuen Abschnitt erstellt.

```csharp
Document doc = new Document();

// Ein leeres Dokument enthält standardmäßig einen Abschnitt,
// das untergeordnete Knoten enthält, die wir bearbeiten können.
Assert.AreEqual(1, doc.Sections.Count);

// Verwenden Sie einen Dokumentersteller, um Text zum ersten Abschnitt hinzuzufügen.
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
