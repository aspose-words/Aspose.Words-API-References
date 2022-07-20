---
title: SequenceSeparator
second_title: Aspose.Words per .NET API Reference
description: Ottiene o imposta la sequenza di caratteri utilizzata per separare i numeri di sequenza e i numeri di pagina.
type: docs
weight: 90
url: /it/net/aspose.words.fields/fieldtoa/sequenceseparator/
---
## FieldToa.SequenceSeparator property

Ottiene o imposta la sequenza di caratteri utilizzata per separare i numeri di sequenza e i numeri di pagina.

```csharp
public string SequenceSeparator { get; set; }
```

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

* class [FieldToa](../../fieldtoa)
* spazio dei nomi [Aspose.Words.Fields](../../fieldtoa)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
