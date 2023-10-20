---
title: Document.Sections
linktitle: Sections
articleTitle: Sections
second_title: Aspose.Words für .NET
description: Document Sections eigendom. Gibt eine Sammlung zurück die alle Abschnitte im Dokument darstellt in C#.
type: docs
weight: 370
url: /de/net/aspose.words/document/sections/
---
## Document.Sections property

Gibt eine Sammlung zurück, die alle Abschnitte im Dokument darstellt.

```csharp
public SectionCollection Sections { get; }
```

## Beispiele

Zeigt, wie Abschnitte in einem Dokument hinzugefügt und entfernt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// Den ersten Abschnitt aus dem Dokument löschen.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// Eine Kopie des nun ersten Abschnitts an das Ende des Dokuments anhängen.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

Zeigt, wie Sie angeben, wie sich ein neuer Abschnitt vom vorherigen trennt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("This text is in section 1.");

// Abschnittswechseltypen bestimmen, wie sich ein neuer Abschnitt vom vorherigen Abschnitt trennt.
// Nachfolgend finden Sie fünf Arten von Abschnittsumbrüchen.
// 1 – Beginnt den nächsten Abschnitt auf einer neuen Seite:
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("This text is in section 2.");

Assert.AreEqual(SectionStart.NewPage, doc.Sections[1].PageSetup.SectionStart);

// 2 – Startet den nächsten Abschnitt auf der aktuellen Seite:
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("This text is in section 3.");

Assert.AreEqual(SectionStart.Continuous, doc.Sections[2].PageSetup.SectionStart);

// 3 – Beginnt den nächsten Abschnitt auf einer neuen geraden Seite:
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Writeln("This text is in section 4.");

Assert.AreEqual(SectionStart.EvenPage, doc.Sections[3].PageSetup.SectionStart);

// 4 – Beginnt den nächsten Abschnitt auf einer neuen ungeraden Seite:
builder.InsertBreak(BreakType.SectionBreakOddPage);
builder.Writeln("This text is in section 5.");

Assert.AreEqual(SectionStart.OddPage, doc.Sections[4].PageSetup.SectionStart);

// 5 – Beginnt den nächsten Abschnitt in einer neuen Spalte:
TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.SetCount(2);

builder.InsertBreak(BreakType.SectionBreakNewColumn);
builder.Writeln("This text is in section 6.");

Assert.AreEqual(SectionStart.NewColumn, doc.Sections[5].PageSetup.SectionStart);

doc.Save(ArtifactsDir + "PageSetup.SetSectionStart.docx");
```

### Siehe auch

* class [SectionCollection](../../sectioncollection/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
