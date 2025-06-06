---
title: FieldDate.UseLastFormat
linktitle: UseLastFormat
articleTitle: UseLastFormat
second_title: Aspose.Words per .NET
description: Scopri come la proprietà UseLastFormat di FieldDate migliora il tuo flusso di lavoro mantenendo l'ultimo formato di data utilizzato per un'integrazione perfetta nelle tue applicazioni.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fielddate/uselastformat/
---
## FieldDate.UseLastFormat property

Ottiene o imposta se utilizzare un formato utilizzato per ultimo dall'applicazione di hosting quando si inserisce un nuovo campo DATA.

```csharp
public bool UseLastFormat { get; set; }
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
