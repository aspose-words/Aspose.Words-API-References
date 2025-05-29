---
title: LayoutEnumerator Class
linktitle: LayoutEnumerator
articleTitle: LayoutEnumerator
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Layout.LayoutEnumerator per un'enumerazione efficiente del layout dei documenti. Esplora la geometria, il testo e la struttura della pagina senza sforzo!
type: docs
weight: 3790
url: /it/net/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class

Enumera le entità del layout di pagina di un documento. È possibile utilizzare questa classe per esplorare il modello di layout di pagina. Le proprietà disponibili sono tipo, geometria, testo e indice di pagina in cui viene renderizzata l'entità, nonché struttura generale e relazioni. Utilizzare una combinazione di[`GetEntity`](../layoutcollector/getentity/) E[`Current`](./current/) spostarsi all'entità che corrisponde a un nodo del documento.

Per saperne di più, visita il[Conversione in formato a pagina fissa](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) articolo di documentazione.

```csharp
public class LayoutEnumerator
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [LayoutEnumerator](layoutenumerator/)(*[Document](../../aspose.words/document/)*) | Inizializza una nuova istanza di questa classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Current](../../aspose.words.layout/layoutenumerator/current/) { get; set; } | Ottiene o imposta la posizione corrente nel modello di layout di pagina. Questa proprietà restituisce un oggetto opaco che corrisponde all'entità di layout corrente. |
| [Document](../../aspose.words.layout/layoutenumerator/document/) { get; } | Ottiene il documento che questa istanza enumera. |
| [Item](../../aspose.words.layout/layoutenumerator/item/) { get; } | Ottiene una proprietà denominata dell'entità. |
| [Kind](../../aspose.words.layout/layoutenumerator/kind/) { get; } | Ottiene il tipo dell'entità corrente. Può essere una stringa vuota, ma mai`null` . |
| [PageIndex](../../aspose.words.layout/layoutenumerator/pageindex/) { get; } | Ottiene l'indice basato su 1 di una pagina che contiene l'entità corrente. |
| [Rectangle](../../aspose.words.layout/layoutenumerator/rectangle/) { get; } | Restituisce il rettangolo di delimitazione dell'entità corrente rispetto all'angolo superiore sinistro della pagina (in punti). |
| [Text](../../aspose.words.layout/layoutenumerator/text/) { get; } | Recupera il testo dell'entità span corrente. Genera un'eccezione per altri tipi di entità. |
| [Type](../../aspose.words.layout/layoutenumerator/type/) { get; } | Ottiene il tipo dell'entità corrente. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [MoveFirstChild](../../aspose.words.layout/layoutenumerator/movefirstchild/)() | Passa alla prima entità figlio. |
| [MoveLastChild](../../aspose.words.layout/layoutenumerator/movelastchild/)() | Passa all'ultima entità figlio. |
| [MoveNext](../../aspose.words.layout/layoutenumerator/movenext/)() | Passa all'entità gemella successiva in ordine visivo. Quando si iterano le righe di un paragrafo suddiviso in più pagine, questo metodo non passerà alla pagina successiva, ma all'entità successiva sulla stessa pagina. |
| [MoveNextLogical](../../aspose.words.layout/layoutenumerator/movenextlogical/)() | Passa all'entità gemella successiva in ordine logico. Quando si ripetono le righe di un paragrafo suddiviso in più pagine, questo metodo passerà alla riga successiva anche se si trova su un'altra pagina. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent)() | Passa all'entità padre. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent_1)(*[LayoutEntityType](../layoutentitytype/)*) | Passa all'entità padre del tipo specificato. |
| [MovePrevious](../../aspose.words.layout/layoutenumerator/moveprevious/)() | Passa all'entità gemella precedente. |
| [MovePreviousLogical](../../aspose.words.layout/layoutenumerator/movepreviouslogical/)() | Passa all'entità gemella precedente in ordine logico. Quando si ripetono le righe di un paragrafo suddiviso in più pagine, questo metodo passerà alla riga precedente anche se si trova su un'altra pagina. |
| [Reset](../../aspose.words.layout/layoutenumerator/reset/)() | Sposta l'enumeratore alla prima pagina del documento. |

## Esempi

Mostra i modi per attraversare le entità di layout di un documento.

```csharp
public void LayoutEnumerator()
{
    // Apre un documento che contiene diverse entità di layout.
    // Le entità di layout sono pagine, celle, righe, linee e altri oggetti inclusi nell'enum LayoutEntityType.
    // Ogni entità di layout occupa uno spazio rettangolare nel corpo del documento.
    Document doc = new Document(MyDir + "Layout entities.docx");

    // Crea un enumeratore in grado di attraversare queste entità come un albero.
    LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

    Assert.AreEqual(doc, layoutEnumerator.Document);

    layoutEnumerator.MoveParent(LayoutEntityType.Page);

    Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);
    Assert.Throws<InvalidOperationException>(() => Console.WriteLine(layoutEnumerator.Text));

    // Possiamo chiamare questo metodo per assicurarci che l'enumeratore si trovi nella prima entità di layout.
    layoutEnumerator.Reset();

    // Ci sono due ordini che determinano come l'enumeratore di layout continua ad attraversare le entità di layout
    // quando incontra entità che si estendono su più pagine.
    // 1 - In ordine visivo:
    // Quando ci si sposta tra i figli di un'entità che si estendono su più pagine,
    // il layout della pagina ha la precedenza e passiamo agli altri elementi figlio di questa pagina, evitando quelli della pagina successiva.
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

    // Il nostro enumeratore si trova ora alla fine della collezione. Possiamo scorrere a ritroso le entità del layout per tornare all'inizio.
    Console.WriteLine("Traversing from last to first, elements between pages separated:");
    TraverseLayoutBackward(layoutEnumerator, 1);

    // 2 - In ordine logico:
    // Quando ci si sposta tra i figli di un'entità che si estendono su più pagine,
    // l'enumeratore si sposterà tra le pagine per attraversare tutte le entità figlio.
    Console.WriteLine("Traversing from first to last, elements between pages mixed:");
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    Console.WriteLine("Traversing from last to first, elements between pages mixed:");
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

