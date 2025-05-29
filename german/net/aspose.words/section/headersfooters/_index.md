---
title: Section.HeadersFooters
linktitle: HeadersFooters
articleTitle: HeadersFooters
second_title: Aspose.Words für .NET
description: Greifen Sie mühelos auf Abschnittskopf- und -fußzeilen zu und verwalten Sie diese mit unserer intuitiven Eigenschaftenfunktion. Verbessern Sie noch heute die Organisation und Präsentation Ihrer Dokumente!
type: docs
weight: 30
url: /de/net/aspose.words/section/headersfooters/
---
## Section.HeadersFooters property

Bietet Zugriff auf die Kopf- und Fußzeilenknoten des Abschnitts.

```csharp
public HeaderFooterCollection HeadersFooters { get; }
```

## Beispiele

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

// Durchlaufen Sie jeden Abschnitt und entfernen Sie Fußzeilen aller Art.
foreach (Section section in doc.OfType<Section>())
{
    // Es gibt drei Arten von Fußzeilen- und Kopfzeilentypen.
    // 1 – Die „Erste“ Kopf-/Fußzeile, die nur auf der ersten Seite eines Abschnitts angezeigt wird.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 – Die „primäre“ Kopf-/Fußzeile, die auf ungeraden Seiten erscheint.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

        // 3 – Die Kopf-/Fußzeile „Gerade“, die auf geraden Seiten erscheint.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

### Siehe auch

* class [HeaderFooterCollection](../../headerfootercollection/)
* class [Section](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
