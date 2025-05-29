---
title: LayoutOptions Class
linktitle: LayoutOptions
articleTitle: LayoutOptions
second_title: Aspose.Words para .NET
description: Descubra Aspose.Words.Layout.LayoutOptions para optimizar el control del diseño del documento y mejorar su experiencia de procesamiento de textos con opciones de personalización flexibles.
type: docs
weight: 3800
url: /es/net/aspose.words.layout/layoutoptions/
---
## LayoutOptions class

Contiene las opciones que permiten controlar el proceso de diseño del documento.

Para obtener más información, visite el[Conversión a formato de página fija](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) Artículo de documentación.

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
| [Callback](../../aspose.words.layout/layoutoptions/callback/) { get; set; } | Obtiene o establece[`IPageLayoutCallback`](../ipagelayoutcallback/) Implementación utilizada por el modelo de diseño de página. |
| [CommentDisplayMode](../../aspose.words.layout/layoutoptions/commentdisplaymode/) { get; set; } | Obtiene o establece la forma en que se representan los comentarios. El valor predeterminado esShowInBalloons . |
| [ContinuousSectionPageNumberingRestart](../../aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/) { get; set; } | Obtiene o establece el modo de comportamiento para calcular los números de página cuando una sección continua reinicia la numeración de páginas. |
| [IgnorePrinterMetrics](../../aspose.words.layout/layoutoptions/ignoreprintermetrics/) { get; set; } | Obtiene o establece la indicación de si se ignora la opción de compatibilidad "Usar métricas de impresora para diseñar el documento". El valor predeterminado es`verdadero` . |
| [KeepOriginalFontMetrics](../../aspose.words.layout/layoutoptions/keeporiginalfontmetrics/) { get; set; } | Obtiene o establece una indicación de si se deben utilizar las métricas de fuente originales después de la sustitución de la fuente. El valor predeterminado es`verdadero` . |
| [RevisionOptions](../../aspose.words.layout/layoutoptions/revisionoptions/) { get; } | Obtiene opciones de revisión. |
| [ShowHiddenText](../../aspose.words.layout/layoutoptions/showhiddentext/) { get; set; } | Obtiene o establece la indicación de si se representa el texto oculto en el documento. El valor predeterminado es`FALSO` . |
| [ShowParagraphMarks](../../aspose.words.layout/layoutoptions/showparagraphmarks/) { get; set; } | Obtiene o establece la indicación de si se representan las marcas de párrafo. El valor predeterminado es`FALSO` . |
| [TextShaperFactory](../../aspose.words.layout/layoutoptions/textshaperfactory/) { get; set; } | Obtiene o establece[`ITextShaperFactory`](../../aspose.words.shaping/itextshaperfactory/) Implementación utilizada para funciones de representación de tipografía avanzada. |

## Observaciones

No se crean instancias de esta clase directamente. Utilice el[`LayoutOptions`](../../aspose.words/document/layoutoptions/) propiedad para acceder a las opciones de diseño para este documento.

Tenga en cuenta que después de cambiar cualquiera de las opciones presentes en esta clase,[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) Se debe llamar al método para que las opciones modificadas se apliquen al diseño.

## Ejemplos

Muestra cómo ocultar texto en un documento de salida renderizado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Inserte texto oculto y luego especifique si deseamos omitirlo del documento renderizado.
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
// Agregue algunos párrafos y luego habilite las marcas de párrafo para mostrar los finales de los párrafos
// con un símbolo pilcrow (¶) cuando renderizamos el documento.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

Muestra cómo alterar la apariencia de las revisiones en un documento de salida renderizado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte una revisión, luego cambie el color de todas las revisiones a verde.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

//Elimina la barra que aparece a la izquierda de cada línea revisada.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### Ver también

* espacio de nombres [Aspose.Words.Layout](../../aspose.words.layout/)
* asamblea [Aspose.Words](../../)
