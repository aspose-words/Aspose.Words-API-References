---
title: FindReplaceOptions Class
linktitle: FindReplaceOptions
articleTitle: FindReplaceOptions
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.FindReplaceOptions per funzionalità avanzate di ricerca e sostituzione, migliorando la modifica dei documenti con precisione e flessibilità.
type: docs
weight: 5350
url: /it/net/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class

Specifica le opzioni per le operazioni di ricerca/sostituzione.

Per saperne di più, visita il[Trova e sostituisci](https://docs.aspose.com/words/net/find-and-replace/) articolo di documentazione.

```csharp
public class FindReplaceOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FindReplaceOptions](findreplaceoptions/#constructor)() | Inizializza una nuova istanza della classe FindReplaceOptions con impostazioni predefinite. |
| [FindReplaceOptions](findreplaceoptions/#constructor_1)(*[FindReplaceDirection](../findreplacedirection/)*) | Inizializza una nuova istanza della classe FindReplaceOptions con la direzione specificata. |
| [FindReplaceOptions](findreplaceoptions/#constructor_3)(*[IReplacingCallback](../ireplacingcallback/)*) | Inizializza una nuova istanza della classe FindReplaceOptions con il callback di sostituzione specificato. |
| [FindReplaceOptions](findreplaceoptions/#constructor_2)(*[FindReplaceDirection](../findreplacedirection/), [IReplacingCallback](../ireplacingcallback/)*) | Inizializza una nuova istanza della classe FindReplaceOptions con la direzione specificata e il callback di sostituzione. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [ApplyFont](../../aspose.words.replacing/findreplaceoptions/applyfont/) { get; } | Formattazione del testo applicata al nuovo contenuto. |
| [ApplyParagraphFormat](../../aspose.words.replacing/findreplaceoptions/applyparagraphformat/) { get; } | Formattazione del paragrafo applicata al nuovo contenuto. |
| [Direction](../../aspose.words.replacing/findreplaceoptions/direction/) { get; set; } | Seleziona la direzione per la sostituzione. Il valore predefinito èForward . |
| [FindWholeWordsOnly](../../aspose.words.replacing/findreplaceoptions/findwholewordsonly/) { get; set; } | True indica che oldValue deve essere una parola autonoma. |
| [IgnoreDeleted](../../aspose.words.replacing/findreplaceoptions/ignoredeleted/) { get; set; } | Ottiene o imposta un valore booleano che indica di ignorare il testo all'interno delle revisioni di eliminazione. Il valore predefinito è`falso` . |
| [IgnoreFieldCodes](../../aspose.words.replacing/findreplaceoptions/ignorefieldcodes/) { get; set; } | Ottiene o imposta un valore booleano che indica di ignorare il testo all'interno dei codici di campo. Il valore predefinito è`falso` . |
| [IgnoreFields](../../aspose.words.replacing/findreplaceoptions/ignorefields/) { get; set; } | Ottiene o imposta un valore booleano che indica di ignorare il testo all'interno dei campi. Il valore predefinito è`falso` . |
| [IgnoreFootnotes](../../aspose.words.replacing/findreplaceoptions/ignorefootnotes/) { get; set; } | Ottiene o imposta un valore booleano che indica di ignorare le note a piè di pagina. Il valore predefinito è`falso` . |
| [IgnoreInserted](../../aspose.words.replacing/findreplaceoptions/ignoreinserted/) { get; set; } | Ottiene o imposta un valore booleano che indica di ignorare il testo all'interno delle revisioni di inserimento. Il valore predefinito è`falso` . |
| [IgnoreShapes](../../aspose.words.replacing/findreplaceoptions/ignoreshapes/) { get; set; } | Ottiene o imposta un valore booleano che indica di ignorare le forme all'interno di un testo. |
| [IgnoreStructuredDocumentTags](../../aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/) { get; set; } | Ottiene o imposta un valore booleano che indica di ignorare il contenuto di[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) . Il valore predefinito è`falso` . |
| [LegacyMode](../../aspose.words.replacing/findreplaceoptions/legacymode/) { get; set; } | Ottiene o imposta un valore booleano che indica che viene utilizzato il vecchio algoritmo di ricerca/sostituzione. |
| [MatchCase](../../aspose.words.replacing/findreplaceoptions/matchcase/) { get; set; } | Vero indica un confronto con distinzione tra maiuscole e minuscole, falso indica un confronto senza distinzione tra maiuscole e minuscole. |
| [ReplacementFormat](../../aspose.words.replacing/findreplaceoptions/replacementformat/) { get; set; } | Specifica il formato della sostituzione. Il valore predefinito èText . |
| [ReplacingCallback](../../aspose.words.replacing/findreplaceoptions/replacingcallback/) { get; set; } | Metodo definito dall'utente che viene chiamato prima di ogni occorrenza di sostituzione. |
| [SmartParagraphBreakReplacement](../../aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/) { get; set; } | Ottiene o imposta un valore booleano che indica se è consentito sostituire il paragrafo break quando non esiste un paragrafo gemello successivo. |
| [UseLegacyOrder](../../aspose.words.replacing/findreplaceoptions/uselegacyorder/) { get; set; } | Vero indica che una ricerca di testo viene eseguita in sequenza dall'alto verso il basso considerando le caselle di testo. Il valore predefinito è`falso` . |
| [UseSubstitutions](../../aspose.words.replacing/findreplaceoptions/usesubstitutions/) { get; set; } | Ottiene o imposta un valore booleano che indica se riconoscere e utilizzare le sostituzioni all'interno dei modelli di sostituzione. Il valore predefinito è`falso` . |

## Esempi

Mostra come attivare o disattivare la distinzione tra maiuscole e minuscole quando si esegue un'operazione di ricerca e sostituzione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
FindReplaceOptions options = new FindReplaceOptions();

// Imposta il flag "MatchCase" su "true" per applicare la distinzione tra maiuscole e minuscole durante la ricerca delle stringhe da sostituire.
// Impostare il flag "MatchCase" su "false" per ignorare la distinzione tra maiuscole e minuscole durante la ricerca del testo da sostituire.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

Mostra come attivare o disattivare operazioni di ricerca e sostituzione autonome di sole parole.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
FindReplaceOptions options = new FindReplaceOptions();

// Imposta il flag "FindWholeWordsOnly" su "true" per sostituire il testo trovato se non fa parte di un'altra parola.
// Imposta il flag "FindWholeWordsOnly" su "false" per sostituire tutto il testo, indipendentemente da ciò che lo circonda.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Replacing](../../aspose.words.replacing/)
* assemblea [Aspose.Words](../../)
