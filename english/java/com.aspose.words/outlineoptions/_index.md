---
title: OutlineOptions
linktitle: OutlineOptions
second_title: Aspose.Words for Java API Reference
description: Allows to specify outline options in Java.
type: docs
weight: 438
url: /java/com.aspose.words/outlineoptions/
---

**Inheritance:**
java.lang.Object
```
public class OutlineOptions
```

Allows to specify outline options.

To learn more, visit the [ Save a Document ][Save a Document] documentation article.


[Save a Document]: https://docs.aspose.com/words/java/save-a-document/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getBookmarksOutlineLevels()](#getBookmarksOutlineLevels) | Allows to specify individual bookmarks outline level. |
| [getClass()](#getClass) |  |
| [getCreateMissingOutlineLevels()](#getCreateMissingOutlineLevels) | Gets or sets a value determining whether or not to create missing outline levels when the document is exported. |
| [getCreateOutlinesForHeadingsInTables()](#getCreateOutlinesForHeadingsInTables) | Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables. |
| [getDefaultBookmarksOutlineLevel()](#getDefaultBookmarksOutlineLevel) | Specifies the default level in the document outline at which to display Word bookmarks. |
| [getExpandedOutlineLevels()](#getExpandedOutlineLevels) | Specifies how many levels in the document outline to show expanded when the file is viewed. |
| [getHeadingsOutlineLevels()](#getHeadingsOutlineLevels) | Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the document outline. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setCreateMissingOutlineLevels(boolean value)](#setCreateMissingOutlineLevels-boolean) | Gets or sets a value determining whether or not to create missing outline levels when the document is exported. |
| [setCreateOutlinesForHeadingsInTables(boolean value)](#setCreateOutlinesForHeadingsInTables-boolean) | Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables. |
| [setDefaultBookmarksOutlineLevel(int value)](#setDefaultBookmarksOutlineLevel-int) | Specifies the default level in the document outline at which to display Word bookmarks. |
| [setExpandedOutlineLevels(int value)](#setExpandedOutlineLevels-int) | Specifies how many levels in the document outline to show expanded when the file is viewed. |
| [setHeadingsOutlineLevels(int value)](#setHeadingsOutlineLevels-int) | Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the document outline. |
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
### getBookmarksOutlineLevels() {#getBookmarksOutlineLevels}
```
public BookmarksOutlineLevelCollection getBookmarksOutlineLevels()
```


Allows to specify individual bookmarks outline level.

 **Remarks:** 

If bookmark level is not specified in this collection then [getDefaultBookmarksOutlineLevel()](../../com.aspose.words/outlineoptions/\#getDefaultBookmarksOutlineLevel) / [setDefaultBookmarksOutlineLevel(int)](../../com.aspose.words/outlineoptions/\#setDefaultBookmarksOutlineLevel-int) value is used.

 **Examples:** 

Shows how to set outline levels for bookmarks.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```

**Returns:**
[BookmarksOutlineLevelCollection](../../com.aspose.words/bookmarksoutlinelevelcollection/) - The corresponding [BookmarksOutlineLevelCollection](../../com.aspose.words/bookmarksoutlinelevelcollection/) value.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getCreateMissingOutlineLevels() {#getCreateMissingOutlineLevels}
```
public boolean getCreateMissingOutlineLevels()
```


Gets or sets a value determining whether or not to create missing outline levels when the document is exported.

Default value for this property is  false .

**Returns:**
boolean - The corresponding  boolean  value.
### getCreateOutlinesForHeadingsInTables() {#getCreateOutlinesForHeadingsInTables}
```
public boolean getCreateOutlinesForHeadingsInTables()
```


Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables.

 **Remarks:** 

Default value is  false .

**Returns:**
boolean - The corresponding  boolean  value.
### getDefaultBookmarksOutlineLevel() {#getDefaultBookmarksOutlineLevel}
```
public int getDefaultBookmarksOutlineLevel()
```


Specifies the default level in the document outline at which to display Word bookmarks.

 **Remarks:** 

Individual bookmarks level could be specified using [getBookmarksOutlineLevels()](../../com.aspose.words/outlineoptions/\#getBookmarksOutlineLevels) property.

Specify 0 and Word bookmarks will not be displayed in the document outline. Specify 1 and Word bookmarks will be displayed in the document outline at level 1; 2 for level 2 and so on.

Default is 0. Valid range is 0 to 9.

**Returns:**
int - The corresponding  int  value.
### getExpandedOutlineLevels() {#getExpandedOutlineLevels}
```
public int getExpandedOutlineLevels()
```


Specifies how many levels in the document outline to show expanded when the file is viewed.

 **Remarks:** 

Note that this options will not work when saving to XPS.

Specify 0 and the document outline will be collapsed; specify 1 and the first level items in the outline will be expanded and so on.

Default is 0. Valid range is 0 to 9.

**Returns:**
int - The corresponding  int  value.
### getHeadingsOutlineLevels() {#getHeadingsOutlineLevels}
```
public int getHeadingsOutlineLevels()
```


Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the document outline.

 **Remarks:** 

Specify 0 for no headings in the outline; specify 1 for one level of headings in the outline and so on.

Default is 0. Valid range is 0 to 9.

**Returns:**
int - The corresponding  int  value.
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




### setCreateMissingOutlineLevels(boolean value) {#setCreateMissingOutlineLevels-boolean}
```
public void setCreateMissingOutlineLevels(boolean value)
```


Gets or sets a value determining whether or not to create missing outline levels when the document is exported.

Default value for this property is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setCreateOutlinesForHeadingsInTables(boolean value) {#setCreateOutlinesForHeadingsInTables-boolean}
```
public void setCreateOutlinesForHeadingsInTables(boolean value)
```


Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables.

 **Remarks:** 

Default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setDefaultBookmarksOutlineLevel(int value) {#setDefaultBookmarksOutlineLevel-int}
```
public void setDefaultBookmarksOutlineLevel(int value)
```


Specifies the default level in the document outline at which to display Word bookmarks.

 **Remarks:** 

Individual bookmarks level could be specified using [getBookmarksOutlineLevels()](../../com.aspose.words/outlineoptions/\#getBookmarksOutlineLevels) property.

Specify 0 and Word bookmarks will not be displayed in the document outline. Specify 1 and Word bookmarks will be displayed in the document outline at level 1; 2 for level 2 and so on.

Default is 0. Valid range is 0 to 9.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setExpandedOutlineLevels(int value) {#setExpandedOutlineLevels-int}
```
public void setExpandedOutlineLevels(int value)
```


Specifies how many levels in the document outline to show expanded when the file is viewed.

 **Remarks:** 

Note that this options will not work when saving to XPS.

Specify 0 and the document outline will be collapsed; specify 1 and the first level items in the outline will be expanded and so on.

Default is 0. Valid range is 0 to 9.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setHeadingsOutlineLevels(int value) {#setHeadingsOutlineLevels-int}
```
public void setHeadingsOutlineLevels(int value)
```


Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the document outline.

 **Remarks:** 

Specify 0 for no headings in the outline; specify 1 for one level of headings in the outline and so on.

Default is 0. Valid range is 0 to 9.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

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

