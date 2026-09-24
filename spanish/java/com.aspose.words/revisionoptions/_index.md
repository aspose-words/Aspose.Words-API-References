---
title: "RevisionOptions"
linktitle: "RevisionOptions"
second_title: "Aspose.Words para Java"
description: "Permite controlar cómo se manejan las revisiones del documento durante el proceso de diseño en Java."
type: docs
weight: 584
url: /es/java/com.aspose.words/revisionoptions/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class RevisionOptions implements Cloneable
```

Permite controlar cómo se manejan las revisiones del documento durante el proceso de maquetación.

Para obtener más información, visite el artículo de documentación [ Converting to Fixed-page Format ][Converting to Fixed-page Format].

 **Examples:** 

Muestra cómo alterar la apariencia de las revisiones en un documento de salida renderizado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a revision, then change the color of all revisions to green.
 builder.writeln("This is not a revision.");
 doc.startTrackRevisions("John Doe", new Date());
 builder.writeln("This is a revision.");
 doc.stopTrackRevisions();
 builder.writeln("This is not a revision.");

 // Remove the bar that appears to the left of every revised line.
 doc.getLayoutOptions().getRevisionOptions().setInsertedTextColor(RevisionColor.BRIGHT_GREEN);
 doc.getLayoutOptions().getRevisionOptions().setShowRevisionBars(false);
 doc.getLayoutOptions().getRevisionOptions().setRevisionBarsPosition(HorizontalAlignment.RIGHT);

 doc.save(getArtifactsDir() + "Revision.LayoutOptionsRevisions.pdf");
 
```


[Converting to Fixed-page Format]: https://docs.aspose.com/words/java/converting-to-fixed-page-format/
## Métodos

