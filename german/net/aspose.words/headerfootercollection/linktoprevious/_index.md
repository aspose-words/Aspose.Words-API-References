---
title: HeaderFooterCollection.LinkToPrevious
linktitle: LinkToPrevious
articleTitle: LinkToPrevious
second_title: Aspose.Words für .NET
description: Entdecken Sie die Methode LinkToPrevious in HeaderFooterCollection, um Kopf- und Fußzeilen in Ihren Dokumentabschnitten einfach zu verbinden oder zu trennen und so eine nahtlose Formatierung zu erreichen.
type: docs
weight: 20
url: /de/net/aspose.words/headerfootercollection/linktoprevious/
---
## LinkToPrevious(*bool*) {#linktoprevious_1}

Verknüpft oder trennt alle Kopf- und Fußzeilen mit den entsprechenden Kopf- und Fußzeilen im vorherigen Abschnitt.

```csharp
public void LinkToPrevious(bool isLinkToPrevious)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| isLinkToPrevious | Boolean | `WAHR` um die Kopf- und Fußzeilen mit dem vorherigen Abschnitt zu verknüpfen; `FALSCH` um die Verknüpfung aufzuheben. |

## Bemerkungen

Wenn Kopf- oder Fußzeilen nicht vorhanden sind, werden sie automatisch erstellt.

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

* class [HeaderFooterCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## LinkToPrevious(*[HeaderFooterType](../../headerfootertype/), bool*) {#linktoprevious}

Verknüpft die angegebene Kopf- oder Fußzeile mit der entsprechenden Kopf- oder Fußzeile im vorherigen Abschnitt oder hebt die Verknüpfung auf.

```csharp
public void LinkToPrevious(HeaderFooterType headerFooterType, bool isLinkToPrevious)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| headerFooterType | HeaderFooterType | A[`HeaderFooterType`](../../headerfootertype/) value , der die Kopf- oder Fußzeile angibt, die verknüpft bzw. deren Verknüpfung aufgehoben werden soll. |
| isLinkToPrevious | Boolean | `WAHR` um die Kopf- oder Fußzeile mit dem vorherigen Abschnitt zu verknüpfen; `FALSCH` um die Verknüpfung aufzuheben. |

## Bemerkungen

Wenn die Kopf- oder Fußzeile des angegebenen Typs nicht vorhanden ist, wird sie automatisch erstellt.

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

* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooterCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
