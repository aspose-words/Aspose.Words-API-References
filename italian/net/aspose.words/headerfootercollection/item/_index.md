---
title: HeaderFooterCollection.Item
second_title: Aspose.Words per .NET API Reference
description: HeaderFooterCollection proprietà. Recupera aHeaderFooter allindice indicato.
type: docs
weight: 10
url: /it/net/aspose.words/headerfootercollection/item/
---
## HeaderFooterCollection indexer (1 of 2)

Recupera a[`HeaderFooter`](../../headerfooter/) all'indice indicato.

```csharp
public HeaderFooter this[int index] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| index | Un indice nella raccolta. |

### Osservazioni

L'indice è a base zero.

Gli indici negativi sono consentiti e indicano l'accesso dal retro della raccolta. Ad esempio -1 significa l'ultimo elemento, -2 significa il penultimo e così via.

Se indice è maggiore o uguale al numero di elementi nell'elenco, restituisce un riferimento null.

Se indice è negativo e il suo valore assoluto è maggiore del numero di elementi nell'elenco, restituisce un riferimento null.

### Esempi

Mostra come collegare intestazioni e piè di pagina tra le sezioni.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

// Passa alla prima sezione e crea un'intestazione e un piè di pagina. Per impostazione predefinita,
// l'intestazione e il piè di pagina appariranno solo nelle pagine della sezione che li contiene.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// Possiamo collegare le intestazioni/piè di pagina di una sezione alle intestazioni/piè di pagina della sezione precedente
// per consentire alla sezione di collegamento di visualizzare le intestazioni/piè di pagina della sezione collegata.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// Ogni sezione avrà comunque i propri oggetti intestazione/piè di pagina. Quando colleghiamo le sezioni,
// la sezione di collegamento mostrerà l'intestazione/i piè di pagina della sezione collegata mantenendo i propri.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// Collega le intestazioni/piè di pagina della terza sezione alle intestazioni/piè di pagina della seconda sezione.
// La seconda sezione è già collegata all'intestazione/piè di pagina della prima sezione,
// quindi il collegamento alla seconda sezione creerà una catena di collegamenti.
// La prima, la seconda e ora la terza sezione mostreranno tutte le intestazioni della prima sezione.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// Possiamo scollegare l'intestazione/piè di pagina di una sezione precedente passando "false" quando chiamiamo il metodo LinkToPrevious.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// Possiamo anche selezionare solo un tipo specifico di intestazione/piè di pagina da collegare utilizzando questo metodo.
// La terza sezione ora avrà lo stesso piè di pagina della seconda e della prima sezione, ma non l'intestazione.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// L'intestazione/piè di pagina della prima sezione non possono collegarsi a nulla perché non esiste una sezione precedente.
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

// Tutte le intestazioni/piè di pagina della seconda sezione sono collegati alle intestazioni/piè di pagina della prima sezione.
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count);
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious));

// Nella terza sezione, solo il piè di pagina è collegato al piè di pagina della prima sezione tramite la seconda sezione.
Assert.AreEqual(6, doc.Sections[2].HeadersFooters.Count);
Assert.AreEqual(5, doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));
Assert.True(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### Guarda anche

* class [HeaderFooter](../../headerfooter/)
* class [HeaderFooterCollection](../)
* spazio dei nomi [Aspose.Words](../../headerfootercollection/)
* assemblea [Aspose.Words](../../../)

---

## HeaderFooterCollection indexer (2 of 2)

Recupera a[`HeaderFooter`](../../headerfooter/) del tipo specificato.

```csharp
public HeaderFooter this[HeaderFooterType headerFooterType] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| headerFooterType | UN[`HeaderFooterType`](../../headerfootertype/) value che specifica il tipo di intestazione/piè di pagina da recuperare. |

### Osservazioni

Restituisce`nullo` se l'intestazione/piè di pagina del tipo specificato non viene trovata.

### Esempi

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

// Scorri ogni sezione e rimuovi piè di pagina di ogni tipo.
foreach (Section section in doc.OfType<Section>())
{
    // Esistono tre tipi di piè di pagina e di intestazione.
    // 1 - L'intestazione/piè di pagina "Prima", che appare solo sulla prima pagina di una sezione.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - L'intestazione/piè di pagina "Primario", che appare sulle pagine dispari.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - L'intestazione/piè di pagina "Pari", che appare sulle pagine pari.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

### Guarda anche

* class [HeaderFooter](../../headerfooter/)
* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooterCollection](../)
* spazio dei nomi [Aspose.Words](../../headerfootercollection/)
* assemblea [Aspose.Words](../../../)


