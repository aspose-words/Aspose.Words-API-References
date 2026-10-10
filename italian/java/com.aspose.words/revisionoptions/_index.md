---
title: "RevisionOptions"
linktitle: "RevisionOptions"
second_title: "Aspose.Words per Java"
description: "Consente di controllare come le revisioni del documento vengono gestite durante il processo di layout in Java."
type: docs
weight: 584
url: /it/java/com.aspose.words/revisionoptions/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class RevisionOptions implements Cloneable
```

Consente di controllare come le revisioni del documento vengono gestite durante il processo di layout.

Per saperne di più, visita l'articolo di documentazione [ Converting to Fixed-page Format ][Converting to Fixed-page Format].

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni in un documento di output renderizzato.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getCommentColor()](#getCommentColor) | Consente di specificare il colore da utilizzare per i commenti. |
| [getDeleteCellColor()](#getDeleteCellColor) | Consente di specificare il colore da utilizzare per le celle eliminate [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [getDeletedTextColor()](#getDeletedTextColor) | Consente di specificare il colore da utilizzare per il contenuto eliminato [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [getDeletedTextEffect()](#getDeletedTextEffect) | Consente di specificare l'effetto da applicare al contenuto eliminato [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [getInsertCellColor()](#getInsertCellColor) | Consente di specificare il colore da utilizzare per le celle inserite [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [getInsertedTextColor()](#getInsertedTextColor) | Consente di specificare il colore da utilizzare per il contenuto inserito [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [getInsertedTextEffect()](#getInsertedTextEffect) | Consente di specificare l'effetto da applicare al contenuto inserito [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [getMeasurementUnit()](#getMeasurementUnit) | Consente di specificare le unità di misura per i commenti di revisione. |
| [getMovedFromTextColor()](#getMovedFromTextColor) | Consente di specificare il colore da utilizzare per le aree da cui è stato spostato il contenuto [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [getMovedFromTextEffect()](#getMovedFromTextEffect) | Consente di specificare l'effetto da applicare alle aree da cui è stato spostato il contenuto [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [getMovedToTextColor()](#getMovedToTextColor) | Consente di specificare il colore da utilizzare per le aree verso cui è stato spostato il contenuto [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [getMovedToTextEffect()](#getMovedToTextEffect) | Consente di specificare l'effetto da applicare alle aree verso cui è stato spostato il contenuto [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [getRevisedPropertiesColor()](#getRevisedPropertiesColor) | Consente di specificare il colore da utilizzare per il contenuto con modifiche delle proprietà di formattazione [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE) Il valore predefinito è [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT). |
| [getRevisedPropertiesEffect()](#getRevisedPropertiesEffect) | Consente di specificare l'effetto per le aree di contenuto con modifiche delle proprietà di formattazione [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE) Il valore predefinito è [RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect/\#NONE). |
| [getRevisionBarsColor()](#getRevisionBarsColor) | Consente di specificare il colore da utilizzare per le barre laterali che identificano le righe del documento contenenti informazioni revisionate. |
| [getRevisionBarsPosition()](#getRevisionBarsPosition) | Restituisce la posizione di rendering delle barre di revisione. |
| [getRevisionBarsWidth()](#getRevisionBarsWidth) | Ottiene la larghezza delle barre di revisione, punti. |
| [getShowInBalloons()](#getShowInBalloons) | Consente di specificare se le revisioni vengono visualizzate nei balloon. |
| [getShowOriginalRevision()](#getShowOriginalRevision) | Consente di specificare se il testo originale deve essere mostrato al posto di quello revisionato. |
| [getShowRevisionBars()](#getShowRevisionBars) | Consente di specificare se le barre di revisione devono essere visualizzate vicino alle righe contenenti contenuto revisionato. |
| [getShowRevisionMarks()](#getShowRevisionMarks) | Consente di specificare se il testo della revisione deve essere contrassegnato con una formattazione speciale. |
| [setCommentColor(int value)](#setCommentColor-int) | Consente di specificare il colore da utilizzare per i commenti. |
| [setDeleteCellColor(int value)](#setDeleteCellColor-int) | Consente di specificare il colore da utilizzare per le celle eliminate [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [setDeletedTextColor(int value)](#setDeletedTextColor-int) | Consente di specificare il colore da utilizzare per il contenuto eliminato [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [setDeletedTextEffect(int value)](#setDeletedTextEffect-int) | Consente di specificare l'effetto da applicare al contenuto eliminato [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [setInsertCellColor(int value)](#setInsertCellColor-int) | Consente di specificare il colore da utilizzare per le celle inserite [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [setInsertedTextColor(int value)](#setInsertedTextColor-int) | Consente di specificare il colore da utilizzare per il contenuto inserito [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [setInsertedTextEffect(int value)](#setInsertedTextEffect-int) | Consente di specificare l'effetto da applicare al contenuto inserito [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [setMeasurementUnit(int value)](#setMeasurementUnit-int) | Consente di specificare le unità di misura per i commenti di revisione. |
| [setMovedFromTextColor(int value)](#setMovedFromTextColor-int) | Consente di specificare il colore da utilizzare per le aree da cui è stato spostato il contenuto [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [setMovedFromTextEffect(int value)](#setMovedFromTextEffect-int) | Consente di specificare l'effetto da applicare alle aree da cui è stato spostato il contenuto [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [setMovedToTextColor(int value)](#setMovedToTextColor-int) | Consente di specificare il colore da utilizzare per le aree verso cui è stato spostato il contenuto [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [setMovedToTextEffect(int value)](#setMovedToTextEffect-int) | Consente di specificare l'effetto da applicare alle aree verso cui è stato spostato il contenuto [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [setRevisedPropertiesColor(int value)](#setRevisedPropertiesColor-int) | Consente di specificare il colore da utilizzare per il contenuto con modifiche delle proprietà di formattazione [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE) Il valore predefinito è [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT). |
| [setRevisedPropertiesEffect(int value)](#setRevisedPropertiesEffect-int) | Consente di specificare l'effetto per le aree di contenuto con modifiche delle proprietà di formattazione [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE) Il valore predefinito è [RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect/\#NONE). |
| [setRevisionBarsColor(int value)](#setRevisionBarsColor-int) | Consente di specificare il colore da utilizzare per le barre laterali che identificano le righe del documento contenenti informazioni revisionate. |
| [setRevisionBarsPosition(int value)](#setRevisionBarsPosition-int) | Imposta la posizione di rendering delle barre di revisione. |
| [setRevisionBarsWidth(float value)](#setRevisionBarsWidth-float) | Imposta la larghezza delle barre di revisione, punti. |
| [setShowInBalloons(int value)](#setShowInBalloons-int) | Consente di specificare se le revisioni vengono visualizzate nei balloon. |
| [setShowOriginalRevision(boolean value)](#setShowOriginalRevision-boolean) | Consente di specificare se il testo originale deve essere mostrato al posto di quello revisionato. |
| [setShowRevisionBars(boolean value)](#setShowRevisionBars-boolean) | Consente di specificare se le barre di revisione devono essere visualizzate vicino alle righe contenenti contenuto revisionato. |
| [setShowRevisionMarks(boolean value)](#setShowRevisionMarks-boolean) | Consente di specificare se il testo della revisione deve essere contrassegnato con una formattazione speciale. |
### getCommentColor() {#getCommentColor}
```
public int getCommentColor()
```


Consente di specificare il colore da utilizzare per i commenti. Il valore predefinito è [RevisionColor.RED](../../com.aspose.words/revisioncolor/\#RED).

 **Remarks:** 

Se si imposta questa proprietà sui valori [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR) o [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT), il risultato sarà che questa proprietà verrà impostata sul colore predefinito.

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni.

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
int - Il valore int corrispondente. Il valore restituito è una delle costanti di [RevisionColor](../../com.aspose.words/revisioncolor/).
### getDeleteCellColor() {#getDeleteCellColor}
```
public int getDeleteCellColor()
```


Consente di specificare il colore da utilizzare per le celle eliminate [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). Il valore predefinito è [RevisionColor.PINK](../../com.aspose.words/revisioncolor/\#PINK).

 **Examples:** 

Mostra come lavorare con il colore di revisione per l'inserimento/cancellazione di celle.

```

 Document doc = new Document(getMyDir() + "Cell revisions.docx");

 doc.getLayoutOptions().getRevisionOptions().setInsertCellColor(RevisionColor.BLUE);
 doc.getLayoutOptions().getRevisionOptions().setDeleteCellColor(RevisionColor.DARK_RED);

 doc.save(getArtifactsDir() + "Revision.RevisionCellColor.pdf");
 
