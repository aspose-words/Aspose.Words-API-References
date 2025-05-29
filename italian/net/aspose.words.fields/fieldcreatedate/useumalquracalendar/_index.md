---
title: FieldCreateDate.UseUmAlQuraCalendar
linktitle: UseUmAlQuraCalendar
articleTitle: UseUmAlQuraCalendar
second_title: Aspose.Words per .NET
description: Gestisci i formati delle date senza sforzo con la proprietà FieldCreateDate UseUmAlQuraCalendar. Passa al calendario UmAlQura per una gestione precisa delle date.
type: docs
weight: 40
url: /it/net/aspose.words.fields/fieldcreatedate/useumalquracalendar/
---
## FieldCreateDate.UseUmAlQuraCalendar property

Ottiene o imposta se utilizzare il calendario Um-al-Qura.

```csharp
public bool UseUmAlQuraCalendar { get; set; }
```

## Esempi

Mostra come utilizzare il campo CREATEDATE per visualizzare la data/ora di creazione del documento.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was created:");

// Possiamo utilizzare il campo CREATEDATE per visualizzare la data e l'ora di creazione del documento.
// Di seguito sono riportati tre diversi tipi di calendario in base ai quali il campo CREATEDATE può visualizzare la data/ora.
// 1 - Calendario lunare islamico:
builder.Write("According to the Lunar Calendar - ");
FieldCreateDate field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" CREATEDATE  \\h", field.GetFieldCode());

// 2 - Calendario di Umm al-Qura:
builder.Write("\nAccording to the Umm al-Qura Calendar - ");
field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" CREATEDATE  \\u", field.GetFieldCode());

// 3 - Calendario nazionale indiano:
builder.Write("\nAccording to the Indian National Calendar - ");
field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" CREATEDATE  \\s", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CREATEDATE.docx");
```

### Guarda anche

* class [FieldCreateDate](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
