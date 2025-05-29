---
title: FieldPrintDate.UseSakaEraCalendar
linktitle: UseSakaEraCalendar
articleTitle: UseSakaEraCalendar
second_title: Aspose.Words per .NET
description: Gestisci i tuoi appuntamenti senza sforzo con la funzione Calendario Saka Era di FieldPrintDate. Attivala facilmente per un'integrazione perfetta e un'esperienza utente migliorata.
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldprintdate/usesakaeracalendar/
---
## FieldPrintDate.UseSakaEraCalendar property

Ottiene o imposta se utilizzare il calendario dell'era Saka.

```csharp
public bool UseSakaEraCalendar { get; set; }
```

## Esempi

Mostra i campi PRINTDATE letti.

```csharp
Document doc = new Document(MyDir + "Field sample - PRINTDATE.docx");

// Quando un documento viene stampato da una stampante o stampato come PDF (ma non esportato in PDF),
// I campi PRINTDATE visualizzeranno la data/ora dell'operazione di stampa.
// Se non è stata eseguita alcuna stampa, in questi campi verrà visualizzato "0/0/0000".
FieldPrintDate field = (FieldPrintDate)doc.Range.Fields[0];

Assert.AreEqual("3/25/2020 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE ", field.GetFieldCode());

// Di seguito sono riportati tre diversi tipi di calendario in base ai quali viene utilizzato il campo PRINTDATE
// può visualizzare la data e l'ora dell'ultima operazione di stampa.
// 1 - Calendario lunare islamico:
field = (FieldPrintDate)doc.Range.Fields[1];

Assert.True(field.UseLunarCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\h", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[2];

// 2 - Calendario di Umm al-Qura:
Assert.True(field.UseUmAlQuraCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\u", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[3];

// 3 - Calendario nazionale indiano:
Assert.True(field.UseSakaEraCalendar);
Assert.AreEqual("1/5/1942 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\s", field.GetFieldCode());
```

### Guarda anche

* class [FieldPrintDate](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
