---
title: FieldDate.UseLunarCalendar
linktitle: UseLunarCalendar
articleTitle: UseLunarCalendar
second_title: Aspose.Words per .NET
description: Ottimizza la gestione delle date con la proprietà UseLunarCalendar di FieldDate. Passa facilmente dal calendario lunare Hijri a quello ebraico per funzionalità avanzate.
type: docs
weight: 30
url: /it/net/aspose.words.fields/fielddate/uselunarcalendar/
---
## FieldDate.UseLunarCalendar property

Ottiene o imposta se utilizzare il calendario lunare Hijri o quello ebraico.

```csharp
public bool UseLunarCalendar { get; set; }
```

## Esempi

Mostra come utilizzare i campi DATA per visualizzare le date in base a diversi tipi di calendari.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Se vogliamo che il testo del documento visualizzi sempre la data corretta, possiamo utilizzare un campo DATA.
// Di seguito sono riportati tre tipi di calendari culturali che un campo DATA può utilizzare per visualizzare una data.
// 1 - Calendario lunare islamico:
FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLunarCalendar = true;
Assert.AreEqual(" DATE  \\h", field.GetFieldCode());
builder.Writeln();

// 2 - Calendario di Umm al-Qura:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseUmAlQuraCalendar = true;
Assert.AreEqual(" DATE  \\u", field.GetFieldCode());
builder.Writeln();

// 3 - Calendario nazionale indiano:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseSakaEraCalendar = true;
Assert.AreEqual(" DATE  \\s", field.GetFieldCode());
builder.Writeln();

// Inserire un campo DATA e impostare il suo tipo di calendario su quello utilizzato per ultimo dall'applicazione host.
// In Microsoft Word, il tipo sarà quello utilizzato più di recente nella finestra di dialogo Inserisci -> Testo -> Data e ora.
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLastFormat = true;
Assert.AreEqual(" DATE  \\l", field.GetFieldCode());
builder.Writeln();

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATE.docx");
```

### Guarda anche

* class [FieldDate](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
