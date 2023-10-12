---
title: Enum LayoutEntityType
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Layout.LayoutEntityType enum. Tipi delle entità di layout.
type: docs
weight: 3330
url: /it/net/aspose.words.layout/layoutentitytype/
---
## LayoutEntityType enumeration

Tipi delle entità di layout.

```csharp
[Flags]
public enum LayoutEntityType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Valore predefinito. |
| Page | `1` | Rappresenta la pagina di un documento. La pagina può avereColumn ,HeaderFooter EComment entità secondarie. |
| Column | `2` | Rappresenta una colonna di testo su una pagina. La colonna può avere le stesse entità secondarie diCell , inoltreFootnote ,Endnote ENoteSeparator entità. |
| Row | `8` | Rappresenta una riga della tabella. La riga può avereCell come entità figlie. |
| Cell | `10` | Rappresenta una cella di tabella. La cella può avereLine ERow entità secondarie. |
| Line | `20` | Rappresenta una riga di caratteri di testo e oggetti in linea. La riga può avereSpan entità secondarie. |
| Span | `40` | Rappresenta uno o più caratteri in una riga. Sono inclusi caratteri speciali come indicatori di inizio/fine campo, segnalibri e commenti. Lo span potrebbe non avere entità secondarie. |
| Footnote | `100` | Rappresenta il segnaposto per il contenuto della nota a piè di pagina. La nota a piè di pagina potrebbe avereNote entità secondarie. |
| Endnote | `200` | Rappresenta il segnaposto per il contenuto della nota di chiusura. La nota di chiusura potrebbe avereNote entità secondarie. |
| Note | `4000` | Rappresenta il segnaposto per il contenuto della nota. La nota potrebbe avereLine ERow entità secondarie. |
| HeaderFooter | `400` | Rappresenta il segnaposto per il contenuto di intestazione/piè di pagina su una pagina. HeaderFooter potrebbe avereLine ERow entità secondarie. |
| TextBox | `800` | Rappresenta l'area di testo all'interno di una forma. La casella di testo può avereLine ERow entità secondarie. |
| Comment | `1000` | Rappresenta il segnaposto per il contenuto del commento. Il commento potrebbe avereLine ERow entità secondarie. |
| NoteSeparator | `2000` | Rappresenta il separatore di note a piè di pagina/note di chiusura. NoteSeparator può avereLine ERow entità secondarie. |

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


