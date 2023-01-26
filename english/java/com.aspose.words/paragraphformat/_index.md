---
title: ParagraphFormat
second_title: Aspose.Words for Java API Reference
description: Represents all the formatting for a paragraph.
type: docs
weight: 450
url: /java/com.aspose.words/paragraphformat/
---

**Inheritance:**
java.lang.Object
```
public class ParagraphFormat
```

Represents all the formatting for a paragraph.

To learn more, visit the [ Working with Paragraphs ][Working with Paragraphs] documentation article.


[Working with Paragraphs]: https://docs.aspose.com/words/java/working-with-paragraphs/
## Methods

| Method | Description |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Resets to default paragraph formatting. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int) |  |
| [getAddSpaceBetweenFarEastAndAlpha()](#getAddSpaceBetweenFarEastAndAlpha) | Gets a flag indicating whether inter-character spacing is automatically adjusted between regions of Latin text and regions of East Asian text in the current paragraph. |
| [getAddSpaceBetweenFarEastAndDigit()](#getAddSpaceBetweenFarEastAndDigit) | Gets a flag indicating whether inter-character spacing is automatically adjusted between regions of numbers and regions of East Asian text in the current paragraph. |
| [getAlignment()](#getAlignment) | Gets text alignment for the paragraph. |
| [getBidi()](#getBidi) | Gets whether this is a right-to-left paragraph. |
| [getBorders()](#getBorders) | Gets collection of borders of the paragraph. |
| [getCharacterUnitFirstLineIndent()](#getCharacterUnitFirstLineIndent) | Gets the value (in characters) for the first-line or hanging indent. |
| [getCharacterUnitLeftIndent()](#getCharacterUnitLeftIndent) | Gets the left indent value (in characters) for the specified paragraphs. |
| [getCharacterUnitRightIndent()](#getCharacterUnitRightIndent) | Gets the right indent value (in characters) for the specified paragraphs. |
| [getClass()](#getClass) |  |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getDropCapPosition()](#getDropCapPosition) | Gets the position for a drop cap text. |
| [getFarEastLineBreakControl()](#getFarEastLineBreakControl) | Gets a flag indicating whether East Asian line-breaking rules are applied to the current paragraph. |
| [getFirstLineIndent()](#getFirstLineIndent) | Gets the value (in points) for a first line or hanging indent. |
| [getHangingPunctuation()](#getHangingPunctuation) | Gets a flag indicating whether hanging punctuation is enabled for the current paragraph. |
| [getKeepTogether()](#getKeepTogether) | True if all lines in the paragraph are to remain on the same page. |
| [getKeepWithNext()](#getKeepWithNext) | True if the paragraph is to remains on the same page as the paragraph that follows it. |
| [getLeftIndent()](#getLeftIndent) | Gets the value (in points) that represents the left indent for paragraph. |
| [getLineSpacing()](#getLineSpacing) | Gets the line spacing (in points) for the paragraph. |
| [getLineSpacingRule()](#getLineSpacingRule) | Gets the line spacing for the paragraph. |
| [getLineUnitAfter()](#getLineUnitAfter) | Gets the amount of spacing (in gridlines) after the paragraphs. |
| [getLineUnitBefore()](#getLineUnitBefore) | Gets the amount of spacing (in gridlines) before the paragraphs. |
| [getLinesToDrop()](#getLinesToDrop) | Gets the number of lines of the paragraph text used to calculate the drop cap height. |
| [getNoSpaceBetweenParagraphsOfSameStyle()](#getNoSpaceBetweenParagraphsOfSameStyle) | When  true , [getSpaceBefore()](../../com.aspose.words/paragraphformat\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat\#setSpaceBefore-double) and [getSpaceAfter()](../../com.aspose.words/paragraphformat\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat\#setSpaceAfter-double) will be ignored between the paragraphs of the same style. |
| [getOutlineLevel()](#getOutlineLevel) | Specifies the outline level of the paragraph in the document. |
| [getPageBreakBefore()](#getPageBreakBefore) | True if a page break is forced before the paragraph. |
| [getRightIndent()](#getRightIndent) | Gets the value (in points) that represents the right indent for paragraph. |
| [getShading()](#getShading) | Returns a [Shading](../../com.aspose.words/shading) object that refers to the shading formatting for the paragraph. |
| [getSnapToGrid()](#getSnapToGrid) | Specifies whether the current paragraph should use the document grid lines per page settings when laying out the contents in the paragraph. |
| [getSpaceAfter()](#getSpaceAfter) | Gets the amount of spacing (in points) after the paragraph. |
| [getSpaceAfterAuto()](#getSpaceAfterAuto) | True if the amount of spacing after the paragraph is set automatically. |
| [getSpaceBefore()](#getSpaceBefore) | Gets the amount of spacing (in points) before the paragraph. |
| [getSpaceBeforeAuto()](#getSpaceBeforeAuto) | True if the amount of spacing before the paragraph is set automatically. |
| [getStyle()](#getStyle) | Gets the paragraph style applied to this formatting. |
| [getStyleIdentifier()](#getStyleIdentifier) | Gets the locale independent style identifier of the paragraph style applied to this formatting. |
| [getStyleName()](#getStyleName) | Gets the name of the paragraph style applied to this formatting. |
| [getSuppressAutoHyphens()](#getSuppressAutoHyphens) | Specifies whether the current paragraph should be exempted from any hyphenation which is applied in the document settings. |
| [getSuppressLineNumbers()](#getSuppressLineNumbers) | Specifies whether the current paragraph's lines should be exempted from line numbering which is applied in the parent section. |
| [getTabStops()](#getTabStops) | Gets the collection of custom tab stops defined for this object. |
| [getWidowControl()](#getWidowControl) | True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph. |
| [getWordWrap()](#getWordWrap) | If this property is  false , Latin text in the middle of a word can be wrapped for the current paragraph. |
| [hashCode()](#hashCode) |  |
| [isHeading()](#isHeading) | True when the paragraph style is one of the built-in Heading styles. |
| [isListItem()](#isListItem) | True when the paragraph is an item in a bulleted or numbered list. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setAddSpaceBetweenFarEastAndAlpha(boolean value)](#setAddSpaceBetweenFarEastAndAlpha-boolean) | Sets a flag indicating whether inter-character spacing is automatically adjusted between regions of Latin text and regions of East Asian text in the current paragraph. |
| [setAddSpaceBetweenFarEastAndDigit(boolean value)](#setAddSpaceBetweenFarEastAndDigit-boolean) | Sets a flag indicating whether inter-character spacing is automatically adjusted between regions of numbers and regions of East Asian text in the current paragraph. |
| [setAlignment(int value)](#setAlignment-int) | Sets text alignment for the paragraph. |
| [setBidi(boolean value)](#setBidi-boolean) | Sets whether this is a right-to-left paragraph. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setCharacterUnitFirstLineIndent(double value)](#setCharacterUnitFirstLineIndent-double) | Sets the value (in characters) for the first-line or hanging indent. |
| [setCharacterUnitLeftIndent(double value)](#setCharacterUnitLeftIndent-double) | Sets the left indent value (in characters) for the specified paragraphs. |
| [setCharacterUnitRightIndent(double value)](#setCharacterUnitRightIndent-double) | Sets the right indent value (in characters) for the specified paragraphs. |
| [setDropCapPosition(int value)](#setDropCapPosition-int) | Sets the position for a drop cap text. |
| [setFarEastLineBreakControl(boolean value)](#setFarEastLineBreakControl-boolean) | Sets a flag indicating whether East Asian line-breaking rules are applied to the current paragraph. |
| [setFirstLineIndent(double value)](#setFirstLineIndent-double) | Sets the value (in points) for a first line or hanging indent. |
| [setHangingPunctuation(boolean value)](#setHangingPunctuation-boolean) | Sets a flag indicating whether hanging punctuation is enabled for the current paragraph. |
| [setKeepTogether(boolean value)](#setKeepTogether-boolean) | True if all lines in the paragraph are to remain on the same page. |
| [setKeepWithNext(boolean value)](#setKeepWithNext-boolean) | True if the paragraph is to remains on the same page as the paragraph that follows it. |
| [setLeftIndent(double value)](#setLeftIndent-double) | Sets the value (in points) that represents the left indent for paragraph. |
| [setLineSpacing(double value)](#setLineSpacing-double) | Sets the line spacing (in points) for the paragraph. |
| [setLineSpacingRule(int value)](#setLineSpacingRule-int) | Sets the line spacing for the paragraph. |
| [setLineUnitAfter(double value)](#setLineUnitAfter-double) | Sets the amount of spacing (in gridlines) after the paragraphs. |
| [setLineUnitBefore(double value)](#setLineUnitBefore-double) | Sets the amount of spacing (in gridlines) before the paragraphs. |
| [setLinesToDrop(int value)](#setLinesToDrop-int) | Sets the number of lines of the paragraph text used to calculate the drop cap height. |
| [setNoSpaceBetweenParagraphsOfSameStyle(boolean value)](#setNoSpaceBetweenParagraphsOfSameStyle-boolean) | When  true , [getSpaceBefore()](../../com.aspose.words/paragraphformat\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat\#setSpaceBefore-double) and [getSpaceAfter()](../../com.aspose.words/paragraphformat\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat\#setSpaceAfter-double) will be ignored between the paragraphs of the same style. |
| [setOutlineLevel(int value)](#setOutlineLevel-int) | Specifies the outline level of the paragraph in the document. |
| [setPageBreakBefore(boolean value)](#setPageBreakBefore-boolean) | True if a page break is forced before the paragraph. |
| [setRightIndent(double value)](#setRightIndent-double) | Sets the value (in points) that represents the right indent for paragraph. |
| [setSnapToGrid(boolean value)](#setSnapToGrid-boolean) | Specifies whether the current paragraph should use the document grid lines per page settings when laying out the contents in the paragraph. |
| [setSpaceAfter(double value)](#setSpaceAfter-double) | Sets the amount of spacing (in points) after the paragraph. |
| [setSpaceAfterAuto(boolean value)](#setSpaceAfterAuto-boolean) | True if the amount of spacing after the paragraph is set automatically. |
| [setSpaceBefore(double value)](#setSpaceBefore-double) | Sets the amount of spacing (in points) before the paragraph. |
| [setSpaceBeforeAuto(boolean value)](#setSpaceBeforeAuto-boolean) | True if the amount of spacing before the paragraph is set automatically. |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style) | Sets the paragraph style applied to this formatting. |
| [setStyleIdentifier(int value)](#setStyleIdentifier-int) | Sets the locale independent style identifier of the paragraph style applied to this formatting. |
| [setStyleName(String value)](#setStyleName-java.lang.String) | Sets the name of the paragraph style applied to this formatting. |
| [setSuppressAutoHyphens(boolean value)](#setSuppressAutoHyphens-boolean) | Specifies whether the current paragraph should be exempted from any hyphenation which is applied in the document settings. |
| [setSuppressLineNumbers(boolean value)](#setSuppressLineNumbers-boolean) | Specifies whether the current paragraph's lines should be exempted from line numbering which is applied in the parent section. |
| [setWidowControl(boolean value)](#setWidowControl-boolean) | True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph. |
| [setWordWrap(boolean value)](#setWordWrap-boolean) | If this property is  false , Latin text in the middle of a word can be wrapped for the current paragraph. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Resets to default paragraph formatting. Default paragraph formatting is Normal style, left aligned, no indentation, no spacing, no borders and no shading.

### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int}
```
public Object fetchInheritedBorderAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedShadingAttr(int key) {#fetchInheritedShadingAttr-int}
```
public Object fetchInheritedShadingAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getAddSpaceBetweenFarEastAndAlpha() {#getAddSpaceBetweenFarEastAndAlpha}
```
public boolean getAddSpaceBetweenFarEastAndAlpha()
```


Gets a flag indicating whether inter-character spacing is automatically adjusted between regions of Latin text and regions of East Asian text in the current paragraph.

**Returns:**
boolean - A flag indicating whether inter-character spacing is automatically adjusted between regions of Latin text and regions of East Asian text in the current paragraph.
### getAddSpaceBetweenFarEastAndDigit() {#getAddSpaceBetweenFarEastAndDigit}
```
public boolean getAddSpaceBetweenFarEastAndDigit()
```


Gets a flag indicating whether inter-character spacing is automatically adjusted between regions of numbers and regions of East Asian text in the current paragraph.

**Returns:**
boolean - A flag indicating whether inter-character spacing is automatically adjusted between regions of numbers and regions of East Asian text in the current paragraph.
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


Gets text alignment for the paragraph.

**Returns:**
int - Text alignment for the paragraph. The returned value is one of [ParagraphAlignment](../../com.aspose.words/paragraphalignment) constants.
### getBidi() {#getBidi}
```
public boolean getBidi()
```


Gets whether this is a right-to-left paragraph.

When  true , the runs and other inline objects in this paragraph are laid out right to left.

**Returns:**
boolean - Whether this is a right-to-left paragraph.
### getBorders() {#getBorders}
```
public BorderCollection getBorders()
```


Gets collection of borders of the paragraph.

**Returns:**
[BorderCollection](../../com.aspose.words/bordercollection) - Collection of borders of the paragraph.
### getCharacterUnitFirstLineIndent() {#getCharacterUnitFirstLineIndent}
```
public double getCharacterUnitFirstLineIndent()
```


Gets the value (in characters) for the first-line or hanging indent.

Use positive values to set the first-line indent, and negative values to set the hanging indent.

**Returns:**
double - The value (in characters) for the first-line or hanging indent.
### getCharacterUnitLeftIndent() {#getCharacterUnitLeftIndent}
```
public double getCharacterUnitLeftIndent()
```


Gets the left indent value (in characters) for the specified paragraphs.

**Returns:**
double - The left indent value (in characters) for the specified paragraphs.
### getCharacterUnitRightIndent() {#getCharacterUnitRightIndent}
```
public double getCharacterUnitRightIndent()
```


Gets the right indent value (in characters) for the specified paragraphs.

**Returns:**
double - The right indent value (in characters) for the specified paragraphs.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDropCapPosition() {#getDropCapPosition}
```
public int getDropCapPosition()
```


Gets the position for a drop cap text.

**Returns:**
int - The position for a drop cap text. The returned value is one of [DropCapPosition](../../com.aspose.words/dropcapposition) constants.
### getFarEastLineBreakControl() {#getFarEastLineBreakControl}
```
public boolean getFarEastLineBreakControl()
```


Gets a flag indicating whether East Asian line-breaking rules are applied to the current paragraph.

**Returns:**
boolean - A flag indicating whether East Asian line-breaking rules are applied to the current paragraph.
### getFirstLineIndent() {#getFirstLineIndent}
```
public double getFirstLineIndent()
```


Gets the value (in points) for a first line or hanging indent.

Use positive values to set the first-line indent, and negative values to set the hanging indent.

**Returns:**
double - The value (in points) for a first line or hanging indent.
### getHangingPunctuation() {#getHangingPunctuation}
```
public boolean getHangingPunctuation()
```


Gets a flag indicating whether hanging punctuation is enabled for the current paragraph.

**Returns:**
boolean - A flag indicating whether hanging punctuation is enabled for the current paragraph.
### getKeepTogether() {#getKeepTogether}
```
public boolean getKeepTogether()
```


True if all lines in the paragraph are to remain on the same page.

**Returns:**
boolean - The corresponding  boolean  value.
### getKeepWithNext() {#getKeepWithNext}
```
public boolean getKeepWithNext()
```


True if the paragraph is to remains on the same page as the paragraph that follows it.

**Returns:**
boolean - The corresponding  boolean  value.
### getLeftIndent() {#getLeftIndent}
```
public double getLeftIndent()
```


Gets the value (in points) that represents the left indent for paragraph.

**Returns:**
double - The value (in points) that represents the left indent for paragraph.
### getLineSpacing() {#getLineSpacing}
```
public double getLineSpacing()
```


Gets the line spacing (in points) for the paragraph.

When [getLineSpacingRule()](../../com.aspose.words/paragraphformat\#getLineSpacingRule) / [setLineSpacingRule(int)](../../com.aspose.words/paragraphformat\#setLineSpacingRule-int) property is set to [LineSpacingRule.AT\_LEAST](../../com.aspose.words/linespacingrule\#AT-LEAST), the line spacing can be greater than or equal to, but never less than the specified [getLineSpacing()](../../com.aspose.words/paragraphformat\#getLineSpacing) / [setLineSpacing(double)](../../com.aspose.words/paragraphformat\#setLineSpacing-double) value.

When [getLineSpacingRule()](../../com.aspose.words/paragraphformat\#getLineSpacingRule) / [setLineSpacingRule(int)](../../com.aspose.words/paragraphformat\#setLineSpacingRule-int) property is set to [LineSpacingRule.EXACTLY](../../com.aspose.words/linespacingrule\#EXACTLY), the line spacing never changes from the specified [getLineSpacing()](../../com.aspose.words/paragraphformat\#getLineSpacing) / [setLineSpacing(double)](../../com.aspose.words/paragraphformat\#setLineSpacing-double) value, even if a larger font is used within the paragraph.

**Returns:**
double - The line spacing (in points) for the paragraph.
### getLineSpacingRule() {#getLineSpacingRule}
```
public int getLineSpacingRule()
```


Gets the line spacing for the paragraph.

**Returns:**
int - The line spacing for the paragraph. The returned value is one of [LineSpacingRule](../../com.aspose.words/linespacingrule) constants.
### getLineUnitAfter() {#getLineUnitAfter}
```
public double getLineUnitAfter()
```


Gets the amount of spacing (in gridlines) after the paragraphs.

**Returns:**
double - The amount of spacing (in gridlines) after the paragraphs.
### getLineUnitBefore() {#getLineUnitBefore}
```
public double getLineUnitBefore()
```


Gets the amount of spacing (in gridlines) before the paragraphs.

**Returns:**
double - The amount of spacing (in gridlines) before the paragraphs.
### getLinesToDrop() {#getLinesToDrop}
```
public int getLinesToDrop()
```


Gets the number of lines of the paragraph text used to calculate the drop cap height.

**Returns:**
int - The number of lines of the paragraph text used to calculate the drop cap height.
### getNoSpaceBetweenParagraphsOfSameStyle() {#getNoSpaceBetweenParagraphsOfSameStyle}
```
public boolean getNoSpaceBetweenParagraphsOfSameStyle()
```


When  true , [getSpaceBefore()](../../com.aspose.words/paragraphformat\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat\#setSpaceBefore-double) and [getSpaceAfter()](../../com.aspose.words/paragraphformat\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat\#setSpaceAfter-double) will be ignored between the paragraphs of the same style.

This setting only takes affect when applied to a paragraph style. If applied to a paragraph directly, it has no effect.

**Returns:**
boolean - The corresponding  boolean  value.
### getOutlineLevel() {#getOutlineLevel}
```
public int getOutlineLevel()
```


Specifies the outline level of the paragraph in the document.

**Returns:**
int - The corresponding  int  value. The returned value is one of [OutlineLevel](../../com.aspose.words/outlinelevel) constants.
### getPageBreakBefore() {#getPageBreakBefore}
```
public boolean getPageBreakBefore()
```


True if a page break is forced before the paragraph.

**Returns:**
boolean - The corresponding  boolean  value.
### getRightIndent() {#getRightIndent}
```
public double getRightIndent()
```


Gets the value (in points) that represents the right indent for paragraph.

**Returns:**
double - The value (in points) that represents the right indent for paragraph.
### getShading() {#getShading}
```
public Shading getShading()
```


Returns a [Shading](../../com.aspose.words/shading) object that refers to the shading formatting for the paragraph.

**Returns:**
[Shading](../../com.aspose.words/shading) - A [Shading](../../com.aspose.words/shading) object that refers to the shading formatting for the paragraph.
### getSnapToGrid() {#getSnapToGrid}
```
public boolean getSnapToGrid()
```


Specifies whether the current paragraph should use the document grid lines per page settings when laying out the contents in the paragraph.

**Returns:**
boolean - The corresponding  boolean  value.
### getSpaceAfter() {#getSpaceAfter}
```
public double getSpaceAfter()
```


Gets the amount of spacing (in points) after the paragraph.

Has no effect when [getSpaceAfterAuto()](../../com.aspose.words/paragraphformat\#getSpaceAfterAuto) / [setSpaceAfterAuto(boolean)](../../com.aspose.words/paragraphformat\#setSpaceAfterAuto-boolean) is  true .

Valid values \\u200b\\u200brange from 0 to 1584 inclusive.

**Returns:**
double - The amount of spacing (in points) after the paragraph.
### getSpaceAfterAuto() {#getSpaceAfterAuto}
```
public boolean getSpaceAfterAuto()
```


True if the amount of spacing after the paragraph is set automatically.

When set to  true , overrides the effect of [getSpaceAfter()](../../com.aspose.words/paragraphformat\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat\#setSpaceAfter-double).

When you set paragraph Space Before and Space After to Auto, Microsoft Word adds 14 points spacing between paragraphs automatically according to the following rules:

 *  Normally, spacing is added after all paragraphs.
 *  In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
 *  In a nested bulleted or numbered list spacing is not added.
 *  Spacing is normally added after a table.
 *  Spacing is not added after a table if it is the last block in a table cell.
 *  Spacing is not added after the last paragraph in a table cell.

**Returns:**
boolean - The corresponding  boolean  value.
### getSpaceBefore() {#getSpaceBefore}
```
public double getSpaceBefore()
```


Gets the amount of spacing (in points) before the paragraph.

Has no effect when [getSpaceBeforeAuto()](../../com.aspose.words/paragraphformat\#getSpaceBeforeAuto) / [setSpaceBeforeAuto(boolean)](../../com.aspose.words/paragraphformat\#setSpaceBeforeAuto-boolean) is  true .

Valid values range from 0 to 1584 inclusive.

**Returns:**
double - The amount of spacing (in points) before the paragraph.
### getSpaceBeforeAuto() {#getSpaceBeforeAuto}
```
public boolean getSpaceBeforeAuto()
```


True if the amount of spacing before the paragraph is set automatically.

When set to  true , overrides the effect of [getSpaceBefore()](../../com.aspose.words/paragraphformat\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat\#setSpaceBefore-double).

When you set paragraph Space Before and Space After to Auto, Microsoft Word adds 14 points spacing between paragraphs automatically according to the following rules:

 *  Normally, spacing is added after all paragraphs.
 *  In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
 *  In a nested bulleted or numbered list spacing is not added.
 *  Spacing is normally added after a table.
 *  Spacing is not added after a table if it is the last block in a table cell.
 *  Spacing is not added after the last paragraph in a table cell.

**Returns:**
boolean - The corresponding  boolean  value.
### getStyle() {#getStyle}
```
public Style getStyle()
```


Gets the paragraph style applied to this formatting.

**Returns:**
[Style](../../com.aspose.words/style) - The paragraph style applied to this formatting.
### getStyleIdentifier() {#getStyleIdentifier}
```
public int getStyleIdentifier()
```


Gets the locale independent style identifier of the paragraph style applied to this formatting.

**Returns:**
int - The locale independent style identifier of the paragraph style applied to this formatting. The returned value is one of [StyleIdentifier](../../com.aspose.words/styleidentifier) constants.
### getStyleName() {#getStyleName}
```
public String getStyleName()
```


Gets the name of the paragraph style applied to this formatting.

**Returns:**
java.lang.String - The name of the paragraph style applied to this formatting.
### getSuppressAutoHyphens() {#getSuppressAutoHyphens}
```
public boolean getSuppressAutoHyphens()
```


Specifies whether the current paragraph should be exempted from any hyphenation which is applied in the document settings.

**Returns:**
boolean - The corresponding  boolean  value.
### getSuppressLineNumbers() {#getSuppressLineNumbers}
```
public boolean getSuppressLineNumbers()
```


Specifies whether the current paragraph's lines should be exempted from line numbering which is applied in the parent section.

**Returns:**
boolean - The corresponding  boolean  value.
### getTabStops() {#getTabStops}
```
public TabStopCollection getTabStops()
```


Gets the collection of custom tab stops defined for this object.

**Returns:**
[TabStopCollection](../../com.aspose.words/tabstopcollection) - The collection of custom tab stops defined for this object.
### getWidowControl() {#getWidowControl}
```
public boolean getWidowControl()
```


True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph.

**Returns:**
boolean - The corresponding  boolean  value.
### getWordWrap() {#getWordWrap}
```
public boolean getWordWrap()
```


If this property is  false , Latin text in the middle of a word can be wrapped for the current paragraph. Otherwise Latin text is wrapped by whole words.

**Returns:**
boolean - The corresponding  boolean  value.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### isHeading() {#isHeading}
```
public boolean isHeading()
```


True when the paragraph style is one of the built-in Heading styles.

**Returns:**
boolean - The corresponding  boolean  value.
### isListItem() {#isListItem}
```
public boolean isListItem()
```


True when the paragraph is an item in a bulleted or numbered list.

**Returns:**
boolean - The corresponding  boolean  value.
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### setAddSpaceBetweenFarEastAndAlpha(boolean value) {#setAddSpaceBetweenFarEastAndAlpha-boolean}
```
public void setAddSpaceBetweenFarEastAndAlpha(boolean value)
```


Sets a flag indicating whether inter-character spacing is automatically adjusted between regions of Latin text and regions of East Asian text in the current paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether inter-character spacing is automatically adjusted between regions of Latin text and regions of East Asian text in the current paragraph. |

### setAddSpaceBetweenFarEastAndDigit(boolean value) {#setAddSpaceBetweenFarEastAndDigit-boolean}
```
public void setAddSpaceBetweenFarEastAndDigit(boolean value)
```


Sets a flag indicating whether inter-character spacing is automatically adjusted between regions of numbers and regions of East Asian text in the current paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether inter-character spacing is automatically adjusted between regions of numbers and regions of East Asian text in the current paragraph. |

### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


Sets text alignment for the paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Text alignment for the paragraph. The value must be one of [ParagraphAlignment](../../com.aspose.words/paragraphalignment) constants. |

### setBidi(boolean value) {#setBidi-boolean}
```
public void setBidi(boolean value)
```


Sets whether this is a right-to-left paragraph.

When  true , the runs and other inline objects in this paragraph are laid out right to left.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether this is a right-to-left paragraph. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setCharacterUnitFirstLineIndent(double value) {#setCharacterUnitFirstLineIndent-double}
```
public void setCharacterUnitFirstLineIndent(double value)
```


Sets the value (in characters) for the first-line or hanging indent.

Use positive values to set the first-line indent, and negative values to set the hanging indent.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The value (in characters) for the first-line or hanging indent. |

### setCharacterUnitLeftIndent(double value) {#setCharacterUnitLeftIndent-double}
```
public void setCharacterUnitLeftIndent(double value)
```


Sets the left indent value (in characters) for the specified paragraphs.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The left indent value (in characters) for the specified paragraphs. |

### setCharacterUnitRightIndent(double value) {#setCharacterUnitRightIndent-double}
```
public void setCharacterUnitRightIndent(double value)
```


Sets the right indent value (in characters) for the specified paragraphs.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The right indent value (in characters) for the specified paragraphs. |

### setDropCapPosition(int value) {#setDropCapPosition-int}
```
public void setDropCapPosition(int value)
```


Sets the position for a drop cap text.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The position for a drop cap text. The value must be one of [DropCapPosition](../../com.aspose.words/dropcapposition) constants. |

### setFarEastLineBreakControl(boolean value) {#setFarEastLineBreakControl-boolean}
```
public void setFarEastLineBreakControl(boolean value)
```


Sets a flag indicating whether East Asian line-breaking rules are applied to the current paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether East Asian line-breaking rules are applied to the current paragraph. |

### setFirstLineIndent(double value) {#setFirstLineIndent-double}
```
public void setFirstLineIndent(double value)
```


Sets the value (in points) for a first line or hanging indent.

Use positive values to set the first-line indent, and negative values to set the hanging indent.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The value (in points) for a first line or hanging indent. |

### setHangingPunctuation(boolean value) {#setHangingPunctuation-boolean}
```
public void setHangingPunctuation(boolean value)
```


Sets a flag indicating whether hanging punctuation is enabled for the current paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether hanging punctuation is enabled for the current paragraph. |

### setKeepTogether(boolean value) {#setKeepTogether-boolean}
```
public void setKeepTogether(boolean value)
```


True if all lines in the paragraph are to remain on the same page.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setKeepWithNext(boolean value) {#setKeepWithNext-boolean}
```
public void setKeepWithNext(boolean value)
```


True if the paragraph is to remains on the same page as the paragraph that follows it.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setLeftIndent(double value) {#setLeftIndent-double}
```
public void setLeftIndent(double value)
```


Sets the value (in points) that represents the left indent for paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The value (in points) that represents the left indent for paragraph. |

### setLineSpacing(double value) {#setLineSpacing-double}
```
public void setLineSpacing(double value)
```


Sets the line spacing (in points) for the paragraph.

When [getLineSpacingRule()](../../com.aspose.words/paragraphformat\#getLineSpacingRule) / [setLineSpacingRule(int)](../../com.aspose.words/paragraphformat\#setLineSpacingRule-int) property is set to [LineSpacingRule.AT\_LEAST](../../com.aspose.words/linespacingrule\#AT-LEAST), the line spacing can be greater than or equal to, but never less than the specified [getLineSpacing()](../../com.aspose.words/paragraphformat\#getLineSpacing) / [setLineSpacing(double)](../../com.aspose.words/paragraphformat\#setLineSpacing-double) value.

When [getLineSpacingRule()](../../com.aspose.words/paragraphformat\#getLineSpacingRule) / [setLineSpacingRule(int)](../../com.aspose.words/paragraphformat\#setLineSpacingRule-int) property is set to [LineSpacingRule.EXACTLY](../../com.aspose.words/linespacingrule\#EXACTLY), the line spacing never changes from the specified [getLineSpacing()](../../com.aspose.words/paragraphformat\#getLineSpacing) / [setLineSpacing(double)](../../com.aspose.words/paragraphformat\#setLineSpacing-double) value, even if a larger font is used within the paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The line spacing (in points) for the paragraph. |

### setLineSpacingRule(int value) {#setLineSpacingRule-int}
```
public void setLineSpacingRule(int value)
```


Sets the line spacing for the paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The line spacing for the paragraph. The value must be one of [LineSpacingRule](../../com.aspose.words/linespacingrule) constants. |

### setLineUnitAfter(double value) {#setLineUnitAfter-double}
```
public void setLineUnitAfter(double value)
```


Sets the amount of spacing (in gridlines) after the paragraphs.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of spacing (in gridlines) after the paragraphs. |

### setLineUnitBefore(double value) {#setLineUnitBefore-double}
```
public void setLineUnitBefore(double value)
```


Sets the amount of spacing (in gridlines) before the paragraphs.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of spacing (in gridlines) before the paragraphs. |

### setLinesToDrop(int value) {#setLinesToDrop-int}
```
public void setLinesToDrop(int value)
```


Sets the number of lines of the paragraph text used to calculate the drop cap height.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The number of lines of the paragraph text used to calculate the drop cap height. |

### setNoSpaceBetweenParagraphsOfSameStyle(boolean value) {#setNoSpaceBetweenParagraphsOfSameStyle-boolean}
```
public void setNoSpaceBetweenParagraphsOfSameStyle(boolean value)
```


When  true , [getSpaceBefore()](../../com.aspose.words/paragraphformat\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat\#setSpaceBefore-double) and [getSpaceAfter()](../../com.aspose.words/paragraphformat\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat\#setSpaceAfter-double) will be ignored between the paragraphs of the same style.

This setting only takes affect when applied to a paragraph style. If applied to a paragraph directly, it has no effect.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setOutlineLevel(int value) {#setOutlineLevel-int}
```
public void setOutlineLevel(int value)
```


Specifies the outline level of the paragraph in the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [OutlineLevel](../../com.aspose.words/outlinelevel) constants. |

### setPageBreakBefore(boolean value) {#setPageBreakBefore-boolean}
```
public void setPageBreakBefore(boolean value)
```


True if a page break is forced before the paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setRightIndent(double value) {#setRightIndent-double}
```
public void setRightIndent(double value)
```


Sets the value (in points) that represents the right indent for paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The value (in points) that represents the right indent for paragraph. |

### setSnapToGrid(boolean value) {#setSnapToGrid-boolean}
```
public void setSnapToGrid(boolean value)
```


Specifies whether the current paragraph should use the document grid lines per page settings when laying out the contents in the paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setSpaceAfter(double value) {#setSpaceAfter-double}
```
public void setSpaceAfter(double value)
```


Sets the amount of spacing (in points) after the paragraph.

Has no effect when [getSpaceAfterAuto()](../../com.aspose.words/paragraphformat\#getSpaceAfterAuto) / [setSpaceAfterAuto(boolean)](../../com.aspose.words/paragraphformat\#setSpaceAfterAuto-boolean) is  true .

Valid values \\u200b\\u200brange from 0 to 1584 inclusive.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of spacing (in points) after the paragraph. |

### setSpaceAfterAuto(boolean value) {#setSpaceAfterAuto-boolean}
```
public void setSpaceAfterAuto(boolean value)
```


True if the amount of spacing after the paragraph is set automatically.

When set to  true , overrides the effect of [getSpaceAfter()](../../com.aspose.words/paragraphformat\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat\#setSpaceAfter-double).

When you set paragraph Space Before and Space After to Auto, Microsoft Word adds 14 points spacing between paragraphs automatically according to the following rules:

 *  Normally, spacing is added after all paragraphs.
 *  In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
 *  In a nested bulleted or numbered list spacing is not added.
 *  Spacing is normally added after a table.
 *  Spacing is not added after a table if it is the last block in a table cell.
 *  Spacing is not added after the last paragraph in a table cell.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setSpaceBefore(double value) {#setSpaceBefore-double}
```
public void setSpaceBefore(double value)
```


Sets the amount of spacing (in points) before the paragraph.

Has no effect when [getSpaceBeforeAuto()](../../com.aspose.words/paragraphformat\#getSpaceBeforeAuto) / [setSpaceBeforeAuto(boolean)](../../com.aspose.words/paragraphformat\#setSpaceBeforeAuto-boolean) is  true .

Valid values range from 0 to 1584 inclusive.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of spacing (in points) before the paragraph. |

### setSpaceBeforeAuto(boolean value) {#setSpaceBeforeAuto-boolean}
```
public void setSpaceBeforeAuto(boolean value)
```


True if the amount of spacing before the paragraph is set automatically.

When set to  true , overrides the effect of [getSpaceBefore()](../../com.aspose.words/paragraphformat\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat\#setSpaceBefore-double).

When you set paragraph Space Before and Space After to Auto, Microsoft Word adds 14 points spacing between paragraphs automatically according to the following rules:

 *  Normally, spacing is added after all paragraphs.
 *  In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
 *  In a nested bulleted or numbered list spacing is not added.
 *  Spacing is normally added after a table.
 *  Spacing is not added after a table if it is the last block in a table cell.
 *  Spacing is not added after the last paragraph in a table cell.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setStyle(Style value) {#setStyle-com.aspose.words.Style}
```
public void setStyle(Style value)
```


Sets the paragraph style applied to this formatting.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style) | The paragraph style applied to this formatting. |

### setStyleIdentifier(int value) {#setStyleIdentifier-int}
```
public void setStyleIdentifier(int value)
```


Sets the locale independent style identifier of the paragraph style applied to this formatting.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The locale independent style identifier of the paragraph style applied to this formatting. The value must be one of [StyleIdentifier](../../com.aspose.words/styleidentifier) constants. |

### setStyleName(String value) {#setStyleName-java.lang.String}
```
public void setStyleName(String value)
```


Sets the name of the paragraph style applied to this formatting.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the paragraph style applied to this formatting. |

### setSuppressAutoHyphens(boolean value) {#setSuppressAutoHyphens-boolean}
```
public void setSuppressAutoHyphens(boolean value)
```


Specifies whether the current paragraph should be exempted from any hyphenation which is applied in the document settings.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setSuppressLineNumbers(boolean value) {#setSuppressLineNumbers-boolean}
```
public void setSuppressLineNumbers(boolean value)
```


Specifies whether the current paragraph's lines should be exempted from line numbering which is applied in the parent section.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setWidowControl(boolean value) {#setWidowControl-boolean}
```
public void setWidowControl(boolean value)
```


True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setWordWrap(boolean value) {#setWordWrap-boolean}
```
public void setWordWrap(boolean value)
```


If this property is  false , Latin text in the middle of a word can be wrapped for the current paragraph. Otherwise Latin text is wrapped by whole words.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

