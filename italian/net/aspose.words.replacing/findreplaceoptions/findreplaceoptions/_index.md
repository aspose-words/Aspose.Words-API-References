---
title: FindReplaceOptions
linktitle: FindReplaceOptions
articleTitle: FindReplaceOptions
second_title: Aspose.Words per .NET
description: Scopri il costruttore FindReplaceOptions per inizializzare facilmente una nuova istanza con impostazioni predefinite, migliorando le funzionalità di ricerca e sostituzione.
type: docs
weight: 10
url: /it/net/aspose.words.replacing/findreplaceoptions/findreplaceoptions/
---
## FindReplaceOptions() {#constructor}

Inizializza una nuova istanza della classe FindReplaceOptions con impostazioni predefinite.

```csharp
public FindReplaceOptions()
```

## Esempi

Mostra come riconoscere e utilizzare le sostituzioni all'interno dei modelli di sostituzione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Jason gave money to Paul.");

Regex regex = new Regex(@"([A-z]+) gave money to ([A-z]+)");

FindReplaceOptions options = new FindReplaceOptions();
options.UseSubstitutions = true;

// L'utilizzo della modalità legacy non supporta molte funzionalità avanzate, quindi dobbiamo impostarla su "false".
options.LegacyMode = false;

doc.Range.Replace(regex, @"$2 took money from $1", options);

Assert.AreEqual(doc.GetText(), "Paul took money from Jason.\f");
```

### Guarda anche

* class [FindReplaceOptions](../)
* spazio dei nomi [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assemblea [Aspose.Words](../../../)

---

## FindReplaceOptions(*[FindReplaceDirection](../../findreplacedirection/)*) {#constructor_1}

Inizializza una nuova istanza della classe FindReplaceOptions con la direzione specificata.

```csharp
public FindReplaceOptions(FindReplaceDirection direction)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| direction | FindReplaceDirection | Direzione dell'operazione di ricerca e sostituzione. |

### Guarda anche

* enum [FindReplaceDirection](../../findreplacedirection/)
* class [FindReplaceOptions](../)
* spazio dei nomi [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assemblea [Aspose.Words](../../../)

---

## FindReplaceOptions(*[IReplacingCallback](../../ireplacingcallback/)*) {#constructor_3}

Inizializza una nuova istanza della classe FindReplaceOptions con il callback di sostituzione specificato.

```csharp
public FindReplaceOptions(IReplacingCallback replacingCallback)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| replacingCallback | IReplacingCallback | Callback da utilizzare per sostituire il testo trovato. |

## Esempi

Mostra come tenere traccia dell'ordine in cui un'operazione di sostituzione del testo attraversa i nodi.

```csharp
public void Order(bool differentFirstPageHeaderFooter)
{
    Document doc = new Document(MyDir + "Header and footer types.docx");

    Section firstPageSection = doc.FirstSection;

    ReplaceLog logger = new ReplaceLog();
    FindReplaceOptions options = new FindReplaceOptions(logger);

    // L'utilizzo di un'intestazione/piè di pagina diverso per la prima pagina inciderà sull'ordine di ricerca.
    firstPageSection.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;
    doc.Range.Replace(new Regex("(header|footer)"), "", options);

    if (differentFirstPageHeaderFooter)
        Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", 
            logger.Text.Replace("\r", ""));
    else
        Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", 
            logger.Text.Replace("\r", ""));
}

/// <summary>
/// Durante un'operazione di ricerca e sostituzione, registra il contenuto di ogni nodo che contiene testo che l'operazione 'trova',
/// nello stato in cui si trova prima che avvenga la sostituzione.
/// Verrà visualizzato l'ordine in cui l'operazione di sostituzione del testo attraversa i nodi.
/// </summary>
private class ReplaceLog : IReplacingCallback
{
    public ReplaceAction Replacing(ReplacingArgs args)
    {
        mTextBuilder.AppendLine(args.MatchNode.GetText());
        return ReplaceAction.Skip;
    }

    internal string Text => mTextBuilder.ToString();

    private readonly StringBuilder mTextBuilder = new StringBuilder();
}
```

### Guarda anche

* interface [IReplacingCallback](../../ireplacingcallback/)
* class [FindReplaceOptions](../)
* spazio dei nomi [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assemblea [Aspose.Words](../../../)

---

## FindReplaceOptions(*[FindReplaceDirection](../../findreplacedirection/), [IReplacingCallback](../../ireplacingcallback/)*) {#constructor_2}

Inizializza una nuova istanza della classe FindReplaceOptions con la direzione specificata e il callback di sostituzione.

```csharp
public FindReplaceOptions(FindReplaceDirection direction, IReplacingCallback replacingCallback)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| direction | FindReplaceDirection | Direzione dell'operazione di ricerca e sostituzione. |
| replacingCallback | IReplacingCallback | Callback da utilizzare per sostituire il testo trovato. |

### Guarda anche

* enum [FindReplaceDirection](../../findreplacedirection/)
* interface [IReplacingCallback](../../ireplacingcallback/)
* class [FindReplaceOptions](../)
* spazio dei nomi [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assemblea [Aspose.Words](../../../)
