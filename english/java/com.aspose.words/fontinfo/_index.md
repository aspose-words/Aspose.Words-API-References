---
title: FontInfo
second_title: Aspose.Words for Java API Reference
description: Specifies information about a font used in the document.
type: docs
weight: 280
url: /java/com.aspose.words/fontinfo/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class FontInfo implements Cloneable
```

Specifies information about a font used in the document.

To learn more, visit the **Working with Fonts** documentation article.

You do not create instances of this class directly. Use the [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase\#getFontInfos--) property to access the collection of fonts defined in a document.
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAltName()](#getAltName--) | Gets the alternate name for the font. |
| [getCharset()](#getCharset--) | Gets the character set for the font. |
| [getClass()](#getClass--) |  |
| [getEmbeddedFont(int format, int style)](#getEmbeddedFont-int-int-) |  |
| [getEmbeddedFontAsOpenType(int style)](#getEmbeddedFontAsOpenType-int-) |  |
| [getFamily()](#getFamily--) | Gets the font family this font belongs to. |
| [getName()](#getName--) | Gets the name of the font. |
| [getPanose()](#getPanose--) | Gets the PANOSE typeface classification number. |
| [getPitch()](#getPitch--) | The pitch indicates if the font is fixed pitch, proportionally spaced, or relies on a default setting. |
| [hashCode()](#hashCode--) |  |
| [isTrueType()](#isTrueType--) | Indicates that this font is a TrueType or OpenType font as opposed to a raster or vector font. |
| [isTrueType(boolean value)](#isTrueType-boolean-) | Indicates that this font is a TrueType or OpenType font as opposed to a raster or vector font. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAltName(String value)](#setAltName-java.lang.String-) | Sets the alternate name for the font. |
| [setCharset(int value)](#setCharset-int-) | Sets the character set for the font. |
| [setFamily(int value)](#setFamily-int-) | Sets the font family this font belongs to. |
| [setPanose(byte[] value)](#setPanose-byte---) | Sets the PANOSE typeface classification number. |
| [setPitch(int value)](#setPitch-int-) | The pitch indicates if the font is fixed pitch, proportionally spaced, or relies on a default setting. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getAltName() {#getAltName--}
```
public String getAltName()
```


Gets the alternate name for the font.

Cannot be  null . Can be an empty string.

**Returns:**
java.lang.String - The alternate name for the font.
### getCharset() {#getCharset--}
```
public int getCharset()
```


Gets the character set for the font.

**Returns:**
int - The character set for the font.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getEmbeddedFont(int format, int style) {#getEmbeddedFont-int-int-}
```
public byte[] getEmbeddedFont(int format, int style)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| format | int |  |
| style | int |  |

**Returns:**
byte[]
### getEmbeddedFontAsOpenType(int style) {#getEmbeddedFontAsOpenType-int-}
```
public byte[] getEmbeddedFontAsOpenType(int style)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| style | int |  |

**Returns:**
byte[]
### getFamily() {#getFamily--}
```
public int getFamily()
```


Gets the font family this font belongs to.

**Returns:**
int - The font family this font belongs to. The returned value is one of [FontFamily](../../com.aspose.words/fontfamily) constants.
### getName() {#getName--}
```
public String getName()
```


Gets the name of the font.

Cannot be  null . Can be an empty string.

**Returns:**
java.lang.String - The name of the font.
### getPanose() {#getPanose--}
```
public byte[] getPanose()
```


Gets the PANOSE typeface classification number.

PANOSE is a compact 10-byte description of a fonts critical visual characteristics, such as contrast, weight, and serif style. The digits represent Family Kind, Serif Style, Weight, Proportion, Contrast, Stroke Variation, Arm Style, Letterform, Midline, and X-Height.

Can be  null .

**Returns:**
byte[] - The PANOSE typeface classification number.
### getPitch() {#getPitch--}
```
public int getPitch()
```


The pitch indicates if the font is fixed pitch, proportionally spaced, or relies on a default setting.

**Returns:**
int - The corresponding  int  value. The returned value is one of [FontPitch](../../com.aspose.words/fontpitch) constants.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### isTrueType() {#isTrueType--}
```
public boolean isTrueType()
```


Indicates that this font is a TrueType or OpenType font as opposed to a raster or vector font. Default is true.

**Returns:**
boolean - The corresponding  boolean  value.
### isTrueType(boolean value) {#isTrueType-boolean-}
```
public void isTrueType(boolean value)
```


Indicates that this font is a TrueType or OpenType font as opposed to a raster or vector font. Default is true.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setAltName(String value) {#setAltName-java.lang.String-}
```
public void setAltName(String value)
```


Sets the alternate name for the font.

Cannot be  null . Can be an empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The alternate name for the font. |

### setCharset(int value) {#setCharset-int-}
```
public void setCharset(int value)
```


Sets the character set for the font.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The character set for the font. |

### setFamily(int value) {#setFamily-int-}
```
public void setFamily(int value)
```


Sets the font family this font belongs to.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The font family this font belongs to. The value must be one of [FontFamily](../../com.aspose.words/fontfamily) constants. |

### setPanose(byte[] value) {#setPanose-byte---}
```
public void setPanose(byte[] value)
```


Sets the PANOSE typeface classification number.

PANOSE is a compact 10-byte description of a fonts critical visual characteristics, such as contrast, weight, and serif style. The digits represent Family Kind, Serif Style, Weight, Proportion, Contrast, Stroke Variation, Arm Style, Letterform, Midline, and X-Height.

Can be  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | byte[] | The PANOSE typeface classification number. |

### setPitch(int value) {#setPitch-int-}
```
public void setPitch(int value)
```


The pitch indicates if the font is fixed pitch, proportionally spaced, or relies on a default setting.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [FontPitch](../../com.aspose.words/fontpitch) constants. |

### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

