---
title: Item
second_title: Aspose.Words für .NET-API-Referenz
description: Ruft a Kopfzeile Fußzeile am angegebenen Index.
type: docs
weight: 10
url: /de/net/aspose.words/headerfootercollection/item/
---
## HeaderFooterCollection indexer (1 of 2)

Ruft a **Kopfzeile Fußzeile** am angegebenen Index.

```csharp
public HeaderFooter this[int index] { get; }
```

| Parameter | Beschreibung |
| --- | --- |
| index | Ein Index in die Sammlung. |

### Bemerkungen

Der Index ist nullbasiert.

Negative Indizes sind zulässig und zeigen den Zugriff von der Rückseite der Sammlung an. Zum Beispiel bedeutet -1 das letzte Element, -2 bedeutet das vorletzte und so weiter.

Wenn der Index größer oder gleich der Anzahl der Elemente in der Liste ist, wird eine Nullreferenz zurückgegeben.

Wenn der Index negativ ist und sein absoluter Wert größer als die Anzahl der Elemente in der Liste ist, wird eine Nullreferenz zurückgegeben.

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

* class [HeaderFooter](../../headerfooter)
* class [HeaderFooterCollection](../../headerfootercollection)
* namensraum [Aspose.Words](../../headerfootercollection)
* Montage [Aspose.Words](../../../)

---

## HeaderFooterCollection indexer (2 of 2)

Ruft a **Kopfzeile Fußzeile** des angegebenen Typs.

```csharp
public HeaderFooter this[HeaderFooterType headerFooterType] { get; }
```

| Parameter | Beschreibung |
| --- | --- |
| headerFooterType | EIN[`HeaderFooterType`](../../headerfootertype) value , der den Typ der abzurufenden Kopf-/Fußzeile angibt. |

### Bemerkungen

Gibt null zurück, wenn die Kopf-/Fußzeile des angegebenen Typs nicht gefunden wird.

### Beispiele

Zeigt, wie Text in der Fußzeile eines Dokuments ersetzt wird.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

Zeigt, wie alle Fußzeilen aus einem Dokument gelöscht werden.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Jeden Abschnitt durchlaufen und Fußzeilen aller Art entfernen.
foreach (Section section in doc.OfType<Section>())
{
    // Es gibt drei Arten von Fußzeilen- und Kopfzeilentypen.
    // 1 - Die "erste" Kopf-/Fußzeile, die nur auf der ersten Seite eines Abschnitts erscheint.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - Die "primäre" Kopf-/Fußzeile, die auf ungeraden Seiten erscheint.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - Die "gerade" Kopf-/Fußzeile, die auf geraden Seiten erscheint.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

### Siehe auch

* class [HeaderFooter](../../headerfooter)
* enum [HeaderFooterType](../../headerfootertype)
* class [HeaderFooterCollection](../../headerfootercollection)
* namensraum [Aspose.Words](../../headerfootercollection)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
