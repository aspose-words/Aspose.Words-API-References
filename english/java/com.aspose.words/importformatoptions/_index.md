---
title: ImportFormatOptions
second_title: Aspose.Words for Java API Reference
description: Allows to specify various import options to format output.
type: docs
weight: 349
url: /java/com.aspose.words/importformatoptions/
---

**Inheritance:**
java.lang.Object
```
public class ImportFormatOptions
```

Allows to specify various import options to format output.

To learn more, visit the [ Specify Load Options ][Specify Load Options] documentation article.


[Specify Load Options]: https://docs.aspose.com/words/java/specify-load-options/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getForceCopyStyles()](#getForceCopyStyles) | Gets a boolean value indicating either to copy conflicting styles in [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode. |
| [getIgnoreHeaderFooter()](#getIgnoreHeaderFooter) | Gets a boolean value that specifies that source formatting of headers/footers content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode is used. |
| [getIgnoreTextBoxes()](#getIgnoreTextBoxes) | Gets a boolean value that specifies that source formatting of textboxes content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode is used. |
| [getKeepSourceNumbering()](#getKeepSourceNumbering) | Gets a boolean value that specifies how the numbering will be imported when it clashes in source and destination documents. |
| [getMergePastedLists()](#getMergePastedLists) | Gets a boolean value that specifies whether pasted lists will be merged with surrounding lists. |
| [getSmartStyleBehavior()](#getSmartStyleBehavior) | Gets a boolean value that specifies how styles will be imported when they have equal names in source and destination documents. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setForceCopyStyles(boolean value)](#setForceCopyStyles-boolean) | Sets a boolean value indicating either to copy conflicting styles in [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode. |
| [setIgnoreHeaderFooter(boolean value)](#setIgnoreHeaderFooter-boolean) | Sets a boolean value that specifies that source formatting of headers/footers content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode is used. |
| [setIgnoreTextBoxes(boolean value)](#setIgnoreTextBoxes-boolean) | Sets a boolean value that specifies that source formatting of textboxes content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode is used. |
| [setKeepSourceNumbering(boolean value)](#setKeepSourceNumbering-boolean) | Sets a boolean value that specifies how the numbering will be imported when it clashes in source and destination documents. |
| [setMergePastedLists(boolean value)](#setMergePastedLists-boolean) | Sets a boolean value that specifies whether pasted lists will be merged with surrounding lists. |
| [setSmartStyleBehavior(boolean value)](#setSmartStyleBehavior-boolean) | Sets a boolean value that specifies how styles will be imported when they have equal names in source and destination documents. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
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
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getForceCopyStyles() {#getForceCopyStyles}
```
public boolean getForceCopyStyles()
```


Gets a boolean value indicating either to copy conflicting styles in [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode. The default value is  false .

By default, if a matching style already exists in a destination document, the source style formatting is expanded into direct node attributes and the style of this node is reset to a default.

When this option is set to  true , the source style will be forcibly copied into destination document with unique name and applied to the imported node.

Note, in this case it is not guaranteed that formatting of the imported node in destination document will be preserved.

**Returns:**
boolean - A boolean value indicating either to copy conflicting styles in [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode.
### getIgnoreHeaderFooter() {#getIgnoreHeaderFooter}
```
public boolean getIgnoreHeaderFooter()
```


Gets a boolean value that specifies that source formatting of headers/footers content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode is used. The default value is  true .

**Returns:**
boolean - A boolean value that specifies that source formatting of headers/footers content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode is used.
### getIgnoreTextBoxes() {#getIgnoreTextBoxes}
```
public boolean getIgnoreTextBoxes()
```


Gets a boolean value that specifies that source formatting of textboxes content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode is used. The default value is  true .

**Returns:**
boolean - A boolean value that specifies that source formatting of textboxes content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode is used.
### getKeepSourceNumbering() {#getKeepSourceNumbering}
```
public boolean getKeepSourceNumbering()
```


Gets a boolean value that specifies how the numbering will be imported when it clashes in source and destination documents. The default value is  false .

**Returns:**
boolean - A boolean value that specifies how the numbering will be imported when it clashes in source and destination documents.
### getMergePastedLists() {#getMergePastedLists}
```
public boolean getMergePastedLists()
```


Gets a boolean value that specifies whether pasted lists will be merged with surrounding lists. The default value is  false .

**Returns:**
boolean - A boolean value that specifies whether pasted lists will be merged with surrounding lists.
### getSmartStyleBehavior() {#getSmartStyleBehavior}
```
public boolean getSmartStyleBehavior()
```


Gets a boolean value that specifies how styles will be imported when they have equal names in source and destination documents. The default value is  false .

When this option is **enabled**, the source style will be expanded into a direct attributes inside a destination document, if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) importing mode is used.

When this option is **disabled**, the source style will be expanded only if it is numbered. Existing destination attributes will not be overridden, including lists.

**Returns:**
boolean - A boolean value that specifies how styles will be imported when they have equal names in source and destination documents.
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




### setForceCopyStyles(boolean value) {#setForceCopyStyles-boolean}
```
public void setForceCopyStyles(boolean value)
```


Sets a boolean value indicating either to copy conflicting styles in [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode. The default value is  false .

By default, if a matching style already exists in a destination document, the source style formatting is expanded into direct node attributes and the style of this node is reset to a default.

When this option is set to  true , the source style will be forcibly copied into destination document with unique name and applied to the imported node.

Note, in this case it is not guaranteed that formatting of the imported node in destination document will be preserved.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value indicating either to copy conflicting styles in [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode. |

### setIgnoreHeaderFooter(boolean value) {#setIgnoreHeaderFooter-boolean}
```
public void setIgnoreHeaderFooter(boolean value)
```


Sets a boolean value that specifies that source formatting of headers/footers content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode is used. The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value that specifies that source formatting of headers/footers content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode is used. |

### setIgnoreTextBoxes(boolean value) {#setIgnoreTextBoxes-boolean}
```
public void setIgnoreTextBoxes(boolean value)
```


Sets a boolean value that specifies that source formatting of textboxes content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode is used. The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value that specifies that source formatting of textboxes content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode is used. |

### setKeepSourceNumbering(boolean value) {#setKeepSourceNumbering-boolean}
```
public void setKeepSourceNumbering(boolean value)
```


Sets a boolean value that specifies how the numbering will be imported when it clashes in source and destination documents. The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value that specifies how the numbering will be imported when it clashes in source and destination documents. |

### setMergePastedLists(boolean value) {#setMergePastedLists-boolean}
```
public void setMergePastedLists(boolean value)
```


Sets a boolean value that specifies whether pasted lists will be merged with surrounding lists. The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value that specifies whether pasted lists will be merged with surrounding lists. |

### setSmartStyleBehavior(boolean value) {#setSmartStyleBehavior-boolean}
```
public void setSmartStyleBehavior(boolean value)
```


Sets a boolean value that specifies how styles will be imported when they have equal names in source and destination documents. The default value is  false .

When this option is **enabled**, the source style will be expanded into a direct attributes inside a destination document, if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) importing mode is used.

When this option is **disabled**, the source style will be expanded only if it is numbered. Existing destination attributes will not be overridden, including lists.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value that specifies how styles will be imported when they have equal names in source and destination documents. |

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

