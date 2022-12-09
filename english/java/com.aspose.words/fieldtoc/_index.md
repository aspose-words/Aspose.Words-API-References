---
title: FieldToc
second_title: Aspose.Words for Java API Reference
description: Implements the TOC field.
type: docs
weight: 256
url: /java/com.aspose.words/fieldtoc/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldToc extends Field
```

Implements the TOC field.

To learn more, visit the [ Working with Fields ][Working with Fields] documentation article.

Builds a table of contents (which can also be a table of figures) using the entries specified by TC fields, their heading levels, and specified styles, and inserts that table at this place in the document.


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getAreCustomStylesSpecified()](#getAreCustomStylesSpecified) |  |
| [getBookmarkName()](#getBookmarkName) | Gets the name of the bookmark that marks the portion of the document used to build the table. |
| [getCaptionlessTableOfFiguresLabel()](#getCaptionlessTableOfFiguresLabel) | Gets the name of the sequence identifier used when building a table of figures that does not include caption's label and number. |
| [getClass()](#getClass) |  |
| [getCustomStyles()](#getCustomStyles) | Gets a list of styles other than the built-in heading styles to include in the table of contents. |
| [getDisplayResult()](#getDisplayResult) | Gets the text that represents the displayed field result. |
| [getEnd()](#getEnd) | Gets the node that represents the field end. |
| [getEntryIdentifier()](#getEntryIdentifier) | Gets a string that should match type identifiers of TC fields being included. |
| [getEntryLevelRange()](#getEntryLevelRange) | Gets a range of levels of the table of contents entries to be included. |
| [getEntrySeparator()](#getEntrySeparator) | Gets a sequence of characters that separate an entry and its page number. |
| [getEntryTypeCore()](#getEntryTypeCore) |  |
| [getFieldCode()](#getFieldCode) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFormat()](#getFormat) | Gets a [FieldFormat](../../com.aspose.words/fieldformat) object that provides typed access to field's formatting. |
| [getHeadingLevelRange()](#getHeadingLevelRange) | Gets a range of heading levels to include. |
| [getHideInWebLayout()](#getHideInWebLayout) | Gets whether to hide tab leader and page numbers in Web layout view. |
| [getIncludeRefDocFields()](#getIncludeRefDocFields) |  |
| [getIncludeTocEntryFields()](#getIncludeTocEntryFields) |  |
| [getInsertHyperlinks()](#getInsertHyperlinks) | Gets whether to make the table of contents entries hyperlinks. |
| [getLevelForCustomStyle(Paragraph paragraph, Style style)](#getLevelForCustomStyle-com.aspose.words.Paragraph-com.aspose.words.Style) |  |
| [getLocaleId()](#getLocaleId) | Gets the LCID of the field. |
| [getPageNumberOmittingLevelRange()](#getPageNumberOmittingLevelRange) | Gets a range of levels of the table of contents entries from which to omits page numbers. |
| [getPrefixedSequenceIdentifier()](#getPrefixedSequenceIdentifier) | Gets the identifier of a sequence for which a prefix should be added to the entry's page number. |
| [getPreserveLineBreaks()](#getPreserveLineBreaks) | Gets whether to preserve newline characters within table entries. |
| [getPreserveTabs()](#getPreserveTabs) | Gets whether to preserve tab entries within table entries. |
| [getRangeBookmark()](#getRangeBookmark) |  |
| [getResult()](#getResult) | Gets text that is between the field separator and field end. |
| [getSeparator()](#getSeparator) | Gets the node that represents the field separator. |
| [getSequenceSeparator()](#getSequenceSeparator) | Gets the character sequence that is used to separate sequence numbers and page numbers. |
| [getSkipTables()](#getSkipTables) |  |
| [getStart()](#getStart) | Gets the node that represents the start of the field. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String) |  |
| [getTableOfFiguresLabel()](#getTableOfFiguresLabel) | Gets the name of the sequence identifier used when building a table of figures. |
| [getType()](#getType) | Gets the Microsoft Word field type. |
| [getUseParagraphOutlineLevel()](#getUseParagraphOutlineLevel) | Gets whether to use the applied paragraph outline level. |
| [hashCode()](#hashCode) |  |
| [isBookmarkRangeSpecified()](#isBookmarkRangeSpecified) |  |
| [isDirty()](#isDirty) | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isDirty(boolean value)](#isDirty-boolean) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isEntryLevelRangeSpecified()](#isEntryLevelRangeSpecified) |  |
| [isHeadingLevelRangeSpecified()](#isHeadingLevelRangeSpecified) |  |
| [isLocked()](#isLocked) | Gets whether the field is locked (should not recalculate its result). |
| [isLocked(boolean value)](#isLocked-boolean) | Sets whether the field is locked (should not recalculate its result). |
| [isTableOfFigures()](#isTableOfFigures) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [remove()](#remove) | Removes the field from the document. |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String) | Sets the name of the bookmark that marks the portion of the document used to build the table. |
| [setCaptionlessTableOfFiguresLabel(String value)](#setCaptionlessTableOfFiguresLabel-java.lang.String) | Sets the name of the sequence identifier used when building a table of figures that does not include caption's label and number. |
| [setCustomStyles(String value)](#setCustomStyles-java.lang.String) | Sets a list of styles other than the built-in heading styles to include in the table of contents. |
| [setEntryIdentifier(String value)](#setEntryIdentifier-java.lang.String) | Sets a string that should match type identifiers of TC fields being included. |
| [setEntryLevelRange(String value)](#setEntryLevelRange-java.lang.String) | Sets a range of levels of the table of contents entries to be included. |
| [setEntrySeparator(String value)](#setEntrySeparator-java.lang.String) | Sets a sequence of characters that separate an entry and its page number. |
| [setHeadingLevelRange(String value)](#setHeadingLevelRange-java.lang.String) | Sets a range of heading levels to include. |
| [setHideInWebLayout(boolean value)](#setHideInWebLayout-boolean) | Sets whether to hide tab leader and page numbers in Web layout view. |
| [setInsertHyperlinks(boolean value)](#setInsertHyperlinks-boolean) | Sets whether to make the table of contents entries hyperlinks. |
| [setLocaleId(int value)](#setLocaleId-int) | Sets the LCID of the field. |
| [setPageNumberOmittingLevelRange(String value)](#setPageNumberOmittingLevelRange-java.lang.String) | Sets a range of levels of the table of contents entries from which to omits page numbers. |
| [setPrefixedSequenceIdentifier(String value)](#setPrefixedSequenceIdentifier-java.lang.String) | Sets the identifier of a sequence for which a prefix should be added to the entry's page number. |
| [setPreserveLineBreaks(boolean value)](#setPreserveLineBreaks-boolean) | Sets whether to preserve newline characters within table entries. |
| [setPreserveTabs(boolean value)](#setPreserveTabs-boolean) | Sets whether to preserve tab entries within table entries. |
| [setResult(String value)](#setResult-java.lang.String) | Sets text that is between the field separator and field end. |
| [setSequenceSeparator(String value)](#setSequenceSeparator-java.lang.String) | Sets the character sequence that is used to separate sequence numbers and page numbers. |
| [setTableOfFiguresLabel(String value)](#setTableOfFiguresLabel-java.lang.String) | Sets the name of the sequence identifier used when building a table of figures. |
| [setUseParagraphOutlineLevel(boolean value)](#setUseParagraphOutlineLevel-boolean) | Sets whether to use the applied paragraph outline level. |
| [toString()](#toString) |  |
| [unlink()](#unlink) | Performs the field unlink. |
| [update()](#update) | Performs the field update. |
| [update(boolean ignoreMergeFormat)](#update-boolean) | Performs a field update. |
| [updatePageNumbers()](#updatePageNumbers) | Updates the page numbers for items in this table of contents. |
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
### getAreCustomStylesSpecified() {#getAreCustomStylesSpecified}
```
public boolean getAreCustomStylesSpecified()
```




**Returns:**
boolean
### getBookmarkName() {#getBookmarkName}
```
public String getBookmarkName()
```


Gets the name of the bookmark that marks the portion of the document used to build the table.

**Returns:**
java.lang.String - The name of the bookmark that marks the portion of the document used to build the table.
### getCaptionlessTableOfFiguresLabel() {#getCaptionlessTableOfFiguresLabel}
```
public String getCaptionlessTableOfFiguresLabel()
```


Gets the name of the sequence identifier used when building a table of figures that does not include caption's label and number.

**Returns:**
java.lang.String - The name of the sequence identifier used when building a table of figures that does not include caption's label and number.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getCustomStyles() {#getCustomStyles}
```
public String getCustomStyles()
```


Gets a list of styles other than the built-in heading styles to include in the table of contents.

**Returns:**
java.lang.String - A list of styles other than the built-in heading styles to include in the table of contents.
### getDisplayResult() {#getDisplayResult}
```
public String getDisplayResult()
```


Gets the text that represents the displayed field result. The [Document.updateListLabels()](../../com.aspose.words/document\#updateListLabels) method must be called to obtain correct value for the [FieldListNum](../../com.aspose.words/fieldlistnum), [FieldAutoNum](../../com.aspose.words/fieldautonum), [FieldAutoNumOut](../../com.aspose.words/fieldautonumout) and [FieldAutoNumLgl](../../com.aspose.words/fieldautonumlgl) fields.

**Returns:**
java.lang.String - The text that represents the displayed field result.
### getEnd() {#getEnd}
```
public FieldEnd getEnd()
```


Gets the node that represents the field end.

**Returns:**
[FieldEnd](../../com.aspose.words/fieldend) - The node that represents the field end.
### getEntryIdentifier() {#getEntryIdentifier}
```
public String getEntryIdentifier()
```


Gets a string that should match type identifiers of TC fields being included.

**Returns:**
java.lang.String - A string that should match type identifiers of TC fields being included.
### getEntryLevelRange() {#getEntryLevelRange}
```
public String getEntryLevelRange()
```


Gets a range of levels of the table of contents entries to be included.

**Returns:**
java.lang.String - A range of levels of the table of contents entries to be included.
### getEntrySeparator() {#getEntrySeparator}
```
public String getEntrySeparator()
```


Gets a sequence of characters that separate an entry and its page number.

**Returns:**
java.lang.String - A sequence of characters that separate an entry and its page number.
### getEntryTypeCore() {#getEntryTypeCore}
```
public int getEntryTypeCore()
```




**Returns:**
int
### getFieldCode() {#getFieldCode}
```
public String getFieldCode()
```


Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.

**Returns:**
java.lang.String
### getFieldCode(boolean includeChildFieldCodes) {#getFieldCode-boolean}
```
public String getFieldCode(boolean includeChildFieldCodes)
```


Returns text between field start and field separator (or field end if there is no separator).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| includeChildFieldCodes | boolean | \{ true  if child field codes should be included. |

**Returns:**
java.lang.String
### getFormat() {#getFormat}
```
public FieldFormat getFormat()
```


Gets a [FieldFormat](../../com.aspose.words/fieldformat) object that provides typed access to field's formatting.

**Returns:**
[FieldFormat](../../com.aspose.words/fieldformat) - A [FieldFormat](../../com.aspose.words/fieldformat) object that provides typed access to field's formatting.
### getHeadingLevelRange() {#getHeadingLevelRange}
```
public String getHeadingLevelRange()
```


Gets a range of heading levels to include.

**Returns:**
java.lang.String - A range of heading levels to include.
### getHideInWebLayout() {#getHideInWebLayout}
```
public boolean getHideInWebLayout()
```


Gets whether to hide tab leader and page numbers in Web layout view.

**Returns:**
boolean - Whether to hide tab leader and page numbers in Web layout view.
### getIncludeRefDocFields() {#getIncludeRefDocFields}
```
public boolean getIncludeRefDocFields()
```




**Returns:**
boolean
### getIncludeTocEntryFields() {#getIncludeTocEntryFields}
```
public boolean getIncludeTocEntryFields()
```




**Returns:**
boolean
### getInsertHyperlinks() {#getInsertHyperlinks}
```
public boolean getInsertHyperlinks()
```


Gets whether to make the table of contents entries hyperlinks.

**Returns:**
boolean - Whether to make the table of contents entries hyperlinks.
### getLevelForCustomStyle(Paragraph paragraph, Style style) {#getLevelForCustomStyle-com.aspose.words.Paragraph-com.aspose.words.Style}
```
public int getLevelForCustomStyle(Paragraph paragraph, Style style)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| paragraph | [Paragraph](../../com.aspose.words/paragraph) |  |
| style | [Style](../../com.aspose.words/style) |  |

