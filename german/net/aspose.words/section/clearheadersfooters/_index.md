---
title: Section.ClearHeadersFooters
linktitle: ClearHeadersFooters
articleTitle: ClearHeadersFooters
second_title: Aspose.Words für .NET
description: Section ClearHeadersFooters methode. Löscht die Kopf und Fußzeilen dieses Abschnitts in C#.
type: docs
weight: 100
url: /de/net/aspose.words/section/clearheadersfooters/
---
## Section.ClearHeadersFooters method

Löscht die Kopf- und Fußzeilen dieses Abschnitts.

```csharp
public void ClearHeadersFooters()
```

## Bemerkungen

Der Text aller Kopf- und Fußzeilen wird gelöscht, aber[`HeaderFooter`](../../headerfooter/) Objekte selbst werden nicht entfernt.

Dadurch werden die Kopf- und Fußzeilen dieses Abschnitts mit den Kopf- und Fußzeilen des vorherigen Abschnitts verknüpft.

## Beispiele

Zeigt, wie der Inhalt aller Kopf- und Fußzeilen in einem Abschnitt gelöscht wird.

```csharp
Document doc = new Document();

Assert.AreEqual(0, doc.FirstSection.HeadersFooters.Count);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("This is the primary header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("This is the primary footer.");

Assert.AreEqual(2, doc.FirstSection.HeadersFooters.Count);

Assert.AreEqual("This is the primary header.", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("This is the primary footer.", doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());

// Alle Kopf- und Fußzeilen in diesem Abschnitt von ihrem gesamten Inhalt befreien.
// Die Kopf- und Fußzeilen selbst sind weiterhin vorhanden, können aber nicht angezeigt werden.
doc.FirstSection.ClearHeadersFooters();

Assert.AreEqual(2, doc.FirstSection.HeadersFooters.Count);

Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());
```

### Siehe auch

* class [Section](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
