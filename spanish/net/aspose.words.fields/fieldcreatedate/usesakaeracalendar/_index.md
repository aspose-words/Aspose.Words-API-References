---
title: FieldCreateDate.UseSakaEraCalendar
linktitle: UseSakaEraCalendar
articleTitle: UseSakaEraCalendar
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldCreateDate UseSakaEraCalendar para administrar fácilmente las configuraciones del calendario de Saka Era en sus aplicaciones para un mejor manejo de las fechas.
type: docs
weight: 30
url: /es/net/aspose.words.fields/fieldcreatedate/usesakaeracalendar/
---
## FieldCreateDate.UseSakaEraCalendar property

Obtiene o establece si se utilizará el calendario de la Era Saka.

```csharp
public bool UseSakaEraCalendar { get; set; }
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
