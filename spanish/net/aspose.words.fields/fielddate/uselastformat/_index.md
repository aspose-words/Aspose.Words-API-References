---
title: FieldDate.UseLastFormat
linktitle: UseLastFormat
articleTitle: UseLastFormat
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad FieldDate UseLastFormat mejora su flujo de trabajo al conservar el último formato de fecha utilizado para una integración perfecta en sus aplicaciones.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fielddate/uselastformat/
---
## FieldDate.UseLastFormat property

Obtiene o establece si se debe utilizar un formato utilizado por última vez por la aplicación de alojamiento al insertar un nuevo campo FECHA.

```csharp
public bool UseLastFormat { get; set; }
```

## Ejemplos

Muestra cómo utilizar los campos FECHA para mostrar fechas según diferentes tipos de calendarios.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si queremos que el texto del documento siempre muestre la fecha correcta, podemos utilizar un campo FECHA.
// A continuación se muestran tres tipos de calendarios culturales que un campo FECHA puede utilizar para mostrar una fecha.
// 1 - Calendario lunar islámico:
FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLunarCalendar = true;
Assert.AreEqual(" DATE  \\h", field.GetFieldCode());
builder.Writeln();

// 2 - Calendario de Umm al-Qura:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseUmAlQuraCalendar = true;
Assert.AreEqual(" DATE  \\u", field.GetFieldCode());
builder.Writeln();

// 3 - Calendario Nacional Indio:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseSakaEraCalendar = true;
Assert.AreEqual(" DATE  \\s", field.GetFieldCode());
builder.Writeln();

// Inserte un campo FECHA y establezca su tipo de calendario al último utilizado por la aplicación host.
// En Microsoft Word, el tipo será el utilizado más recientemente en el cuadro de diálogo Insertar -> Texto -> Fecha y hora.
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLastFormat = true;
Assert.AreEqual(" DATE  \\l", field.GetFieldCode());
builder.Writeln();

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATE.docx");
```

### Ver también

* class [FieldDate](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
