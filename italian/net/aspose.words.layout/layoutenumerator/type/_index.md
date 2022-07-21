---
title: Type
second_title: Aspose.Words per .NET API Reference
description: Ottiene il tipo dellentità corrente.
type: docs
weight: 80
url: /it/net/aspose.words.layout/layoutenumerator/type/
---
## LayoutEnumerator.Type property

Ottiene il tipo dell'entità corrente.

```csharp
public LayoutEntityType Type { get; }
```

### Esempi

Mostra i modi per attraversare le entità di layout di un documento.

```csharp
public void LayoutEnumerator()
{
    // Apre un documento che contiene una varietà di entità di layout.
    // Le entità di layout sono pagine, celle, righe, righe e altri oggetti inclusi nell'enumerazione LayoutEntityType.
    // Ogni entità di layout ha uno spazio rettangolare che occupa nel corpo del documento.
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
    // il layout della pagina ha la precedenza e ci spostiamo su altri elementi figlio in questa pagina ed evitiamo quelli nella successiva.
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

    // Il nostro enumeratore è ora alla fine della raccolta. Possiamo attraversare le entità del layout all'indietro per tornare all'inizio.
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
/// Enumera la raccolta di entità di layout di layoutEnumerator front-to-back,
/// in modo approfondito e nell'ordine "Visivo".
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
/// in modo approfondito e nell'ordine "Visivo".
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
/// Enumera la raccolta di entità di layout di layoutEnumerator front-to-back,
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
/// Stampa le informazioni sull'entità corrente di layoutEnumerator sulla console, mentre indenta il testo con caratteri di tabulazione
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

* enum [LayoutEntityType](../../layoutentitytype)
* class [LayoutEnumerator](../../layoutenumerator)
* spazio dei nomi [Aspose.Words.Layout](../../layoutenumerator)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
