---
title: RevisionOptions
linktitle: RevisionOptions
second_title: Aspose.Words for Java
description: Allows to control how document revisions are handled during layout process in Java.
type: docs
weight: 573
url: /java/com.aspose.words/revisionoptions/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class RevisionOptions implements Cloneable
```

Allows to control how document revisions are handled during layout process.

To learn more, visit the [ Converting to Fixed-page Format ][Converting to Fixed-page Format] documentation article.

 **Examples:** 

Shows how to alter the appearance of revisions in a rendered output document.

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
## Methods

| Method | Description |
| --- | --- |
| [getCommentColor()](#getCommentColor) | Allows to specify the color to be used for comments. |
| [getDeleteCellColor()](#getDeleteCellColor) | Allows to specify the color to be used for deleted cells [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [getDeletedTextColor()](#getDeletedTextColor) | Allows to specify the color to be used for deleted content [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [getDeletedTextEffect()](#getDeletedTextEffect) | Allows to specify the effect to be applied to the deleted content [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [getInsertCellColor()](#getInsertCellColor) | Allows to specify the color to be used for inserted cells [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [getInsertedTextColor()](#getInsertedTextColor) | Allows to specify the color to be used for inserted content [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [getInsertedTextEffect()](#getInsertedTextEffect) | Allows to specify the effect to be applied to the inserted content [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [getMeasurementUnit()](#getMeasurementUnit) | Allows to specify the measurement units for revision comments. |
| [getMovedFromTextColor()](#getMovedFromTextColor) | Allows to specify the color to be used for areas where content was moved from [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [getMovedFromTextEffect()](#getMovedFromTextEffect) | Allows to specify the effect to be applied to the areas where content was moved from [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [getMovedToTextColor()](#getMovedToTextColor) | Allows to specify the color to be used for areas where content was moved to [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [getMovedToTextEffect()](#getMovedToTextEffect) | Allows to specify the effect to be applied to the areas where content was moved to [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [getRevisedPropertiesColor()](#getRevisedPropertiesColor) | Allows to specify the color to be used for content with changes of formatting properties [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE) Default value is [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT). |
| [getRevisedPropertiesEffect()](#getRevisedPropertiesEffect) | Allows to specify the effect for content areas with changes of formatting properties [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE) Default value is [RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect/\#NONE) |
| [getRevisionBarsColor()](#getRevisionBarsColor) | Allows to specify the color to be used for side bars that identify document lines containing revised information. |
| [getRevisionBarsPosition()](#getRevisionBarsPosition) | Gets rendering position of revision bars. |
| [getRevisionBarsWidth()](#getRevisionBarsWidth) | Gets width of revision bars, points. |
| [getShowInBalloons()](#getShowInBalloons) | Allows to specify whether the revisions are rendered in the balloons. |
| [getShowOriginalRevision()](#getShowOriginalRevision) | Allows to specify whether the original text should be shown instead of revised one. |
| [getShowRevisionBars()](#getShowRevisionBars) | Allows to specify whether revision bars should be rendered near lines containing revised content. |
| [getShowRevisionMarks()](#getShowRevisionMarks) | Allow to specify whether revision text should be marked with special formatting markup. |
| [setCommentColor(int value)](#setCommentColor-int) | Allows to specify the color to be used for comments. |
| [setDeleteCellColor(int value)](#setDeleteCellColor-int) | Allows to specify the color to be used for deleted cells [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [setDeletedTextColor(int value)](#setDeletedTextColor-int) | Allows to specify the color to be used for deleted content [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [setDeletedTextEffect(int value)](#setDeletedTextEffect-int) | Allows to specify the effect to be applied to the deleted content [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [setInsertCellColor(int value)](#setInsertCellColor-int) | Allows to specify the color to be used for inserted cells [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [setInsertedTextColor(int value)](#setInsertedTextColor-int) | Allows to specify the color to be used for inserted content [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [setInsertedTextEffect(int value)](#setInsertedTextEffect-int) | Allows to specify the effect to be applied to the inserted content [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [setMeasurementUnit(int value)](#setMeasurementUnit-int) | Allows to specify the measurement units for revision comments. |
| [setMovedFromTextColor(int value)](#setMovedFromTextColor-int) | Allows to specify the color to be used for areas where content was moved from [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [setMovedFromTextEffect(int value)](#setMovedFromTextEffect-int) | Allows to specify the effect to be applied to the areas where content was moved from [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [setMovedToTextColor(int value)](#setMovedToTextColor-int) | Allows to specify the color to be used for areas where content was moved to [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [setMovedToTextEffect(int value)](#setMovedToTextEffect-int) | Allows to specify the effect to be applied to the areas where content was moved to [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [setRevisedPropertiesColor(int value)](#setRevisedPropertiesColor-int) | Allows to specify the color to be used for content with changes of formatting properties [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE) Default value is [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT). |
| [setRevisedPropertiesEffect(int value)](#setRevisedPropertiesEffect-int) | Allows to specify the effect for content areas with changes of formatting properties [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE) Default value is [RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect/\#NONE) |
| [setRevisionBarsColor(int value)](#setRevisionBarsColor-int) | Allows to specify the color to be used for side bars that identify document lines containing revised information. |
| [setRevisionBarsPosition(int value)](#setRevisionBarsPosition-int) | Sets rendering position of revision bars. |
| [setRevisionBarsWidth(float value)](#setRevisionBarsWidth-float) | Sets width of revision bars, points. |
| [setShowInBalloons(int value)](#setShowInBalloons-int) | Allows to specify whether the revisions are rendered in the balloons. |
| [setShowOriginalRevision(boolean value)](#setShowOriginalRevision-boolean) | Allows to specify whether the original text should be shown instead of revised one. |
| [setShowRevisionBars(boolean value)](#setShowRevisionBars-boolean) | Allows to specify whether revision bars should be rendered near lines containing revised content. |
| [setShowRevisionMarks(boolean value)](#setShowRevisionMarks-boolean) | Allow to specify whether revision text should be marked with special formatting markup. |
### getCommentColor() {#getCommentColor}
```
public int getCommentColor()
```


Allows to specify the color to be used for comments. Default value is [RevisionColor.RED](../../com.aspose.words/revisioncolor/\#RED).

 **Remarks:** 

If set this property to [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR) or [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT) values, as the result this property will be set to default color.

 **Examples:** 

Shows how to modify the appearance of revisions.

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
int - The corresponding  int  value. The returned value is one of [RevisionColor](../../com.aspose.words/revisioncolor/) constants.
### getDeleteCellColor() {#getDeleteCellColor}
```
public int getDeleteCellColor()
```


Allows to specify the color to be used for deleted cells [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). Default value is [RevisionColor.PINK](../../com.aspose.words/revisioncolor/\#PINK).

 **Examples:** 

Shows how to work with insert/delete cell revision color.

```

 Document doc = new Document(getMyDir() + "Cell revisions.docx");

 doc.getLayoutOptions().getRevisionOptions().setInsertCellColor(RevisionColor.BLUE);
 doc.getLayoutOptions().getRevisionOptions().setDeleteCellColor(RevisionColor.DARK_RED);

 doc.save(getArtifactsDir() + "Revision.RevisionCellColor.pdf");
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [RevisionColor](../../com.aspose.words/revisioncolor/) constants.
### getDeletedTextColor() {#getDeletedTextColor}
```
public int getDeletedTextColor()
```


