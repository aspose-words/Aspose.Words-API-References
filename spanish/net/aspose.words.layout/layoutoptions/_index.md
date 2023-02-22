---
title: Class LayoutOptions
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Layout.LayoutOptions clase. Contiene las opciones que permiten controlar el proceso de maquetación del documento.
type: docs
weight: 3150
url: /es/net/aspose.words.layout/layoutoptions/
---
## LayoutOptions class

Contiene las opciones que permiten controlar el proceso de maquetación del documento.

```csharp
public class LayoutOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [LayoutOptions](layoutoptions/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Callback](../../aspose.words.layout/layoutoptions/callback/) { get; set; } | Obtiene o establece[`IPageLayoutCallback`](../ipagelayoutcallback/)implementación utilizada por el modelo de diseño de página. |
| [CommentDisplayMode](../../aspose.words.layout/layoutoptions/commentdisplaymode/) { get; set; } | Obtiene o establece la forma en que se representan los comentarios. El valor predeterminado esShowInBalloons . |
| [ContinuousSectionPageNumberingRestart](../../aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/) { get; set; } | Obtiene o establece el modo de comportamiento para calcular los números de página cuando una sección continua reinicia la numeración de páginas. |
| [IgnorePrinterMetrics](../../aspose.words.layout/layoutoptions/ignoreprintermetrics/) { get; set; } | Obtiene o establece una indicación de si se ignora la opción de compatibilidad "Usar métricas de impresora para diseñar el documento". El valor predeterminado es Verdadero. |
| [RevisionOptions](../../aspose.words.layout/layoutoptions/revisionoptions/) { get; } | Obtiene opciones de revisión. |
| [ShowHiddenText](../../aspose.words.layout/layoutoptions/showhiddentext/) { get; set; } | Obtiene o establece una indicación de si se representa el texto oculto en el documento. El valor predeterminado es Falso. |
| [ShowParagraphMarks](../../aspose.words.layout/layoutoptions/showparagraphmarks/) { get; set; } | Obtiene o establece la indicación de si se representan las marcas de párrafo. El valor predeterminado es Falso. |
| [TextShaperFactory](../../aspose.words.layout/layoutoptions/textshaperfactory/) { get; set; } | Obtiene o establece[`ITextShaperFactory`](../../aspose.words.shaping/itextshaperfactory/) implementación utilizada para funciones de representación de tipografía avanzada. |

### Observaciones

No crea instancias de esta clase directamente. Utilizar el[`LayoutOptions`](../../aspose.words/document/layoutoptions/)propiedad para acceder a las opciones de diseño de este documento.

Tenga en cuenta que después de cambiar cualquiera de las opciones presentes en esta clase,[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) Se debe llamar a method para que las opciones modificadas se apliquen al diseño.

### Ejemplos

Muestra cómo ocultar texto en un documento de salida renderizado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Insertar texto oculto, luego especificar si deseamos omitirlo de un documento renderizado.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

Muestra cómo mostrar marcas de párrafo en un documento de salida renderizado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Agregue algunos párrafos, luego habilite las marcas de párrafo para mostrar los extremos de los párrafos
// con un símbolo de almohada (¶) cuando renderizamos el documento.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

Muestra cómo modificar la apariencia de las revisiones en un documento de salida renderizado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte una revisión, luego cambie el color de todas las revisiones a verde.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Elimina la barra que aparece a la izquierda de cada línea revisada.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### Ver también

* espacio de nombres [Aspose.Words.Layout](../../aspose.words.layout/)
* asamblea [Aspose.Words](../../)


