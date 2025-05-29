---
title: FieldDate.UseUmAlQuraCalendar
linktitle: UseUmAlQuraCalendar
articleTitle: UseUmAlQuraCalendar
second_title: Aspose.Words para .NET
description: Descubre la propiedad FieldDate UseUmAlQuraCalendar para gestionar fácilmente las fechas con el calendario UmalQura. ¡Mejora tu gestión de fechas hoy mismo!
type: docs
weight: 50
url: /es/net/aspose.words.fields/fielddate/useumalquracalendar/
---
## FieldDate.UseUmAlQuraCalendar property

Obtiene o establece si se debe utilizar el calendario Um-al-Qura.

```csharp
public bool UseUmAlQuraCalendar { get; set; }
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
