---
title: HeaderFooterCollection Class
linktitle: HeaderFooterCollection
articleTitle: HeaderFooterCollection
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.HeaderFooterCollection per un accesso semplice e digitato ai nodi Section HeaderFooter, semplificando la gestione dei documenti e migliorando il flusso di lavoro.
type: docs
weight: 3540
url: /it/net/aspose.words/headerfootercollection/
---
## HeaderFooterCollection class

Fornisce accesso tipizzato a[`HeaderFooter`](../headerfooter/) nodi di un[`Section`](../section/) .

Per saperne di più, visita il[Lavorare con intestazioni e piè di pagina](https://docs.aspose.com/words/net/working-with-headers-and-footers/) articolo di documentazione.

```csharp
public class HeaderFooterCollection : NodeCollection
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Ottiene il numero di nodi nella raccolta. |
| [Item](../../aspose.words/headerfootercollection/item/) { get; } | Recupera un[`HeaderFooter`](../headerfooter/) all'indice dato. (3 indexers) |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Aggiunge un nodo alla fine della raccolta. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Rimuove tutti i nodi da questa raccolta e dal documento. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Determina se un nodo è nella raccolta. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Fornisce una semplice iterazione in stile "foreach" sulla raccolta di nodi. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Restituisce l'indice basato su zero del nodo specificato. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Inserisce un nodo nella raccolta all'indice specificato. |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious_1)(*bool*) | Collega o scollega tutte le intestazioni e i piè di pagina alle intestazioni e ai piè di pagina corrispondenti nella sezione precedente. |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious)(*[HeaderFooterType](../headerfootertype/), bool*) | Collega o scollega l'intestazione o il piè di pagina specificato all'intestazione o al piè di pagina corrispondente nella sezione precedente. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Rimuove il nodo dalla raccolta e dal documento. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Rimuove il nodo all'indice specificato dalla raccolta e dal documento. |
| [ToArray](../../aspose.words/headerfootercollection/toarray/#toarray)() | Copia tutto`IntestazionePiè di pagina` s dalla raccolta a una nuova serie di`IntestazionePiè di pagina` s. (2 methods) |

## Osservazioni

Può essercene al massimo uno[`HeaderFooter`](../headerfooter/)

di ciascuno[`HeaderFooterType`](../headerfootertype/) per [`Section`](../section/) .

[`HeaderFooter`](../headerfooter/) gli oggetti possono presentarsi in qualsiasi ordine nella raccolta.

## Esempi

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

Mostra come creare un'intestazione e un piè di pagina.

```csharp
Document doc = new Document();

// Crea un'intestazione e aggiungi un paragrafo. Il testo in quel paragrafo
// apparirà in cima a ogni pagina di questa sezione, sopra il testo principale.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Crea un piè di pagina e aggiungi un paragrafo. Il testo in quel paragrafo
// apparirà in fondo a ogni pagina di questa sezione, sotto il testo principale.
HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FooterPrimary);
doc.FirstSection.HeadersFooters.Add(footer);

para = footer.AppendParagraph("My footer.");

Assert.False(footer.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

Assert.AreEqual(footer, para.ParentStory);
Assert.AreEqual(footer.ParentSection, para.ParentSection);
Assert.AreEqual(footer.ParentSection, header.ParentSection);

doc.Save(ArtifactsDir + "HeaderFooter.Create.docx");
```

### Guarda anche

* class [NodeCollection](../nodecollection/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
