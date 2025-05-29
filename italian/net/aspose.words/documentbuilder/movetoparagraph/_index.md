---
title: DocumentBuilder.MoveToParagraph
linktitle: MoveToParagraph
articleTitle: MoveToParagraph
second_title: Aspose.Words per .NET
description: Esplora senza sforzo il tuo documento con il metodo MoveToParagraph di DocumentBuilder, che consente di spostare rapidamente il cursore su qualsiasi paragrafo della sezione.
type: docs
weight: 600
url: /it/net/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder.MoveToParagraph method

Sposta il cursore su un paragrafo nella sezione corrente.

```csharp
public void MoveToParagraph(int paragraphIndex, int characterIndex)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| paragraphIndex | Int32 | Indice del paragrafo a cui spostarsi. |
| characterIndex | Int32 | L'indice del carattere all'interno del paragrafo. Un valore negativo consente di specificare una posizione dalla fine del paragrafo. Usare -1 per spostarsi alla fine di il paragrafo. |

## Osservazioni

La navigazione viene eseguita all'interno della storia corrente della sezione corrente. Cioè, se hai spostato il cursore sull'intestazione principale della prima sezione, allora*paragraphIndex* specificato l'indice del paragrafo all'interno di quell'intestazione di quella sezione.

Quando*paragraphIndex* è maggiore o uguale a 0, specifica un indice da l'inizio della sezione con 0 come primo paragrafo. Quando*paragraphIndex* è minore di 0, ha specificato un indice dalla fine della sezione con -1 come ultimo paragrafo.

## Esempi

Mostra come spostare la posizione del cursore di un costruttore su un paragrafo specificato.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(22, paragraphs.Count);

// Crea un generatore di documenti per modificare il documento. Il cursore del generatore,
// che è il punto in cui inserirà nuovi nodi quando chiamiamo i suoi metodi di costruzione del documento,
// si trova attualmente all'inizio del documento.
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.AreEqual(0, paragraphs.IndexOf(builder.CurrentParagraph));

// Spostando il cursore su un paragrafo diverso, il cursore verrà posizionato davanti a quel paragrafo.
builder.MoveToParagraph(2, 0);
// Qualsiasi nuovo contenuto che aggiungeremo verrà inserito in quel momento.
builder.Writeln("This is a new third paragraph. ");
```

### Guarda anche

* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
