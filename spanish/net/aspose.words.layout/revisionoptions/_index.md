---
title: RevisionOptions Class
linktitle: RevisionOptions
articleTitle: RevisionOptions
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Layout.RevisionOptions para administrar de manera eficiente las revisiones de documentos y mejorar su proceso de diseño para obtener resultados óptimos.
type: docs
weight: 3840
url: /es/net/aspose.words.layout/revisionoptions/
---
## RevisionOptions class

Permite controlar cómo se manejan las revisiones del documento durante el proceso de diseño.

Para obtener más información, visite el[Conversión a formato de página fija](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) Artículo de documentación.

```csharp
public class RevisionOptions
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CommentColor](../../aspose.words.layout/revisionoptions/commentcolor/) { get; set; } | Permite especificar el color que se utilizará para los comentarios. El valor predeterminado esRed . |
| [DeleteCellColor](../../aspose.words.layout/revisionoptions/deletecellcolor/) { get; set; } | Permite especificar el color que se utilizará para las celdas eliminadasDeletion . El valor predeterminado esPink . |
| [DeletedTextColor](../../aspose.words.layout/revisionoptions/deletedtextcolor/) { get; set; } | Permite especificar el color que se utilizará para el contenido eliminadoDeletion . El valor predeterminado esByAuthor . |
| [DeletedTextEffect](../../aspose.words.layout/revisionoptions/deletedtexteffect/) { get; set; } | Permite especificar el efecto que se aplicará al contenido eliminadoDeletion . El valor predeterminado esStrikeThrough |
| [InsertCellColor](../../aspose.words.layout/revisionoptions/insertcellcolor/) { get; set; } | Permite especificar el color que se utilizará para las celdas insertadasInsertion . El valor predeterminado esBlue . |
| [InsertedTextColor](../../aspose.words.layout/revisionoptions/insertedtextcolor/) { get; set; } | Permite especificar el color que se utilizará para el contenido insertadoInsertion . El valor predeterminado esByAuthor . |
| [InsertedTextEffect](../../aspose.words.layout/revisionoptions/insertedtexteffect/) { get; set; } | Permite especificar el efecto que se aplicará al contenido insertadoInsertion . El valor predeterminado esUnderline . |
| [MeasurementUnit](../../aspose.words.layout/revisionoptions/measurementunit/) { get; set; } | Permite especificar las unidades de medida para los comentarios de revisión. El valor predeterminado esCentimeters |
| [MovedFromTextColor](../../aspose.words.layout/revisionoptions/movedfromtextcolor/) { get; set; } | Permite especificar el color que se utilizará en las áreas desde donde se movió el contenidoMoving . El valor predeterminado esByAuthor . |
| [MovedFromTextEffect](../../aspose.words.layout/revisionoptions/movedfromtexteffect/) { get; set; } | Permite especificar el efecto que se aplicará a las áreas desde donde se movió el contenidoMoving . El valor predeterminado esDoubleStrikeThrough |
| [MovedToTextColor](../../aspose.words.layout/revisionoptions/movedtotextcolor/) { get; set; } | Permite especificar el color que se utilizará en las áreas donde se movió el contenido.Moving . El valor predeterminado esByAuthor . |
| [MovedToTextEffect](../../aspose.words.layout/revisionoptions/movedtotexteffect/) { get; set; } | Permite especificar el efecto que se aplicará a las áreas donde se movió el contenido.Moving . El valor predeterminado esDoubleUnderline |
| [RevisedPropertiesColor](../../aspose.words.layout/revisionoptions/revisedpropertiescolor/) { get; set; } | Permite especificar el color que se utilizará para el contenido con cambios en las propiedades de formatoFormatChange El valor predeterminado esNoHighlight . |
| [RevisedPropertiesEffect](../../aspose.words.layout/revisionoptions/revisedpropertieseffect/) { get; set; } | Permite especificar el efecto para las áreas de contenido con cambios en las propiedades de formatoFormatChange El valor predeterminado esNone |
| [RevisionBarsColor](../../aspose.words.layout/revisionoptions/revisionbarscolor/) { get; set; } | Permite especificar el color que se utilizará para las barras laterales que identifican las líneas del documento que contienen información revisada. El valor predeterminado esRed . |
| [RevisionBarsPosition](../../aspose.words.layout/revisionoptions/revisionbarsposition/) { get; set; } | Obtiene o establece la posición de representación de las barras de revisión. El valor predeterminado esOutside . |
| [RevisionBarsWidth](../../aspose.words.layout/revisionoptions/revisionbarswidth/) { get; set; } | Obtiene o establece el ancho de las barras de revisión, puntos. |
| [ShowInBalloons](../../aspose.words.layout/revisionoptions/showinballoons/) { get; set; } | Permite especificar si las revisiones se representan en los globos. El valor predeterminado esNone . |
| [ShowOriginalRevision](../../aspose.words.layout/revisionoptions/showoriginalrevision/) { get; set; } | Permite especificar si se debe mostrar el texto original en lugar del revisado. El valor predeterminado es`FALSO` . |
| [ShowRevisionBars](../../aspose.words.layout/revisionoptions/showrevisionbars/) { get; set; } | Permite especificar si las barras de revisión deben representarse cerca de las líneas que contienen contenido revisado. El valor predeterminado es`verdadero` . |
| [ShowRevisionMarks](../../aspose.words.layout/revisionoptions/showrevisionmarks/) { get; set; } | Permite especificar si el texto de revisión debe marcarse con un marcado de formato especial. El valor predeterminado es`verdadero` . |

## Ejemplos

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
