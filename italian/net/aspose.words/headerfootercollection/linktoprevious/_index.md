---
title: HeaderFooterCollection.LinkToPrevious
linktitle: LinkToPrevious
articleTitle: LinkToPrevious
second_title: Aspose.Words per .NET
description: Scopri il metodo LinkToPrevious in HeaderFooterCollection per collegare o scollegare facilmente intestazioni e piè di pagina nelle sezioni del documento, per una formattazione fluida.
type: docs
weight: 20
url: /it/net/aspose.words/headerfootercollection/linktoprevious/
---
## LinkToPrevious(*bool*) {#linktoprevious_1}

Collega o scollega tutte le intestazioni e i piè di pagina alle intestazioni e ai piè di pagina corrispondenti nella sezione precedente.

```csharp
public void LinkToPrevious(bool isLinkToPrevious)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| isLinkToPrevious | Boolean | `VERO` per collegare le intestazioni e i piè di pagina alla sezione precedente; `falso` per scollegarli. |

## Osservazioni

Se una qualsiasi delle intestazioni o dei piè di pagina non esiste, viene creata automaticamente.

## Esempi

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
// per consentire alla sezione di collegamento di visualizzare le intestazioni/i piè di pagina della sezione collegata.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// Ogni sezione avrà comunque i propri oggetti intestazione/piè di pagina. Quando colleghiamo le sezioni,
// la sezione di collegamento visualizzerà l'intestazione/piè di pagina della sezione collegata mantenendo i propri.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// Collega le intestazioni/i piè di pagina della terza sezione alle intestazioni/i piè di pagina della seconda sezione.
// La seconda sezione è già collegata all'intestazione/piè di pagina della prima sezione,
// quindi il collegamento alla seconda sezione creerà una catena di collegamenti.
// La prima, la seconda e ora la terza sezione visualizzeranno tutte le intestazioni della prima sezione.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// Possiamo scollegare l'intestazione/piè di pagina di una sezione precedente passando "false" quando si chiama il metodo LinkToPrevious.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// Possiamo anche selezionare solo un tipo specifico di intestazione/piè di pagina da collegare utilizzando questo metodo.
// La terza sezione avrà ora lo stesso piè di pagina della seconda e della prima sezione, ma non l'intestazione.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// L'intestazione e i piè di pagina della prima sezione non possono collegarsi a nulla perché non esiste una sezione precedente.
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

// Tutte le intestazioni e i piè di pagina della seconda sezione sono collegati alle intestazioni e ai piè di pagina della prima sezione.
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count);
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious));

// Nella terza sezione, solo il piè di pagina è collegato al piè di pagina della prima sezione tramite la seconda sezione.
Assert.AreEqual(6, doc.Sections[2].HeadersFooters.Count);
Assert.AreEqual(5, doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));
Assert.True(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### Guarda anche

* class [HeaderFooterCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## LinkToPrevious(*[HeaderFooterType](../../headerfootertype/), bool*) {#linktoprevious}

Collega o scollega l'intestazione o il piè di pagina specificato all'intestazione o al piè di pagina corrispondente nella sezione precedente.

```csharp
public void LinkToPrevious(HeaderFooterType headerFooterType, bool isLinkToPrevious)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| headerFooterType | HeaderFooterType | UN[`HeaderFooterType`](../../headerfootertype/) value che specifica l'intestazione o il piè di pagina da collegare/scollegare. |
| isLinkToPrevious | Boolean | `VERO` per collegare l'intestazione o il piè di pagina alla sezione precedente; `falso` per scollegare. |

## Osservazioni

Se l'intestazione o il piè di pagina del tipo specificato non esiste, viene creato automaticamente.

## Esempi

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
// per consentire alla sezione di collegamento di visualizzare le intestazioni/i piè di pagina della sezione collegata.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// Ogni sezione avrà comunque i propri oggetti intestazione/piè di pagina. Quando colleghiamo le sezioni,
// la sezione di collegamento visualizzerà l'intestazione/piè di pagina della sezione collegata mantenendo i propri.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// Collega le intestazioni/i piè di pagina della terza sezione alle intestazioni/i piè di pagina della seconda sezione.
// La seconda sezione è già collegata all'intestazione/piè di pagina della prima sezione,
// quindi il collegamento alla seconda sezione creerà una catena di collegamenti.
// La prima, la seconda e ora la terza sezione visualizzeranno tutte le intestazioni della prima sezione.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// Possiamo scollegare l'intestazione/piè di pagina di una sezione precedente passando "false" quando si chiama il metodo LinkToPrevious.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// Possiamo anche selezionare solo un tipo specifico di intestazione/piè di pagina da collegare utilizzando questo metodo.
// La terza sezione avrà ora lo stesso piè di pagina della seconda e della prima sezione, ma non l'intestazione.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// L'intestazione e i piè di pagina della prima sezione non possono collegarsi a nulla perché non esiste una sezione precedente.
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

// Tutte le intestazioni e i piè di pagina della seconda sezione sono collegati alle intestazioni e ai piè di pagina della prima sezione.
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count);
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious));

// Nella terza sezione, solo il piè di pagina è collegato al piè di pagina della prima sezione tramite la seconda sezione.
Assert.AreEqual(6, doc.Sections[2].HeadersFooters.Count);
Assert.AreEqual(5, doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));
Assert.True(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### Guarda anche

* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooterCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
