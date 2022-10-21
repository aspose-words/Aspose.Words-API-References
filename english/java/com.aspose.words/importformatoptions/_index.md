---
title: ImportFormatOptions
second_title: Aspose.Words for Java API Reference
description: Allows to specify various import options to format output.
type: docs
weight: 347
url: /java/com.aspose.words/importformatoptions/
---

**Inheritance:**
java.lang.Object
```
public class ImportFormatOptions
```

Allows to specify various import options to format output.

To learn more, visit the **Specify Load Options** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getSmartStyleBehavior()](#getSmartStyleBehavior--) | Gets a boolean value that specifies how styles will be imported when they have equal names in source and destination documents. |
| [setSmartStyleBehavior(boolean value)](#setSmartStyleBehavior-boolean-) | Sets a boolean value that specifies how styles will be imported when they have equal names in source and destination documents. |
| [getKeepSourceNumbering()](#getKeepSourceNumbering--) | Gets a boolean value that specifies how the numbering will be imported when it clashes in source and destination documents. |
| [setKeepSourceNumbering(boolean value)](#setKeepSourceNumbering-boolean-) | Sets a boolean value that specifies how the numbering will be imported when it clashes in source and destination documents. |
| [getIgnoreTextBoxes()](#getIgnoreTextBoxes--) | Gets a boolean value that specifies that source formatting of textboxes content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode is used. |
| [setIgnoreTextBoxes(boolean value)](#setIgnoreTextBoxes-boolean-) | Sets a boolean value that specifies that source formatting of textboxes content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode is used. |
| [getIgnoreHeaderFooter()](#getIgnoreHeaderFooter--) | Gets a boolean value that specifies that source formatting of headers/footers content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode is used. |
| [setIgnoreHeaderFooter(boolean value)](#setIgnoreHeaderFooter-boolean-) | Sets a boolean value that specifies that source formatting of headers/footers content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode is used. |
| [getMergePastedLists()](#getMergePastedLists--) | Gets a boolean value that specifies whether pasted lists will be merged with surrounding lists. |
| [setMergePastedLists(boolean value)](#setMergePastedLists-boolean-) | Sets a boolean value that specifies whether pasted lists will be merged with surrounding lists. |
| [getForceCopyStyles()](#getForceCopyStyles--) | Gets a boolean value indicating either to copy conflicting styles in [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode. |
| [setForceCopyStyles(boolean value)](#setForceCopyStyles-boolean-) | Sets a boolean value indicating either to copy conflicting styles in [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode. |
### getSmartStyleBehavior() {#getSmartStyleBehavior--}
```
public boolean getSmartStyleBehavior()
```


Gets a boolean value that specifies how styles will be imported when they have equal names in source and destination documents. The default value is  false .

When this option is **enabled**, the source style will be expanded into a direct attributes inside a destination document, if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) importing mode is used.

When this option is **disabled**, the source style will be expanded only if it is numbered. Existing destination attributes will not be overridden, including lists.

**Returns:**
boolean - A boolean value that specifies how styles will be imported when they have equal names in source and destination documents.
### setSmartStyleBehavior(boolean value) {#setSmartStyleBehavior-boolean-}
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

### getKeepSourceNumbering() {#getKeepSourceNumbering--}
```
public boolean getKeepSourceNumbering()
```


Gets a boolean value that specifies how the numbering will be imported when it clashes in source and destination documents. The default value is  false .

**Returns:**
boolean - A boolean value that specifies how the numbering will be imported when it clashes in source and destination documents.
### setKeepSourceNumbering(boolean value) {#setKeepSourceNumbering-boolean-}
```
public void setKeepSourceNumbering(boolean value)
```


Sets a boolean value that specifies how the numbering will be imported when it clashes in source and destination documents. The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value that specifies how the numbering will be imported when it clashes in source and destination documents. |

### getIgnoreTextBoxes() {#getIgnoreTextBoxes--}
```
public boolean getIgnoreTextBoxes()
```


Gets a boolean value that specifies that source formatting of textboxes content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode is used. The default value is  true .

**Returns:**
boolean - A boolean value that specifies that source formatting of textboxes content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode is used.
### setIgnoreTextBoxes(boolean value) {#setIgnoreTextBoxes-boolean-}
```
public void setIgnoreTextBoxes(boolean value)
```


Sets a boolean value that specifies that source formatting of textboxes content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode is used. The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value that specifies that source formatting of textboxes content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode is used. |

### getIgnoreHeaderFooter() {#getIgnoreHeaderFooter--}
```
public boolean getIgnoreHeaderFooter()
```


Gets a boolean value that specifies that source formatting of headers/footers content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode is used. The default value is  true .

**Returns:**
boolean - A boolean value that specifies that source formatting of headers/footers content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode is used.
### setIgnoreHeaderFooter(boolean value) {#setIgnoreHeaderFooter-boolean-}
```
public void setIgnoreHeaderFooter(boolean value)
```


Sets a boolean value that specifies that source formatting of headers/footers content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode is used. The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value that specifies that source formatting of headers/footers content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode is used. |

### getMergePastedLists() {#getMergePastedLists--}
```
public boolean getMergePastedLists()
```


Gets a boolean value that specifies whether pasted lists will be merged with surrounding lists. The default value is  false .

**Returns:**
boolean - A boolean value that specifies whether pasted lists will be merged with surrounding lists.
### setMergePastedLists(boolean value) {#setMergePastedLists-boolean-}
```
public void setMergePastedLists(boolean value)
```


Sets a boolean value that specifies whether pasted lists will be merged with surrounding lists. The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value that specifies whether pasted lists will be merged with surrounding lists. |

### getForceCopyStyles() {#getForceCopyStyles--}
```
public boolean getForceCopyStyles()
```


Gets a boolean value indicating either to copy conflicting styles in [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode. The default value is  false .

By default, if a matching style already exists in a destination document, the source style formatting is expanded into direct node attributes and the style of this node is reset to a default.

When this option is set to  true , the source style will be forcibly copied into destination document with unique name and applied to the imported node.

Note, in this case it is not guaranteed that formatting of the imported node in destination document will be preserved.

**Returns:**
boolean - A boolean value indicating either to copy conflicting styles in [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) mode.
### setForceCopyStyles(boolean value) {#setForceCopyStyles-boolean-}
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

