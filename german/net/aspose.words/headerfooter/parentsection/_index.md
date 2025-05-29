---
title: HeaderFooter.ParentSection
linktitle: ParentSection
articleTitle: ParentSection
second_title: Aspose.Words für .NET
description: Entdecken Sie die HeaderFooter ParentSection-Eigenschaft, um einfach auf den übergeordneten Abschnitt Ihrer Story zuzugreifen und so die Struktur und Organisation Ihres Dokuments zu verbessern.
type: docs
weight: 60
url: /de/net/aspose.words/headerfooter/parentsection/
---
## HeaderFooter.ParentSection property

Ruft den übergeordneten Abschnitt dieser Story ab.

```csharp
public Section ParentSection { get; }
```

## Bemerkungen

`ParentSection` ist gleichbedeutend mit[`ParentNode`](../../node/parentnode/) gegossen zu[`Section`](../../section/).

## Beispiele

Zeigt, wie Kopf- und Fußzeilen zwischen Abschnitten verknüpft werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

// Wechseln Sie zum ersten Abschnitt und erstellen Sie eine Kopf- und eine Fußzeile. Standardmäßig
// Die Kopf- und Fußzeile werden auf den Seiten nur in dem Abschnitt angezeigt, der sie enthält.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// Wir können die Kopf-/Fußzeilen eines Abschnitts mit den Kopf-/Fußzeilen des vorherigen Abschnitts verknüpfen
// um dem Verknüpfungsabschnitt die Anzeige der Kopf-/Fußzeilen des verknüpften Abschnitts zu ermöglichen.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// Jeder Abschnitt verfügt weiterhin über eigene Kopf-/Fußzeilenobjekte. Wenn wir Abschnitte verknüpfen,
// Der Verknüpfungsbereich zeigt die Kopf-/Fußzeilen des verknüpften Bereichs an, behält aber seine eigenen bei.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// Verknüpfen Sie die Kopf-/Fußzeilen des dritten Abschnitts mit den Kopf-/Fußzeilen des zweiten Abschnitts.
// Der zweite Abschnitt ist bereits mit den Kopf-/Fußzeilen des ersten Abschnitts verknüpft.
// Durch die Verknüpfung mit dem zweiten Abschnitt wird also eine Linkkette erstellt.
// Der erste, zweite und jetzt auch der dritte Abschnitt zeigen alle die Überschriften des ersten Abschnitts an.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// Wir können die Verknüpfung der Kopf-/Fußzeilen eines vorherigen Abschnitts aufheben, indem wir beim Aufrufen der Methode LinkToPrevious „false“ übergeben.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// Mit dieser Methode können wir auch nur einen bestimmten Kopf-/Fußzeilentyp zum Verknüpfen auswählen.
// Der dritte Abschnitt hat jetzt dieselbe Fußzeile wie der zweite und erste Abschnitt, jedoch nicht die Kopfzeile.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// Die Kopf-/Fußzeilen des ersten Abschnitts können keine Verknüpfungen herstellen, da kein vorheriger Abschnitt vorhanden ist.
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

// Alle Kopf-/Fußzeilen des zweiten Abschnitts sind mit den Kopf-/Fußzeilen des ersten Abschnitts verknüpft.
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count);
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious));

// Im dritten Abschnitt wird nur der Footer über den zweiten Abschnitt mit dem Footer des ersten Abschnitts verknüpft.
Assert.AreEqual(6, doc.Sections[2].HeadersFooters.Count);
Assert.AreEqual(5, doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));
Assert.True(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### Siehe auch

* class [Section](../../section/)
* class [HeaderFooter](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
