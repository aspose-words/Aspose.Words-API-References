---
title: StructuredDocumentTag.FullDate
linktitle: FullDate
articleTitle: FullDate
second_title: Aspose.Words para .NET
description: Descubra la propiedad StructuredDocumentTag FullDate, que captura la fecha y hora completas para mejorar la precisión y el seguimiento de los documentos.
type: docs
weight: 130
url: /es/net/aspose.words.markup/structureddocumenttag/fulldate/
---
## StructuredDocumentTag.FullDate property

Especifica la fecha y hora completas ingresadas por última vez en este**TED** .

```csharp
public DateTime FullDate { get; set; }
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

* class [StructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
