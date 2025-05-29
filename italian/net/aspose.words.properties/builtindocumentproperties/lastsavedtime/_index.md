---
title: BuiltInDocumentProperties.LastSavedTime
linktitle: LastSavedTime
articleTitle: LastSavedTime
second_title: Aspose.Words per .NET
description: Scopri la proprietà LastSavedTime di BuiltInDocumentProperties per monitorare facilmente l'ora dell'ultimo salvataggio del tuo documento in UTC. Migliora la tua gestione dei documenti oggi stesso!
type: docs
weight: 180
url: /it/net/aspose.words.properties/builtindocumentproperties/lastsavedtime/
---
## BuiltInDocumentProperties.LastSavedTime property

Ottiene o imposta l'ora dell'ultimo salvataggio in UTC.

```csharp
public DateTime LastSavedTime { get; set; }
```

## Osservazioni

Per i documenti originati dal formato RTF questa proprietà restituisce l'ora locale dell'ultima operazione di salvataggio.

Aspose.Words non aggiorna questa proprietà.

## Esempi

Mostra come lavorare con le proprietà del documento nella categoria "Origine".

```csharp
// Apriamo un documento che abbiamo creato e modificato utilizzando Microsoft Word.
Document doc = new Document(MyDir + "Properties.docx");
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// Le seguenti proprietà integrate contengono informazioni relative alla creazione e alla modifica di questo documento.
// Possiamo fare clic con il pulsante destro del mouse su questo documento in Esplora risorse e trovare
// queste proprietà tramite la categoria "Proprietà" -> "Dettagli" -> "Origine".
// Campi come PRINTDATE ed EDITTIME possono visualizzare questi valori nel corpo del documento.
Console.WriteLine($"Created using {properties.NameOfApplication}, on {properties.CreatedTime}");
Console.WriteLine($"Minutes spent editing: {properties.TotalEditingTime}");
Console.WriteLine($"Date/time last printed: {properties.LastPrinted}");
Console.WriteLine($"Template document: {properties.Template}");

// Possiamo anche modificare i valori delle proprietà integrate.
properties.Company = "Doe Ltd.";
properties.Manager = "Jane Doe";
properties.Version = 5;
properties.RevisionNumber++;

// Microsoft Word aggiorna automaticamente le seguenti proprietà quando salviamo il documento.
// Per utilizzare queste proprietà con Aspose.Words, dovremo impostare manualmente i relativi valori.
properties.LastSavedBy = "John Doe";
properties.LastSavedTime = DateTime.Now;

// Possiamo fare clic con il pulsante destro del mouse su questo documento in Esplora risorse e trovare these properties in "Properties" -> "Details" -> "Origin".
doc.Save(ArtifactsDir + "DocumentProperties.Origin.docx");
```

Mostra come utilizzare il campo SAVEDATE per visualizzare la data/ora dell'operazione di salvataggio più recente del documento eseguita tramite Microsoft Word.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was last saved:");

// Possiamo utilizzare il campo SAVEDATE per visualizzare la data e l'ora dell'ultima operazione di salvataggio sul documento.
// L'operazione di salvataggio a cui si riferiscono questi campi è il salvataggio manuale in un'applicazione come Microsoft Word,
// non il metodo Save del documento.
// Di seguito sono riportati tre diversi tipi di calendario in base ai quali il campo SAVEDATE può visualizzare la data/ora.
// 1 - Calendario lunare islamico:
builder.Write("According to the Lunar Calendar - ");
FieldSaveDate field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" SAVEDATE  \\h", field.GetFieldCode());

// 2 - Calendario di Umm al-Qura:
builder.Write("\nAccording to the Umm al-Qura calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\u", field.GetFieldCode());

// 3 - Calendario nazionale indiano:
builder.Write("\nAccording to the Indian National calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\s", field.GetFieldCode());

// I campi SAVEDATE ricavano i loro valori di data/ora dalla proprietà integrata LastSavedTime.
// Il metodo Save del documento non aggiornerà questo valore, ma possiamo comunque aggiornarlo manualmente.
doc.BuiltInDocumentProperties.LastSavedTime = DateTime.Now;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SAVEDATE.docx");
```

### Guarda anche

* class [BuiltInDocumentProperties](../)
* spazio dei nomi [Aspose.Words.Properties](../../../aspose.words.properties/)
* assemblea [Aspose.Words](../../../)
