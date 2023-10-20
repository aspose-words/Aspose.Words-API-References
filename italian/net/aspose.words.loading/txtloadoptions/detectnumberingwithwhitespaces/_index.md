---
title: TxtLoadOptions.DetectNumberingWithWhitespaces
linktitle: DetectNumberingWithWhitespaces
articleTitle: DetectNumberingWithWhitespaces
second_title: Aspose.Words per .NET
description: TxtLoadOptions DetectNumberingWithWhitespaces proprietà. Permette di specificare come vengono riconosciuti gli elementi dellelenco numerato quando il documento viene importato dal formato testo normale. Il valore predefinito èVERO in C#.
type: docs
weight: 30
url: /it/net/aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/
---
## TxtLoadOptions.DetectNumberingWithWhitespaces property

Permette di specificare come vengono riconosciuti gli elementi dell'elenco numerato quando il documento viene importato dal formato testo normale. Il valore predefinito è`VERO`.

```csharp
public bool DetectNumberingWithWhitespaces { get; set; }
```

## Osservazioni

Se questa opzione è impostata su`falso`, l'algoritmo di riconoscimento degli elenchi rileva i paragrafi dell'elenco, quando i numeri dell'elenco terminano con punto, parentesi destra o simboli di punto elenco (come "•", "*", "-" o "o").

Se questa opzione è impostata su`VERO`gli spazi vengono utilizzati anche come delimitatori dei numeri dell'elenco: l'algoritmo di riconoscimento dell'elenco per la numerazione in stile arabo (1., 1.1.2.) utilizza sia gli spazi bianchi che i simboli punto (".").

## Esempi

Mostra come rilevare gli elenchi durante il caricamento di documenti in testo normale.

```csharp
// Crea un documento di testo in chiaro in una stringa con quattro parti separate che possiamo interpretare come elenchi,
// con delimitatori diversi. Dopo aver caricato il documento di testo in chiaro in un oggetto "Documento",
// Aspose.Words rileverà sempre i primi tre elenchi e aggiungerà un oggetto "Lista".
// per ciascuno alla proprietà "Liste" del documento.
const string textDoc = "Full stop delimiters:\n" +
                       "1. First list item 1\n" +
                       "2. First list item 2\n" +
                       "3. First list item 3\n\n" +
                       "Right bracket delimiters:\n" +
                       "1) Second list item 1\n" +
                       "2) Second list item 2\n" +
                       "3) Second list item 3\n\n" +
                       "Bullet delimiters:\n" +
                       "• Third list item 1\n" +
                       "• Third list item 2\n" +
                       "• Third list item 3\n\n" +
                       "Whitespace delimiters:\n" +
                       "1 Fourth list item 1\n" +
                       "2 Fourth list item 2\n" +
                       "3 Fourth list item 3";

// Crea un oggetto "TxtLoadOptions", che possiamo passare al costruttore di un documento
// per modificare il modo in cui carichiamo un documento di testo normale.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Imposta la proprietà "DetectNumberingWithWhitespaces" su "true" per rilevare gli elementi numerati
// con delimitatori di spazi bianchi, come il quarto elenco nel nostro documento, come elenchi.
// Ciò potrebbe anche rilevare erroneamente i paragrafi che iniziano con numeri come elenchi.
// Imposta la proprietà "DetectNumberingWithWhitespaces" su "false"
// per non creare elenchi di elementi numerati con delimitatori di spazi bianchi.
loadOptions.DetectNumberingWithWhitespaces = detectNumberingWithWhitespaces;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(textDoc)), loadOptions);

if (detectNumberingWithWhitespaces)
{
    Assert.AreEqual(4, doc.Lists.Count);
    Assert.True(doc.FirstSection.Body.Paragraphs.Any(p => p.GetText().Contains("Fourth list") && ((Paragraph)p).IsListItem));
}
else
{
    Assert.AreEqual(3, doc.Lists.Count);
    Assert.False(doc.FirstSection.Body.Paragraphs.Any(p => p.GetText().Contains("Fourth list") && ((Paragraph)p).IsListItem));
}
```

### Guarda anche

* class [TxtLoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
