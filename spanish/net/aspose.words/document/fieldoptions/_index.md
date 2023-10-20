---
title: Document.FieldOptions
linktitle: FieldOptions
articleTitle: FieldOptions
second_title: Aspose.Words para .NET
description: Document FieldOptions propiedad. Obtiene unFieldOptions objeto que representa opciones para controlar el manejo de campos en el documento en C#.
type: docs
weight: 120
url: /es/net/aspose.words/document/fieldoptions/
---
## Document.FieldOptions property

Obtiene un[`FieldOptions`](../../../aspose.words.fields/fieldoptions/) objeto que representa opciones para controlar el manejo de campos en el documento.

```csharp
public FieldOptions FieldOptions { get; }
```

## Ejemplos

Muestra cómo especificar el origen de la referencia cultural utilizada para el formato de fecha durante una actualización de campo o combinación de correspondencia.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta dos campos combinados con configuración regional alemana.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Establece la cultura actual en inglés de EE. UU. después de preservar su valor original en una variable.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Esta combinación utilizará la cultura del hilo actual para formatear la fecha, inglés de EE. UU.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Configure la siguiente combinación para obtener su valor cultural del código de campo. El valor de esa cultura será el alemán.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// El primer resultado de la fusión contiene una fecha formateada en inglés, mientras que el segundo está en alemán.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Restaura la cultura original del hilo.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Ver también

* class [FieldOptions](../../../aspose.words.fields/fieldoptions/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
