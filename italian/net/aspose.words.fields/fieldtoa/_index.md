---
title: FieldToa Class
linktitle: FieldToa
articleTitle: FieldToa
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fields.FieldToa per un'implementazione fluida dei campi TOA. Migliora l'elaborazione dei tuoi documenti con potenti funzionalità oggi stesso!
type: docs
weight: 2930
url: /it/net/aspose.words.fields/fieldtoa/
---
## FieldToa class

Implementa il campo TOA.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class FieldToa : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldToa](fieldtoa/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldtoa/bookmarkname/) { get; set; } | Ottiene o imposta il nome del segnalibro che contrassegna la parte del documento utilizzata per creare la tabella. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [EntryCategory](../../aspose.words.fields/fieldtoa/entrycategory/) { get; set; } | Ottiene o imposta la categoria integrale per le voci incluse nella tabella. |
| [EntrySeparator](../../aspose.words.fields/fieldtoa/entryseparator/) { get; set; } | Ottiene o imposta la sequenza di caratteri utilizzata per separare una voce della tabella delle fonti e il suo numero di pagina. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ottiene un[`FieldFormat`](../fieldformat/)oggetto che fornisce accesso tipizzato alla formattazione del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [PageNumberListSeparator](../../aspose.words.fields/fieldtoa/pagenumberlistseparator/) { get; set; } | Ottiene o imposta la sequenza di caratteri utilizzata per separare due numeri di pagina in un elenco di numeri di pagina. |
| [PageRangeSeparator](../../aspose.words.fields/fieldtoa/pagerangeseparator/) { get; set; } | Ottiene o imposta la sequenza di caratteri utilizzata per separare l'inizio e la fine di un intervallo di pagine. |
| [RemoveEntryFormatting](../../aspose.words.fields/fieldtoa/removeentryformatting/) { get; set; } | Ottiene o imposta se rimuovere la formattazione del testo della voce nel documento dalla voce nella tabella delle fonti. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ottiene o imposta il testo compreso tra il separatore di campo e la fine del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere`null` . |
| [SequenceName](../../aspose.words.fields/fieldtoa/sequencename/) { get; set; } | Ottiene o imposta il nome di una sequenza il cui numero è incluso nel numero di pagina. |
| [SequenceSeparator](../../aspose.words.fields/fieldtoa/sequenceseparator/) { get; set; } | Ottiene o imposta la sequenza di caratteri utilizzata per separare i numeri di sequenza e i numeri di pagina. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ottiene il tipo di campo di Microsoft Word. |
| [UseHeading](../../aspose.words.fields/fieldtoa/useheading/) { get; set; } | Ottiene o imposta se includere l'intestazione di categoria per le voci in una tabella delle autorità. |
| [UsePassim](../../aspose.words.fields/fieldtoa/usepassim/) { get; set; } | Ottiene o imposta se sostituire cinque o più riferimenti di pagina diversi alla stessa autorità con "passim", che viene utilizzato per indicare che una parola o un passaggio si verifica frequentemente nell'opera citata. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è un separatore). Sono inclusi sia il codice di campo che il risultato del campo dei campi figlio. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è separatore). |
| [Remove](../../aspose.words.fields/field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo nodo figlio del suo nodo padre, restituisce il paragrafo padre. Se il campo è già stato rimosso, restituisce`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Esegue l'aggiornamento del campo. Genera un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Esegue un aggiornamento di campo. Genera un'eccezione se il campo è già in fase di aggiornamento. |

## Osservazioni

Crea una tabella delle autorità (vale a dire un elenco dei riferimenti in un documento legale, come i riferimenti a casi, statuti e norme, insieme ai numeri delle pagine in cui compaiono i riferimenti) utilizzando le voci specificate dai campi TA.

## Esempi

Mostra come creare e personalizzare una tabella delle autorità utilizzando i campi TOA e TA.

```csharp
public void FieldTOA()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Inserisci un campo TOA, che creerà una voce per ogni campo TA nel documento,
    // visualizzazione delle citazioni lunghe e dei numeri di pagina per ogni voce.
    FieldToa fieldToa = (FieldToa)builder.InsertField(FieldType.FieldTOA, false);

    // Imposta la categoria di ingresso per la nostra tabella. Questa TOA ora includerà solo i campi TA
    // che hanno un valore corrispondente nella loro proprietà EntryCategory.
    fieldToa.EntryCategory = "1";

    // Inoltre, la categoria della Tabella delle Autorità all'indice 1 è "Casi",
    // che verrà visualizzato come titolo della nostra tabella se impostiamo questa variabile su true.
    fieldToa.UseHeading = true;

    // Possiamo filtrare ulteriormente i campi TA assegnando un segnalibro in modo che siano compresi nei limiti TOA.
    fieldToa.BookmarkName = "MyBookmark";

    // Per impostazione predefinita, viene visualizzata una tabulazione tratteggiata a tutta pagina tra la citazione del campo TA
    // e il suo numero di pagina. Possiamo sostituirlo con qualsiasi testo inseriamo in questa proprietà.
    // L'inserimento di un carattere di tabulazione manterrà la tabulazione originale.
    fieldToa.EntrySeparator = " \t p.";

    // Se abbiamo più voci TA che condividono la stessa citazione lunga,
    // tutti i rispettivi numeri di pagina verranno visualizzati su una riga.
    // Possiamo usare questa proprietà per specificare una stringa che separerà i numeri di pagina.
    fieldToa.PageNumberListSeparator = " & p. ";

    // Possiamo impostarlo su true per far sì che la nostra tabella visualizzi la parola "passim"
    // se ci sono cinque o più numeri di pagina in una riga.
    fieldToa.UsePassim = true;

    // Un campo TA può fare riferimento a un intervallo di pagine.
    // Possiamo specificare una stringa da visualizzare tra il numero di pagina iniziale e quello finale per tali intervalli.
    fieldToa.PageRangeSeparator = " to ";

    // Il formato dei campi TA verrà trasferito nella nostra tabella.
    // Possiamo disattivarlo impostando il flag RemoveEntryFormatting.
    fieldToa.RemoveEntryFormatting = true;
    builder.Font.Color = Color.Green;
    builder.Font.Name = "Arial Black";

    Assert.AreEqual(" TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f", fieldToa.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Questo campo TA non apparirà come voce nel TOA poiché è esterno
    // i limiti del segnalibro specificati dalla proprietà BookmarkName del TOA.
    FieldTA fieldTA = InsertToaEntry(builder, "1", "Source 1");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 1\"", fieldTA.GetFieldCode());

    // Questo campo TA si trova all'interno del segnalibro,
    // ma la categoria della voce non corrisponde a quella della tabella, quindi il campo TA non la includerà.
    builder.StartBookmark("MyBookmark");
    fieldTA = InsertToaEntry(builder, "2", "Source 2");

    // Questa voce apparirà nella tabella.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");

    // Una tabella TOA non visualizza citazioni brevi,
    // ma possiamo usarli come scorciatoia per fare riferimento a nomi sorgente voluminosi a cui fanno riferimento più campi TA.
    fieldTA.ShortCitation = "S.3";

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\s S.3", fieldTA.GetFieldCode());

    // Possiamo formattare il numero di pagina per renderlo grassetto/corsivo utilizzando le seguenti proprietà.
    // Continueremo a vedere questi effetti se impostiamo la tabella in modo che ignori la formattazione.
    fieldTA = InsertToaEntry(builder, "1", "Source 2");
    fieldTA.IsBold = true;
    fieldTA.IsItalic = true;

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 2\" \\b \\i", fieldTA.GetFieldCode());

    // Possiamo configurare i campi TA in modo che le voci TOA facciano riferimento a un intervallo di pagine su cui si estende un segnalibro.
    // Nota che questa voce fa riferimento alla stessa fonte di quella precedente per condividere una riga nella nostra tabella.
    // Questa riga conterrà il numero di pagina della voce sopra e l'intervallo di pagine di questa voce,
    // con l'elenco delle pagine della tabella e i separatori degli intervalli dei numeri di pagina tra i numeri di pagina.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");
    fieldTA.PageRangeBookmarkName = "MyMultiPageBookmark";

    builder.StartBookmark("MyMultiPageBookmark");
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.EndBookmark("MyMultiPageBookmark");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark", fieldTA.GetFieldCode());

    // Se abbiamo abilitato la funzionalità "Passim" della nostra tabella, questa verrà attivata se ci saranno 5 o più voci TA con la stessa origine.
    for (int i = 0; i < 5; i++)
    {
        InsertToaEntry(builder, "1", "Source 4");
    }

    builder.EndBookmark("MyBookmark");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOA.TA.docx");
}

private static FieldTA InsertToaEntry(DocumentBuilder builder, string entryCategory, string longCitation)
{
    FieldTA field = (FieldTA)builder.InsertField(FieldType.FieldTOAEntry, false);
    field.EntryCategory = entryCategory;
    field.LongCitation = longCitation;

    builder.InsertBreak(BreakType.PageBreak);

    return field;
}
```

### Guarda anche

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
