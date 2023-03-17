---
title: Font
linktitle: Font
second_title: Aspose.Words for Java API Reference
description: Contains font attributes font name font size color and so on for an object in Java.
type: docs
weight: 277
url: /java/com.aspose.words/font/
---

**Inheritance:**
java.lang.Object
```
public class Font
```

Contains font attributes (font name, font size, color, and so on) for an object.

To learn more, visit the [ Working with Fonts ][Working with Fonts] documentation article.

You do not create instances of the [Font](../../com.aspose.words/font/) class directly. You just use [Font](../../com.aspose.words/font/) to access the font properties of the various objects such as [Run](../../com.aspose.words/run/), [Paragraph](../../com.aspose.words/paragraph/), [Style](../../com.aspose.words/style/), [DocumentBuilder](../../com.aspose.words/documentbuilder/).


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Methods

| Method | Description |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Resets to default font formatting. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int) |  |
| [getAllCaps()](#getAllCaps) | True if the font is formatted as all capital letters. |
| [getAutoColor()](#getAutoColor) | Returns the present calculated color of the text (black or white) to be used for 'auto color'. |
| [getBidi()](#getBidi) | Specifies whether the contents of this run shall have right-to-left characteristics. |
| [getBold()](#getBold) | True if the font is formatted as bold. |
| [getBoldBi()](#getBoldBi) | True if the right-to-left text is formatted as bold. |
| [getBorder()](#getBorder) | Returns a [Border](../../com.aspose.words/border/) object that specifies border for the font. |
| [getClass()](#getClass) |  |
| [getColor()](#getColor) | Gets the color of the font. |
| [getComplexScript()](#getComplexScript) | Specifies whether the contents of this run shall be treated as complex script text regardless of their Unicode character values when determining the formatting for this run. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getDoubleStrikeThrough()](#getDoubleStrikeThrough) | True if the font is formatted as double strikethrough text. |
| [getEmboss()](#getEmboss) | True if the font is formatted as embossed. |
| [getEmphasisMark()](#getEmphasisMark) | Gets the emphasis mark applied to this formatting. |
| [getEngrave()](#getEngrave) | True if the font is formatted as engraved. |
| [getFill()](#getFill) | Gets fill formatting for the [Font](../../com.aspose.words/font/). |
| [getFillType()](#getFillType) |  |
| [getFillableBackColor()](#getFillableBackColor) |  |
| [getFillableBackThemeColor()](#getFillableBackThemeColor) |  |
| [getFillableBackTintAndShade()](#getFillableBackTintAndShade) |  |
| [getFillableForeColor()](#getFillableForeColor) |  |
| [getFillableForeThemeColor()](#getFillableForeThemeColor) |  |
| [getFillableForeTintAndShade()](#getFillableForeTintAndShade) |  |
| [getFillableImageBytes()](#getFillableImageBytes) |  |
| [getFillableTransparency()](#getFillableTransparency) |  |
| [getFillableVisible()](#getFillableVisible) |  |
| [getFilledColor()](#getFilledColor) |  |
| [getGradientAngle()](#getGradientAngle) |  |
| [getGradientStops()](#getGradientStops) |  |
| [getGradientStyle()](#getGradientStyle) |  |
| [getGradientVariant()](#getGradientVariant) |  |
| [getHidden()](#getHidden) | True if the font is formatted as hidden text. |
| [getHighlightColor()](#getHighlightColor) | Gets the highlight (marker) color. |
| [getItalic()](#getItalic) | True if the font is formatted as italic. |
| [getItalicBi()](#getItalicBi) | True if the right-to-left text is formatted as italic. |
| [getKerning()](#getKerning) | Gets the font size at which kerning starts. |
| [getLineSpacing()](#getLineSpacing) | Returns line spacing of this font (in points). |
| [getLocaleId()](#getLocaleId) | Gets the locale identifier (language) of the formatted characters. |
| [getLocaleIdBi()](#getLocaleIdBi) | Gets the locale identifier (language) of the formatted right-to-left characters. |
| [getLocaleIdFarEast()](#getLocaleIdFarEast) | Gets the locale identifier (language) of the formatted Asian characters. |
| [getName()](#getName) | Gets the name of the font. |
| [getNameAscii()](#getNameAscii) | Gets the font used for Latin text (characters with character codes from 0 (zero) through 127). |
| [getNameBi()](#getNameBi) | Gets the name of the font in a right-to-left language document. |
| [getNameFarEast()](#getNameFarEast) | Gets an East Asian font name. |
| [getNameOther()](#getNameOther) | Gets the font used for characters with character codes from 128 through 255. |
| [getNoProofing()](#getNoProofing) | True when the formatted characters are not to be spell checked. |
| [getOn()](#getOn) |  |
| [getOpacity()](#getOpacity) |  |
| [getOutline()](#getOutline) | True if the font is formatted as outline. |
| [getPatternType()](#getPatternType) |  |
| [getPosition()](#getPosition) | Gets the position of text (in points) relative to the base line. |
| [getPresetTexture()](#getPresetTexture) |  |
| [getRotateWithObject()](#getRotateWithObject) |  |
| [getScaling()](#getScaling) | Gets character width scaling in percent. |
| [getShading()](#getShading) | Returns a [Shading](../../com.aspose.words/shading/) object that refers to the shading formatting for the font. |
| [getShadow()](#getShadow) | True if the font is formatted as shadowed. |
| [getSize()](#getSize) | Gets the font size in points. |
| [getSizeBi()](#getSizeBi) | Gets the font size in points used in a right-to-left document. |
| [getSmallCaps()](#getSmallCaps) | True if the font is formatted as small capital letters. |
| [getSnapToGrid()](#getSnapToGrid) | Specifies whether the current font should use the document grid characters per line settings when laying out. |
| [getSpacing()](#getSpacing) | Gets the spacing (in points) between characters . |
| [getStrikeThrough()](#getStrikeThrough) | True if the font is formatted as strikethrough text. |
| [getStyle()](#getStyle) | Gets the character style applied to this formatting. |
| [getStyleIdentifier()](#getStyleIdentifier) | Gets the locale independent style identifier of the character style applied to this formatting. |
| [getStyleName()](#getStyleName) | Gets the name of the character style applied to this formatting. |
| [getSubscript()](#getSubscript) | True if the font is formatted as subscript. |
| [getSuperscript()](#getSuperscript) | True if the font is formatted as superscript. |
| [getTextEffect()](#getTextEffect) | Gets the font animation effect. |
| [getTextureAlignment()](#getTextureAlignment) |  |
| [getThemeColor()](#getThemeColor) | Gets the theme color in the applied color scheme that is associated with this [Font](../../com.aspose.words/font/) object. |
| [getThemeFont()](#getThemeFont) | Gets the theme font in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object. |
| [getThemeFontAscii()](#getThemeFontAscii) | Gets the theme font used for Latin text (characters with character codes from 0 (zero) through 127) in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object. |
| [getThemeFontBi()](#getThemeFontBi) | Gets the theme font in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object in a right-to-left language document. |
| [getThemeFontFarEast()](#getThemeFontFarEast) | Gets the East Asian theme font in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object. |
| [getThemeFontOther()](#getThemeFontOther) | Gets the theme font used for characters with character codes from 128 through 255 in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object. |
| [getTintAndShade()](#getTintAndShade) | Gets a double value that lightens or darkens a color. |
| [getUnderline()](#getUnderline) | Gets the type of underline applied to the font. |
| [getUnderlineColor()](#getUnderlineColor) | Gets the color of the underline applied to the font. |
| [hasDmlEffect(int dmlEffectType)](#hasDmlEffect-int) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [oneColorGradient(int style, int variant, double degree)](#oneColorGradient-int-int-double) |  |
| [patterned(int patternType)](#patterned-int) |  |
| [presetTextured(int presetTexture)](#presetTextured-int) |  |
| [setAllCaps(boolean value)](#setAllCaps-boolean) | True if the font is formatted as all capital letters. |
| [setBidi(boolean value)](#setBidi-boolean) | Specifies whether the contents of this run shall have right-to-left characteristics. |
| [setBold(boolean value)](#setBold-boolean) | True if the font is formatted as bold. |
| [setBoldBi(boolean value)](#setBoldBi-boolean) | True if the right-to-left text is formatted as bold. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setColor(Color value)](#setColor-java.awt.Color) | Sets the color of the font. |
| [setComplexScript(boolean value)](#setComplexScript-boolean) | Specifies whether the contents of this run shall be treated as complex script text regardless of their Unicode character values when determining the formatting for this run. |
| [setDoubleStrikeThrough(boolean value)](#setDoubleStrikeThrough-boolean) | True if the font is formatted as double strikethrough text. |
| [setEmboss(boolean value)](#setEmboss-boolean) | True if the font is formatted as embossed. |
| [setEmphasisMark(int value)](#setEmphasisMark-int) | Sets the emphasis mark applied to this formatting. |
| [setEngrave(boolean value)](#setEngrave-boolean) | True if the font is formatted as engraved. |
| [setFillableBackColor(Color value)](#setFillableBackColor-java.awt.Color) |  |
| [setFillableBackThemeColor(int value)](#setFillableBackThemeColor-int) |  |
| [setFillableBackTintAndShade(double value)](#setFillableBackTintAndShade-double) |  |
| [setFillableForeColor(Color value)](#setFillableForeColor-java.awt.Color) |  |
| [setFillableForeThemeColor(int value)](#setFillableForeThemeColor-int) |  |
| [setFillableForeTintAndShade(double value)](#setFillableForeTintAndShade-double) |  |
| [setFillableTransparency(double value)](#setFillableTransparency-double) |  |
| [setFillableVisible(boolean value)](#setFillableVisible-boolean) |  |
| [setFilledColor(Color value)](#setFilledColor-java.awt.Color) |  |
| [setGradientAngle(double value)](#setGradientAngle-double) |  |
| [setHidden(boolean value)](#setHidden-boolean) | True if the font is formatted as hidden text. |
| [setHighlightColor(Color value)](#setHighlightColor-java.awt.Color) | Sets the highlight (marker) color. |
| [setImage(byte[] imageBytes)](#setImage-byte) |  |
| [setItalic(boolean value)](#setItalic-boolean) | True if the font is formatted as italic. |
| [setItalicBi(boolean value)](#setItalicBi-boolean) | True if the right-to-left text is formatted as italic. |
| [setKerning(double value)](#setKerning-double) | Sets the font size at which kerning starts. |
| [setLocaleId(int value)](#setLocaleId-int) | Sets the locale identifier (language) of the formatted characters. |
| [setLocaleIdBi(int value)](#setLocaleIdBi-int) | Sets the locale identifier (language) of the formatted right-to-left characters. |
| [setLocaleIdFarEast(int value)](#setLocaleIdFarEast-int) | Sets the locale identifier (language) of the formatted Asian characters. |
| [setName(String value)](#setName-java.lang.String) | Sets the name of the font. |
| [setNameAscii(String value)](#setNameAscii-java.lang.String) | Sets the font used for Latin text (characters with character codes from 0 (zero) through 127). |
| [setNameBi(String value)](#setNameBi-java.lang.String) | Sets the name of the font in a right-to-left language document. |
| [setNameFarEast(String value)](#setNameFarEast-java.lang.String) | Sets an East Asian font name. |
| [setNameOther(String value)](#setNameOther-java.lang.String) | Sets the font used for characters with character codes from 128 through 255. |
| [setNoProofing(boolean value)](#setNoProofing-boolean) | True when the formatted characters are not to be spell checked. |
| [setOn(boolean value)](#setOn-boolean) |  |
| [setOpacity(double value)](#setOpacity-double) |  |
| [setOutline(boolean value)](#setOutline-boolean) | True if the font is formatted as outline. |
| [setPosition(double value)](#setPosition-double) | Sets the position of text (in points) relative to the base line. |
| [setRotateWithObject(boolean value)](#setRotateWithObject-boolean) |  |
| [setScaling(int value)](#setScaling-int) | Sets character width scaling in percent. |
| [setShadow(boolean value)](#setShadow-boolean) | True if the font is formatted as shadowed. |
| [setSize(double value)](#setSize-double) | Sets the font size in points. |
| [setSizeBi(double value)](#setSizeBi-double) | Sets the font size in points used in a right-to-left document. |
| [setSmallCaps(boolean value)](#setSmallCaps-boolean) | True if the font is formatted as small capital letters. |
| [setSnapToGrid(boolean value)](#setSnapToGrid-boolean) | Specifies whether the current font should use the document grid characters per line settings when laying out. |
| [setSpacing(double value)](#setSpacing-double) | Sets the spacing (in points) between characters . |
| [setStrikeThrough(boolean value)](#setStrikeThrough-boolean) | True if the font is formatted as strikethrough text. |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style) | Sets the character style applied to this formatting. |
| [setStyleIdentifier(int value)](#setStyleIdentifier-int) | Sets the locale independent style identifier of the character style applied to this formatting. |
| [setStyleName(String value)](#setStyleName-java.lang.String) | Sets the name of the character style applied to this formatting. |
| [setSubscript(boolean value)](#setSubscript-boolean) | True if the font is formatted as subscript. |
| [setSuperscript(boolean value)](#setSuperscript-boolean) | True if the font is formatted as superscript. |
| [setTextEffect(int value)](#setTextEffect-int) | Sets the font animation effect. |
| [setTextureAlignment(int value)](#setTextureAlignment-int) |  |
| [setThemeColor(int value)](#setThemeColor-int) | Sets the theme color in the applied color scheme that is associated with this [Font](../../com.aspose.words/font/) object. |
| [setThemeFont(int value)](#setThemeFont-int) | Sets the theme font in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object. |
| [setThemeFontAscii(int value)](#setThemeFontAscii-int) | Sets the theme font used for Latin text (characters with character codes from 0 (zero) through 127) in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object. |
| [setThemeFontBi(int value)](#setThemeFontBi-int) | Sets the theme font in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object in a right-to-left language document. |
| [setThemeFontFarEast(int value)](#setThemeFontFarEast-int) | Sets the East Asian theme font in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object. |
| [setThemeFontOther(int value)](#setThemeFontOther-int) | Sets the theme font used for characters with character codes from 128 through 255 in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object. |
| [setTintAndShade(double value)](#setTintAndShade-double) | Sets a double value that lightens or darkens a color. |
| [setUnderline(int value)](#setUnderline-int) | Sets the type of underline applied to the font. |
| [setUnderlineColor(Color value)](#setUnderlineColor-java.awt.Color) | Sets the color of the underline applied to the font. |
| [solid()](#solid) |  |
| [toString()](#toString) |  |
| [twoColorGradient(int style, int variant)](#twoColorGradient-int-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Resets to default font formatting.

Removes all font formatting specified explicitly on the object from which [Font](../../com.aspose.words/font/) was obtained so the font formatting will be inherited from the appropriate parent.

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
### getAllCaps() {#getAllCaps}
```
public boolean getAllCaps()
```


True if the font is formatted as all capital letters.

**Returns:**
boolean - The corresponding  boolean  value.
### getAutoColor() {#getAutoColor}
```
public Color getAutoColor()
```


Returns the present calculated color of the text (black or white) to be used for 'auto color'. If the color is not 'auto' then returns [getColor()](../../com.aspose.words/font/\#getColor) / [setColor(java.awt.Color)](../../com.aspose.words/font/\#setColor-java.awt.Color).

When text has 'automatic color', the actual color of text is calculated automatically so that it is readable against the background color. As you change the background color, the text color will automatically switch to black or white in MS Word to maximize legibility.

**Returns:**
java.awt.Color - The present calculated color of the text (black or white) to be used for 'auto color'.
### getBidi() {#getBidi}
```
public boolean getBidi()
```


Specifies whether the contents of this run shall have right-to-left characteristics.

This property, when on, shall not be used with strongly left-to-right text. Any behavior under that condition is unspecified. This property, when off, shall not be used with strong right-to-left text. Any behavior under that condition is unspecified.

When the contents of this run are displayed, all characters shall be treated as complex script characters for formatting purposes. This means that [getBoldBi()](../../com.aspose.words/font/\#getBoldBi) / [setBoldBi(boolean)](../../com.aspose.words/font/\#setBoldBi-boolean), [getItalicBi()](../../com.aspose.words/font/\#getItalicBi) / [setItalicBi(boolean)](../../com.aspose.words/font/\#setItalicBi-boolean), [getSizeBi()](../../com.aspose.words/font/\#getSizeBi) / [setSizeBi(double)](../../com.aspose.words/font/\#setSizeBi-double) and a corresponding font name will be used when rendering this run.

Also, when the contents of this run are displayed, this property acts as a right-to-left override for characters which are classified as "weak types" and "neutral types".

**Returns:**
boolean - The corresponding  boolean  value.
### getBold() {#getBold}
```
public boolean getBold()
```


True if the font is formatted as bold.

**Returns:**
boolean - The corresponding  boolean  value.
### getBoldBi() {#getBoldBi}
```
public boolean getBoldBi()
```


True if the right-to-left text is formatted as bold.

**Returns:**
boolean - The corresponding  boolean  value.
### getBorder() {#getBorder}
```
public Border getBorder()
```


Returns a [Border](../../com.aspose.words/border/) object that specifies border for the font.

**Returns:**
[Border](../../com.aspose.words/border/) - A [Border](../../com.aspose.words/border/) object that specifies border for the font.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getColor() {#getColor}
```
public Color getColor()
```


Gets the color of the font.

**Returns:**
java.awt.Color - The color of the font.
### getComplexScript() {#getComplexScript}
```
public boolean getComplexScript()
```


Specifies whether the contents of this run shall be treated as complex script text regardless of their Unicode character values when determining the formatting for this run.

**Returns:**
boolean - The corresponding  boolean  value.
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
### getDoubleStrikeThrough() {#getDoubleStrikeThrough}
```
public boolean getDoubleStrikeThrough()
```


True if the font is formatted as double strikethrough text.

**Returns:**
boolean - The corresponding  boolean  value.
### getEmboss() {#getEmboss}
```
public boolean getEmboss()
```


True if the font is formatted as embossed.

**Returns:**
boolean - The corresponding  boolean  value.
### getEmphasisMark() {#getEmphasisMark}
```
public int getEmphasisMark()
```


Gets the emphasis mark applied to this formatting.

**Returns:**
int - The emphasis mark applied to this formatting. The returned value is one of [EmphasisMark](../../com.aspose.words/emphasismark/) constants.
### getEngrave() {#getEngrave}
```
public boolean getEngrave()
```


True if the font is formatted as engraved.

**Returns:**
boolean - The corresponding  boolean  value.
### getFill() {#getFill}
```
public Fill getFill()
```


Gets fill formatting for the [Font](../../com.aspose.words/font/).

**Returns:**
[Fill](../../com.aspose.words/fill/) - Fill formatting for the [Font](../../com.aspose.words/font/).
### getFillType() {#getFillType}
```
public int getFillType()
```




**Returns:**
int
### getFillableBackColor() {#getFillableBackColor}
```
public Color getFillableBackColor()
```




**Returns:**
java.awt.Color
### getFillableBackThemeColor() {#getFillableBackThemeColor}
```
public int getFillableBackThemeColor()
```




**Returns:**
int
### getFillableBackTintAndShade() {#getFillableBackTintAndShade}
```
public double getFillableBackTintAndShade()
```




**Returns:**
double
### getFillableForeColor() {#getFillableForeColor}
```
public Color getFillableForeColor()
```




**Returns:**
java.awt.Color
### getFillableForeThemeColor() {#getFillableForeThemeColor}
```
public int getFillableForeThemeColor()
```




**Returns:**
int
### getFillableForeTintAndShade() {#getFillableForeTintAndShade}
```
public double getFillableForeTintAndShade()
```




**Returns:**
double
### getFillableImageBytes() {#getFillableImageBytes}
```
public byte[] getFillableImageBytes()
```




**Returns:**
byte[]
### getFillableTransparency() {#getFillableTransparency}
```
public double getFillableTransparency()
```




**Returns:**
double
### getFillableVisible() {#getFillableVisible}
```
public boolean getFillableVisible()
```




**Returns:**
boolean
### getFilledColor() {#getFilledColor}
```
public Color getFilledColor()
```




**Returns:**
java.awt.Color
### getGradientAngle() {#getGradientAngle}
```
public double getGradientAngle()
```




**Returns:**
double
### getGradientStops() {#getGradientStops}
```
public GradientStopCollection getGradientStops()
```




**Returns:**
[GradientStopCollection](../../com.aspose.words/gradientstopcollection/)
### getGradientStyle() {#getGradientStyle}
```
public int getGradientStyle()
```




**Returns:**
int
### getGradientVariant() {#getGradientVariant}
```
public int getGradientVariant()
```




**Returns:**
int
### getHidden() {#getHidden}
```
public boolean getHidden()
```


True if the font is formatted as hidden text.

**Returns:**
boolean - The corresponding  boolean  value.
### getHighlightColor() {#getHighlightColor}
```
public Color getHighlightColor()
```


Gets the highlight (marker) color.

**Returns:**
java.awt.Color - The highlight (marker) color.
### getItalic() {#getItalic}
```
public boolean getItalic()
```


True if the font is formatted as italic.

**Returns:**
boolean - The corresponding  boolean  value.
### getItalicBi() {#getItalicBi}
```
public boolean getItalicBi()
```


True if the right-to-left text is formatted as italic.

**Returns:**
boolean - The corresponding  boolean  value.
### getKerning() {#getKerning}
```
public double getKerning()
```


Gets the font size at which kerning starts.

**Returns:**
double - The font size at which kerning starts.
### getLineSpacing() {#getLineSpacing}
```
public double getLineSpacing()
```


Returns line spacing of this font (in points).

**Returns:**
double - Line spacing of this font (in points).
### getLocaleId() {#getLocaleId}
```
public int getLocaleId()
```


Gets the locale identifier (language) of the formatted characters. For the list of locale identifiers see https://msdn.microsoft.com/en-us/library/cc233965.aspx

**Returns:**
int - The locale identifier (language) of the formatted characters.
### getLocaleIdBi() {#getLocaleIdBi}
```
public int getLocaleIdBi()
```


Gets the locale identifier (language) of the formatted right-to-left characters. For the list of locale identifiers see https://msdn.microsoft.com/en-us/library/cc233965.aspx

**Returns:**
int - The locale identifier (language) of the formatted right-to-left characters.
### getLocaleIdFarEast() {#getLocaleIdFarEast}
```
public int getLocaleIdFarEast()
```


Gets the locale identifier (language) of the formatted Asian characters. For the list of locale identifiers see https://msdn.microsoft.com/en-us/library/cc233965.aspx

**Returns:**
int - The locale identifier (language) of the formatted Asian characters.
### getName() {#getName}
```
public String getName()
```


Gets the name of the font.

When getting, returns [getNameAscii()](../../com.aspose.words/font/\#getNameAscii) / [setNameAscii(java.lang.String)](../../com.aspose.words/font/\#setNameAscii-java.lang.String).

When setting, sets [getNameAscii()](../../com.aspose.words/font/\#getNameAscii) / [setNameAscii(java.lang.String)](../../com.aspose.words/font/\#setNameAscii-java.lang.String), [getNameBi()](../../com.aspose.words/font/\#getNameBi) / [setNameBi(java.lang.String)](../../com.aspose.words/font/\#setNameBi-java.lang.String), [getNameFarEast()](../../com.aspose.words/font/\#getNameFarEast) / [setNameFarEast(java.lang.String)](../../com.aspose.words/font/\#setNameFarEast-java.lang.String) and [getNameOther()](../../com.aspose.words/font/\#getNameOther) / [setNameOther(java.lang.String)](../../com.aspose.words/font/\#setNameOther-java.lang.String) to the specified value.

**Returns:**
java.lang.String - The name of the font.
### getNameAscii() {#getNameAscii}
```
public String getNameAscii()
```


Gets the font used for Latin text (characters with character codes from 0 (zero) through 127).

**Returns:**
java.lang.String - The font used for Latin text (characters with character codes from 0 (zero) through 127).
### getNameBi() {#getNameBi}
```
public String getNameBi()
```


Gets the name of the font in a right-to-left language document.

**Returns:**
java.lang.String - The name of the font in a right-to-left language document.
### getNameFarEast() {#getNameFarEast}
```
public String getNameFarEast()
```


Gets an East Asian font name.

**Returns:**
java.lang.String - An East Asian font name.
### getNameOther() {#getNameOther}
```
public String getNameOther()
```


Gets the font used for characters with character codes from 128 through 255.

**Returns:**
java.lang.String - The font used for characters with character codes from 128 through 255.
### getNoProofing() {#getNoProofing}
```
public boolean getNoProofing()
```


True when the formatted characters are not to be spell checked.

**Returns:**
boolean - The corresponding  boolean  value.
### getOn() {#getOn}
```
public boolean getOn()
```




**Returns:**
boolean
### getOpacity() {#getOpacity}
```
public double getOpacity()
```




**Returns:**
double
### getOutline() {#getOutline}
```
public boolean getOutline()
```


True if the font is formatted as outline.

**Returns:**
boolean - The corresponding  boolean  value.
### getPatternType() {#getPatternType}
```
public int getPatternType()
```




**Returns:**
int
### getPosition() {#getPosition}
```
public double getPosition()
```


Gets the position of text (in points) relative to the base line. A positive number raises the text, and a negative number lowers it.

**Returns:**
double - The position of text (in points) relative to the base line.
### getPresetTexture() {#getPresetTexture}
```
public int getPresetTexture()
```




**Returns:**
int
### getRotateWithObject() {#getRotateWithObject}
```
public boolean getRotateWithObject()
```




**Returns:**
boolean
### getScaling() {#getScaling}
```
public int getScaling()
```


Gets character width scaling in percent.

**Returns:**
int - Character width scaling in percent.
### getShading() {#getShading}
```
public Shading getShading()
```


Returns a [Shading](../../com.aspose.words/shading/) object that refers to the shading formatting for the font.

**Returns:**
[Shading](../../com.aspose.words/shading/) - A [Shading](../../com.aspose.words/shading/) object that refers to the shading formatting for the font.
### getShadow() {#getShadow}
```
public boolean getShadow()
```


True if the font is formatted as shadowed.

**Returns:**
boolean - The corresponding  boolean  value.
### getSize() {#getSize}
```
public double getSize()
```


Gets the font size in points.

**Returns:**
double - The font size in points.
### getSizeBi() {#getSizeBi}
```
public double getSizeBi()
```


Gets the font size in points used in a right-to-left document.

**Returns:**
double - The font size in points used in a right-to-left document.
### getSmallCaps() {#getSmallCaps}
```
public boolean getSmallCaps()
```


True if the font is formatted as small capital letters.

**Returns:**
boolean - The corresponding  boolean  value.
### getSnapToGrid() {#getSnapToGrid}
```
public boolean getSnapToGrid()
```


Specifies whether the current font should use the document grid characters per line settings when laying out.

**Returns:**
boolean - The corresponding  boolean  value.
### getSpacing() {#getSpacing}
```
public double getSpacing()
```


Gets the spacing (in points) between characters .

**Returns:**
double - The spacing (in points) between characters .
### getStrikeThrough() {#getStrikeThrough}
```
public boolean getStrikeThrough()
```


True if the font is formatted as strikethrough text.

**Returns:**
boolean - The corresponding  boolean  value.
### getStyle() {#getStyle}
```
public Style getStyle()
```


Gets the character style applied to this formatting.

**Returns:**
[Style](../../com.aspose.words/style/) - The character style applied to this formatting.
### getStyleIdentifier() {#getStyleIdentifier}
```
public int getStyleIdentifier()
```


Gets the locale independent style identifier of the character style applied to this formatting.

**Returns:**
int - The locale independent style identifier of the character style applied to this formatting. The returned value is one of [StyleIdentifier](../../com.aspose.words/styleidentifier/) constants.
### getStyleName() {#getStyleName}
```
public String getStyleName()
```


Gets the name of the character style applied to this formatting.

**Returns:**
java.lang.String - The name of the character style applied to this formatting.
### getSubscript() {#getSubscript}
```
public boolean getSubscript()
```


True if the font is formatted as subscript.

**Returns:**
boolean - The corresponding  boolean  value.
### getSuperscript() {#getSuperscript}
```
public boolean getSuperscript()
```


True if the font is formatted as superscript.

**Returns:**
boolean - The corresponding  boolean  value.
### getTextEffect() {#getTextEffect}
```
public int getTextEffect()
```


Gets the font animation effect.

**Returns:**
int - The font animation effect. The returned value is one of [TextEffect](../../com.aspose.words/texteffect/) constants.
### getTextureAlignment() {#getTextureAlignment}
```
public int getTextureAlignment()
```




**Returns:**
int
### getThemeColor() {#getThemeColor}
```
public int getThemeColor()
```


Gets the theme color in the applied color scheme that is associated with this [Font](../../com.aspose.words/font/) object.

**Returns:**
int - The theme color in the applied color scheme that is associated with this [Font](../../com.aspose.words/font/) object. The returned value is one of [ThemeColor](../../com.aspose.words/themecolor/) constants.
### getThemeFont() {#getThemeFont}
```
public int getThemeFont()
```


Gets the theme font in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object.

**Returns:**
int - The theme font in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object. The returned value is one of [ThemeFont](../../com.aspose.words/themefont/) constants.
### getThemeFontAscii() {#getThemeFontAscii}
```
public int getThemeFontAscii()
```


Gets the theme font used for Latin text (characters with character codes from 0 (zero) through 127) in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object.

**Returns:**
int - The theme font used for Latin text (characters with character codes from 0 (zero) through 127) in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object. The returned value is one of [ThemeFont](../../com.aspose.words/themefont/) constants.
### getThemeFontBi() {#getThemeFontBi}
```
public int getThemeFontBi()
```


Gets the theme font in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object in a right-to-left language document.

**Returns:**
int - The theme font in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object in a right-to-left language document. The returned value is one of [ThemeFont](../../com.aspose.words/themefont/) constants.
### getThemeFontFarEast() {#getThemeFontFarEast}
```
public int getThemeFontFarEast()
```


Gets the East Asian theme font in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object.

**Returns:**
int - The East Asian theme font in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object. The returned value is one of [ThemeFont](../../com.aspose.words/themefont/) constants.
### getThemeFontOther() {#getThemeFontOther}
```
public int getThemeFontOther()
```


Gets the theme font used for characters with character codes from 128 through 255 in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object.

**Returns:**
int - The theme font used for characters with character codes from 128 through 255 in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object. The returned value is one of [ThemeFont](../../com.aspose.words/themefont/) constants.
### getTintAndShade() {#getTintAndShade}
```
public double getTintAndShade()
```


Gets a double value that lightens or darkens a color.

The allowed values are in range from -1 (darkest) to 1 (lightest) for this property. Zero (0) is neutral. Attempting to set this property to a value less than -1 or more than 1 results in a java.lang.IllegalArgumentException.

Setting this property for [Font](../../com.aspose.words/font/) object with non-theme colors results in a java.lang.IllegalStateException.

**Returns:**
double - A double value that lightens or darkens a color.
### getUnderline() {#getUnderline}
```
public int getUnderline()
```


Gets the type of underline applied to the font.

**Returns:**
int - The type of underline applied to the font. The returned value is one of [Underline](../../com.aspose.words/underline/) constants.
### getUnderlineColor() {#getUnderlineColor}
```
public Color getUnderlineColor()
```


Gets the color of the underline applied to the font.

**Returns:**
java.awt.Color - The color of the underline applied to the font.
### hasDmlEffect(int dmlEffectType) {#hasDmlEffect-int}
```
public boolean hasDmlEffect(int dmlEffectType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dmlEffectType | int |  |

**Returns:**
boolean
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### oneColorGradient(int style, int variant, double degree) {#oneColorGradient-int-int-double}
```
public void oneColorGradient(int style, int variant, double degree)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| style | int |  |
| variant | int |  |
| degree | double |  |

### patterned(int patternType) {#patterned-int}
```
public void patterned(int patternType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| patternType | int |  |

### presetTextured(int presetTexture) {#presetTextured-int}
```
public void presetTextured(int presetTexture)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| presetTexture | int |  |

### setAllCaps(boolean value) {#setAllCaps-boolean}
```
public void setAllCaps(boolean value)
```


True if the font is formatted as all capital letters.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setBidi(boolean value) {#setBidi-boolean}
```
public void setBidi(boolean value)
```


Specifies whether the contents of this run shall have right-to-left characteristics.

This property, when on, shall not be used with strongly left-to-right text. Any behavior under that condition is unspecified. This property, when off, shall not be used with strong right-to-left text. Any behavior under that condition is unspecified.

When the contents of this run are displayed, all characters shall be treated as complex script characters for formatting purposes. This means that [getBoldBi()](../../com.aspose.words/font/\#getBoldBi) / [setBoldBi(boolean)](../../com.aspose.words/font/\#setBoldBi-boolean), [getItalicBi()](../../com.aspose.words/font/\#getItalicBi) / [setItalicBi(boolean)](../../com.aspose.words/font/\#setItalicBi-boolean), [getSizeBi()](../../com.aspose.words/font/\#getSizeBi) / [setSizeBi(double)](../../com.aspose.words/font/\#setSizeBi-double) and a corresponding font name will be used when rendering this run.

Also, when the contents of this run are displayed, this property acts as a right-to-left override for characters which are classified as "weak types" and "neutral types".

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setBold(boolean value) {#setBold-boolean}
```
public void setBold(boolean value)
```


True if the font is formatted as bold.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setBoldBi(boolean value) {#setBoldBi-boolean}
```
public void setBoldBi(boolean value)
```


True if the right-to-left text is formatted as bold.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Sets the color of the font.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The color of the font. |

### setComplexScript(boolean value) {#setComplexScript-boolean}
```
public void setComplexScript(boolean value)
```


Specifies whether the contents of this run shall be treated as complex script text regardless of their Unicode character values when determining the formatting for this run.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setDoubleStrikeThrough(boolean value) {#setDoubleStrikeThrough-boolean}
```
public void setDoubleStrikeThrough(boolean value)
```


True if the font is formatted as double strikethrough text.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setEmboss(boolean value) {#setEmboss-boolean}
```
public void setEmboss(boolean value)
```


True if the font is formatted as embossed.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setEmphasisMark(int value) {#setEmphasisMark-int}
```
public void setEmphasisMark(int value)
```


Sets the emphasis mark applied to this formatting.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The emphasis mark applied to this formatting. The value must be one of [EmphasisMark](../../com.aspose.words/emphasismark/) constants. |

### setEngrave(boolean value) {#setEngrave-boolean}
```
public void setEngrave(boolean value)
```


True if the font is formatted as engraved.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setFillableBackColor(Color value) {#setFillableBackColor-java.awt.Color}
```
public void setFillableBackColor(Color value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color |  |

### setFillableBackThemeColor(int value) {#setFillableBackThemeColor-int}
```
public void setFillableBackThemeColor(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setFillableBackTintAndShade(double value) {#setFillableBackTintAndShade-double}
```
public void setFillableBackTintAndShade(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setFillableForeColor(Color value) {#setFillableForeColor-java.awt.Color}
```
public void setFillableForeColor(Color value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color |  |

### setFillableForeThemeColor(int value) {#setFillableForeThemeColor-int}
```
public void setFillableForeThemeColor(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setFillableForeTintAndShade(double value) {#setFillableForeTintAndShade-double}
```
public void setFillableForeTintAndShade(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setFillableTransparency(double value) {#setFillableTransparency-double}
```
public void setFillableTransparency(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setFillableVisible(boolean value) {#setFillableVisible-boolean}
```
public void setFillableVisible(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### setFilledColor(Color value) {#setFilledColor-java.awt.Color}
```
public void setFilledColor(Color value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color |  |

### setGradientAngle(double value) {#setGradientAngle-double}
```
public void setGradientAngle(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setHidden(boolean value) {#setHidden-boolean}
```
public void setHidden(boolean value)
```


True if the font is formatted as hidden text.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setHighlightColor(Color value) {#setHighlightColor-java.awt.Color}
```
public void setHighlightColor(Color value)
```


Sets the highlight (marker) color.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The highlight (marker) color. |

### setImage(byte[] imageBytes) {#setImage-byte}
```
public void setImage(byte[] imageBytes)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imageBytes | byte[] |  |

### setItalic(boolean value) {#setItalic-boolean}
```
public void setItalic(boolean value)
```


True if the font is formatted as italic.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setItalicBi(boolean value) {#setItalicBi-boolean}
```
public void setItalicBi(boolean value)
```


True if the right-to-left text is formatted as italic.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setKerning(double value) {#setKerning-double}
```
public void setKerning(double value)
```


Sets the font size at which kerning starts.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The font size at which kerning starts. |

### setLocaleId(int value) {#setLocaleId-int}
```
public void setLocaleId(int value)
```


Sets the locale identifier (language) of the formatted characters. For the list of locale identifiers see https://msdn.microsoft.com/en-us/library/cc233965.aspx

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The locale identifier (language) of the formatted characters. |

### setLocaleIdBi(int value) {#setLocaleIdBi-int}
```
public void setLocaleIdBi(int value)
```


Sets the locale identifier (language) of the formatted right-to-left characters. For the list of locale identifiers see https://msdn.microsoft.com/en-us/library/cc233965.aspx

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The locale identifier (language) of the formatted right-to-left characters. |

### setLocaleIdFarEast(int value) {#setLocaleIdFarEast-int}
```
public void setLocaleIdFarEast(int value)
```


Sets the locale identifier (language) of the formatted Asian characters. For the list of locale identifiers see https://msdn.microsoft.com/en-us/library/cc233965.aspx

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The locale identifier (language) of the formatted Asian characters. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Sets the name of the font.

When getting, returns [getNameAscii()](../../com.aspose.words/font/\#getNameAscii) / [setNameAscii(java.lang.String)](../../com.aspose.words/font/\#setNameAscii-java.lang.String).

When setting, sets [getNameAscii()](../../com.aspose.words/font/\#getNameAscii) / [setNameAscii(java.lang.String)](../../com.aspose.words/font/\#setNameAscii-java.lang.String), [getNameBi()](../../com.aspose.words/font/\#getNameBi) / [setNameBi(java.lang.String)](../../com.aspose.words/font/\#setNameBi-java.lang.String), [getNameFarEast()](../../com.aspose.words/font/\#getNameFarEast) / [setNameFarEast(java.lang.String)](../../com.aspose.words/font/\#setNameFarEast-java.lang.String) and [getNameOther()](../../com.aspose.words/font/\#getNameOther) / [setNameOther(java.lang.String)](../../com.aspose.words/font/\#setNameOther-java.lang.String) to the specified value.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the font. |

### setNameAscii(String value) {#setNameAscii-java.lang.String}
```
public void setNameAscii(String value)
```


Sets the font used for Latin text (characters with character codes from 0 (zero) through 127).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The font used for Latin text (characters with character codes from 0 (zero) through 127). |

### setNameBi(String value) {#setNameBi-java.lang.String}
```
public void setNameBi(String value)
```


Sets the name of the font in a right-to-left language document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the font in a right-to-left language document. |

### setNameFarEast(String value) {#setNameFarEast-java.lang.String}
```
public void setNameFarEast(String value)
```


Sets an East Asian font name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | An East Asian font name. |

### setNameOther(String value) {#setNameOther-java.lang.String}
```
public void setNameOther(String value)
```


Sets the font used for characters with character codes from 128 through 255.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The font used for characters with character codes from 128 through 255. |

### setNoProofing(boolean value) {#setNoProofing-boolean}
```
public void setNoProofing(boolean value)
```


True when the formatted characters are not to be spell checked.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setOn(boolean value) {#setOn-boolean}
```
public void setOn(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### setOpacity(double value) {#setOpacity-double}
```
public void setOpacity(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setOutline(boolean value) {#setOutline-boolean}
```
public void setOutline(boolean value)
```


True if the font is formatted as outline.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setPosition(double value) {#setPosition-double}
```
public void setPosition(double value)
```


Sets the position of text (in points) relative to the base line. A positive number raises the text, and a negative number lowers it.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The position of text (in points) relative to the base line. |

### setRotateWithObject(boolean value) {#setRotateWithObject-boolean}
```
public void setRotateWithObject(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### setScaling(int value) {#setScaling-int}
```
public void setScaling(int value)
```


Sets character width scaling in percent.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Character width scaling in percent. |

### setShadow(boolean value) {#setShadow-boolean}
```
public void setShadow(boolean value)
```


True if the font is formatted as shadowed.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setSize(double value) {#setSize-double}
```
public void setSize(double value)
```


Sets the font size in points.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The font size in points. |

### setSizeBi(double value) {#setSizeBi-double}
```
public void setSizeBi(double value)
```


Sets the font size in points used in a right-to-left document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The font size in points used in a right-to-left document. |

### setSmallCaps(boolean value) {#setSmallCaps-boolean}
```
public void setSmallCaps(boolean value)
```


True if the font is formatted as small capital letters.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setSnapToGrid(boolean value) {#setSnapToGrid-boolean}
```
public void setSnapToGrid(boolean value)
```


Specifies whether the current font should use the document grid characters per line settings when laying out.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setSpacing(double value) {#setSpacing-double}
```
public void setSpacing(double value)
```


Sets the spacing (in points) between characters .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The spacing (in points) between characters . |

### setStrikeThrough(boolean value) {#setStrikeThrough-boolean}
```
public void setStrikeThrough(boolean value)
```


True if the font is formatted as strikethrough text.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setStyle(Style value) {#setStyle-com.aspose.words.Style}
```
public void setStyle(Style value)
```


Sets the character style applied to this formatting.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style/) | The character style applied to this formatting. |

### setStyleIdentifier(int value) {#setStyleIdentifier-int}
```
public void setStyleIdentifier(int value)
```


Sets the locale independent style identifier of the character style applied to this formatting.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The locale independent style identifier of the character style applied to this formatting. The value must be one of [StyleIdentifier](../../com.aspose.words/styleidentifier/) constants. |

### setStyleName(String value) {#setStyleName-java.lang.String}
```
public void setStyleName(String value)
```


Sets the name of the character style applied to this formatting.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the character style applied to this formatting. |

### setSubscript(boolean value) {#setSubscript-boolean}
```
public void setSubscript(boolean value)
```


True if the font is formatted as subscript.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setSuperscript(boolean value) {#setSuperscript-boolean}
```
public void setSuperscript(boolean value)
```


True if the font is formatted as superscript.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setTextEffect(int value) {#setTextEffect-int}
```
public void setTextEffect(int value)
```


Sets the font animation effect.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The font animation effect. The value must be one of [TextEffect](../../com.aspose.words/texteffect/) constants. |

### setTextureAlignment(int value) {#setTextureAlignment-int}
```
public void setTextureAlignment(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setThemeColor(int value) {#setThemeColor-int}
```
public void setThemeColor(int value)
```


Sets the theme color in the applied color scheme that is associated with this [Font](../../com.aspose.words/font/) object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The theme color in the applied color scheme that is associated with this [Font](../../com.aspose.words/font/) object. The value must be one of [ThemeColor](../../com.aspose.words/themecolor/) constants. |

### setThemeFont(int value) {#setThemeFont-int}
```
public void setThemeFont(int value)
```


Sets the theme font in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The theme font in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object. The value must be one of [ThemeFont](../../com.aspose.words/themefont/) constants. |

### setThemeFontAscii(int value) {#setThemeFontAscii-int}
```
public void setThemeFontAscii(int value)
```


Sets the theme font used for Latin text (characters with character codes from 0 (zero) through 127) in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The theme font used for Latin text (characters with character codes from 0 (zero) through 127) in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object. The value must be one of [ThemeFont](../../com.aspose.words/themefont/) constants. |

### setThemeFontBi(int value) {#setThemeFontBi-int}
```
public void setThemeFontBi(int value)
```


Sets the theme font in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object in a right-to-left language document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The theme font in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object in a right-to-left language document. The value must be one of [ThemeFont](../../com.aspose.words/themefont/) constants. |

### setThemeFontFarEast(int value) {#setThemeFontFarEast-int}
```
public void setThemeFontFarEast(int value)
```


Sets the East Asian theme font in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The East Asian theme font in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object. The value must be one of [ThemeFont](../../com.aspose.words/themefont/) constants. |

### setThemeFontOther(int value) {#setThemeFontOther-int}
```
public void setThemeFontOther(int value)
```


Sets the theme font used for characters with character codes from 128 through 255 in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The theme font used for characters with character codes from 128 through 255 in the applied font scheme that is associated with this [Font](../../com.aspose.words/font/) object. The value must be one of [ThemeFont](../../com.aspose.words/themefont/) constants. |

### setTintAndShade(double value) {#setTintAndShade-double}
```
public void setTintAndShade(double value)
```


Sets a double value that lightens or darkens a color.

The allowed values are in range from -1 (darkest) to 1 (lightest) for this property. Zero (0) is neutral. Attempting to set this property to a value less than -1 or more than 1 results in a java.lang.IllegalArgumentException.

Setting this property for [Font](../../com.aspose.words/font/) object with non-theme colors results in a java.lang.IllegalStateException.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | A double value that lightens or darkens a color. |

### setUnderline(int value) {#setUnderline-int}
```
public void setUnderline(int value)
```


Sets the type of underline applied to the font.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The type of underline applied to the font. The value must be one of [Underline](../../com.aspose.words/underline/) constants. |

### setUnderlineColor(Color value) {#setUnderlineColor-java.awt.Color}
```
public void setUnderlineColor(Color value)
```


Sets the color of the underline applied to the font.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The color of the underline applied to the font. |

### solid() {#solid}
```
public void solid()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### twoColorGradient(int style, int variant) {#twoColorGradient-int-int}
```
public void twoColorGradient(int style, int variant)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| style | int |  |
| variant | int |  |

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