| Método | Descripción |
| --- | --- |
| [getCommentColor()](#getCommentColor) | Permite especificar el color a usar para los comentarios. |
| [getDeleteCellColor()](#getDeleteCellColor) | Permite especificar el color a usar para las celdas eliminadas [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [getDeletedTextColor()](#getDeletedTextColor) | Permite especificar el color a usar para el contenido eliminado [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [getDeletedTextEffect()](#getDeletedTextEffect) | Permite especificar el efecto a aplicar al contenido eliminado [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [getInsertCellColor()](#getInsertCellColor) | Permite especificar el color a usar para las celdas insertadas [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [getInsertedTextColor()](#getInsertedTextColor) | Permite especificar el color a usar para el contenido insertado [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [getInsertedTextEffect()](#getInsertedTextEffect) | Permite especificar el efecto a aplicar al contenido insertado [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [getMeasurementUnit()](#getMeasurementUnit) | Permite especificar las unidades de medida para los comentarios de revisión. |
| [getMovedFromTextColor()](#getMovedFromTextColor) | Permite especificar el color a usar para las áreas de donde se movió el contenido [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [getMovedFromTextEffect()](#getMovedFromTextEffect) | Permite especificar el efecto a aplicar a las áreas de donde se movió el contenido [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [getMovedToTextColor()](#getMovedToTextColor) | Permite especificar el color a usar para las áreas a donde se movió el contenido [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [getMovedToTextEffect()](#getMovedToTextEffect) | Permite especificar el efecto a aplicar a las áreas a donde se movió el contenido [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [getRevisedPropertiesColor()](#getRevisedPropertiesColor) | Permite especificar el color a usar para el contenido con cambios en propiedades de formato [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE). El valor predeterminado es [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT). |
| [getRevisedPropertiesEffect()](#getRevisedPropertiesEffect) | Permite especificar el efecto para áreas de contenido con cambios en propiedades de formato [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE). El valor predeterminado es [RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect/\#NONE). |
| [getRevisionBarsColor()](#getRevisionBarsColor) | Permite especificar el color a usar para las barras laterales que identifican las líneas del documento que contienen información revisada. |
| [getRevisionBarsPosition()](#getRevisionBarsPosition) | Obtiene la posición de renderizado de las barras de revisión. |
| [getRevisionBarsWidth()](#getRevisionBarsWidth) | Obtiene el ancho de las barras de revisión, puntos. |
| [getShowInBalloons()](#getShowInBalloons) | Permite especificar si las revisiones se renderizan en los globos. |
| [getShowOriginalRevision()](#getShowOriginalRevision) | Permite especificar si el texto original debe mostrarse en lugar del revisado. |
| [getShowRevisionBars()](#getShowRevisionBars) | Permite especificar si las barras de revisión deben renderizarse cerca de las líneas que contienen contenido revisado. |
| [getShowRevisionMarks()](#getShowRevisionMarks) | Permite especificar si el texto de revisión debe marcarse con un formato especial. |
| [setCommentColor(int value)](#setCommentColor-int) | Permite especificar el color a usar para los comentarios. |
| [setDeleteCellColor(int value)](#setDeleteCellColor-int) | Permite especificar el color a usar para las celdas eliminadas [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [setDeletedTextColor(int value)](#setDeletedTextColor-int) | Permite especificar el color a usar para el contenido eliminado [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [setDeletedTextEffect(int value)](#setDeletedTextEffect-int) | Permite especificar el efecto a aplicar al contenido eliminado [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [setInsertCellColor(int value)](#setInsertCellColor-int) | Permite especificar el color a usar para las celdas insertadas [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [setInsertedTextColor(int value)](#setInsertedTextColor-int) | Permite especificar el color a usar para el contenido insertado [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [setInsertedTextEffect(int value)](#setInsertedTextEffect-int) | Permite especificar el efecto a aplicar al contenido insertado [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [setMeasurementUnit(int value)](#setMeasurementUnit-int) | Permite especificar las unidades de medida para los comentarios de revisión. |
| [setMovedFromTextColor(int value)](#setMovedFromTextColor-int) | Permite especificar el color a usar para las áreas de donde se movió el contenido [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [setMovedFromTextEffect(int value)](#setMovedFromTextEffect-int) | Permite especificar el efecto a aplicar a las áreas de donde se movió el contenido [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [setMovedToTextColor(int value)](#setMovedToTextColor-int) | Permite especificar el color a usar para las áreas a donde se movió el contenido [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [setMovedToTextEffect(int value)](#setMovedToTextEffect-int) | Permite especificar el efecto a aplicar a las áreas a donde se movió el contenido [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [setRevisedPropertiesColor(int value)](#setRevisedPropertiesColor-int) | Permite especificar el color a usar para el contenido con cambios en propiedades de formato [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE). El valor predeterminado es [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT). |
| [setRevisedPropertiesEffect(int value)](#setRevisedPropertiesEffect-int) | Permite especificar el efecto para áreas de contenido con cambios en propiedades de formato [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE). El valor predeterminado es [RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect/\#NONE). |
| [setRevisionBarsColor(int value)](#setRevisionBarsColor-int) | Permite especificar el color a usar para las barras laterales que identifican las líneas del documento que contienen información revisada. |
| [setRevisionBarsPosition(int value)](#setRevisionBarsPosition-int) | Establece la posición de renderizado de las barras de revisión. |
| [setRevisionBarsWidth(float value)](#setRevisionBarsWidth-float) | Establece el ancho de las barras de revisión, puntos. |
| [setShowInBalloons(int value)](#setShowInBalloons-int) | Permite especificar si las revisiones se renderizan en los globos. |
| [setShowOriginalRevision(boolean value)](#setShowOriginalRevision-boolean) | Permite especificar si el texto original debe mostrarse en lugar del revisado. |
| [setShowRevisionBars(boolean value)](#setShowRevisionBars-boolean) | Permite especificar si las barras de revisión deben renderizarse cerca de las líneas que contienen contenido revisado. |
| [setShowRevisionMarks(boolean value)](#setShowRevisionMarks-boolean) | Permite especificar si el texto de revisión debe marcarse con un formato especial. |
### getCommentColor() {#getCommentColor}
```
public int getCommentColor()
```


Permite especificar el color que se usará para los comentarios. El valor predeterminado es [RevisionColor.RED](../../com.aspose.words/revisioncolor/\#RED).

 **Remarks:** 

Si se establece esta propiedad a los valores [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR) o [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT), como resultado esta propiedad se establecerá al color predeterminado.

 **Examples:** 

Muestra cómo modificar la apariencia de las revisiones.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int - El valor entero correspondiente. El valor devuelto es uno de los constantes de [RevisionColor](../../com.aspose.words/revisioncolor/).
### getDeleteCellColor() {#getDeleteCellColor}
```
public int getDeleteCellColor()
```


Permite especificar el color que se usará para celdas eliminadas [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). El valor predeterminado es [RevisionColor.PINK](../../com.aspose.words/revisioncolor/\#PINK).

 **Examples:** 

Muestra cómo trabajar con el color de revisión de inserción/eliminación de celdas.

```

 Document doc = new Document(getMyDir() + "Cell revisions.docx");

 doc.getLayoutOptions().getRevisionOptions().setInsertCellColor(RevisionColor.BLUE);
 doc.getLayoutOptions().getRevisionOptions().setDeleteCellColor(RevisionColor.DARK_RED);

 doc.save(getArtifactsDir() + "Revision.RevisionCellColor.pdf");
 
```

**Returns:**
int - El valor entero correspondiente. El valor devuelto es uno de los constantes de [RevisionColor](../../com.aspose.words/revisioncolor/).
### getDeletedTextColor() {#getDeletedTextColor}
```
public int getDeletedTextColor()
```


Permite especificar el color que se usará para contenido eliminado [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). El valor predeterminado es [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Muestra cómo modificar la apariencia de las revisiones.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int - El valor entero correspondiente. El valor devuelto es uno de los constantes de [RevisionColor](../../com.aspose.words/revisioncolor/).
### getDeletedTextEffect() {#getDeletedTextEffect}
```
public int getDeletedTextEffect()
```


Permite especificar el efecto que se aplicará al contenido eliminado [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). El valor predeterminado es [RevisionTextEffect.STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect/\#STRIKE-THROUGH)

 **Examples:** 

Muestra cómo modificar la apariencia de las revisiones.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int - El valor entero correspondiente. El valor devuelto es uno de los constantes de [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/).
### getInsertCellColor() {#getInsertCellColor}
```
public int getInsertCellColor()
```


Permite especificar el color que se usará para celdas insertadas [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). El valor predeterminado es [RevisionColor.BLUE](../../com.aspose.words/revisioncolor/\#BLUE).

 **Examples:** 

Muestra cómo trabajar con el color de revisión de inserción/eliminación de celdas.

```

 Document doc = new Document(getMyDir() + "Cell revisions.docx");

 doc.getLayoutOptions().getRevisionOptions().setInsertCellColor(RevisionColor.BLUE);
 doc.getLayoutOptions().getRevisionOptions().setDeleteCellColor(RevisionColor.DARK_RED);

 doc.save(getArtifactsDir() + "Revision.RevisionCellColor.pdf");
 
```

**Returns:**
int - El valor entero correspondiente. El valor devuelto es uno de los constantes de [RevisionColor](../../com.aspose.words/revisioncolor/).
### getInsertedTextColor() {#getInsertedTextColor}
```
public int getInsertedTextColor()
```


Permite especificar el color que se usará para contenido insertado [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). El valor predeterminado es [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Muestra cómo alterar la apariencia de las revisiones en un documento de salida renderizado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a revision, then change the color of all revisions to green.
 builder.writeln("This is not a revision.");
 doc.startTrackRevisions("John Doe", new Date());
 builder.writeln("This is a revision.");
 doc.stopTrackRevisions();
 builder.writeln("This is not a revision.");

 // Remove the bar that appears to the left of every revised line.
 doc.getLayoutOptions().getRevisionOptions().setInsertedTextColor(RevisionColor.BRIGHT_GREEN);
 doc.getLayoutOptions().getRevisionOptions().setShowRevisionBars(false);
 doc.getLayoutOptions().getRevisionOptions().setRevisionBarsPosition(HorizontalAlignment.RIGHT);

 doc.save(getArtifactsDir() + "Revision.LayoutOptionsRevisions.pdf");
 
```

**Returns:**
int - El valor entero correspondiente. El valor devuelto es uno de los constantes de [RevisionColor](../../com.aspose.words/revisioncolor/).
### getInsertedTextEffect() {#getInsertedTextEffect}
```
public int getInsertedTextEffect()
```


Permite especificar el efecto que se aplicará al contenido insertado [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). El valor predeterminado es [RevisionTextEffect.UNDERLINE](../../com.aspose.words/revisiontexteffect/\#UNDERLINE).

**Returns:**
int - El valor entero correspondiente. El valor devuelto es uno de los constantes de [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/).
### getMeasurementUnit() {#getMeasurementUnit}
```
public int getMeasurementUnit()
```


Permite especificar las unidades de medida para los comentarios de revisión. El valor predeterminado es [MeasurementUnits.CENTIMETERS](../../com.aspose.words/measurementunits/\#CENTIMETERS)

**Returns:**
int - El valor entero correspondiente. El valor devuelto es uno de los constantes de [MeasurementUnits](../../com.aspose.words/measurementunits/).
### getMovedFromTextColor() {#getMovedFromTextColor}
```
public int getMovedFromTextColor()
```


Permite especificar el color que se usará para las áreas donde el contenido se movió desde [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). El valor predeterminado es [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Muestra cómo modificar la apariencia de las revisiones.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int - El valor entero correspondiente. El valor devuelto es uno de los constantes de [RevisionColor](../../com.aspose.words/revisioncolor/).
### getMovedFromTextEffect() {#getMovedFromTextEffect}
```
public int getMovedFromTextEffect()
```


Permite especificar el efecto que se aplicará a las áreas donde el contenido se movió desde [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). El valor predeterminado es [RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect/\#DOUBLE-STRIKE-THROUGH)

 **Examples:** 

Muestra cómo modificar la apariencia de las revisiones.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int - El valor entero correspondiente. El valor devuelto es uno de los constantes de [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/).
### getMovedToTextColor() {#getMovedToTextColor}
```
public int getMovedToTextColor()
```


Permite especificar el color que se usará para las áreas donde el contenido se movió a [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). El valor predeterminado es [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Muestra cómo modificar la apariencia de las revisiones.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int - El valor entero correspondiente. El valor devuelto es uno de los constantes de [RevisionColor](../../com.aspose.words/revisioncolor/).
### getMovedToTextEffect() {#getMovedToTextEffect}
```
public int getMovedToTextEffect()
```


Permite especificar el efecto que se aplicará a las áreas donde el contenido se movió a [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). El valor predeterminado es [RevisionTextEffect.DOUBLE\_UNDERLINE](../../com.aspose.words/revisiontexteffect/\#DOUBLE-UNDERLINE)

**Returns:**
int - El valor entero correspondiente. El valor devuelto es uno de los constantes de [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/).
### getRevisedPropertiesColor() {#getRevisedPropertiesColor}
```
public int getRevisedPropertiesColor()
```


Permite especificar el color a usar para el contenido con cambios en propiedades de formato [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE). El valor predeterminado es [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT).

 **Examples:** 

Muestra cómo modificar la apariencia de las revisiones.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int - El valor entero correspondiente. El valor devuelto es uno de los constantes de [RevisionColor](../../com.aspose.words/revisioncolor/).
### getRevisedPropertiesEffect() {#getRevisedPropertiesEffect}
```
public int getRevisedPropertiesEffect()
```


Permite especificar el efecto para áreas de contenido con cambios en propiedades de formato [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE). El valor predeterminado es [RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect/\#NONE).

**Returns:**
int - El valor entero correspondiente. El valor devuelto es uno de los constantes de [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/).
### getRevisionBarsColor() {#getRevisionBarsColor}
```
public int getRevisionBarsColor()
```


Permite especificar el color que se usará para las barras laterales que identifican las líneas del documento que contienen información revisada. El valor predeterminado es [RevisionColor.RED](../../com.aspose.words/revisioncolor/\#RED).

 **Remarks:** 

Establecer esta propiedad a los valores [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR) o [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT) provocará que las barras de revisión se oculten del diseño.

 **Examples:** 

Muestra cómo modificar la apariencia de las revisiones.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int - El valor entero correspondiente. El valor devuelto es uno de los constantes de [RevisionColor](../../com.aspose.words/revisioncolor/).
### getRevisionBarsPosition() {#getRevisionBarsPosition}
```
public int getRevisionBarsPosition()
```


Obtiene la posición de renderizado de las barras de revisión. El valor predeterminado es [HorizontalAlignment.OUTSIDE](../../com.aspose.words/horizontalalignment/\#OUTSIDE).

**Returns:**
int - Posición de renderizado de las barras de revisión. El valor devuelto es una de las constantes de [HorizontalAlignment](../../com.aspose.words/horizontalalignment/).
### getRevisionBarsWidth() {#getRevisionBarsWidth}
```
public float getRevisionBarsWidth()
```


Obtiene el ancho de las barras de revisión, puntos.

 **Examples:** 

Muestra cómo modificar la apariencia de las revisiones.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
float - Ancho de las barras de revisión, puntos.
### getShowInBalloons() {#getShowInBalloons}
```
public int getShowInBalloons()
```


Permite especificar si las revisiones se renderizan en los globos. El valor predeterminado es [ShowInBalloons.NONE](../../com.aspose.words/showinballoons/\#NONE).

 **Remarks:** 

Tenga en cuenta que las revisiones no se renderizan en globos para [CommentDisplayMode.SHOW\_IN\_ANNOTATIONS](../../com.aspose.words/commentdisplaymode/\#SHOW-IN-ANNOTATIONS).

 **Examples:** 

Muestra cómo mostrar las revisiones en globos.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // By default, text that is a revision has a different color to differentiate it from the other non-revision text.
 // Set a revision option to show more details about each revision in a balloon on the page's right margin.
 doc.getLayoutOptions().getRevisionOptions().setShowInBalloons(ShowInBalloons.FORMAT_AND_DELETE);
 doc.save(getArtifactsDir() + "Revision.ShowRevisionBalloons.pdf");
 
```

Muestra cómo modificar la apariencia de las revisiones.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int - El valor entero correspondiente. El valor devuelto es una de las constantes de [ShowInBalloons](../../com.aspose.words/showinballoons/).
### getShowOriginalRevision() {#getShowOriginalRevision}
```
public boolean getShowOriginalRevision()
```


Permite especificar si el texto original debe mostrarse en lugar del revisado. El valor predeterminado es false.

 **Examples:** 

Muestra cómo modificar la apariencia de las revisiones.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getShowRevisionBars() {#getShowRevisionBars}
```
public boolean getShowRevisionBars()
```


Permite especificar si las barras de revisión deben renderizarse cerca de las líneas que contienen contenido revisado. El valor predeterminado es true.

 **Examples:** 

Muestra cómo alterar la apariencia de las revisiones en un documento de salida renderizado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a revision, then change the color of all revisions to green.
 builder.writeln("This is not a revision.");
 doc.startTrackRevisions("John Doe", new Date());
 builder.writeln("This is a revision.");
 doc.stopTrackRevisions();
 builder.writeln("This is not a revision.");

 // Remove the bar that appears to the left of every revised line.
 doc.getLayoutOptions().getRevisionOptions().setInsertedTextColor(RevisionColor.BRIGHT_GREEN);
 doc.getLayoutOptions().getRevisionOptions().setShowRevisionBars(false);
 doc.getLayoutOptions().getRevisionOptions().setRevisionBarsPosition(HorizontalAlignment.RIGHT);

 doc.save(getArtifactsDir() + "Revision.LayoutOptionsRevisions.pdf");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getShowRevisionMarks() {#getShowRevisionMarks}
```
public boolean getShowRevisionMarks()
```


Permita especificar si el texto de revisión debe marcarse con un marcado de formato especial. El valor predeterminado es true.

 **Examples:** 

Muestra cómo modificar la apariencia de las revisiones.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### setCommentColor(int value) {#setCommentColor-int}
```
public void setCommentColor(int value)
```


Permite especificar el color que se usará para los comentarios. El valor predeterminado es [RevisionColor.RED](../../com.aspose.words/revisioncolor/\#RED).

 **Remarks:** 

Si se establece esta propiedad a los valores [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR) o [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT), como resultado esta propiedad se establecerá al color predeterminado.

 **Examples:** 

Muestra cómo modificar la apariencia de las revisiones.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser una de las constantes de [RevisionColor](../../com.aspose.words/revisioncolor/). |

### setDeleteCellColor(int value) {#setDeleteCellColor-int}
```
public void setDeleteCellColor(int value)
```


Permite especificar el color que se usará para celdas eliminadas [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). El valor predeterminado es [RevisionColor.PINK](../../com.aspose.words/revisioncolor/\#PINK).

 **Examples:** 

Muestra cómo trabajar con el color de revisión de inserción/eliminación de celdas.

```

 Document doc = new Document(getMyDir() + "Cell revisions.docx");

 doc.getLayoutOptions().getRevisionOptions().setInsertCellColor(RevisionColor.BLUE);
 doc.getLayoutOptions().getRevisionOptions().setDeleteCellColor(RevisionColor.DARK_RED);

 doc.save(getArtifactsDir() + "Revision.RevisionCellColor.pdf");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser una de las constantes de [RevisionColor](../../com.aspose.words/revisioncolor/). |

### setDeletedTextColor(int value) {#setDeletedTextColor-int}
```
public void setDeletedTextColor(int value)
```


Permite especificar el color que se usará para contenido eliminado [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). El valor predeterminado es [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Muestra cómo modificar la apariencia de las revisiones.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser una de las constantes de [RevisionColor](../../com.aspose.words/revisioncolor/). |

### setDeletedTextEffect(int value) {#setDeletedTextEffect-int}
```
public void setDeletedTextEffect(int value)
```


Permite especificar el efecto que se aplicará al contenido eliminado [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). El valor predeterminado es [RevisionTextEffect.STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect/\#STRIKE-THROUGH)

 **Examples:** 

Muestra cómo modificar la apariencia de las revisiones.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser una de las constantes de [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/). |

### setInsertCellColor(int value) {#setInsertCellColor-int}
```
public void setInsertCellColor(int value)
```


Permite especificar el color que se usará para celdas insertadas [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). El valor predeterminado es [RevisionColor.BLUE](../../com.aspose.words/revisioncolor/\#BLUE).

 **Examples:** 

Muestra cómo trabajar con el color de revisión de inserción/eliminación de celdas.

```

 Document doc = new Document(getMyDir() + "Cell revisions.docx");

 doc.getLayoutOptions().getRevisionOptions().setInsertCellColor(RevisionColor.BLUE);
 doc.getLayoutOptions().getRevisionOptions().setDeleteCellColor(RevisionColor.DARK_RED);

 doc.save(getArtifactsDir() + "Revision.RevisionCellColor.pdf");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser una de las constantes de [RevisionColor](../../com.aspose.words/revisioncolor/). |

### setInsertedTextColor(int value) {#setInsertedTextColor-int}
```
public void setInsertedTextColor(int value)
```


Permite especificar el color que se usará para contenido insertado [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). El valor predeterminado es [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Muestra cómo alterar la apariencia de las revisiones en un documento de salida renderizado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a revision, then change the color of all revisions to green.
 builder.writeln("This is not a revision.");
 doc.startTrackRevisions("John Doe", new Date());
 builder.writeln("This is a revision.");
 doc.stopTrackRevisions();
 builder.writeln("This is not a revision.");

 // Remove the bar that appears to the left of every revised line.
 doc.getLayoutOptions().getRevisionOptions().setInsertedTextColor(RevisionColor.BRIGHT_GREEN);
 doc.getLayoutOptions().getRevisionOptions().setShowRevisionBars(false);
 doc.getLayoutOptions().getRevisionOptions().setRevisionBarsPosition(HorizontalAlignment.RIGHT);

 doc.save(getArtifactsDir() + "Revision.LayoutOptionsRevisions.pdf");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser una de las constantes de [RevisionColor](../../com.aspose.words/revisioncolor/). |

### setInsertedTextEffect(int value) {#setInsertedTextEffect-int}
```
public void setInsertedTextEffect(int value)
```


Permite especificar el efecto que se aplicará al contenido insertado [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). El valor predeterminado es [RevisionTextEffect.UNDERLINE](../../com.aspose.words/revisiontexteffect/\#UNDERLINE).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser una de las constantes de [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/). |

### setMeasurementUnit(int value) {#setMeasurementUnit-int}
```
public void setMeasurementUnit(int value)
```


Permite especificar las unidades de medida para los comentarios de revisión. El valor predeterminado es [MeasurementUnits.CENTIMETERS](../../com.aspose.words/measurementunits/\#CENTIMETERS)

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser una de las constantes de [MeasurementUnits](../../com.aspose.words/measurementunits/). |

### setMovedFromTextColor(int value) {#setMovedFromTextColor-int}
```
public void setMovedFromTextColor(int value)
```


Permite especificar el color que se usará para las áreas donde el contenido se movió desde [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). El valor predeterminado es [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Muestra cómo modificar la apariencia de las revisiones.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser una de las constantes de [RevisionColor](../../com.aspose.words/revisioncolor/). |

### setMovedFromTextEffect(int value) {#setMovedFromTextEffect-int}
```
public void setMovedFromTextEffect(int value)
```


Permite especificar el efecto que se aplicará a las áreas donde el contenido se movió desde [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). El valor predeterminado es [RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect/\#DOUBLE-STRIKE-THROUGH)

 **Examples:** 

Muestra cómo modificar la apariencia de las revisiones.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser una de las constantes de [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/). |

### setMovedToTextColor(int value) {#setMovedToTextColor-int}
```
public void setMovedToTextColor(int value)
```


Permite especificar el color que se usará para las áreas donde el contenido se movió a [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). El valor predeterminado es [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Muestra cómo modificar la apariencia de las revisiones.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser una de las constantes de [RevisionColor](../../com.aspose.words/revisioncolor/). |

### setMovedToTextEffect(int value) {#setMovedToTextEffect-int}
```
public void setMovedToTextEffect(int value)
```


Permite especificar el efecto que se aplicará a las áreas donde el contenido se movió a [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). El valor predeterminado es [RevisionTextEffect.DOUBLE\_UNDERLINE](../../com.aspose.words/revisiontexteffect/\#DOUBLE-UNDERLINE)

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser una de las constantes de [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/). |

### setRevisedPropertiesColor(int value) {#setRevisedPropertiesColor-int}
```
public void setRevisedPropertiesColor(int value)
```


Permite especificar el color a usar para el contenido con cambios en propiedades de formato [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE). El valor predeterminado es [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT).

 **Examples:** 

Muestra cómo modificar la apariencia de las revisiones.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser una de las constantes de [RevisionColor](../../com.aspose.words/revisioncolor/). |

### setRevisedPropertiesEffect(int value) {#setRevisedPropertiesEffect-int}
```
public void setRevisedPropertiesEffect(int value)
```


Permite especificar el efecto para áreas de contenido con cambios en propiedades de formato [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE). El valor predeterminado es [RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect/\#NONE).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser una de las constantes de [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/). |

### setRevisionBarsColor(int value) {#setRevisionBarsColor-int}
```
public void setRevisionBarsColor(int value)
```


Permite especificar el color que se usará para las barras laterales que identifican las líneas del documento que contienen información revisada. El valor predeterminado es [RevisionColor.RED](../../com.aspose.words/revisioncolor/\#RED).

 **Remarks:** 

Establecer esta propiedad a los valores [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR) o [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT) provocará que las barras de revisión se oculten del diseño.

 **Examples:** 

Muestra cómo modificar la apariencia de las revisiones.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser una de las constantes de [RevisionColor](../../com.aspose.words/revisioncolor/). |

### setRevisionBarsPosition(int value) {#setRevisionBarsPosition-int}
```
public void setRevisionBarsPosition(int value)
```


Establece la posición de renderizado de las barras de revisión. El valor predeterminado es [HorizontalAlignment.OUTSIDE](../../com.aspose.words/horizontalalignment/\#OUTSIDE).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | Posición de renderizado de las barras de revisión. El valor debe ser una de las constantes de [HorizontalAlignment](../../com.aspose.words/horizontalalignment/). |

### setRevisionBarsWidth(float value) {#setRevisionBarsWidth-float}
```
public void setRevisionBarsWidth(float value)
```


Establece el ancho de las barras de revisión, puntos.

 **Examples:** 

Muestra cómo modificar la apariencia de las revisiones.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | float | Ancho de las barras de revisión, puntos. |

### setShowInBalloons(int value) {#setShowInBalloons-int}
```
public void setShowInBalloons(int value)
```


Permite especificar si las revisiones se renderizan en los globos. El valor predeterminado es [ShowInBalloons.NONE](../../com.aspose.words/showinballoons/\#NONE).

 **Remarks:** 

Tenga en cuenta que las revisiones no se renderizan en globos para [CommentDisplayMode.SHOW\_IN\_ANNOTATIONS](../../com.aspose.words/commentdisplaymode/\#SHOW-IN-ANNOTATIONS).

 **Examples:** 

Muestra cómo mostrar las revisiones en globos.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // By default, text that is a revision has a different color to differentiate it from the other non-revision text.
 // Set a revision option to show more details about each revision in a balloon on the page's right margin.
 doc.getLayoutOptions().getRevisionOptions().setShowInBalloons(ShowInBalloons.FORMAT_AND_DELETE);
 doc.save(getArtifactsDir() + "Revision.ShowRevisionBalloons.pdf");
 
```

Muestra cómo modificar la apariencia de las revisiones.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser una de las constantes de [ShowInBalloons](../../com.aspose.words/showinballoons/). |

### setShowOriginalRevision(boolean value) {#setShowOriginalRevision-boolean}
```
public void setShowOriginalRevision(boolean value)
```


Permite especificar si el texto original debe mostrarse en lugar del revisado. El valor predeterminado es false.

 **Examples:** 

Muestra cómo modificar la apariencia de las revisiones.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setShowRevisionBars(boolean value) {#setShowRevisionBars-boolean}
```
public void setShowRevisionBars(boolean value)
```


Permite especificar si las barras de revisión deben renderizarse cerca de las líneas que contienen contenido revisado. El valor predeterminado es true.

 **Examples:** 

Muestra cómo alterar la apariencia de las revisiones en un documento de salida renderizado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a revision, then change the color of all revisions to green.
 builder.writeln("This is not a revision.");
 doc.startTrackRevisions("John Doe", new Date());
 builder.writeln("This is a revision.");
 doc.stopTrackRevisions();
 builder.writeln("This is not a revision.");

 // Remove the bar that appears to the left of every revised line.
 doc.getLayoutOptions().getRevisionOptions().setInsertedTextColor(RevisionColor.BRIGHT_GREEN);
 doc.getLayoutOptions().getRevisionOptions().setShowRevisionBars(false);
 doc.getLayoutOptions().getRevisionOptions().setRevisionBarsPosition(HorizontalAlignment.RIGHT);

 doc.save(getArtifactsDir() + "Revision.LayoutOptionsRevisions.pdf");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setShowRevisionMarks(boolean value) {#setShowRevisionMarks-boolean}
```
public void setShowRevisionMarks(boolean value)
```


Permita especificar si el texto de revisión debe marcarse con un marcado de formato especial. El valor predeterminado es true.

 **Examples:** 

Muestra cómo modificar la apariencia de las revisiones.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

