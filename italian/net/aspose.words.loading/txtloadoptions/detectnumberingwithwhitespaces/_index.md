---
title: TxtLoadOptions.DetectNumberingWithWhitespaces
linktitle: DetectNumberingWithWhitespaces
articleTitle: DetectNumberingWithWhitespaces
second_title: Aspose.Words per .NET
description: Ottimizza l'importazione dei tuoi documenti con la funzionalità DetectNumberingWithWhitespaces di TxtLoadOptions, garantendo il riconoscimento accurato degli elenchi numerati dal testo normale.
type: docs
weight: 40
url: /it/net/aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/
---
## TxtLoadOptions.DetectNumberingWithWhitespaces property

Consente di specificare come vengono riconosciuti gli elementi dell'elenco numerato quando il documento viene importato dal formato di testo normale. Il valore predefinito è`VERO`.

```csharp
public bool DetectNumberingWithWhitespaces { get; set; }
```

## Osservazioni

Se questa opzione è impostata su`falso`, l'algoritmo di riconoscimento degli elenchi rileva i paragrafi degli elenchi quando i numeri degli elenchi terminano con , ovvero con un punto, una parentesi quadra chiusa o un simbolo di elenco puntato (come "•", "*", "-" o "o").

Se questa opzione è impostata su`VERO`, gli spazi vuoti vengono utilizzati anche come delimitatori dei numeri di elenco: l'algoritmo di riconoscimento degli elenchi per la numerazione in stile arabo (1., 1.1.2.) utilizza sia gli spazi vuoti sia i simboli punto (".").

## Esempi

Mostra come rilevare gli elenchi durante il caricamento di documenti in chiaro.

```csharp
// Crea un documento di testo normale in una stringa con quattro parti separate che possiamo interpretare come elenchi,
// con delimitatori diversi. Dopo aver caricato il documento in chiaro in un oggetto "Documento",
// Aspose.Words rileverà sempre i primi tre elenchi e aggiungerà un oggetto "List"
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

// Creiamo un oggetto "TxtLoadOptions", che possiamo passare al costruttore di un documento
// per modificare il modo in cui carichiamo un documento di testo normale.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Imposta la proprietà "DetectNumberingWithWhitespaces" su "true" per rilevare gli elementi numerati
// con delimitatori di spazi vuoti, come il quarto elenco nel nostro documento, come elenchi.
// Questo potrebbe anche rilevare erroneamente come elenchi i paragrafi che iniziano con numeri.
// Imposta la proprietà "DetectNumberingWithWhitespaces" su "false"
// per non creare elenchi da elementi numerati con delimitatori di spazi.
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
