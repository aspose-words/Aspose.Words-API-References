---
title: FieldPrintDate.UseLunarCalendar
linktitle: UseLunarCalendar
articleTitle: UseLunarCalendar
second_title: Aspose.Words para .NET
description: Gestione fechas fácilmente con la propiedad FieldPrintDate UseLunarCalendar. Alterne fácilmente entre los calendarios lunares hijri y hebreo para una integración perfecta.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldprintdate/uselunarcalendar/
---
## FieldPrintDate.UseLunarCalendar property

Obtiene o establece si se debe utilizar el calendario lunar hijri o el calendario lunar hebreo.

```csharp
public bool UseLunarCalendar { get; set; }
```

## Ejemplos

Muestra los campos PRINTDATE leídos.

```csharp
Document doc = new Document(MyDir + "Field sample - PRINTDATE.docx");

// Cuando un documento se imprime mediante una impresora o se imprime como PDF (pero no se exporta a PDF),
// Los campos PRINTDATE mostrarán la fecha y hora de la operación de impresión.
// Si no se ha realizado ninguna impresión, estos campos mostrarán "0/0/0000".
FieldPrintDate field = (FieldPrintDate)doc.Range.Fields[0];

Assert.AreEqual("3/25/2020 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE ", field.GetFieldCode());

// A continuación se muestran tres tipos de calendario diferentes según los cuales se utiliza el campo PRINTDATE
// Puede mostrar la fecha y hora de la última operación de impresión.
// 1 - Calendario lunar islámico:
field = (FieldPrintDate)doc.Range.Fields[1];

Assert.True(field.UseLunarCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\h", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[2];

// 2 - Calendario de Umm al-Qura:
Assert.True(field.UseUmAlQuraCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\u", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[3];

// 3 - Calendario Nacional Indio:
Assert.True(field.UseSakaEraCalendar);
Assert.AreEqual("1/5/1942 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\s", field.GetFieldCode());
```

### Ver también

* class [FieldPrintDate](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
