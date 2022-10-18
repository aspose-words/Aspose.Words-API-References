---
title: FontSourceBase
second_title: Aspose.Words for Java API Reference
description: This is an abstract base class for the classes that allow the user to specify various font sources.
type: docs
weight: 287
url: /java/com.aspose.words/fontsourcebase/
---

**Inheritance:**
java.lang.Object
```
public abstract class FontSourceBase
```

This is an abstract base class for the classes that allow the user to specify various font sources.

To learn more, visit the **Working with Fonts** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getType()](#getType--) | Returns the type of the font source. |
| [getPriority()](#getPriority--) | Returns the font source priority. |
| [getAvailableFonts()](#getAvailableFonts--) | Returns list of fonts available via this source. |
| [getWarningCallback()](#getWarningCallback--) | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback-) | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |
| [getPriorityInternal()](#getPriorityInternal--) |  |
| [getFontDataInternal()](#getFontDataInternal--) |  |
### getType() {#getType--}
```
public abstract int getType()
```


Returns the type of the font source.

**Returns:**
int - The type of the font source. The returned value is one of [FontSourceType](../../com.aspose.words/fontsourcetype) constants.
### getPriority() {#getPriority--}
```
public int getPriority()
```


Returns the font source priority.

This value is used when there are fonts with the same family name and style in different font sources. In this case Aspose.Words selects the font from the source with the higher priority value.

The default value is 0.

**Returns:**
int - The font source priority.
### getAvailableFonts() {#getAvailableFonts--}
```
public ArrayList getAvailableFonts()
```


Returns list of fonts available via this source.

**Returns:**
java.util.ArrayList
### getWarningCallback() {#getWarningCallback--}
```
public IWarningCallback getWarningCallback()
```


Called during processing of font source when an issue is detected that might result in formatting fidelity loss.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback) value.
### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback-}
```
public void setWarningCallback(IWarningCallback value)
```


Called during processing of font source when an issue is detected that might result in formatting fidelity loss.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback) | The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback) value. |

### getPriorityInternal() {#getPriorityInternal--}
```
public int getPriorityInternal()
```




**Returns:**
int
### getFontDataInternal() {#getFontDataInternal--}
```
public Iterable getFontDataInternal()
```




**Returns:**
java.lang.Iterable