**Returns:**
int
### getLocaleId() {#getLocaleId}
```
public int getLocaleId()
```


Gets the LCID of the field.

**Returns:**
int - The LCID of the field.
### getPageNumberOmittingLevelRange() {#getPageNumberOmittingLevelRange}
```
public String getPageNumberOmittingLevelRange()
```


Gets a range of levels of the table of contents entries from which to omits page numbers.

**Returns:**
java.lang.String - A range of levels of the table of contents entries from which to omits page numbers.
### getPrefixedSequenceIdentifier() {#getPrefixedSequenceIdentifier}
```
public String getPrefixedSequenceIdentifier()
```


Gets the identifier of a sequence for which a prefix should be added to the entry's page number.

**Returns:**
java.lang.String - The identifier of a sequence for which a prefix should be added to the entry's page number.
### getPreserveLineBreaks() {#getPreserveLineBreaks}
```
public boolean getPreserveLineBreaks()
```


Gets whether to preserve newline characters within table entries.

**Returns:**
boolean - Whether to preserve newline characters within table entries.
### getPreserveTabs() {#getPreserveTabs}
```
public boolean getPreserveTabs()
```


Gets whether to preserve tab entries within table entries.

**Returns:**
boolean - Whether to preserve tab entries within table entries.
### getRangeBookmark() {#getRangeBookmark}
```
public Bookmark getRangeBookmark()
```




