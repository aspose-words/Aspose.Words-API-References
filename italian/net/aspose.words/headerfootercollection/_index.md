---
title: Class HeaderFooterCollection
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.HeaderFooterCollection classe. Fornisce laccesso digitato aHeaderFooter nodi di aSection .
type: docs
weight: 3110
url: /it/net/aspose.words/headerfootercollection/
---
## HeaderFooterCollection class

Fornisce l'accesso digitato a[`HeaderFooter`](../headerfooter/) nodi di a[`Section`](../section/) .

Per saperne di più, visita il[Lavorare con intestazioni e piè di pagina](https://docs.aspose.com/words/net/working-with-headers-and-footers/) articolo di documentazione.

```csharp
public class HeaderFooterCollection : NodeCollection
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Ottiene il numero di nodi nella raccolta. |
| [Item](../../aspose.words/headerfootercollection/item/) { get; } | Recupera a[`HeaderFooter`](../headerfooter/) all'indice indicato. (3 indexers) |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | Aggiunge un nodo alla fine della raccolta. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Rimuove tutti i nodi da questa raccolta e dal documento. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | Determina se un nodo è nella raccolta. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Fornisce una semplice iterazione di stile "foreach" sulla raccolta di nodi. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | Restituisce l'indice in base zero del nodo specificato. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | Inserisce un nodo nella raccolta in corrispondenza dell'indice specificato. |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious_1)(bool) | Collega o scollega tutte le intestazioni e i piè di pagina alle intestazioni e ai piè di pagina corrispondenti nella sezione precedente. |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious)(HeaderFooterType, bool) | Collega o scollega l'intestazione o il piè di pagina specificato all'intestazione o al piè di pagina corrispondente nella sezione precedente. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | Rimuove il nodo dalla raccolta e dal documento. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | Rimuove il nodo all'indice specificato dalla raccolta e dal documento. |
| [ToArray](../../aspose.words/headerfootercollection/toarray/#toarray)() | Copia tutto`HeaderFoorter` s dalla raccolta a una nuova serie di`HeaderFoorter` s. (2 methods) |

### Osservazioni

Può essercene al massimo uno[`HeaderFooter`](../headerfooter/)

di ciascun[`HeaderFooterType`](../headerfootertype/) per [`Section`](../section/) .

[`HeaderFooter`](../headerfooter/) gli oggetti possono essere presenti in qualsiasi ordine nella raccolta.

### Esempi

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

Mostra come creare un'intestazione e un piè di pagina.

```csharp
Document doc = new Document();

// Crea un'intestazione e aggiungici un paragrafo. Il testo in quel paragrafo
// apparirà nella parte superiore di ogni pagina di questa sezione, sopra il corpo del testo principale.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Crea un piè di pagina e aggiungivi un paragrafo. Il testo in quel paragrafo
// apparirà in fondo a ogni pagina di questa sezione, sotto il corpo del testo principale.
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


