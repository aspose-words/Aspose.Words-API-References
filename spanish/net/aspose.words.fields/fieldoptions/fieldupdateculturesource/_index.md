---
title: FieldOptions.FieldUpdateCultureSource
linktitle: FieldUpdateCultureSource
articleTitle: FieldUpdateCultureSource
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad FieldUpdateCultureSource mejora el formato del resultado del campo al especificar la cultura deseada para lograr una claridad y facilidad de uso óptimas.
type: docs
weight: 110
url: /es/net/aspose.words.fields/fieldoptions/fieldupdateculturesource/
---
## FieldOptions.FieldUpdateCultureSource property

Especifica qué cultura utilizar para formatear el resultado del campo.

```csharp
public FieldUpdateCultureSource FieldUpdateCultureSource { get; set; }
```

## Observaciones

De forma predeterminada, se utiliza la cultura del hilo actual.

Esta configuración afecta únicamente a los campos de fecha y hora con el modificador de formato \\@.

## Ejemplos

Muestra cómo especificar la fuente de la cultura utilizada para el formato de fecha durante una actualización de campo o una combinación de correspondencia.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar dos campos de combinación con configuración regional alemana.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Establezca la cultura actual en inglés de EE. UU. después de conservar su valor original en una variable.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Esta fusión utilizará la cultura del hilo actual para formatear la fecha, inglés de EE. UU.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Configurar la siguiente fusión para obtener su valor cultural del código de campo. El valor de esa cultura será alemán.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// El primer resultado de la fusión contiene una fecha formateada en inglés, mientras que el segundo está en alemán.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Restaurar la cultura original del hilo.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Ver también

* enum [FieldUpdateCultureSource](../../fieldupdateculturesource/)
* class [FieldOptions](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
