---
title: Field.LocaleId
linktitle: LocaleId
articleTitle: LocaleId
second_title: Aspose.Words per .NET
description: Gestisci la proprietà LocaleId del tuo campo con semplicità. Ottieni o imposta l'LCID per migliorare la localizzazione e l'esperienza utente nelle tue applicazioni.
type: docs
weight: 60
url: /it/net/aspose.words.fields/field/localeid/
---
## Field.LocaleId property

Ottiene o imposta l'LCID del campo.

```csharp
public int LocaleId { get; set; }
```

## Esempi

Mostra come inserire un campo e lavorare con le sue impostazioni locali.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce un campo DATA, quindi stampa la data che verrà visualizzata.
// La formattazione della data è determinata dalla cultura corrente del thread.
Field field = builder.InsertField(@"DATE");
Console.WriteLine($"Today's date, as displayed in the \"{CultureInfo.CurrentCulture.EnglishName}\" culture: {field.Result}");

Assert.AreEqual(1033, field.LocaleId);
// La modifica della cultura del nostro thread avrà un impatto sul risultato del campo DATA.
// Un altro modo per far sì che il campo DATA visualizzi una data in una cultura diversa è utilizzare la sua proprietà LocaleId.
// In questo modo evitiamo di modificare la cultura del thread per ottenere questo effetto.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
CultureInfo de = new CultureInfo("de-DE");
field.LocaleId = de.LCID;
field.Update();

Console.WriteLine($"Today's date, as displayed according to the \"{CultureInfo.GetCultureInfo(field.LocaleId).EnglishName}\" culture: {field.Result}");
```

### Guarda anche

* class [Field](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
