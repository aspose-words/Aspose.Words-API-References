---
title: DocumentBuilder.MoveToParagraph
second_title: Aspose.Words per .NET API Reference
description: DocumentBuilder metodo. Sposta il cursore su un paragrafo della sezione corrente.
type: docs
weight: 570
url: /it/net/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder.MoveToParagraph method

Sposta il cursore su un paragrafo della sezione corrente.

```csharp
public void MoveToParagraph(int paragraphIndex, int characterIndex)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| paragraphIndex | Int32 | L'indice del paragrafo a cui spostarsi. |
| characterIndex | Int32 | L'indice del carattere all'interno del paragrafo. Un valore negativo consente di specificare una posizione dalla fine del paragrafo. Usa -1 per spostarti alla fine di il paragrafo. |

### Osservazioni

La navigazione viene eseguita all'interno della storia corrente della sezione corrente. Cioè, se hai spostato il cursore sull'intestazione principale della prima sezione, allora*paragraphIndex*ha specificato l'indice del paragrafo all'interno dell'intestazione di quella sezione.

Quando*paragraphIndex* è maggiore o uguale a 0, specifica un indice da all'inizio della sezione dove 0 è il primo paragrafo. Quando*paragraphIndex* è inferiore a 0, ha specificato un indice dalla fine della sezione dove -1 è l'ultimo paragrafo.

### Esempi

Mostra come spostare la posizione del cursore di un generatore su un paragrafo specifico.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(22, paragraphs.Count);

// Crea un generatore di documenti per modificare il documento. Il cursore del costruttore,
// qual è il punto in cui inserirà i nuovi nodi quando chiameremo i suoi metodi di costruzione del documento,
// è attualmente all'inizio del documento.
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.AreEqual(0, paragraphs.IndexOf(builder.CurrentParagraph));

// Spostare il cursore su un paragrafo diverso posizionerà il cursore davanti a quel paragrafo.
builder.MoveToParagraph(2, 0);
// Qualsiasi nuovo contenuto che aggiungiamo verrà inserito a quel punto.
builder.Writeln("This is a new third paragraph. ");
```

### Guarda anche

* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)


