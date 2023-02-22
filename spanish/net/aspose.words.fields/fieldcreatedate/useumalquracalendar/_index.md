---
title: FieldCreateDate.UseUmAlQuraCalendar
second_title: Referencia de API de Aspose.Words para .NET
description: FieldCreateDate propiedad. Obtiene o establece si usar el calendario UmalQura.
type: docs
weight: 40
url: /es/net/aspose.words.fields/fieldcreatedate/useumalquracalendar/
---
## FieldCreateDate.UseUmAlQuraCalendar property

Obtiene o establece si usar el calendario Um-al-Qura.

```csharp
public bool UseUmAlQuraCalendar { get; set; }
```

### Ejemplos

Muestra cómo usar el campo CREATEDATE para mostrar la fecha/hora de creación del documento.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was created:");

// Podemos usar el campo CREATEDATE para mostrar la fecha y hora de la creación del documento.
// A continuación se muestran tres tipos de calendario diferentes según los cuales el campo CREATEDATE puede mostrar la fecha/hora.
// 1 - Calendario Lunar Islámico:
builder.Write("According to the Lunar Calendar - ");
FieldCreateDate field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" CREATEDATE  \\h", field.GetFieldCode());

// 2 - Calendario Umm al-Qura:
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
* espacio de nombres [Aspose.Words.Fields](../../fieldcreatedate/)
* asamblea [Aspose.Words](../../../)


