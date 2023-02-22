---
title: FieldDate.UseLunarCalendar
second_title: Referencia de API de Aspose.Words para .NET
description: FieldDate propiedad. Obtiene o establece si se usa el calendario Lunar Hijri o el calendario Lunar Hebreo.
type: docs
weight: 30
url: /es/net/aspose.words.fields/fielddate/uselunarcalendar/
---
## FieldDate.UseLunarCalendar property

Obtiene o establece si se usa el calendario Lunar Hijri o el calendario Lunar Hebreo.

```csharp
public bool UseLunarCalendar { get; set; }
```

### Ejemplos

Muestra cómo usar los campos de FECHA para mostrar fechas de acuerdo con diferentes tipos de calendarios.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si queremos que el texto del documento muestre siempre la fecha correcta, podemos usar un campo FECHA.
// A continuación se muestran tres tipos de calendarios culturales que un campo FECHA puede usar para mostrar una fecha.
// 1 - Calendario Lunar Islámico:
FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLunarCalendar = true;
Assert.AreEqual(" DATE  \\h", field.GetFieldCode());
builder.Writeln();

// 2 - Calendario Umm al-Qura:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseUmAlQuraCalendar = true;
Assert.AreEqual(" DATE  \\u", field.GetFieldCode());
builder.Writeln();

// 3 - Calendario Nacional Indio:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseSakaEraCalendar = true;
Assert.AreEqual(" DATE  \\s", field.GetFieldCode());
builder.Writeln();

// Inserte un campo de FECHA y establezca su tipo de calendario en el último utilizado por la aplicación host.
// En Microsoft Word, el tipo será el utilizado más recientemente en Insertar -> Texto -> Cuadro de diálogo Fecha y hora.
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLastFormat = true;
Assert.AreEqual(" DATE  \\l", field.GetFieldCode());
builder.Writeln();

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATE.docx");
```

### Ver también

* class [FieldDate](../)
* espacio de nombres [Aspose.Words.Fields](../../fielddate/)
* asamblea [Aspose.Words](../../../)


