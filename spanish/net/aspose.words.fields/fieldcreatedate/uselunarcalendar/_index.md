---
title: FieldCreateDate.UseLunarCalendar
linktitle: UseLunarCalendar
articleTitle: UseLunarCalendar
second_title: Aspose.Words para .NET
description: Gestione fácilmente los formatos de fecha con la propiedad FieldCreateDate UseLunarCalendar. Elija entre los calendarios lunares hijri y hebreo para una programación precisa.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldcreatedate/uselunarcalendar/
---
## FieldCreateDate.UseLunarCalendar property

Obtiene o establece si se debe utilizar el calendario lunar hijri o el calendario lunar hebreo.

```csharp
public bool UseLunarCalendar { get; set; }
```

## Ejemplos

Muestra cómo utilizar el campo CREATEDATE para mostrar la fecha y hora de creación del documento.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was created:");

//Podemos utilizar el campo CREATEDATE para mostrar la fecha y hora de creación del documento.
// A continuación se muestran tres tipos de calendario diferentes según los cuales el campo CREATEDATE puede mostrar la fecha/hora.
// 1 - Calendario lunar islámico:
builder.Write("According to the Lunar Calendar - ");
FieldCreateDate field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" CREATEDATE  \\h", field.GetFieldCode());

// 2 - Calendario de Umm al-Qura:
builder.Write("\nAccording to the Umm al-Qura Calendar - ");
field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" CREATEDATE  \\u", field.GetFieldCode());

// 3 - Calendario Nacional Indio:
builder.Write("\nAccording to the Indian National Calendar - ");
field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" CREATEDATE  \\s", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CREATEDATE.docx");
```

### Ver también

* class [FieldCreateDate](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
