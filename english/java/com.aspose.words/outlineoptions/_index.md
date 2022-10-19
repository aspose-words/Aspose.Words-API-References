---
title: OutlineOptions
second_title: Aspose.Words for Java API Reference
description: Allows to specify outline options.
type: docs
weight: 431
url: /java/com.aspose.words/outlineoptions/
---

**Inheritance:**
java.lang.Object
```
public class OutlineOptions
```

Allows to specify outline options.

To learn more, visit the **Save a Document** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getCreateMissingOutlineLevels()](#getCreateMissingOutlineLevels--) | Gets or sets a value determining whether or not to create missing outline levels when the document is exported. |
| [setCreateMissingOutlineLevels(boolean value)](#setCreateMissingOutlineLevels-boolean-) | Gets or sets a value determining whether or not to create missing outline levels when the document is exported. |
| [getHeadingsOutlineLevels()](#getHeadingsOutlineLevels--) | Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the document outline. |
| [setHeadingsOutlineLevels(int value)](#setHeadingsOutlineLevels-int-) | Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the document outline. |
| [getExpandedOutlineLevels()](#getExpandedOutlineLevels--) | Specifies how many levels in the document outline to show expanded when the file is viewed. |
| [setExpandedOutlineLevels(int value)](#setExpandedOutlineLevels-int-) | Specifies how many levels in the document outline to show expanded when the file is viewed. |
| [getDefaultBookmarksOutlineLevel()](#getDefaultBookmarksOutlineLevel--) | Specifies the default level in the document outline at which to display Word bookmarks. |
| [setDefaultBookmarksOutlineLevel(int value)](#setDefaultBookmarksOutlineLevel-int-) | Specifies the default level in the document outline at which to display Word bookmarks. |
| [getBookmarksOutlineLevels()](#getBookmarksOutlineLevels--) | Allows to specify individual bookmarks outline level. |
| [getCreateOutlinesForHeadingsInTables()](#getCreateOutlinesForHeadingsInTables--) | Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables. |
| [setCreateOutlinesForHeadingsInTables(boolean value)](#setCreateOutlinesForHeadingsInTables-boolean-) | Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables. |
### getCreateMissingOutlineLevels() {#getCreateMissingOutlineLevels--}
```
public boolean getCreateMissingOutlineLevels()
```


Gets or sets a value determining whether or not to create missing outline levels when the document is exported.

Default value for this property is **false**.

**Returns:**
boolean - The corresponding  boolean  value.
### setCreateMissingOutlineLevels(boolean value) {#setCreateMissingOutlineLevels-boolean-}
```
public void setCreateMissingOutlineLevels(boolean value)
```


Gets or sets a value determining whether or not to create missing outline levels when the document is exported.

Default value for this property is **false**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getHeadingsOutlineLevels() {#getHeadingsOutlineLevels--}
```
public int getHeadingsOutlineLevels()
```


Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the document outline.

Specify 0 for no headings in the outline; specify 1 for one level of headings in the outline and so on.

Default is 0. Valid range is 0 to 9.

**Returns:**
int - The corresponding  int  value.
### setHeadingsOutlineLevels(int value) {#setHeadingsOutlineLevels-int-}
```
public void setHeadingsOutlineLevels(int value)
```


Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the document outline.

Specify 0 for no headings in the outline; specify 1 for one level of headings in the outline and so on.

Default is 0. Valid range is 0 to 9.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### getExpandedOutlineLevels() {#getExpandedOutlineLevels--}
```
public int getExpandedOutlineLevels()
```


Specifies how many levels in the document outline to show expanded when the file is viewed.

Note that this options will not work when saving to XPS.

Specify 0 and the document outline will be collapsed; specify 1 and the first level items in the outline will be expanded and so on.

Default is 0. Valid range is 0 to 9.

**Returns:**
int - The corresponding  int  value.
### setExpandedOutlineLevels(int value) {#setExpandedOutlineLevels-int-}
```
public void setExpandedOutlineLevels(int value)
```


Specifies how many levels in the document outline to show expanded when the file is viewed.

Note that this options will not work when saving to XPS.

Specify 0 and the document outline will be collapsed; specify 1 and the first level items in the outline will be expanded and so on.

Default is 0. Valid range is 0 to 9.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### getDefaultBookmarksOutlineLevel() {#getDefaultBookmarksOutlineLevel--}
```
public int getDefaultBookmarksOutlineLevel()
```


Specifies the default level in the document outline at which to display Word bookmarks.

Individual bookmarks level could be specified using [getBookmarksOutlineLevels()](../../com.aspose.words/outlineoptions\#getBookmarksOutlineLevels--) property.

Specify 0 and Word bookmarks will not be displayed in the document outline. Specify 1 and Word bookmarks will be displayed in the document outline at level 1; 2 for level 2 and so on.

Default is 0. Valid range is 0 to 9.

**Returns:**
int - The corresponding  int  value.
### setDefaultBookmarksOutlineLevel(int value) {#setDefaultBookmarksOutlineLevel-int-}
```
public void setDefaultBookmarksOutlineLevel(int value)
```


Specifies the default level in the document outline at which to display Word bookmarks.

Individual bookmarks level could be specified using [getBookmarksOutlineLevels()](../../com.aspose.words/outlineoptions\#getBookmarksOutlineLevels--) property.

Specify 0 and Word bookmarks will not be displayed in the document outline. Specify 1 and Word bookmarks will be displayed in the document outline at level 1; 2 for level 2 and so on.

Default is 0. Valid range is 0 to 9.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### getBookmarksOutlineLevels() {#getBookmarksOutlineLevels--}
```
public BookmarksOutlineLevelCollection getBookmarksOutlineLevels()
```


Allows to specify individual bookmarks outline level.

If bookmark level is not specified in this collection then [getDefaultBookmarksOutlineLevel()](../../com.aspose.words/outlineoptions\#getDefaultBookmarksOutlineLevel--) / [setDefaultBookmarksOutlineLevel(int)](../../com.aspose.words/outlineoptions\#setDefaultBookmarksOutlineLevel-int-) value is used.

**Returns:**
[BookmarksOutlineLevelCollection](../../com.aspose.words/bookmarksoutlinelevelcollection) - The corresponding [BookmarksOutlineLevelCollection](../../com.aspose.words/bookmarksoutlinelevelcollection) value.
### getCreateOutlinesForHeadingsInTables() {#getCreateOutlinesForHeadingsInTables--}
```
public boolean getCreateOutlinesForHeadingsInTables()
```


Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables.

Default value is **false**.

**Returns:**
boolean - The corresponding  boolean  value.
### setCreateOutlinesForHeadingsInTables(boolean value) {#setCreateOutlinesForHeadingsInTables-boolean-}
```
public void setCreateOutlinesForHeadingsInTables(boolean value)
```


Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables.

Default value is **false**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