```

**Returns:**
int - Il valore int corrispondente. Il valore restituito è una delle costanti di [RevisionColor](../../com.aspose.words/revisioncolor/).
### getDeletedTextColor() {#getDeletedTextColor}
```
public int getDeletedTextColor()
```


Consente di specificare il colore da utilizzare per il contenuto eliminato [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). Il valore predefinito è [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni.

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
int - Il valore int corrispondente. Il valore restituito è una delle costanti di [RevisionColor](../../com.aspose.words/revisioncolor/).
### getDeletedTextEffect() {#getDeletedTextEffect}
```
public int getDeletedTextEffect()
```


Consente di specificare l'effetto da applicare al contenuto eliminato [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). Il valore predefinito è [RevisionTextEffect.STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect/\#STRIKE-THROUGH).

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni.

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
int - Il valore int corrispondente. Il valore restituito è una delle costanti di [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/).
### getInsertCellColor() {#getInsertCellColor}
```
public int getInsertCellColor()
```


Consente di specificare il colore da utilizzare per le celle inserite [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). Il valore predefinito è [RevisionColor.BLUE](../../com.aspose.words/revisioncolor/\#BLUE).

 **Examples:** 

Mostra come lavorare con il colore di revisione per l'inserimento/cancellazione di celle.

```

 Document doc = new Document(getMyDir() + "Cell revisions.docx");

 doc.getLayoutOptions().getRevisionOptions().setInsertCellColor(RevisionColor.BLUE);
 doc.getLayoutOptions().getRevisionOptions().setDeleteCellColor(RevisionColor.DARK_RED);

 doc.save(getArtifactsDir() + "Revision.RevisionCellColor.pdf");
 
