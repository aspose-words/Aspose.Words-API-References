---
title: Section.HeadersFooters
linktitle: HeadersFooters
articleTitle: HeadersFooters
second_title: Aspose.Words per .NET
description: Accedi e gestisci intestazioni e piè di pagina di sezione senza sforzo con la nostra intuitiva funzione di gestione delle proprietà. Migliora l'organizzazione e la presentazione dei documenti oggi stesso!
type: docs
weight: 30
url: /it/net/aspose.words/section/headersfooters/
---
## Section.HeadersFooters property

Fornisce l'accesso ai nodi delle intestazioni e dei piè di pagina della sezione.

```csharp
public HeaderFooterCollection HeadersFooters { get; }
```

## Esempi

Mostra come sostituire il testo nel piè di pagina di un documento.

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

Mostra come eliminare tutti i piè di pagina da un documento.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Scorrere ogni sezione e rimuovere i piè di pagina di ogni tipo.
foreach (Section section in doc.OfType<Section>())
{
    // Esistono tre tipi di piè di pagina e di intestazione.
    // 1 - L'intestazione/piè di pagina "Prima", che appare solo sulla prima pagina di una sezione.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - L'intestazione/piè di pagina "Principale", che appare sulle pagine dispari.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - L'intestazione/piè di pagina "Pari", che appare nelle pagine pari.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

### Guarda anche

* class [HeaderFooterCollection](../../headerfootercollection/)
* class [Section](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
