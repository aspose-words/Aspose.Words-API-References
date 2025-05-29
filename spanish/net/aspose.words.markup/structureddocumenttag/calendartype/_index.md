---
title: StructuredDocumentTag.CalendarType
linktitle: CalendarType
articleTitle: CalendarType
second_title: Aspose.Words para .NET
description: Descubre la propiedad StructuredDocumentTag CalendarType para personalizar tu tipo de calendario SDT. ¡Mejora tus documentos con opciones de calendario personalizadas!
type: docs
weight: 50
url: /es/net/aspose.words.markup/structureddocumenttag/calendartype/
---
## StructuredDocumentTag.CalendarType property

Especifica el tipo de calendario para este**TED** . El valor predeterminado esDefault

```csharp
public SdtCalendarType CalendarType { get; set; }
```

## Observaciones

El acceso a esta propiedad sólo funcionará paraDate Tipo SDT.

Para todos los demás tipos de SDT se producirá una excepción.

## Ejemplos

Muestra cómo solicitar al usuario que ingrese una fecha con una etiqueta de documento estructurado.

```csharp
Document doc = new Document();

// Inserte una etiqueta de documento estructurado que solicite al usuario que ingrese una fecha.
// En Microsoft Word, este elemento se conoce como "control de contenido del selector de fecha".
// Cuando hacemos clic en la flecha en el extremo derecho de esta etiqueta en Microsoft Word,
//Veremos una ventana emergente en forma de calendario en el que podemos hacer clic.
//Podemos usar esa ventana emergente para seleccionar una fecha que se mostrará en la etiqueta.
StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.Date, MarkupLevel.Inline);

// Muestra la fecha, según la configuración regional del árabe de Arabia Saudita.
sdtDate.DateDisplayLocale = CultureInfo.GetCultureInfo("ar-SA").LCID;

// Establezca el formato con el que se mostrará la fecha.
sdtDate.DateDisplayFormat = "dd MMMM, yyyy";
sdtDate.DateStorageFormat = SdtDateStorageFormat.DateTime;

// Muestra la fecha según el calendario Hijri.
sdtDate.CalendarType = SdtCalendarType.Hijri;

// Antes de que el usuario elija una fecha en Microsoft Word, la etiqueta mostrará el texto "Haga clic aquí para ingresar una fecha".
// Según el calendario de la etiqueta, configure la propiedad "FullDate" para que la etiqueta muestre una fecha predeterminada.
sdtDate.FullDate = new DateTime(1440, 10, 20);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(sdtDate);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Date.docx");
```

### Ver también

* enum [SdtCalendarType](../../sdtcalendartype/)
* class [StructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
