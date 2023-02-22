---
title: HeaderFooter.ParentSection
second_title: Aspose.Words für .NET-API-Referenz
description: HeaderFooter eigendom. Ruft den übergeordneten Abschnitt dieser Story ab.
type: docs
weight: 60
url: /de/net/aspose.words/headerfooter/parentsection/
---
## HeaderFooter.ParentSection property

Ruft den übergeordneten Abschnitt dieser Story ab.

```csharp
public Section ParentSection { get; }
```

### Bemerkungen

**ParentSection** ist äquivalent zu`(Abschnitt)ParentNode`.

### Beispiele

Zeigt, wie Kopf- und Fußzeilen zwischen Abschnitten verknüpft werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

// Gehe zum ersten Abschnitt und erstelle eine Kopf- und eine Fußzeile. Standardmäßig,
// Die Kopf- und Fußzeile erscheinen nur auf Seiten in dem Abschnitt, der sie enthält.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// Wir können die Kopf-/Fußzeilen eines Abschnitts mit den Kopf-/Fußzeilen des vorherigen Abschnitts verknüpfen
// damit der verlinkende Abschnitt die Kopf-/Fußzeilen des verlinkten Abschnitts anzeigen kann.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// Jeder Abschnitt hat weiterhin seine eigenen Kopf-/Fußzeilenobjekte. Wenn wir Abschnitte verknüpfen,
// Der verlinkende Abschnitt zeigt die Kopf-/Fußzeilen des verlinkten Abschnitts an, während er seine eigenen behält.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// Verknüpfen Sie die Kopf-/Fußzeilen des dritten Abschnitts mit den Kopf-/Fußzeilen des zweiten Abschnitts.
// Der zweite Abschnitt ist bereits mit der Kopf-/Fußzeile des ersten Abschnitts verknüpft,
// die Verknüpfung mit dem zweiten Abschnitt erzeugt also eine Verknüpfungskette.
// Der erste, der zweite und jetzt der dritte Abschnitt zeigen alle die Kopfzeilen des ersten Abschnitts an.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// Wir können die Verknüpfung der Kopf-/Fußzeilen eines vorherigen Abschnitts aufheben, indem wir beim Aufrufen der LinkToPrevious-Methode "false" übergeben.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// Mit dieser Methode können wir auch nur einen bestimmten Typ von Kopf-/Fußzeile zum Verlinken auswählen.
// Der dritte Abschnitt hat jetzt dieselbe Fußzeile wie der zweite und der erste Abschnitt, aber nicht die Kopfzeile.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// Die Kopf-/Fußzeilen des ersten Abschnitts können sich nicht mit irgendetwas verknüpfen, da es keinen vorherigen Abschnitt gibt.
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

// Alle Kopf-/Fußzeilen des zweiten Abschnitts sind mit den Kopf-/Fußzeilen des ersten Abschnitts verknüpft.
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count);
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious));

// In der dritten Sektion ist nur die Fußzeile über die zweite Sektion mit der Fußzeile der ersten Sektion verbunden.
Assert.AreEqual(6, doc.Sections[2].HeadersFooters.Count);
Assert.AreEqual(5, doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));
Assert.True(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### Siehe auch

* class [Section](../../section/)
* class [HeaderFooter](../)
* namensraum [Aspose.Words](../../headerfooter/)
* Montage [Aspose.Words](../../../)


