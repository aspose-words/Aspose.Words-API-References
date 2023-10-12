---
title: HeaderFooter.IsLinkedToPrevious
second_title: Aspose.Words für .NET-API-Referenz
description: HeaderFooter eigendom. True wenn diese Kopf oder Fußzeile mit der entsprechenden Kopf oder Fußzeile im vorherigen Abschnitt verknüpft ist.
type: docs
weight: 40
url: /de/net/aspose.words/headerfooter/islinkedtoprevious/
---
## HeaderFooter.IsLinkedToPrevious property

True, wenn diese Kopf- oder Fußzeile mit der entsprechenden Kopf- oder Fußzeile im vorherigen Abschnitt verknüpft ist.

```csharp
public bool IsLinkedToPrevious { get; set; }
```

### Bemerkungen

Standard ist`WAHR`.

Beachten Sie, dass der Inhalt gelöscht wird, wenn Sie eine Kopf- oder Fußzeile verlinken.

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

// Zum ersten Abschnitt wechseln und eine Kopf- und Fußzeile erstellen. Standardmäßig,
// Die Kopf- und Fußzeile werden nur auf Seiten in dem Abschnitt angezeigt, der sie enthält.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// Wir können die Kopf-/Fußzeilen eines Abschnitts mit den Kopf-/Fußzeilen des vorherigen Abschnitts verknüpfen
// damit der verlinkte Abschnitt die Kopf-/Fußzeilen des verlinkten Abschnitts anzeigen kann.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// Jeder Abschnitt wird weiterhin seine eigenen Kopf-/Fußzeilenobjekte haben. Wenn wir Abschnitte verlinken,
// Der verlinkende Abschnitt zeigt die Kopf-/Fußzeilen des verlinkten Abschnitts an, behält aber seine eigenen.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// Verknüpfen Sie die Kopf-/Fußzeilen des dritten Abschnitts mit den Kopf-/Fußzeilen des zweiten Abschnitts.
// Der zweite Abschnitt verlinkt bereits auf die Kopf-/Fußzeilen des ersten Abschnitts,
// Durch die Verknüpfung mit dem zweiten Abschnitt wird also eine Verknüpfungskette erstellt.
// Im ersten, zweiten und jetzt dritten Abschnitt werden alle die Kopfzeilen des ersten Abschnitts angezeigt.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// Wir können die Verknüpfung der Kopf-/Fußzeilen eines vorherigen Abschnitts aufheben, indem wir beim Aufruf der LinkToPrevious-Methode „false“ übergeben.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// Mit dieser Methode können wir auch nur einen bestimmten Kopf-/Fußzeilentyp zum Verknüpfen auswählen.
// Der dritte Abschnitt hat jetzt dieselbe Fußzeile wie der zweite und der erste Abschnitt, jedoch nicht die Kopfzeile.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// Die Kopf-/Fußzeilen des ersten Abschnitts können nicht mit irgendetwas verknüpft werden, da es keinen vorherigen Abschnitt gibt.
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

// Alle Kopf-/Fußzeilen des zweiten Abschnitts sind mit den Kopf-/Fußzeilen des ersten Abschnitts verknüpft.
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count);
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious));

// Im dritten Abschnitt wird nur die Fußzeile über den zweiten Abschnitt mit der Fußzeile des ersten Abschnitts verknüpft.
Assert.AreEqual(6, doc.Sections[2].HeadersFooters.Count);
Assert.AreEqual(5, doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));
Assert.True(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### Siehe auch

* class [HeaderFooter](../)
* namensraum [Aspose.Words](../../headerfooter/)
* Montage [Aspose.Words](../../../)