```

**Returns:**
int - Il valore int corrispondente. Il valore restituito è una delle costanti di [RevisionColor](../../com.aspose.words/revisioncolor/).
### getInsertedTextColor() {#getInsertedTextColor}
```
public int getInsertedTextColor()
```


Consente di specificare il colore da utilizzare per il contenuto inserito [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). Il valore predefinito è [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni in un documento di output renderizzato.

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
int - Il valore int corrispondente. Il valore restituito è una delle costanti di [RevisionColor](../../com.aspose.words/revisioncolor/).
### getInsertedTextEffect() {#getInsertedTextEffect}
```
public int getInsertedTextEffect()
```


Consente di specificare l'effetto da applicare al contenuto inserito [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). Il valore predefinito è [RevisionTextEffect.UNDERLINE](../../com.aspose.words/revisiontexteffect/\#UNDERLINE).

**Returns:**
int - Il valore int corrispondente. Il valore restituito è una delle costanti di [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/).
### getMeasurementUnit() {#getMeasurementUnit}
```
public int getMeasurementUnit()
```


Consente di specificare le unità di misura per i commenti di revisione. Il valore predefinito è [MeasurementUnits.CENTIMETERS](../../com.aspose.words/measurementunits/\#CENTIMETERS).

**Returns:**
int - Il valore int corrispondente. Il valore restituito è una delle costanti di [MeasurementUnits](../../com.aspose.words/measurementunits/).
### getMovedFromTextColor() {#getMovedFromTextColor}
```
public int getMovedFromTextColor()
```


Consente di specificare il colore da utilizzare per le aree da cui il contenuto è stato spostato [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Il valore predefinito è [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni.

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
int - Il valore int corrispondente. Il valore restituito è una delle costanti di [RevisionColor](../../com.aspose.words/revisioncolor/).
### getMovedFromTextEffect() {#getMovedFromTextEffect}
```
public int getMovedFromTextEffect()
```


Consente di specificare l'effetto da applicare alle aree da cui il contenuto è stato spostato [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Il valore predefinito è [RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect/\#DOUBLE-STRIKE-THROUGH).

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni.

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
int - Il valore int corrispondente. Il valore restituito è una delle costanti di [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/).
### getMovedToTextColor() {#getMovedToTextColor}
```
public int getMovedToTextColor()
```


Consente di specificare il colore da utilizzare per le aree verso cui il contenuto è stato spostato [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Il valore predefinito è [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni.

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
int - Il valore int corrispondente. Il valore restituito è una delle costanti di [RevisionColor](../../com.aspose.words/revisioncolor/).
### getMovedToTextEffect() {#getMovedToTextEffect}
```
public int getMovedToTextEffect()
```


Consente di specificare l'effetto da applicare alle aree verso cui il contenuto è stato spostato [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Il valore predefinito è [RevisionTextEffect.DOUBLE\_UNDERLINE](../../com.aspose.words/revisiontexteffect/\#DOUBLE-UNDERLINE).

**Returns:**
int - Il valore int corrispondente. Il valore restituito è una delle costanti di [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/).
### getRevisedPropertiesColor() {#getRevisedPropertiesColor}
```
public int getRevisedPropertiesColor()
```


Consente di specificare il colore da utilizzare per il contenuto con modifiche delle proprietà di formattazione [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE) Il valore predefinito è [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT).

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni.

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
int - Il valore int corrispondente. Il valore restituito è una delle costanti di [RevisionColor](../../com.aspose.words/revisioncolor/).
### getRevisedPropertiesEffect() {#getRevisedPropertiesEffect}
```
public int getRevisedPropertiesEffect()
```


Consente di specificare l'effetto per le aree di contenuto con modifiche delle proprietà di formattazione [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE) Il valore predefinito è [RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect/\#NONE).

**Returns:**
int - Il valore int corrispondente. Il valore restituito è una delle costanti di [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/).
### getRevisionBarsColor() {#getRevisionBarsColor}
```
public int getRevisionBarsColor()
```


Consente di specificare il colore da utilizzare per le barre laterali che identificano le righe del documento contenenti informazioni revisionate. Il valore predefinito è [RevisionColor.RED](../../com.aspose.words/revisioncolor/\#RED).

 **Remarks:** 

Impostare questa proprietà sui valori [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR) o [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT) comporterà la nasconditura delle barre di revisione dal layout.

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni.

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
int - Il valore int corrispondente. Il valore restituito è una delle costanti di [RevisionColor](../../com.aspose.words/revisioncolor/).
### getRevisionBarsPosition() {#getRevisionBarsPosition}
```
public int getRevisionBarsPosition()
```


Ottiene la posizione di rendering delle barre di revisione. Il valore predefinito è [HorizontalAlignment.OUTSIDE](../../com.aspose.words/horizontalalignment/\#OUTSIDE).

**Returns:**
int - Posizione di rendering delle barre di revisione. Il valore restituito è una delle costanti di [HorizontalAlignment](../../com.aspose.words/horizontalalignment/).
### getRevisionBarsWidth() {#getRevisionBarsWidth}
```
public float getRevisionBarsWidth()
```


Ottiene la larghezza delle barre di revisione, punti.

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni.

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
float - Larghezza delle barre di revisione, punti.
### getShowInBalloons() {#getShowInBalloons}
```
public int getShowInBalloons()
```


Consente di specificare se le revisioni vengono visualizzate nei balloon. Il valore predefinito è [ShowInBalloons.NONE](../../com.aspose.words/showinballoons/\#NONE).

 **Remarks:** 

Nota che le revisioni non vengono visualizzate nei balloon per [CommentDisplayMode.SHOW\_IN\_ANNOTATIONS](../../com.aspose.words/commentdisplaymode/\#SHOW-IN-ANNOTATIONS).

 **Examples:** 

Mostra come visualizzare le revisioni nei balloon.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // By default, text that is a revision has a different color to differentiate it from the other non-revision text.
 // Set a revision option to show more details about each revision in a balloon on the page's right margin.
 doc.getLayoutOptions().getRevisionOptions().setShowInBalloons(ShowInBalloons.FORMAT_AND_DELETE);
 doc.save(getArtifactsDir() + "Revision.ShowRevisionBalloons.pdf");
 
```

