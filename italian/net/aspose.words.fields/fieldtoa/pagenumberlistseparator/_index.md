---
title: FieldToa.PageNumberListSeparator
linktitle: PageNumberListSeparator
articleTitle: PageNumberListSeparator
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldToa PageNumberListSeparator per personalizzare gli elenchi dei numeri di pagina con il tuo separatore preferito. Migliora la leggibilità del tuo documento oggi stesso!
type: docs
weight: 50
url: /it/net/aspose.words.fields/fieldtoa/pagenumberlistseparator/
---
## FieldToa.PageNumberListSeparator property

Ottiene o imposta la sequenza di caratteri utilizzata per separare due numeri di pagina in un elenco di numeri di pagina.

```csharp
public string PageNumberListSeparator { get; set; }
```

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

* class [FieldToa](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