/// <summary>
/// Enumerare attraverso la raccolta di entità di layout di layoutEnumerator da davanti a dietro,
/// in modo depth-first e nell'ordine "Visivo".
/// </summary>
private static void TraverseLayoutForward(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveFirstChild())
        {
            TraverseLayoutForward(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MoveNext());
}

/// <summary>
/// Enumerare la raccolta di entità di layout di layoutEnumerator da dietro in avanti,
/// in modo depth-first e nell'ordine "Visivo".
/// </summary>
private static void TraverseLayoutBackward(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveLastChild())
        {
            TraverseLayoutBackward(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MovePrevious());
}

/// <summary>
/// Enumerare attraverso la raccolta di entità di layout di layoutEnumerator da davanti a dietro,
/// in modo depth-first e nell'ordine "logico".
/// </summary>
private static void TraverseLayoutForwardLogical(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveFirstChild())
        {
            TraverseLayoutForwardLogical(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MoveNextLogical());
}

/// <summary>
/// Enumerare la raccolta di entità di layout di layoutEnumerator da dietro in avanti,
/// in modo depth-first e nell'ordine "logico".
/// </summary>
private static void TraverseLayoutBackwardLogical(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveLastChild())
        {
            TraverseLayoutBackwardLogical(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MovePreviousLogical());
}

/// <summary>
/// Stampa le informazioni sull'entità corrente di layoutEnumerator sulla console, mentre rientra il testo con caratteri di tabulazione
/// in base alla sua profondità relativa al nodo radice che abbiamo fornito nell'istanza del costruttore LayoutEnumerator.
/// Il rettangolo che elaboriamo alla fine rappresenta l'area e la posizione che l'entità occupa nel documento.
/// </summary>
private static void PrintCurrentEntity(LayoutEnumerator layoutEnumerator, int indent)
{
    string tabs = new string('\t', indent);

    Console.WriteLine(layoutEnumerator.Kind == string.Empty
        ? $"{tabs}-> Entity type: {layoutEnumerator.Type}"
        : $"{tabs}-> Entity type & kind: {layoutEnumerator.Type}, {layoutEnumerator.Kind}");

    // Solo gli span possono contenere testo.
    if (layoutEnumerator.Type == LayoutEntityType.Span)
        Console.WriteLine($"{tabs}   Span contents: \"{layoutEnumerator.Text}\"");

    RectangleF leRect = layoutEnumerator.Rectangle;
    Console.WriteLine($"{tabs}   Rectangle dimensions {leRect.Width}x{leRect.Height}, X={leRect.X} Y={leRect.Y}");
    Console.WriteLine($"{tabs}   Page {layoutEnumerator.PageIndex}");
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Layout](../../aspose.words.layout/)
* assemblea [Aspose.Words](../../)