Mostra come modificare l'aspetto delle revisioni.

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
int - Il valore int corrispondente. Il valore restituito è una delle costanti di [ShowInBalloons](../../com.aspose.words/showinballoons/).
### getShowOriginalRevision() {#getShowOriginalRevision}
```
public boolean getShowOriginalRevision()
```


Consente di specificare se il testo originale deve essere mostrato al posto di quello revisionato. Il valore predefinito è false.

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni.

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
boolean - Il valore booleano corrispondente.
### getShowRevisionBars() {#getShowRevisionBars}
```
public boolean getShowRevisionBars()
```


Consente di specificare se le barre di revisione devono essere visualizzate vicino alle righe contenenti contenuto revisionato. Il valore predefinito è true.

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni in un documento di output renderizzato.

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
boolean - Il valore booleano corrispondente.
### getShowRevisionMarks() {#getShowRevisionMarks}
```
public boolean getShowRevisionMarks()
```


Consente di specificare se il testo della revisione deve essere contrassegnato con una formattazione speciale. Il valore predefinito è true.

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni.

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
boolean - Il valore booleano corrispondente.
### setCommentColor(int value) {#setCommentColor-int}
```
public void setCommentColor(int value)
```


Consente di specificare il colore da utilizzare per i commenti. Il valore predefinito è [RevisionColor.RED](../../com.aspose.words/revisioncolor/\#RED).

 **Remarks:** 

Se si imposta questa proprietà sui valori [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR) o [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT), il risultato sarà che questa proprietà verrà impostata sul colore predefinito.

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore int corrispondente. Il valore deve essere una delle costanti di [RevisionColor](../../com.aspose.words/revisioncolor/). |

### setDeleteCellColor(int value) {#setDeleteCellColor-int}
```
public void setDeleteCellColor(int value)
```


Consente di specificare il colore da utilizzare per le celle eliminate [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). Il valore predefinito è [RevisionColor.PINK](../../com.aspose.words/revisioncolor/\#PINK).

 **Examples:** 

Mostra come lavorare con il colore di revisione per l'inserimento/cancellazione di celle.

```

 Document doc = new Document(getMyDir() + "Cell revisions.docx");

 doc.getLayoutOptions().getRevisionOptions().setInsertCellColor(RevisionColor.BLUE);
 doc.getLayoutOptions().getRevisionOptions().setDeleteCellColor(RevisionColor.DARK_RED);

 doc.save(getArtifactsDir() + "Revision.RevisionCellColor.pdf");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore int corrispondente. Il valore deve essere una delle costanti di [RevisionColor](../../com.aspose.words/revisioncolor/). |

### setDeletedTextColor(int value) {#setDeletedTextColor-int}
```
public void setDeletedTextColor(int value)
```


Consente di specificare il colore da utilizzare per il contenuto eliminato [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). Il valore predefinito è [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore int corrispondente. Il valore deve essere una delle costanti di [RevisionColor](../../com.aspose.words/revisioncolor/). |

### setDeletedTextEffect(int value) {#setDeletedTextEffect-int}
```
public void setDeletedTextEffect(int value)
```


Consente di specificare l'effetto da applicare al contenuto eliminato [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). Il valore predefinito è [RevisionTextEffect.STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect/\#STRIKE-THROUGH).

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore int corrispondente. Il valore deve essere una delle costanti di [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/). |

### setInsertCellColor(int value) {#setInsertCellColor-int}
```
public void setInsertCellColor(int value)
```


Consente di specificare il colore da utilizzare per le celle inserite [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). Il valore predefinito è [RevisionColor.BLUE](../../com.aspose.words/revisioncolor/\#BLUE).

 **Examples:** 

Mostra come lavorare con il colore di revisione per l'inserimento/cancellazione di celle.

```

 Document doc = new Document(getMyDir() + "Cell revisions.docx");

 doc.getLayoutOptions().getRevisionOptions().setInsertCellColor(RevisionColor.BLUE);
 doc.getLayoutOptions().getRevisionOptions().setDeleteCellColor(RevisionColor.DARK_RED);

 doc.save(getArtifactsDir() + "Revision.RevisionCellColor.pdf");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore int corrispondente. Il valore deve essere una delle costanti di [RevisionColor](../../com.aspose.words/revisioncolor/). |

### setInsertedTextColor(int value) {#setInsertedTextColor-int}
```
public void setInsertedTextColor(int value)
```


Consente di specificare il colore da utilizzare per il contenuto inserito [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). Il valore predefinito è [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni in un documento di output renderizzato.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore int corrispondente. Il valore deve essere una delle costanti di [RevisionColor](../../com.aspose.words/revisioncolor/). |

### setInsertedTextEffect(int value) {#setInsertedTextEffect-int}
```
public void setInsertedTextEffect(int value)
```


Consente di specificare l'effetto da applicare al contenuto inserito [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). Il valore predefinito è [RevisionTextEffect.UNDERLINE](../../com.aspose.words/revisiontexteffect/\#UNDERLINE).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore int corrispondente. Il valore deve essere una delle costanti di [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/). |

### setMeasurementUnit(int value) {#setMeasurementUnit-int}
```
public void setMeasurementUnit(int value)
```


Consente di specificare le unità di misura per i commenti di revisione. Il valore predefinito è [MeasurementUnits.CENTIMETERS](../../com.aspose.words/measurementunits/\#CENTIMETERS).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore int corrispondente. Il valore deve essere una delle costanti di [MeasurementUnits](../../com.aspose.words/measurementunits/). |

### setMovedFromTextColor(int value) {#setMovedFromTextColor-int}
```
public void setMovedFromTextColor(int value)
```


Consente di specificare il colore da utilizzare per le aree da cui il contenuto è stato spostato [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Il valore predefinito è [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore int corrispondente. Il valore deve essere una delle costanti di [RevisionColor](../../com.aspose.words/revisioncolor/). |

### setMovedFromTextEffect(int value) {#setMovedFromTextEffect-int}
```
public void setMovedFromTextEffect(int value)
```


Consente di specificare l'effetto da applicare alle aree da cui il contenuto è stato spostato [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Il valore predefinito è [RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect/\#DOUBLE-STRIKE-THROUGH).

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore int corrispondente. Il valore deve essere una delle costanti di [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/). |

### setMovedToTextColor(int value) {#setMovedToTextColor-int}
```
public void setMovedToTextColor(int value)
```


Consente di specificare il colore da utilizzare per le aree verso cui il contenuto è stato spostato [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Il valore predefinito è [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore int corrispondente. Il valore deve essere una delle costanti di [RevisionColor](../../com.aspose.words/revisioncolor/). |

### setMovedToTextEffect(int value) {#setMovedToTextEffect-int}
```
public void setMovedToTextEffect(int value)
```


Consente di specificare l'effetto da applicare alle aree verso cui il contenuto è stato spostato [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Il valore predefinito è [RevisionTextEffect.DOUBLE\_UNDERLINE](../../com.aspose.words/revisiontexteffect/\#DOUBLE-UNDERLINE).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore int corrispondente. Il valore deve essere una delle costanti di [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/). |

### setRevisedPropertiesColor(int value) {#setRevisedPropertiesColor-int}
```
public void setRevisedPropertiesColor(int value)
```


Consente di specificare il colore da utilizzare per il contenuto con modifiche delle proprietà di formattazione [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE) Il valore predefinito è [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT).

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore int corrispondente. Il valore deve essere una delle costanti di [RevisionColor](../../com.aspose.words/revisioncolor/). |

### setRevisedPropertiesEffect(int value) {#setRevisedPropertiesEffect-int}
```
public void setRevisedPropertiesEffect(int value)
```


Consente di specificare l'effetto per le aree di contenuto con modifiche delle proprietà di formattazione [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE) Il valore predefinito è [RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect/\#NONE).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore int corrispondente. Il valore deve essere una delle costanti di [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/). |

### setRevisionBarsColor(int value) {#setRevisionBarsColor-int}
```
public void setRevisionBarsColor(int value)
```


Consente di specificare il colore da utilizzare per le barre laterali che identificano le righe del documento contenenti informazioni revisionate. Il valore predefinito è [RevisionColor.RED](../../com.aspose.words/revisioncolor/\#RED).

 **Remarks:** 

Impostare questa proprietà sui valori [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR) o [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT) comporterà la nasconditura delle barre di revisione dal layout.

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore int corrispondente. Il valore deve essere una delle costanti di [RevisionColor](../../com.aspose.words/revisioncolor/). |

### setRevisionBarsPosition(int value) {#setRevisionBarsPosition-int}
```
public void setRevisionBarsPosition(int value)
```


Imposta la posizione di rendering delle barre di revisione. Il valore predefinito è [HorizontalAlignment.OUTSIDE](../../com.aspose.words/horizontalalignment/\#OUTSIDE).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Posizione di rendering delle barre di revisione. Il valore deve essere una delle costanti di [HorizontalAlignment](../../com.aspose.words/horizontalalignment/). |

### setRevisionBarsWidth(float value) {#setRevisionBarsWidth-float}
```
public void setRevisionBarsWidth(float value)
```


Imposta la larghezza delle barre di revisione, punti.

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | float | Larghezza delle barre di revisione, punti. |

### setShowInBalloons(int value) {#setShowInBalloons-int}
```
public void setShowInBalloons(int value)
```


Consente di specificare se le revisioni vengono visualizzate nei balloon. Il valore predefinito è [ShowInBalloons.NONE](../../com.aspose.words/showinballoons/\#NONE).

 **Remarks:** 

Nota che le revisioni non vengono visualizzate nei balloon per [CommentDisplayMode.SHOW\_IN\_ANNOTATIONS](../../com.aspose.words/commentdisplaymode/\#SHOW-IN-ANNOTATIONS).

 **Examples:** 

Mostra come visualizzare le revisioni nei balloon.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // By default, text that is a revision has a different color to differentiate it from the other non-revision text.
 // Set a revision option to show more details about each revision in a balloon on the page's right margin.
 doc.getLayoutOptions().getRevisionOptions().setShowInBalloons(ShowInBalloons.FORMAT_AND_DELETE);
 doc.save(getArtifactsDir() + "Revision.ShowRevisionBalloons.pdf");
 
```

Mostra come modificare l'aspetto delle revisioni.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore int corrispondente. Il valore deve essere una delle costanti di [ShowInBalloons](../../com.aspose.words/showinballoons/). |

### setShowOriginalRevision(boolean value) {#setShowOriginalRevision-boolean}
```
public void setShowOriginalRevision(boolean value)
```


Consente di specificare se il testo originale deve essere mostrato al posto di quello revisionato. Il valore predefinito è false.

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setShowRevisionBars(boolean value) {#setShowRevisionBars-boolean}
```
public void setShowRevisionBars(boolean value)
```


Consente di specificare se le barre di revisione devono essere visualizzate vicino alle righe contenenti contenuto revisionato. Il valore predefinito è true.

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni in un documento di output renderizzato.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setShowRevisionMarks(boolean value) {#setShowRevisionMarks-boolean}
```
public void setShowRevisionMarks(boolean value)
```


Consente di specificare se il testo della revisione deve essere contrassegnato con una formattazione speciale. Il valore predefinito è true.

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

