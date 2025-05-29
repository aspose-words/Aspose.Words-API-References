---
title: LayoutEntityType Enum
linktitle: LayoutEntityType
articleTitle: LayoutEntityType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Layout.LayoutEntityType, che presenta diversi tipi di entità di layout per una formattazione avanzata dei documenti e un'integrazione perfetta.
type: docs
weight: 3780
url: /it/net/aspose.words.layout/layoutentitytype/
---
## LayoutEntityType enumeration

Tipi di entità di layout.

```csharp
[Flags]
public enum LayoutEntityType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Valore predefinito. |
| Page | `1` | Rappresenta la pagina di un documento. La pagina potrebbe avereColumn ,HeaderFooter EComment entità figlio. |
| Column | `2` | Rappresenta una colonna di testo su una pagina. La colonna può avere le stesse entità figlio diCell , piùFootnote ,Endnote ENoteSeparator entità. |
| Row | `8` | Rappresenta una riga della tabella. La riga può avereCell come entità figlio. |
| Cell | `10` | Rappresenta una cella della tabella. La cella può avereLine ERow entità figlio. |
| Line | `20` | Rappresenta la riga di caratteri di testo e oggetti in linea. La riga può avereSpan entità figlio. |
| Span | `40` | Rappresenta uno o più caratteri in una riga. Ciò include caratteri speciali come marcatori di inizio/fine campo, segnalibri e commenti. Lo span non può avere entità figlio. |
| Footnote | `100` | Rappresenta il segnaposto per il contenuto della nota a piè di pagina. La nota a piè di pagina può avereNote entità figlio. |
| Endnote | `200` | Rappresenta il segnaposto per il contenuto della nota di chiusura. La nota di chiusura può avereNote entità figlio. |
| Note | `4000` | Rappresenta il segnaposto per il contenuto della nota. La nota potrebbe avereLine ERow entità figlio. |
| HeaderFooter | `400` | Rappresenta il segnaposto per il contenuto dell'intestazione/piè di pagina su una pagina. HeaderFooter può avereLine ERow entità figlio. |
| TextBox | `800` | Rappresenta l'area di testo all'interno di una forma. La casella di testo può avereLine ERow entità figlio. |
| Comment | `1000` | Rappresenta il segnaposto per il contenuto del commento. Il commento potrebbe avereLine ERow entità figlio. |
| NoteSeparator | `2000` | Rappresenta il separatore di note a piè di pagina/note di chiusura. NoteSeparator può avereLine ERow entità figlio. |

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
