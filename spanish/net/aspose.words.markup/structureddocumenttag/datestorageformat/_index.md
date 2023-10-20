---
title: StructuredDocumentTag.DateStorageFormat
linktitle: DateStorageFormat
articleTitle: DateStorageFormat
second_title: Aspose.Words para .NET
description: StructuredDocumentTag DateStorageFormat propiedad. Obtiene/establece el formato en el que se almacena la fecha para una fecha SDT cuandoTEDestá vinculado a un nodo XML en el almacén de datos del documento. El valor predeterminado esDateTime en C#.
type: docs
weight: 110
url: /es/net/aspose.words.markup/structureddocumenttag/datestorageformat/
---
## StructuredDocumentTag.DateStorageFormat property

Obtiene/establece el formato en el que se almacena la fecha para una fecha SDT cuando**TED**está vinculado a un nodo XML en el almacén de datos del documento. El valor predeterminado esDateTime

```csharp
public SdtDateStorageFormat DateStorageFormat { get; set; }
```

## Observaciones

Acceder a esta propiedad sólo funcionará paraDate Tipo SDT.

Para todos los demás tipos de SDT se producirá una excepción.

## Ejemplos

Muestra cómo solicitar al usuario que ingrese una fecha con una etiqueta de documento estructurado.

```csharp
Document doc = new Document();

// Inserte una etiqueta de documento estructurado que solicite al usuario que ingrese una fecha.
// En Microsoft Word, este elemento se conoce como "control de contenido del selector de fecha".
// Cuando hacemos clic en la flecha en el extremo derecho de esta etiqueta en Microsoft Word,
// veremos una ventana emergente en forma de calendario en el que se puede hacer clic.
// Podemos usar esa ventana emergente para seleccionar una fecha en la que se mostrará la etiqueta.
StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.Date, MarkupLevel.Inline);

// Muestra la fecha, según la configuración regional árabe de Arabia Saudita.
sdtDate.DateDisplayLocale = CultureInfo.GetCultureInfo("ar-SA").LCID;

// Establece el formato con el que mostrar la fecha.
sdtDate.DateDisplayFormat = "dd MMMM, yyyy";
sdtDate.DateStorageFormat = SdtDateStorageFormat.DateTime;

// Muestra la fecha según el calendario Hijri.
sdtDate.CalendarType = SdtCalendarType.Hijri;

// Antes de que el usuario elija una fecha en Microsoft Word, la etiqueta mostrará el texto "Haga clic aquí para ingresar una fecha".
// Según el calendario de la etiqueta, establezca la propiedad "FullDate" para que la etiqueta muestre una fecha predeterminada.
sdtDate.FullDate = new DateTime(1440, 10, 20);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(sdtDate);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Date.docx");
```

### Ver también

* enum [SdtDateStorageFormat](../../sdtdatestorageformat/)
* class [StructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
