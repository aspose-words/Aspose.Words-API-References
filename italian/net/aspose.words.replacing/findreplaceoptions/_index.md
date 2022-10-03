---
title: FindReplaceOptions
second_title: Aspose.Words per .NET API Reference
description: Specifica le opzioni per le operazioni di ricerca/sostituzione.
type: docs
weight: 4360
url: /it/net/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class

Specifica le opzioni per le operazioni di ricerca/sostituzione.

```csharp
public class FindReplaceOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FindReplaceOptions](findreplaceoptions/#constructor)() | Default_Costruttore |
| [FindReplaceOptions](findreplaceoptions/#constructor_1)(FindReplaceDirection) |  |
| [FindReplaceOptions](findreplaceoptions/#constructor_3)(IReplacingCallback) |  |
| [FindReplaceOptions](findreplaceoptions/#constructor_2)(FindReplaceDirection, IReplacingCallback) |  |

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
| [LegacyMode](../../aspose.words.replacing/findreplaceoptions/legacymode/) { get; set; } | Ottiene o imposta un valore booleano che indica che viene utilizzato il vecchio algoritmo trova/sostituisci. |
| [MatchCase](../../aspose.words.replacing/findreplaceoptions/matchcase/) { get; set; } | True indica il confronto con distinzione tra maiuscole e minuscole, false indica un confronto senza distinzione tra maiuscole e minuscole. |
| [ReplacingCallback](../../aspose.words.replacing/findreplaceoptions/replacingcallback/) { get; set; } | Il metodo definito dall'utente che viene chiamato prima di ogni occorrenza di sostituzione. |
| [SmartParagraphBreakReplacement](../../aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/) { get; set; } | Ottiene o imposta un valore booleano che indica che è consentito sostituire il paragrafo break quando non è presente un paragrafo di pari livello successivo. |
| [UseLegacyOrder](../../aspose.words.replacing/findreplaceoptions/uselegacyorder/) { get; set; } | True indica che una ricerca di testo viene eseguita in sequenza dall'alto verso il basso considerando le caselle di testo. Il valore predefinito è false. |
| [UseSubstitutions](../../aspose.words.replacing/findreplaceoptions/usesubstitutions/) { get; set; } | Ottiene o imposta un valore booleano che indica se riconoscere e utilizzare le sostituzioni all'interno dei modelli di sostituzione. Il valore predefinito è`falso` . |

### Esempi

Mostra come attivare la distinzione tra maiuscole e minuscole durante l'esecuzione di un'operazione di ricerca e sostituzione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Possiamo usare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
FindReplaceOptions options = new FindReplaceOptions();

// Imposta il flag "MatchCase" su "true" per applicare la distinzione tra maiuscole e minuscole mentre trovi le stringhe da sostituire.
// Imposta il flag "MatchCase" su "false" per ignorare il carattere maiuscolo durante la ricerca del testo da sostituire.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

Mostra come attivare o disattivare le operazioni di ricerca e sostituzione di sole parole autonome.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Possiamo usare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
FindReplaceOptions options = new FindReplaceOptions();

// Imposta il flag "FindWholeWordsOnly" su "true" per sostituire il testo trovato se non fa parte di un'altra parola.
// Imposta il flag "FindWholeWordsOnly" su "false" per sostituire tutto il testo indipendentemente dall'ambiente circostante.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Replacing](../../aspose.words.replacing/)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
