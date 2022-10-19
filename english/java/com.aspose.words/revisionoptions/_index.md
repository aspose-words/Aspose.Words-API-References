---
title: RevisionOptions
second_title: Aspose.Words for Java API Reference
description: Allows to control how document revisions are handled during layout process.
type: docs
weight: 488
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

To learn more, visit the **Converting to Fixed-page Format** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getShowRevisionMarks()](#getShowRevisionMarks--) | Allow to specify whether revision text should be marked with special formatting markup. |
| [setShowRevisionMarks(boolean value)](#setShowRevisionMarks-boolean-) | Allow to specify whether revision text should be marked with special formatting markup. |
| [getShowRevisionBars()](#getShowRevisionBars--) | Allows to specify whether revision bars should be rendered near lines containing revised content. |
| [setShowRevisionBars(boolean value)](#setShowRevisionBars-boolean-) | Allows to specify whether revision bars should be rendered near lines containing revised content. |
| [getShowOriginalRevision()](#getShowOriginalRevision--) | Allows to specify whether the original text should be shown instead of revised one. |
| [setShowOriginalRevision(boolean value)](#setShowOriginalRevision-boolean-) | Allows to specify whether the original text should be shown instead of revised one. |
| [getInsertedTextColor()](#getInsertedTextColor--) | Allows to specify the color to be used for inserted content [RevisionType.INSERTION](../../com.aspose.words/revisiontype\#INSERTION). |
| [setInsertedTextColor(int value)](#setInsertedTextColor-int-) | Allows to specify the color to be used for inserted content [RevisionType.INSERTION](../../com.aspose.words/revisiontype\#INSERTION). |
| [getInsertedTextEffect()](#getInsertedTextEffect--) | Allows to specify the effect to be applied to the inserted content [RevisionType.INSERTION](../../com.aspose.words/revisiontype\#INSERTION). |
| [setInsertedTextEffect(int value)](#setInsertedTextEffect-int-) | Allows to specify the effect to be applied to the inserted content [RevisionType.INSERTION](../../com.aspose.words/revisiontype\#INSERTION). |
| [getDeletedTextColor()](#getDeletedTextColor--) | Allows to specify the color to be used for deleted content [RevisionType.DELETION](../../com.aspose.words/revisiontype\#DELETION). |
| [setDeletedTextColor(int value)](#setDeletedTextColor-int-) | Allows to specify the color to be used for deleted content [RevisionType.DELETION](../../com.aspose.words/revisiontype\#DELETION). |
| [getDeletedTextEffect()](#getDeletedTextEffect--) | Allows to specify the effect to be applied to the deleted content [RevisionType.DELETION](../../com.aspose.words/revisiontype\#DELETION). |
| [setDeletedTextEffect(int value)](#setDeletedTextEffect-int-) | Allows to specify the effect to be applied to the deleted content [RevisionType.DELETION](../../com.aspose.words/revisiontype\#DELETION). |
| [getMovedFromTextColor()](#getMovedFromTextColor--) | Allows to specify the color to be used for areas where content was moved from [RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING). |
| [setMovedFromTextColor(int value)](#setMovedFromTextColor-int-) | Allows to specify the color to be used for areas where content was moved from [RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING). |
| [getMovedFromTextEffect()](#getMovedFromTextEffect--) | Allows to specify the effect to be applied to the areas where content was moved from [RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING). |
| [setMovedFromTextEffect(int value)](#setMovedFromTextEffect-int-) | Allows to specify the effect to be applied to the areas where content was moved from [RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING). |
| [getMovedToTextColor()](#getMovedToTextColor--) | Allows to specify the color to be used for areas where content was moved to [RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING). |
| [setMovedToTextColor(int value)](#setMovedToTextColor-int-) | Allows to specify the color to be used for areas where content was moved to [RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING). |
| [getMovedToTextEffect()](#getMovedToTextEffect--) | Allows to specify the effect to be applied to the areas where content was moved to [RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING). |
| [setMovedToTextEffect(int value)](#setMovedToTextEffect-int-) | Allows to specify the effect to be applied to the areas where content was moved to [RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING). |
| [getRevisedPropertiesColor()](#getRevisedPropertiesColor--) | Allows to specify the color to be used for content with changes of formatting properties [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE) Default value is [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT). |
| [setRevisedPropertiesColor(int value)](#setRevisedPropertiesColor-int-) | Allows to specify the color to be used for content with changes of formatting properties [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE) Default value is [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT). |
| [getRevisedPropertiesEffect()](#getRevisedPropertiesEffect--) | Allows to specify the effect for content areas with changes of formatting properties [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE) Default value is [RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect\#NONE) [RevisionTextEffect.HIDDEN](../../com.aspose.words/revisiontexteffect\#HIDDEN) is not allowed and will cause java.lang.IllegalArgumentException. |
| [setRevisedPropertiesEffect(int value)](#setRevisedPropertiesEffect-int-) | Allows to specify the effect for content areas with changes of formatting properties [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE) Default value is [RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect\#NONE) [RevisionTextEffect.HIDDEN](../../com.aspose.words/revisiontexteffect\#HIDDEN) is not allowed and will cause java.lang.IllegalArgumentException. |
| [getRevisionBarsColor()](#getRevisionBarsColor--) | Allows to specify the color to be used for side bars that identify document lines containing revised information. |
| [setRevisionBarsColor(int value)](#setRevisionBarsColor-int-) | Allows to specify the color to be used for side bars that identify document lines containing revised information. |
| [getRevisionBarsWidth()](#getRevisionBarsWidth--) | Gets width of revision bars, points. |
| [setRevisionBarsWidth(float value)](#setRevisionBarsWidth-float-) | Sets width of revision bars, points. |
| [getRevisionBarsPosition()](#getRevisionBarsPosition--) | Gets rendering position of revision bars. |
| [setRevisionBarsPosition(int value)](#setRevisionBarsPosition-int-) | Sets rendering position of revision bars. |
| [getCommentColor()](#getCommentColor--) | Allows to specify the color to be used for comments. |
| [setCommentColor(int value)](#setCommentColor-int-) | Allows to specify the color to be used for comments. |
| [getShowInBalloons()](#getShowInBalloons--) | Allows to specify whether the revisions are rendered in the balloons. |
| [setShowInBalloons(int value)](#setShowInBalloons-int-) | Allows to specify whether the revisions are rendered in the balloons. |
| [getMeasurementUnit()](#getMeasurementUnit--) | Allows to specify the measurement units for revision comments. |
| [setMeasurementUnit(int value)](#setMeasurementUnit-int-) | Allows to specify the measurement units for revision comments. |
### getShowRevisionMarks() {#getShowRevisionMarks--}
```
public boolean getShowRevisionMarks()
```


Allow to specify whether revision text should be marked with special formatting markup. Default value is True.

**Returns:**
boolean - The corresponding  boolean  value.
### setShowRevisionMarks(boolean value) {#setShowRevisionMarks-boolean-}
```
public void setShowRevisionMarks(boolean value)
```


Allow to specify whether revision text should be marked with special formatting markup. Default value is True.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getShowRevisionBars() {#getShowRevisionBars--}
```
public boolean getShowRevisionBars()
```


Allows to specify whether revision bars should be rendered near lines containing revised content. Default value is True.

**Returns:**
boolean - The corresponding  boolean  value.
### setShowRevisionBars(boolean value) {#setShowRevisionBars-boolean-}
```
public void setShowRevisionBars(boolean value)
```


Allows to specify whether revision bars should be rendered near lines containing revised content. Default value is True.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getShowOriginalRevision() {#getShowOriginalRevision--}
```
public boolean getShowOriginalRevision()
```


Allows to specify whether the original text should be shown instead of revised one. Default value is False.

**Returns:**
boolean - The corresponding  boolean  value.
### setShowOriginalRevision(boolean value) {#setShowOriginalRevision-boolean-}
```
public void setShowOriginalRevision(boolean value)
```


Allows to specify whether the original text should be shown instead of revised one. Default value is False.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getInsertedTextColor() {#getInsertedTextColor--}
```
public int getInsertedTextColor()
```


Allows to specify the color to be used for inserted content [RevisionType.INSERTION](../../com.aspose.words/revisiontype\#INSERTION). Default value is [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR).

**Returns:**
int - The corresponding  int  value. The returned value is one of [RevisionColor](../../com.aspose.words/revisioncolor) constants.
### setInsertedTextColor(int value) {#setInsertedTextColor-int-}
```
public void setInsertedTextColor(int value)
```


Allows to specify the color to be used for inserted content [RevisionType.INSERTION](../../com.aspose.words/revisiontype\#INSERTION). Default value is [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionColor](../../com.aspose.words/revisioncolor) constants. |

### getInsertedTextEffect() {#getInsertedTextEffect--}
```
public int getInsertedTextEffect()
```


Allows to specify the effect to be applied to the inserted content [RevisionType.INSERTION](../../com.aspose.words/revisiontype\#INSERTION). Default value is [RevisionTextEffect.UNDERLINE](../../com.aspose.words/revisiontexteffect\#UNDERLINE). Values of [RevisionTextEffect.HIDDEN](../../com.aspose.words/revisiontexteffect\#HIDDEN) and [RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect\#DOUBLE-STRIKE-THROUGH) are not allowed and will cause java.lang.IllegalArgumentException.

**Returns:**
int - The corresponding  int  value. The returned value is one of [RevisionTextEffect](../../com.aspose.words/revisiontexteffect) constants.
### setInsertedTextEffect(int value) {#setInsertedTextEffect-int-}
```
public void setInsertedTextEffect(int value)
```


Allows to specify the effect to be applied to the inserted content [RevisionType.INSERTION](../../com.aspose.words/revisiontype\#INSERTION). Default value is [RevisionTextEffect.UNDERLINE](../../com.aspose.words/revisiontexteffect\#UNDERLINE). Values of [RevisionTextEffect.HIDDEN](../../com.aspose.words/revisiontexteffect\#HIDDEN) and [RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect\#DOUBLE-STRIKE-THROUGH) are not allowed and will cause java.lang.IllegalArgumentException.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionTextEffect](../../com.aspose.words/revisiontexteffect) constants. |

### getDeletedTextColor() {#getDeletedTextColor--}
```
public int getDeletedTextColor()
```


Allows to specify the color to be used for deleted content [RevisionType.DELETION](../../com.aspose.words/revisiontype\#DELETION). Default value is [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR).

**Returns:**
int - The corresponding  int  value. The returned value is one of [RevisionColor](../../com.aspose.words/revisioncolor) constants.
### setDeletedTextColor(int value) {#setDeletedTextColor-int-}
```
public void setDeletedTextColor(int value)
```


Allows to specify the color to be used for deleted content [RevisionType.DELETION](../../com.aspose.words/revisiontype\#DELETION). Default value is [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionColor](../../com.aspose.words/revisioncolor) constants. |

### getDeletedTextEffect() {#getDeletedTextEffect--}
```
public int getDeletedTextEffect()
```


Allows to specify the effect to be applied to the deleted content [RevisionType.DELETION](../../com.aspose.words/revisiontype\#DELETION). Default value is [RevisionTextEffect.STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect\#STRIKE-THROUGH)

**Returns:**
int - The corresponding  int  value. The returned value is one of [RevisionTextEffect](../../com.aspose.words/revisiontexteffect) constants.
### setDeletedTextEffect(int value) {#setDeletedTextEffect-int-}
```
public void setDeletedTextEffect(int value)
```


Allows to specify the effect to be applied to the deleted content [RevisionType.DELETION](../../com.aspose.words/revisiontype\#DELETION). Default value is [RevisionTextEffect.STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect\#STRIKE-THROUGH)

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionTextEffect](../../com.aspose.words/revisiontexteffect) constants. |

### getMovedFromTextColor() {#getMovedFromTextColor--}
```
public int getMovedFromTextColor()
```


Allows to specify the color to be used for areas where content was moved from [RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING). Default value is [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR).

**Returns:**
int - The corresponding  int  value. The returned value is one of [RevisionColor](../../com.aspose.words/revisioncolor) constants.
### setMovedFromTextColor(int value) {#setMovedFromTextColor-int-}
```
public void setMovedFromTextColor(int value)
```


Allows to specify the color to be used for areas where content was moved from [RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING). Default value is [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionColor](../../com.aspose.words/revisioncolor) constants. |

### getMovedFromTextEffect() {#getMovedFromTextEffect--}
```
public int getMovedFromTextEffect()
```


Allows to specify the effect to be applied to the areas where content was moved from [RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING). Default value is [RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect\#DOUBLE-STRIKE-THROUGH)

**Returns:**
int - The corresponding  int  value. The returned value is one of [RevisionTextEffect](../../com.aspose.words/revisiontexteffect) constants.
### setMovedFromTextEffect(int value) {#setMovedFromTextEffect-int-}
```
public void setMovedFromTextEffect(int value)
```


Allows to specify the effect to be applied to the areas where content was moved from [RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING). Default value is [RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect\#DOUBLE-STRIKE-THROUGH)

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionTextEffect](../../com.aspose.words/revisiontexteffect) constants. |

### getMovedToTextColor() {#getMovedToTextColor--}
```
public int getMovedToTextColor()
```


Allows to specify the color to be used for areas where content was moved to [RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING). Default value is [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR).

**Returns:**
int - The corresponding  int  value. The returned value is one of [RevisionColor](../../com.aspose.words/revisioncolor) constants.
### setMovedToTextColor(int value) {#setMovedToTextColor-int-}
```
public void setMovedToTextColor(int value)
```


Allows to specify the color to be used for areas where content was moved to [RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING). Default value is [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionColor](../../com.aspose.words/revisioncolor) constants. |

### getMovedToTextEffect() {#getMovedToTextEffect--}
```
public int getMovedToTextEffect()
```


Allows to specify the effect to be applied to the areas where content was moved to [RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING). Default value is [RevisionTextEffect.DOUBLE\_UNDERLINE](../../com.aspose.words/revisiontexteffect\#DOUBLE-UNDERLINE) Values of [RevisionTextEffect.HIDDEN](../../com.aspose.words/revisiontexteffect\#HIDDEN) and [RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect\#DOUBLE-STRIKE-THROUGH) are not allowed and will cause java.lang.IllegalArgumentException.

**Returns:**
int - The corresponding  int  value. The returned value is one of [RevisionTextEffect](../../com.aspose.words/revisiontexteffect) constants.
### setMovedToTextEffect(int value) {#setMovedToTextEffect-int-}
```
public void setMovedToTextEffect(int value)
```


Allows to specify the effect to be applied to the areas where content was moved to [RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING). Default value is [RevisionTextEffect.DOUBLE\_UNDERLINE](../../com.aspose.words/revisiontexteffect\#DOUBLE-UNDERLINE) Values of [RevisionTextEffect.HIDDEN](../../com.aspose.words/revisiontexteffect\#HIDDEN) and [RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect\#DOUBLE-STRIKE-THROUGH) are not allowed and will cause java.lang.IllegalArgumentException.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionTextEffect](../../com.aspose.words/revisiontexteffect) constants. |

### getRevisedPropertiesColor() {#getRevisedPropertiesColor--}
```
public int getRevisedPropertiesColor()
```


Allows to specify the color to be used for content with changes of formatting properties [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE) Default value is [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT).

**Returns:**
int - The corresponding  int  value. The returned value is one of [RevisionColor](../../com.aspose.words/revisioncolor) constants.
### setRevisedPropertiesColor(int value) {#setRevisedPropertiesColor-int-}
```
public void setRevisedPropertiesColor(int value)
```


Allows to specify the color to be used for content with changes of formatting properties [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE) Default value is [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionColor](../../com.aspose.words/revisioncolor) constants. |

### getRevisedPropertiesEffect() {#getRevisedPropertiesEffect--}
```
public int getRevisedPropertiesEffect()
```


Allows to specify the effect for content areas with changes of formatting properties [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE) Default value is [RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect\#NONE) [RevisionTextEffect.HIDDEN](../../com.aspose.words/revisiontexteffect\#HIDDEN) is not allowed and will cause java.lang.IllegalArgumentException.

**Returns:**
int - The corresponding  int  value. The returned value is one of [RevisionTextEffect](../../com.aspose.words/revisiontexteffect) constants.
### setRevisedPropertiesEffect(int value) {#setRevisedPropertiesEffect-int-}
```
public void setRevisedPropertiesEffect(int value)
```


Allows to specify the effect for content areas with changes of formatting properties [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE) Default value is [RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect\#NONE) [RevisionTextEffect.HIDDEN](../../com.aspose.words/revisiontexteffect\#HIDDEN) is not allowed and will cause java.lang.IllegalArgumentException.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionTextEffect](../../com.aspose.words/revisiontexteffect) constants. |

### getRevisionBarsColor() {#getRevisionBarsColor--}
```
public int getRevisionBarsColor()
```


Allows to specify the color to be used for side bars that identify document lines containing revised information. Default value is [RevisionColor.RED](../../com.aspose.words/revisioncolor\#RED). Setting this property to [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR) or [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT) values will result in hiding revision bars from the layout.

**Returns:**
int - The corresponding  int  value. The returned value is one of [RevisionColor](../../com.aspose.words/revisioncolor) constants.
### setRevisionBarsColor(int value) {#setRevisionBarsColor-int-}
```
public void setRevisionBarsColor(int value)
```


Allows to specify the color to be used for side bars that identify document lines containing revised information. Default value is [RevisionColor.RED](../../com.aspose.words/revisioncolor\#RED). Setting this property to [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR) or [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT) values will result in hiding revision bars from the layout.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionColor](../../com.aspose.words/revisioncolor) constants. |

### getRevisionBarsWidth() {#getRevisionBarsWidth--}
```
public float getRevisionBarsWidth()
```


Gets width of revision bars, points.

**Returns:**
float - Width of revision bars, points.
### setRevisionBarsWidth(float value) {#setRevisionBarsWidth-float-}
```
public void setRevisionBarsWidth(float value)
```


Sets width of revision bars, points.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | float | Width of revision bars, points. |

### getRevisionBarsPosition() {#getRevisionBarsPosition--}
```
public int getRevisionBarsPosition()
```


Gets rendering position of revision bars. Default value is [HorizontalAlignment.OUTSIDE](../../com.aspose.words/horizontalalignment\#OUTSIDE). Values of [HorizontalAlignment.CENTER](../../com.aspose.words/horizontalalignment\#CENTER) and [HorizontalAlignment.INSIDE](../../com.aspose.words/horizontalalignment\#INSIDE) are not allowed and will cause java.lang.IllegalArgumentException.

**Returns:**
int - Rendering position of revision bars. The returned value is one of [HorizontalAlignment](../../com.aspose.words/horizontalalignment) constants.
### setRevisionBarsPosition(int value) {#setRevisionBarsPosition-int-}
```
public void setRevisionBarsPosition(int value)
```


Sets rendering position of revision bars. Default value is [HorizontalAlignment.OUTSIDE](../../com.aspose.words/horizontalalignment\#OUTSIDE). Values of [HorizontalAlignment.CENTER](../../com.aspose.words/horizontalalignment\#CENTER) and [HorizontalAlignment.INSIDE](../../com.aspose.words/horizontalalignment\#INSIDE) are not allowed and will cause java.lang.IllegalArgumentException.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Rendering position of revision bars. The value must be one of [HorizontalAlignment](../../com.aspose.words/horizontalalignment) constants. |

### getCommentColor() {#getCommentColor--}
```
public int getCommentColor()
```


Allows to specify the color to be used for comments. Default value is [RevisionColor.RED](../../com.aspose.words/revisioncolor\#RED). If set this property to [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR) or [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT) values, as the result this property will be set to default color.

**Returns:**
int - The corresponding  int  value. The returned value is one of [RevisionColor](../../com.aspose.words/revisioncolor) constants.
### setCommentColor(int value) {#setCommentColor-int-}
```
public void setCommentColor(int value)
```


Allows to specify the color to be used for comments. Default value is [RevisionColor.RED](../../com.aspose.words/revisioncolor\#RED). If set this property to [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR) or [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT) values, as the result this property will be set to default color.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RevisionColor](../../com.aspose.words/revisioncolor) constants. |

### getShowInBalloons() {#getShowInBalloons--}
```
public int getShowInBalloons()
```


Allows to specify whether the revisions are rendered in the balloons. Default value is [ShowInBalloons.NONE](../../com.aspose.words/showinballoons\#NONE). Note that revisions are not rendered in balloons for [CommentDisplayMode.SHOW\_IN\_ANNOTATIONS](../../com.aspose.words/commentdisplaymode\#SHOW-IN-ANNOTATIONS).

**Returns:**
int - The corresponding  int  value. The returned value is one of [ShowInBalloons](../../com.aspose.words/showinballoons) constants.
### setShowInBalloons(int value) {#setShowInBalloons-int-}
```
public void setShowInBalloons(int value)
```


Allows to specify whether the revisions are rendered in the balloons. Default value is [ShowInBalloons.NONE](../../com.aspose.words/showinballoons\#NONE). Note that revisions are not rendered in balloons for [CommentDisplayMode.SHOW\_IN\_ANNOTATIONS](../../com.aspose.words/commentdisplaymode\#SHOW-IN-ANNOTATIONS).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [ShowInBalloons](../../com.aspose.words/showinballoons) constants. |

### getMeasurementUnit() {#getMeasurementUnit--}
```
public int getMeasurementUnit()
```


Allows to specify the measurement units for revision comments. Default value is [MeasurementUnits.CENTIMETERS](../../com.aspose.words/measurementunits\#CENTIMETERS)

**Returns:**
int - The corresponding  int  value. The returned value is one of [MeasurementUnits](../../com.aspose.words/measurementunits) constants.
### setMeasurementUnit(int value) {#setMeasurementUnit-int-}
```
public void setMeasurementUnit(int value)
```


Allows to specify the measurement units for revision comments. Default value is [MeasurementUnits.CENTIMETERS](../../com.aspose.words/measurementunits\#CENTIMETERS)

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [MeasurementUnits](../../com.aspose.words/measurementunits) constants. |

