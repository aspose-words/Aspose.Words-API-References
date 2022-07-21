---
title: FieldToa
second_title: Aspose.Words per .NET API Reference
description: Implementa il campo TOA.
type: docs
weight: 2370
url: /it/net/aspose.words.fields/fieldtoa/
---
## FieldToa class

Implementa il campo TOA.

```csharp
public class FieldToa : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldToa](fieldtoa)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldtoa/bookmarkname) { get; set; } | Ottiene o imposta il nome del segnalibro che contrassegna la parte del documento utilizzata per creare la tabella. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [EntryCategory](../../aspose.words.fields/fieldtoa/entrycategory) { get; set; } | Ottiene o imposta la categoria integrale per le voci incluse nella tabella. |
| [EntrySeparator](../../aspose.words.fields/fieldtoa/entryseparator) { get; set; } | Ottiene o imposta la sequenza di caratteri utilizzata per separare una tabella di voci di autorizzazioni e il relativo numero di pagina. |
| [Format](../../aspose.words.fields/field/format) { get; } | Ottiene a[`FieldFormat`](../fieldformat) oggetto che fornisce l'accesso digitato alla formattazione del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolarne il risultato). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [PageNumberListSeparator](../../aspose.words.fields/fieldtoa/pagenumberlistseparator) { get; set; } | Ottiene o imposta la sequenza di caratteri utilizzata per separare due numeri di pagina in un elenco di numeri di pagina. |
| [PageRangeSeparator](../../aspose.words.fields/fieldtoa/pagerangeseparator) { get; set; } | Ottiene o imposta la sequenza di caratteri utilizzata per separare l'inizio e la fine di un intervallo di pagine. |
| [RemoveEntryFormatting](../../aspose.words.fields/fieldtoa/removeentryformatting) { get; set; } | Ottiene o imposta se rimuovere la formattazione del testo della voce nel documento dalla voce nella tabella delle autorizzazioni. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Ottiene o imposta il testo che si trova tra il separatore di campo e la fine del campo. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere nullo. |
| [SequenceName](../../aspose.words.fields/fieldtoa/sequencename) { get; set; } | Ottiene o imposta il nome di una sequenza il cui numero è incluso nel numero di pagina. |
| [SequenceSeparator](../../aspose.words.fields/fieldtoa/sequenceseparator) { get; set; } | Ottiene o imposta la sequenza di caratteri utilizzata per separare i numeri di sequenza e i numeri di pagina. |
| [Start](../../aspose.words.fields/field/start) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Ottiene il tipo di campo di Microsoft Word. |
| [UseHeading](../../aspose.words.fields/fieldtoa/useheading) { get; set; } | Ottiene o imposta se includere l'intestazione di categoria per le voci in una tabella di autorizzazioni. |
| [UsePassim](../../aspose.words.fields/fieldtoa/usepassim) { get; set; } | Ottiene o imposta se sostituire cinque o più diversi riferimenti di pagina alla stessa autorità con "passim", utilizzato per indicare che una parola o un passaggio ricorre frequentemente nell'opera citata. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non è presente alcun separatore). Sono inclusi sia il codice campo che il risultato campo dei campi figlio. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è un separatore). |
| [Remove](../../aspose.words.fields/field/remove)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del suo nodo padre, restituisce il suo paragrafo padre. Se il campo è già stato rimosso, ritorna **nullo** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update)() | Esegue l'aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update)(bool) | Esegue un aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |

### Osservazioni

Costruisce una tabella delle autorità (cioè un elenco dei riferimenti in un documento legale, come riferimenti a casi, statuti e regole, insieme ai numeri delle pagine su cui compaiono i riferimenti) utilizzando le voci specificate da TA campi.

### Esempi

Mostra come creare e personalizzare una tabella di autorizzazioni utilizzando i campi TOA e TA.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Inserisci un campo TOA, che creerà una voce per ogni campo TA nel documento,
    // visualizza citazioni lunghe e numeri di pagina per ogni voce.
    FieldToa fieldToa = (FieldToa)builder.InsertField(FieldType.FieldTOA, false);

    // Imposta la categoria di ingresso per il nostro tavolo. Questo TOA ora includerà solo i campi TA
    // che hanno un valore corrispondente nella loro proprietà EntryCategory.
    fieldToa.EntryCategory = "1";

    // Inoltre, la categoria Table of Authorities all'indice 1 è "Casi",
    // che apparirà come titolo della nostra tabella se impostiamo questa variabile su true.
    fieldToa.UseHeading = true;

    // Possiamo filtrare ulteriormente i campi TA nominando un segnalibro che dovranno rientrare nei limiti TOA.
    fieldToa.BookmarkName = "MyBookmark";

    // Per impostazione predefinita, tra la citazione del campo AT viene visualizzata una scheda con linea tratteggiata a livello di pagina
    // e il suo numero di pagina. Possiamo sostituirlo con qualsiasi testo che inseriamo in questa proprietà.
    // L'inserimento di un carattere di tabulazione conserverà la tabulazione originale.
    fieldToa.EntrySeparator = " \t p.";

    // Se abbiamo più voci TA che condividono la stessa citazione lunga,
    // tutti i rispettivi numeri di pagina verranno visualizzati su una riga.
    // Possiamo usare questa proprietà per specificare una stringa che separerà i loro numeri di pagina.
    fieldToa.PageNumberListSeparator = " & p. ";

    // Possiamo impostarlo su true per fare in modo che la nostra tabella visualizzi la parola "passim"
    // se ci sono cinque o più numeri di pagina in una riga.
    fieldToa.UsePassim = true;

    // Un campo TA può fare riferimento a un intervallo di pagine.
    // Possiamo specificare qui una stringa da visualizzare tra i numeri di pagina iniziale e finale per tali intervalli.
    fieldToa.PageRangeSeparator = " to ";

    // Il formato dei campi TA verrà trasferito nella nostra tabella.
    // Possiamo disabilitarlo impostando il flag RemoveEntryFormatting.
    fieldToa.RemoveEntryFormatting = true;
    builder.Font.Color = Color.Green;
    builder.Font.Name = "Arial Black";

    Assert.AreEqual(" TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f", fieldToa.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Questo campo TA non apparirà come voce nel TOA poiché è esterno
    // i limiti del segnalibro specificati dalla proprietà BookmarkName di TOA.
    FieldTA fieldTA = InsertToaEntry(builder, "1", "Source 1");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 1\"", fieldTA.GetFieldCode());

    // Questo campo TA è all'interno del segnalibro,
    // ma la categoria della voce non corrisponde a quella della tabella, quindi il campo TA non la includerà.
    builder.StartBookmark("MyBookmark");
    fieldTA = InsertToaEntry(builder, "2", "Source 2");

    // Questa voce apparirà nella tabella.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");

    // Una tabella TOA non mostra citazioni brevi,
    // ma possiamo usarli come scorciatoia per fare riferimento a nomi di sorgenti voluminosi a cui fanno riferimento più campi TA.
    fieldTA.ShortCitation = "S.3";

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\s S.3", fieldTA.GetFieldCode());

    // Possiamo formattare il numero di pagina in grassetto/corsivo usando le seguenti proprietà.
    // Vedremo ancora questi effetti se impostiamo la nostra tabella per ignorare la formattazione.
    fieldTA = InsertToaEntry(builder, "1", "Source 2");
    fieldTA.IsBold = true;
    fieldTA.IsItalic = true;

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 2\" \\b \\i", fieldTA.GetFieldCode());

    // Possiamo configurare i campi TA in modo che le loro voci TOA facciano riferimento a un intervallo di pagine su cui si estende un segnalibro.
    // Nota che questa voce si riferisce alla stessa fonte di quella sopra per condividere una riga nella nostra tabella.
    // Questa riga avrà il numero di pagina della voce sopra e l'intervallo di pagine di questa voce,
    // con l'elenco di pagine della tabella e i separatori di intervalli di numeri di pagina tra i numeri di pagina.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");
    fieldTA.PageRangeBookmarkName = "MyMultiPageBookmark";

    builder.StartBookmark("MyMultiPageBookmark");
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.EndBookmark("MyMultiPageBookmark");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark", fieldTA.GetFieldCode());

    // Se abbiamo abilitato la funzione "Passim" della nostra tabella, avere 5 o più voci TA con la stessa fonte la invocherà.
    for (int i = 0; i < 5; i++)
    {
        InsertToaEntry(builder, "1", "Source 4");
    }

    builder.EndBookmark("MyBookmark");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOA.TA.docx");

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

* class [Field](../field)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