**Returns:**
[Bookmark](../../com.aspose.words/bookmark)
### getResult() {#getResult}
```
public String getResult()
```


Gets text that is between the field separator and field end.

**Returns:**
java.lang.String - Text that is between the field separator and field end.
### getSeparator() {#getSeparator}
```
public FieldSeparator getSeparator()
```


Gets the node that represents the field separator. Can be  null .

**Returns:**
[FieldSeparator](../../com.aspose.words/fieldseparator) - The node that represents the field separator.
### getSequenceSeparator() {#getSequenceSeparator}
```
public String getSequenceSeparator()
```


Gets the character sequence that is used to separate sequence numbers and page numbers.

**Returns:**
java.lang.String - The character sequence that is used to separate sequence numbers and page numbers.
### getSkipTables() {#getSkipTables}
```
public boolean getSkipTables()
```




**Returns:**
boolean
### getStart() {#getStart}
```
public FieldStart getStart()
```


Gets the node that represents the start of the field.

**Returns:**
[FieldStart](../../com.aspose.words/fieldstart) - The node that represents the start of the field.
### getSwitchType(String switchName) {#getSwitchType-java.lang.String}
```
public int getSwitchType(String switchName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| switchName | java.lang.String |  |

**Returns:**
int
### getTableOfFiguresLabel() {#getTableOfFiguresLabel}
```
public String getTableOfFiguresLabel()
```


Gets the name of the sequence identifier used when building a table of figures.

**Returns:**
java.lang.String - The name of the sequence identifier used when building a table of figures.
### getType() {#getType}
```
public int getType()
```


Gets the Microsoft Word field type.

**Returns:**
int - The Microsoft Word field type. The returned value is one of [FieldType](../../com.aspose.words/fieldtype) constants.
### getUseParagraphOutlineLevel() {#getUseParagraphOutlineLevel}
```
public boolean getUseParagraphOutlineLevel()
```


Gets whether to use the applied paragraph outline level.

**Returns:**
boolean - Whether to use the applied paragraph outline level.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### isBookmarkRangeSpecified() {#isBookmarkRangeSpecified}
```
public boolean isBookmarkRangeSpecified()
```




**Returns:**
boolean
### isDirty() {#isDirty}
```
public boolean isDirty()
```


Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.

**Returns:**
boolean - Whether the current result of the field is no longer correct (stale) due to other modifications made to the document.
### isDirty(boolean value) {#isDirty-boolean}
```
public void isDirty(boolean value)
```


Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |

### isEntryLevelRangeSpecified() {#isEntryLevelRangeSpecified}
```
public boolean isEntryLevelRangeSpecified()
```




**Returns:**
boolean
### isHeadingLevelRangeSpecified() {#isHeadingLevelRangeSpecified}
```
public boolean isHeadingLevelRangeSpecified()
```




**Returns:**
boolean
### isLocked() {#isLocked}
```
public boolean isLocked()
```


Gets whether the field is locked (should not recalculate its result).

**Returns:**
boolean - Whether the field is locked (should not recalculate its result).
### isLocked(boolean value) {#isLocked-boolean}
```
public void isLocked(boolean value)
```


Sets whether the field is locked (should not recalculate its result).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether the field is locked (should not recalculate its result). |

### isTableOfFigures() {#isTableOfFigures}
```
public boolean isTableOfFigures()
```




**Returns:**
boolean
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### remove() {#remove}
```
public Node remove()
```


Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns  null .

**Returns:**
[Node](../../com.aspose.words/node)
### setBookmarkName(String value) {#setBookmarkName-java.lang.String}
```
public void setBookmarkName(String value)
```


Sets the name of the bookmark that marks the portion of the document used to build the table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the bookmark that marks the portion of the document used to build the table. |

### setCaptionlessTableOfFiguresLabel(String value) {#setCaptionlessTableOfFiguresLabel-java.lang.String}
```
public void setCaptionlessTableOfFiguresLabel(String value)
```


Sets the name of the sequence identifier used when building a table of figures that does not include caption's label and number.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the sequence identifier used when building a table of figures that does not include caption's label and number. |

### setCustomStyles(String value) {#setCustomStyles-java.lang.String}
```
public void setCustomStyles(String value)
```


Sets a list of styles other than the built-in heading styles to include in the table of contents.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A list of styles other than the built-in heading styles to include in the table of contents. |

### setEntryIdentifier(String value) {#setEntryIdentifier-java.lang.String}
```
public void setEntryIdentifier(String value)
```


Sets a string that should match type identifiers of TC fields being included.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A string that should match type identifiers of TC fields being included. |

### setEntryLevelRange(String value) {#setEntryLevelRange-java.lang.String}
```
public void setEntryLevelRange(String value)
```


Sets a range of levels of the table of contents entries to be included.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A range of levels of the table of contents entries to be included. |

### setEntrySeparator(String value) {#setEntrySeparator-java.lang.String}
```
public void setEntrySeparator(String value)
```


Sets a sequence of characters that separate an entry and its page number.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A sequence of characters that separate an entry and its page number. |

### setHeadingLevelRange(String value) {#setHeadingLevelRange-java.lang.String}
```
public void setHeadingLevelRange(String value)
```


Sets a range of heading levels to include.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A range of heading levels to include. |

### setHideInWebLayout(boolean value) {#setHideInWebLayout-boolean}
```
public void setHideInWebLayout(boolean value)
```


Sets whether to hide tab leader and page numbers in Web layout view.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to hide tab leader and page numbers in Web layout view. |

### setInsertHyperlinks(boolean value) {#setInsertHyperlinks-boolean}
```
public void setInsertHyperlinks(boolean value)
```


Sets whether to make the table of contents entries hyperlinks.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to make the table of contents entries hyperlinks. |

### setLocaleId(int value) {#setLocaleId-int}
```
public void setLocaleId(int value)
```


Sets the LCID of the field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The LCID of the field. |

### setPageNumberOmittingLevelRange(String value) {#setPageNumberOmittingLevelRange-java.lang.String}
```
public void setPageNumberOmittingLevelRange(String value)
```


Sets a range of levels of the table of contents entries from which to omits page numbers.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A range of levels of the table of contents entries from which to omits page numbers. |

### setPrefixedSequenceIdentifier(String value) {#setPrefixedSequenceIdentifier-java.lang.String}
```
public void setPrefixedSequenceIdentifier(String value)
```


Sets the identifier of a sequence for which a prefix should be added to the entry's page number.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The identifier of a sequence for which a prefix should be added to the entry's page number. |

### setPreserveLineBreaks(boolean value) {#setPreserveLineBreaks-boolean}
```
public void setPreserveLineBreaks(boolean value)
```


Sets whether to preserve newline characters within table entries.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to preserve newline characters within table entries. |

### setPreserveTabs(boolean value) {#setPreserveTabs-boolean}
```
public void setPreserveTabs(boolean value)
```


Sets whether to preserve tab entries within table entries.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to preserve tab entries within table entries. |

### setResult(String value) {#setResult-java.lang.String}
```
public void setResult(String value)
```


Sets text that is between the field separator and field end.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Text that is between the field separator and field end. |

### setSequenceSeparator(String value) {#setSequenceSeparator-java.lang.String}
```
public void setSequenceSeparator(String value)
```


Sets the character sequence that is used to separate sequence numbers and page numbers.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The character sequence that is used to separate sequence numbers and page numbers. |

### setTableOfFiguresLabel(String value) {#setTableOfFiguresLabel-java.lang.String}
```
public void setTableOfFiguresLabel(String value)
```


Sets the name of the sequence identifier used when building a table of figures.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the sequence identifier used when building a table of figures. |

### setUseParagraphOutlineLevel(boolean value) {#setUseParagraphOutlineLevel-boolean}
```
public void setUseParagraphOutlineLevel(boolean value)
```


Sets whether to use the applied paragraph outline level.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to use the applied paragraph outline level. |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### unlink() {#unlink}
```
public boolean unlink()
```


Performs the field unlink.

Replaces the field with its most recent result.

Some fields, such as XE (Index Entry) fields and SEQ (Sequence) fields, cannot be unlinked.

**Returns:**
boolean - \{ true  if the field has been unlinked, otherwise  false .
### update() {#update}
```
public void update()
```


Performs the field update. Throws if the field is being updated already.

### update(boolean ignoreMergeFormat) {#update-boolean}
```
public void update(boolean ignoreMergeFormat)
```


Performs a field update. Throws if the field is being updated already.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ignoreMergeFormat | boolean | If  true  then direct field result formatting is abandoned, regardless of the MERGEFORMAT switch, otherwise normal update is performed. |

### updatePageNumbers() {#updatePageNumbers}
```
public boolean updatePageNumbers()
```


Updates the page numbers for items in this table of contents.

**Returns:**
boolean - \{ true  if the operation is successful. If any of the related TOC bookmarks was removed,  false  will be returned.
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

