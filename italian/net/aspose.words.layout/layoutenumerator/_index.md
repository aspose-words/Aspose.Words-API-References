---
title: Class LayoutEnumerator
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Layout.LayoutEnumerator classe. Enumera le entità di layout di pagina di un documento. Puoi utilizzare questa classe per esplorare il modello di layout di pagina. Le proprietà disponibili sono tipo geometria testo e indice di pagina in cui viene visualizzata lentità nonché struttura e relazioni generali. Utilizza una combinazione diGetEntity ECurrent passare allentità che corrisponde a un nodo del documento.
type: docs
weight: 3340
url: /it/net/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class

Enumera le entità di layout di pagina di un documento. Puoi utilizzare questa classe per esplorare il modello di layout di pagina. Le proprietà disponibili sono tipo, geometria, testo e indice di pagina in cui viene visualizzata l'entità, nonché struttura e relazioni generali. Utilizza una combinazione di[`GetEntity`](../layoutcollector/getentity/) E[`Current`](./current/) passare all'entità che corrisponde a un nodo del documento.

Per saperne di più, visita il[Conversione nel formato a pagina fissa](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) articolo di documentazione.

```csharp
public class LayoutEnumerator
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [LayoutEnumerator](layoutenumerator/)(Document) | Inizializza la nuova istanza di questa classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Current](../../aspose.words.layout/layoutenumerator/current/) { get; set; } | Ottiene o imposta la posizione corrente nel modello di layout della pagina. Questa proprietà restituisce un oggetto opaco che corrisponde all'entità di layout corrente. |
| [Document](../../aspose.words.layout/layoutenumerator/document/) { get; } | Ottiene il documento enumerato da questa istanza. |
| [Item](../../aspose.words.layout/layoutenumerator/item/) { get; } | Ottiene una proprietà denominata dell'entità. |
| [Kind](../../aspose.words.layout/layoutenumerator/kind/) { get; } | Ottiene il tipo dell'entità corrente. Può essere una stringa vuota ma mai`nullo` . |
| [PageIndex](../../aspose.words.layout/layoutenumerator/pageindex/) { get; } | Ottiene l'indice in base 1 di una pagina che contiene l'entità corrente. |
| [Rectangle](../../aspose.words.layout/layoutenumerator/rectangle/) { get; } | Restituisce il rettangolo di delimitazione dell'entità corrente rispetto all'angolo superiore sinistro della pagina (in punti). |
| [Text](../../aspose.words.layout/layoutenumerator/text/) { get; } | Ottiene il testo dell'entità span corrente. Lancia per altri tipi di entità. |
| [Type](../../aspose.words.layout/layoutenumerator/type/) { get; } | Ottiene il tipo dell'entità corrente. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [MoveFirstChild](../../aspose.words.layout/layoutenumerator/movefirstchild/)() | Passa alla prima entità figlio. |
| [MoveLastChild](../../aspose.words.layout/layoutenumerator/movelastchild/)() | Passa all'ultima entità figlio. |
| [MoveNext](../../aspose.words.layout/layoutenumerator/movenext/)() | Passa all'entità di pari livello successiva in ordine visivo. Quando si ripetono le righe di un paragrafo interrotte su più pagine, questo metodo non si sposterà alla pagina successiva ma piuttosto si sposterà all'entità successiva sulla stessa pagina. |
| [MoveNextLogical](../../aspose.words.layout/layoutenumerator/movenextlogical/)() | Passa all'entità di pari livello successiva in ordine logico. Quando si ripetono le righe di un paragrafo interrotte su più pagine, questo metodo si sposterà alla riga successiva anche se risiede su un'altra pagina. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent)() | Passa all'entità principale. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent_1)(LayoutEntityType) | Passa all'entità principale del tipo specificato. |
| [MovePrevious](../../aspose.words.layout/layoutenumerator/moveprevious/)() | Passa all'entità gemella precedente. |
| [MovePreviousLogical](../../aspose.words.layout/layoutenumerator/movepreviouslogical/)() | Passa all'entità gemella precedente in ordine logico. Quando si ripetono le righe di un paragrafo spezzate su più pagine, questo metodo si sposterà alla riga precedente anche se risiede su un'altra pagina. |
| [Reset](../../aspose.words.layout/layoutenumerator/reset/)() | Sposta l'enumeratore alla prima pagina del documento. |

### Esempi

Mostra le modalità per attraversare le entità di layout di un documento.

```csharp
public void LayoutEnumerator()
{
    // Apre un documento che contiene una varietà di entità di layout.
    // Le entità di layout sono pagine, celle, righe, linee e altri oggetti inclusi nell'enumerazione LayoutEntityType.
    // Ogni entità di layout ha uno spazio rettangolare che occupa nel corpo del documento.
    Document doc = new Document(MyDir + "Layout entities.docx");

    // Crea un enumeratore che possa attraversare queste entità come un albero.
    LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

    Assert.AreEqual(doc, layoutEnumerator.Document);

    layoutEnumerator.MoveParent(LayoutEntityType.Page);

    Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);
    Assert.Throws<InvalidOperationException>(() => Console.WriteLine(layoutEnumerator.Text));

    // Possiamo chiamare questo metodo per assicurarci che l'enumeratore si trovi nella prima entità di layout.
    layoutEnumerator.Reset();

    // Esistono due ordini che determinano il modo in cui l'enumeratore di layout continua ad attraversare le entità di layout
    // quando incontra entità che si estendono su più pagine.
    // 1 - In ordine visivo:
    // Quando ci si sposta tra i figli di un'entità che si estendono su più pagine,
    // il layout della pagina ha la precedenza e ci spostiamo su altri elementi secondari in questa pagina ed evitiamo quelli nella successiva.
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

    // Il nostro enumeratore è ora alla fine della raccolta. Possiamo attraversare le entità del layout all'indietro per tornare all'inizio.
    Console.WriteLine("Traversing from last to first, elements between pages separated:");
    TraverseLayoutBackward(layoutEnumerator, 1);

    // 2 - In ordine logico:
    // Quando ci si sposta tra i figli di un'entità che si estendono su più pagine,
    // l'enumeratore si sposterà tra le pagine per attraversare tutte le entità figlie.
    Console.WriteLine("Traversing from first to last, elements between pages mixed:");
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    Console.WriteLine("Traversing from last to first, elements between pages mixed:");
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

/// <summary>
/// Enumera la raccolta di entità di layout di layoutEnumerator dalla parte anteriore a quella posteriore,
/// in modo approfondito e nell'ordine "visivo".
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
/// Enumera la raccolta di entità di layout di layoutEnumerator dall'inizio alla fine,
/// in modo approfondito e nell'ordine "visivo".
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
/// Enumera la raccolta di entità di layout di layoutEnumerator dalla parte anteriore a quella posteriore,
/// in modo approfondito e nell'ordine "logico".
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
/// Enumera la raccolta di entità di layout di layoutEnumerator dall'inizio alla fine,
/// in modo approfondito e nell'ordine "logico".
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
/// Stampa le informazioni sull'entità corrente di layoutEnumerator sulla console, facendo rientrare il testo con caratteri di tabulazione
/// in base alla sua profondità rispetto al nodo radice che abbiamo fornito nell'istanza del costruttore LayoutEnumerator.
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


