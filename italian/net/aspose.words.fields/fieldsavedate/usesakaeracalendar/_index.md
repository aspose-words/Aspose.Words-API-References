---
title: FieldSaveDate.UseSakaEraCalendar
linktitle: UseSakaEraCalendar
articleTitle: UseSakaEraCalendar
second_title: Aspose.Words per .NET
description: Gestisci le date senza sforzo con la funzione Calendario Saka Era di FieldSaveDate. Attiva e disattiva facilmente le impostazioni per un monitoraggio e un'organizzazione ottimizzati delle date.
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldsavedate/usesakaeracalendar/
---
## FieldSaveDate.UseSakaEraCalendar property

Ottiene o imposta se utilizzare il calendario dell'era Saka.

```csharp
public bool UseSakaEraCalendar { get; set; }
```

## Esempi

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

* class [FieldSaveDate](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