Allows to specify the color to be used for deleted content [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). Default value is [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Shows how to modify the appearance of revisions.

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
int - The corresponding  int  value. The returned value is one of [RevisionColor](../../com.aspose.words/revisioncolor/) constants.
### getDeletedTextEffect() {#getDeletedTextEffect}
```
public int getDeletedTextEffect()
```


Allows to specify the effect to be applied to the deleted content [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). Default value is [RevisionTextEffect.STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect/\#STRIKE-THROUGH)

 **Examples:** 

Shows how to modify the appearance of revisions.

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
int - The corresponding  int  value. The returned value is one of [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/) constants.
### getInsertCellColor() {#getInsertCellColor}
```
public int getInsertCellColor()
```


Allows to specify the color to be used for inserted cells [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). Default value is [RevisionColor.BLUE](../../com.aspose.words/revisioncolor/\#BLUE).

 **Examples:** 

Shows how to work with insert/delete cell revision color.

```

 Document doc = new Document(getMyDir() + "Cell revisions.docx");

 doc.getLayoutOptions().getRevisionOptions().setInsertCellColor(RevisionColor.BLUE);
 doc.getLayoutOptions().getRevisionOptions().setDeleteCellColor(RevisionColor.DARK_RED);

 doc.save(getArtifactsDir() + "Revision.RevisionCellColor.pdf");
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [RevisionColor](../../com.aspose.words/revisioncolor/) constants.
### getInsertedTextColor() {#getInsertedTextColor}
```
public int getInsertedTextColor()
```


Allows to specify the color to be used for inserted content [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). Default value is [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Shows how to alter the appearance of revisions in a rendered output document.

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
int - The corresponding  int  value. The returned value is one of [RevisionColor](../../com.aspose.words/revisioncolor/) constants.
### getInsertedTextEffect() {#getInsertedTextEffect}
```
public int getInsertedTextEffect()
```


Allows to specify the effect to be applied to the inserted content [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). Default value is [RevisionTextEffect.UNDERLINE](../../com.aspose.words/revisiontexteffect/\#UNDERLINE).

**Returns:**
int - The corresponding  int  value. The returned value is one of [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/) constants.
### getMeasurementUnit() {#getMeasurementUnit}
```
public int getMeasurementUnit()
```


Allows to specify the measurement units for revision comments. Default value is [MeasurementUnits.CENTIMETERS](../../com.aspose.words/measurementunits/\#CENTIMETERS)

 **Examples:** 

Shows how to make a saved document conform to an older ODT schema.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 OdtSaveOptions saveOptions = new OdtSaveOptions();
 {
     saveOptions.setMeasureUnit(OdtSaveMeasureUnit.CENTIMETERS);
     saveOptions.isStrictSchema11(exportToOdt11Specs);
 }

 doc.save(getArtifactsDir() + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [MeasurementUnits](../../com.aspose.words/measurementunits/) constants.
### getMovedFromTextColor() {#getMovedFromTextColor}
```
public int getMovedFromTextColor()
```


Allows to specify the color to be used for areas where content was moved from [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Default value is [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Shows how to modify the appearance of revisions.

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
int - The corresponding  int  value. The returned value is one of [RevisionColor](../../com.aspose.words/revisioncolor/) constants.
### getMovedFromTextEffect() {#getMovedFromTextEffect}
```
public int getMovedFromTextEffect()
```


Allows to specify the effect to be applied to the areas where content was moved from [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Default value is [RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect/\#DOUBLE-STRIKE-THROUGH)

 **Examples:** 

Shows how to modify the appearance of revisions.

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
int - The corresponding  int  value. The returned value is one of [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/) constants.
### getMovedToTextColor() {#getMovedToTextColor}
```
public int getMovedToTextColor()
```


Allows to specify the color to be used for areas where content was moved to [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Default value is [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Shows how to modify the appearance of revisions.

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
int - The corresponding  int  value. The returned value is one of [RevisionColor](../../com.aspose.words/revisioncolor/) constants.
### getMovedToTextEffect() {#getMovedToTextEffect}
```
public int getMovedToTextEffect()
```


Allows to specify the effect to be applied to the areas where content was moved to [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Default value is [RevisionTextEffect.DOUBLE\_UNDERLINE](../../com.aspose.words/revisiontexteffect/\#DOUBLE-UNDERLINE)

**Returns:**
int - The corresponding  int  value. The returned value is one of [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/) constants.
### getRevisedPropertiesColor() {#getRevisedPropertiesColor}
```
public int getRevisedPropertiesColor()
```


Allows to specify the color to be used for content with changes of formatting properties [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE) Default value is [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT).

 **Examples:** 

Shows how to modify the appearance of revisions.

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
int - The corresponding  int  value. The returned value is one of [RevisionColor](../../com.aspose.words/revisioncolor/) constants.
### getRevisedPropertiesEffect() {#getRevisedPropertiesEffect}
```
public int getRevisedPropertiesEffect()
```


Allows to specify the effect for content areas with changes of formatting properties [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE) Default value is [RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect/\#NONE)

**Returns:**
int - The corresponding  int  value. The returned value is one of [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/) constants.
### getRevisionBarsColor() {#getRevisionBarsColor}
```
public int getRevisionBarsColor()
```


Allows to specify the color to be used for side bars that identify document lines containing revised information. Default value is [RevisionColor.RED](../../com.aspose.words/revisioncolor/\#RED).

 **Remarks:** 

Setting this property to [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR) or [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT) values will result in hiding revision bars from the layout.

 **Examples:** 

Shows how to modify the appearance of revisions.

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
int - The corresponding  int  value. The returned value is one of [RevisionColor](../../com.aspose.words/revisioncolor/) constants.
### getRevisionBarsPosition() {#getRevisionBarsPosition}
```
public int getRevisionBarsPosition()
```


Gets rendering position of revision bars. Default value is [HorizontalAlignment.OUTSIDE](../../com.aspose.words/horizontalalignment/\#OUTSIDE).

**Returns:**
int - Rendering position of revision bars. The returned value is one of [HorizontalAlignment](../../com.aspose.words/horizontalalignment/) constants.
### getRevisionBarsWidth() {#getRevisionBarsWidth}
```
public float getRevisionBarsWidth()
```


Gets width of revision bars, points.

 **Examples:** 

Shows how to modify the appearance of revisions.

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
float - Width of revision bars, points.
### getShowInBalloons() {#getShowInBalloons}
```
public int getShowInBalloons()
```


Allows to specify whether the revisions are rendered in the balloons. Default value is [ShowInBalloons.NONE](../../com.aspose.words/showinballoons/\#NONE).

 **Remarks:** 

Note that revisions are not rendered in balloons for [CommentDisplayMode.SHOW\_IN\_ANNOTATIONS](../../com.aspose.words/commentdisplaymode/\#SHOW-IN-ANNOTATIONS).

 **Examples:** 

Shows how to display revisions in balloons.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // By default, text that is a revision has a different color to differentiate it from the other non-revision text.
 // Set a revision option to show more details about each revision in a balloon on the page's right margin.
 doc.getLayoutOptions().getRevisionOptions().setShowInBalloons(ShowInBalloons.FORMAT_AND_DELETE);
 doc.save(getArtifactsDir() + "Revision.ShowRevisionBalloons.pdf");
 
```

Shows how to modify the appearance of revisions.

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
int - The corresponding  int  value. The returned value is one of [ShowInBalloons](../../com.aspose.words/showinballoons/) constants.
### getShowOriginalRevision() {#getShowOriginalRevision}
```
public boolean getShowOriginalRevision()
```


Allows to specify whether the original text should be shown instead of revised one. Default value is  false .

 **Examples:** 

Shows how to modify the appearance of revisions.

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
boolean - The corresponding  boolean  value.
### getShowRevisionBars() {#getShowRevisionBars}
```
public boolean getShowRevisionBars()
```


Allows to specify whether revision bars should be rendered near lines containing revised content. Default value is  true .

 **Examples:** 

Shows how to alter the appearance of revisions in a rendered output document.

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
boolean - The corresponding  boolean  value.
### getShowRevisionMarks() {#getShowRevisionMarks}
```
public boolean getShowRevisionMarks()
```


Allow to specify whether revision text should be marked with special formatting markup. Default value is  true .

 **Examples:** 

Shows how to modify the appearance of revisions.

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
boolean - The corresponding  boolean  value.
### setCommentColor(int value) {#setCommentColor-int}
```
public void setCommentColor(int value)
```


Allows to specify the color to be used for comments. Default value is [RevisionColor.RED](../../com.aspose.words/revisioncolor/\#RED).

 **Remarks:** 

If set this property to [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR) or [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT) values, as the result this property will be set to default color.

 **Examples:** 

Shows how to modify the appearance of revisions.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionColor](../../com.aspose.words/revisioncolor/) constants. |

### setDeleteCellColor(int value) {#setDeleteCellColor-int}
```
public void setDeleteCellColor(int value)
```


Allows to specify the color to be used for deleted cells [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). Default value is [RevisionColor.PINK](../../com.aspose.words/revisioncolor/\#PINK).

 **Examples:** 

Shows how to work with insert/delete cell revision color.

```

 Document doc = new Document(getMyDir() + "Cell revisions.docx");

 doc.getLayoutOptions().getRevisionOptions().setInsertCellColor(RevisionColor.BLUE);
 doc.getLayoutOptions().getRevisionOptions().setDeleteCellColor(RevisionColor.DARK_RED);

 doc.save(getArtifactsDir() + "Revision.RevisionCellColor.pdf");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionColor](../../com.aspose.words/revisioncolor/) constants. |

### setDeletedTextColor(int value) {#setDeletedTextColor-int}
```
public void setDeletedTextColor(int value)
```


Allows to specify the color to be used for deleted content [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). Default value is [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Shows how to modify the appearance of revisions.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionColor](../../com.aspose.words/revisioncolor/) constants. |

### setDeletedTextEffect(int value) {#setDeletedTextEffect-int}
```
public void setDeletedTextEffect(int value)
```


Allows to specify the effect to be applied to the deleted content [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). Default value is [RevisionTextEffect.STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect/\#STRIKE-THROUGH)

 **Examples:** 

Shows how to modify the appearance of revisions.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/) constants. |

### setInsertCellColor(int value) {#setInsertCellColor-int}
```
public void setInsertCellColor(int value)
```


Allows to specify the color to be used for inserted cells [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). Default value is [RevisionColor.BLUE](../../com.aspose.words/revisioncolor/\#BLUE).

 **Examples:** 

Shows how to work with insert/delete cell revision color.

```

 Document doc = new Document(getMyDir() + "Cell revisions.docx");

 doc.getLayoutOptions().getRevisionOptions().setInsertCellColor(RevisionColor.BLUE);
 doc.getLayoutOptions().getRevisionOptions().setDeleteCellColor(RevisionColor.DARK_RED);

 doc.save(getArtifactsDir() + "Revision.RevisionCellColor.pdf");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionColor](../../com.aspose.words/revisioncolor/) constants. |

### setInsertedTextColor(int value) {#setInsertedTextColor-int}
```
public void setInsertedTextColor(int value)
```


Allows to specify the color to be used for inserted content [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). Default value is [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Shows how to alter the appearance of revisions in a rendered output document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionColor](../../com.aspose.words/revisioncolor/) constants. |

### setInsertedTextEffect(int value) {#setInsertedTextEffect-int}
```
public void setInsertedTextEffect(int value)
```


Allows to specify the effect to be applied to the inserted content [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). Default value is [RevisionTextEffect.UNDERLINE](../../com.aspose.words/revisiontexteffect/\#UNDERLINE).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/) constants. |

### setMeasurementUnit(int value) {#setMeasurementUnit-int}
```
public void setMeasurementUnit(int value)
```


Allows to specify the measurement units for revision comments. Default value is [MeasurementUnits.CENTIMETERS](../../com.aspose.words/measurementunits/\#CENTIMETERS)

 **Examples:** 

Shows how to make a saved document conform to an older ODT schema.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 OdtSaveOptions saveOptions = new OdtSaveOptions();
 {
     saveOptions.setMeasureUnit(OdtSaveMeasureUnit.CENTIMETERS);
     saveOptions.isStrictSchema11(exportToOdt11Specs);
 }

 doc.save(getArtifactsDir() + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [MeasurementUnits](../../com.aspose.words/measurementunits/) constants. |

### setMovedFromTextColor(int value) {#setMovedFromTextColor-int}
```
public void setMovedFromTextColor(int value)
```


Allows to specify the color to be used for areas where content was moved from [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Default value is [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Shows how to modify the appearance of revisions.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionColor](../../com.aspose.words/revisioncolor/) constants. |

### setMovedFromTextEffect(int value) {#setMovedFromTextEffect-int}
```
public void setMovedFromTextEffect(int value)
```


Allows to specify the effect to be applied to the areas where content was moved from [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Default value is [RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect/\#DOUBLE-STRIKE-THROUGH)

 **Examples:** 

Shows how to modify the appearance of revisions.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/) constants. |

### setMovedToTextColor(int value) {#setMovedToTextColor-int}
```
public void setMovedToTextColor(int value)
```


Allows to specify the color to be used for areas where content was moved to [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Default value is [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Shows how to modify the appearance of revisions.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionColor](../../com.aspose.words/revisioncolor/) constants. |

### setMovedToTextEffect(int value) {#setMovedToTextEffect-int}
```
public void setMovedToTextEffect(int value)
```


Allows to specify the effect to be applied to the areas where content was moved to [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Default value is [RevisionTextEffect.DOUBLE\_UNDERLINE](../../com.aspose.words/revisiontexteffect/\#DOUBLE-UNDERLINE)

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/) constants. |

### setRevisedPropertiesColor(int value) {#setRevisedPropertiesColor-int}
```
public void setRevisedPropertiesColor(int value)
```


Allows to specify the color to be used for content with changes of formatting properties [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE) Default value is [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT).

 **Examples:** 

Shows how to modify the appearance of revisions.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionColor](../../com.aspose.words/revisioncolor/) constants. |

### setRevisedPropertiesEffect(int value) {#setRevisedPropertiesEffect-int}
```
public void setRevisedPropertiesEffect(int value)
```


Allows to specify the effect for content areas with changes of formatting properties [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE) Default value is [RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect/\#NONE)

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/) constants. |

### setRevisionBarsColor(int value) {#setRevisionBarsColor-int}
```
public void setRevisionBarsColor(int value)
```


Allows to specify the color to be used for side bars that identify document lines containing revised information. Default value is [RevisionColor.RED](../../com.aspose.words/revisioncolor/\#RED).

 **Remarks:** 

Setting this property to [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR) or [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT) values will result in hiding revision bars from the layout.

 **Examples:** 

Shows how to modify the appearance of revisions.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionColor](../../com.aspose.words/revisioncolor/) constants. |

### setRevisionBarsPosition(int value) {#setRevisionBarsPosition-int}
```
public void setRevisionBarsPosition(int value)
```


Sets rendering position of revision bars. Default value is [HorizontalAlignment.OUTSIDE](../../com.aspose.words/horizontalalignment/\#OUTSIDE).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Rendering position of revision bars. The value must be one of [HorizontalAlignment](../../com.aspose.words/horizontalalignment/) constants. |

### setRevisionBarsWidth(float value) {#setRevisionBarsWidth-float}
```
public void setRevisionBarsWidth(float value)
```


Sets width of revision bars, points.

 **Examples:** 

Shows how to modify the appearance of revisions.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | float | Width of revision bars, points. |

### setShowInBalloons(int value) {#setShowInBalloons-int}
```
public void setShowInBalloons(int value)
```


Allows to specify whether the revisions are rendered in the balloons. Default value is [ShowInBalloons.NONE](../../com.aspose.words/showinballoons/\#NONE).

 **Remarks:** 

Note that revisions are not rendered in balloons for [CommentDisplayMode.SHOW\_IN\_ANNOTATIONS](../../com.aspose.words/commentdisplaymode/\#SHOW-IN-ANNOTATIONS).

 **Examples:** 

Shows how to display revisions in balloons.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // By default, text that is a revision has a different color to differentiate it from the other non-revision text.
 // Set a revision option to show more details about each revision in a balloon on the page's right margin.
 doc.getLayoutOptions().getRevisionOptions().setShowInBalloons(ShowInBalloons.FORMAT_AND_DELETE);
 doc.save(getArtifactsDir() + "Revision.ShowRevisionBalloons.pdf");
 
```

Shows how to modify the appearance of revisions.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [ShowInBalloons](../../com.aspose.words/showinballoons/) constants. |

### setShowOriginalRevision(boolean value) {#setShowOriginalRevision-boolean}
```
public void setShowOriginalRevision(boolean value)
```


Allows to specify whether the original text should be shown instead of revised one. Default value is  false .

 **Examples:** 

Shows how to modify the appearance of revisions.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setShowRevisionBars(boolean value) {#setShowRevisionBars-boolean}
```
public void setShowRevisionBars(boolean value)
```


Allows to specify whether revision bars should be rendered near lines containing revised content. Default value is  true .

 **Examples:** 

Shows how to alter the appearance of revisions in a rendered output document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setShowRevisionMarks(boolean value) {#setShowRevisionMarks-boolean}
```
public void setShowRevisionMarks(boolean value)
```


Allow to specify whether revision text should be marked with special formatting markup. Default value is  true .

 **Examples:** 

Shows how to modify the appearance of revisions.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

