---
title: FieldSaveDate.UseUmAlQuraCalendar
linktitle: UseUmAlQuraCalendar
articleTitle: UseUmAlQuraCalendar
second_title: Aspose.Words para .NET
description: Gestione sus fechas fácilmente con la propiedad FieldSaveDate. Active y desactive fácilmente el calendario de UmalQura para optimizar la programación y la planificación.
type: docs
weight: 40
url: /es/net/aspose.words.fields/fieldsavedate/useumalquracalendar/
---
## FieldSaveDate.UseUmAlQuraCalendar property

Obtiene o establece si se debe utilizar el calendario Um-al-Qura.

```csharp
public bool UseUmAlQuraCalendar { get; set; }
```

## Ejemplos

Muestra cómo utilizar el campo SAVEDATE para mostrar la fecha y hora de la operación de guardado más reciente del documento realizada con Microsoft Word.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was last saved:");

//Podemos utilizar el campo SAVEDATE para mostrar la fecha y hora de la última operación de guardado en el documento.
// La operación de guardado a la que se refieren estos campos es el guardado manual en una aplicación como Microsoft Word,
// no es el método Guardar del documento.
// A continuación se muestran tres tipos de calendario diferentes según los cuales el campo SAVEDATE puede mostrar la fecha/hora.
// 1 - Calendario lunar islámico:
builder.Write("According to the Lunar Calendar - ");
FieldSaveDate field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" SAVEDATE  \\h", field.GetFieldCode());

// 2 - Calendario de Umm al-Qura:
builder.Write("\nAccording to the Umm al-Qura calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\u", field.GetFieldCode());

// 3 - Calendario nacional indio:
builder.Write("\nAccording to the Indian National calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\s", field.GetFieldCode());

// Los campos SAVEDATE obtienen sus valores de fecha y hora de la propiedad incorporada LastSavedTime.
// El método Guardar del documento no actualizará este valor, pero aún podemos actualizarlo manualmente.
doc.BuiltInDocumentProperties.LastSavedTime = DateTime.Now;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SAVEDATE.docx");
```

### Ver también

* class [FieldSaveDate](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
