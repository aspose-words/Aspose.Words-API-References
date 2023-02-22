---
title: TxtLoadOptions.DetectNumberingWithWhitespaces
second_title: Aspose.Words per .NET API Reference
description: TxtLoadOptions proprietà. Consente di specificare come vengono riconosciute le voci di elenco numerate quando il documento viene importato dal formato di testo normale. Il valore predefinito è true.
type: docs
weight: 20
url: /it/net/aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/
---
## TxtLoadOptions.DetectNumberingWithWhitespaces property

Consente di specificare come vengono riconosciute le voci di elenco numerate quando il documento viene importato dal formato di testo normale. Il valore predefinito è true.

```csharp
public bool DetectNumberingWithWhitespaces { get; set; }
```

### Osservazioni

Se questa opzione è impostata su false, l'algoritmo di riconoscimento degli elenchi rileva i paragrafi dell'elenco, quando i numeri dell'elenco terminano con punti, parentesi o punti elenco (come "•", "*", "-" o "o").

Se questa opzione è impostata su true, gli spazi bianchi vengono utilizzati anche come delimitatori del numero di elenchi: l'algoritmo di riconoscimento degli elenchi per la numerazione in stile arabo (1., 1.1.2.) utilizza sia gli spazi bianchi che i simboli punto (".").

### Esempi

Mostra come rilevare gli elenchi durante il caricamento di documenti in testo normale.

```csharp
// Crea un documento in chiaro in una stringa con quattro parti separate che possiamo interpretare come elenchi,
// con diversi delimitatori. Dopo aver caricato il documento di testo in chiaro in un oggetto "Documento",
// Aspose.Words rileverà sempre i primi tre elenchi e aggiungerà un oggetto "Elenco".
// per ciascuno alla proprietà "Elenchi" del documento.
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
// Questo potrebbe anche rilevare erroneamente paragrafi che iniziano con numeri come elenchi.
// Imposta la proprietà "DetectNumberingWithWhitespaces" su "false"
// per non creare elenchi da elementi numerati con delimitatori di spazi bianchi.
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
* spazio dei nomi [Aspose.Words.Loading](../../txtloadoptions/)
* assemblea [Aspose.Words](../../../)


