---
title: FieldToc
second_title: Aspose.Words for Java API Reference
description: Implements the TOC field.
type: docs
weight: 255
url: /java/com.aspose.words/fieldtoc/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldToc extends Field
```

Implements the TOC field.

To learn more, visit the **Working with Fields** documentation article.

Builds a table of contents (which can also be a table of figures) using the entries specified by TC fields, their heading levels, and specified styles, and inserts that table at this place in the document.
## Methods

| Method | Description |
| --- | --- |
| [updatePageNumbers()](#updatePageNumbers--) | Updates the page numbers for items in this table of contents. |
| [getLevelForCustomStyle(Paragraph paragraph, Style style)](#getLevelForCustomStyle-com.aspose.words.Paragraph-com.aspose.words.Style-) |  |
| [getSkipTables()](#getSkipTables--) |  |
| [getIncludeRefDocFields()](#getIncludeRefDocFields--) |  |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getIncludeTocEntryFields()](#getIncludeTocEntryFields--) |  |
| [getEntryTypeCore()](#getEntryTypeCore--) |  |
| [isHeadingLevelRangeSpecified()](#isHeadingLevelRangeSpecified--) |  |
| [isEntryLevelRangeSpecified()](#isEntryLevelRangeSpecified--) |  |
| [getAreCustomStylesSpecified()](#getAreCustomStylesSpecified--) |  |
| [isTableOfFigures()](#isTableOfFigures--) |  |
| [getBookmarkName()](#getBookmarkName--) | Gets the name of the bookmark that marks the portion of the document used to build the table. |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String-) | Sets the name of the bookmark that marks the portion of the document used to build the table. |
| [getTableOfFiguresLabel()](#getTableOfFiguresLabel--) | Gets the name of the sequence identifier used when building a table of figures. |
| [setTableOfFiguresLabel(String value)](#setTableOfFiguresLabel-java.lang.String-) | Sets the name of the sequence identifier used when building a table of figures. |
| [getCaptionlessTableOfFiguresLabel()](#getCaptionlessTableOfFiguresLabel--) | Gets the name of the sequence identifier used when building a table of figures that does not include caption's label and number. |
| [setCaptionlessTableOfFiguresLabel(String value)](#setCaptionlessTableOfFiguresLabel-java.lang.String-) | Sets the name of the sequence identifier used when building a table of figures that does not include caption's label and number. |
| [isBookmarkRangeSpecified()](#isBookmarkRangeSpecified--) |  |
| [getRangeBookmark()](#getRangeBookmark--) |  |
| [getSequenceSeparator()](#getSequenceSeparator--) | Gets the character sequence that is used to separate sequence numbers and page numbers. |
| [setSequenceSeparator(String value)](#setSequenceSeparator-java.lang.String-) | Sets the character sequence that is used to separate sequence numbers and page numbers. |
| [getEntryIdentifier()](#getEntryIdentifier--) | Gets a string that should match type identifiers of TC fields being included. |
| [setEntryIdentifier(String value)](#setEntryIdentifier-java.lang.String-) | Sets a string that should match type identifiers of TC fields being included. |
| [getInsertHyperlinks()](#getInsertHyperlinks--) | Gets whether to make the table of contents entries hyperlinks. |
| [setInsertHyperlinks(boolean value)](#setInsertHyperlinks-boolean-) | Sets whether to make the table of contents entries hyperlinks. |
| [getEntryLevelRange()](#getEntryLevelRange--) | Gets a range of levels of the table of contents entries to be included. |
| [setEntryLevelRange(String value)](#setEntryLevelRange-java.lang.String-) | Sets a range of levels of the table of contents entries to be included. |
| [getPageNumberOmittingLevelRange()](#getPageNumberOmittingLevelRange--) | Gets a range of levels of the table of contents entries from which to omits page numbers. |
| [setPageNumberOmittingLevelRange(String value)](#setPageNumberOmittingLevelRange-java.lang.String-) | Sets a range of levels of the table of contents entries from which to omits page numbers. |
| [getHeadingLevelRange()](#getHeadingLevelRange--) | Gets a range of heading levels to include. |
| [setHeadingLevelRange(String value)](#setHeadingLevelRange-java.lang.String-) | Sets a range of heading levels to include. |
| [getEntrySeparator()](#getEntrySeparator--) | Gets a sequence of characters that separate an entry and its page number. |
| [setEntrySeparator(String value)](#setEntrySeparator-java.lang.String-) | Sets a sequence of characters that separate an entry and its page number. |
| [getPrefixedSequenceIdentifier()](#getPrefixedSequenceIdentifier--) | Gets the identifier of a sequence for which a prefix should be added to the entry's page number. |
| [setPrefixedSequenceIdentifier(String value)](#setPrefixedSequenceIdentifier-java.lang.String-) | Sets the identifier of a sequence for which a prefix should be added to the entry's page number. |
| [getCustomStyles()](#getCustomStyles--) | Gets a list of styles other than the built-in heading styles to include in the table of contents. |
| [setCustomStyles(String value)](#setCustomStyles-java.lang.String-) | Sets a list of styles other than the built-in heading styles to include in the table of contents. |
| [getUseParagraphOutlineLevel()](#getUseParagraphOutlineLevel--) | Gets whether to use the applied paragraph outline level. |
| [setUseParagraphOutlineLevel(boolean value)](#setUseParagraphOutlineLevel-boolean-) | Sets whether to use the applied paragraph outline level. |
| [getPreserveTabs()](#getPreserveTabs--) | Gets whether to preserve tab entries within table entries. |
| [setPreserveTabs(boolean value)](#setPreserveTabs-boolean-) | Sets whether to preserve tab entries within table entries. |
| [getPreserveLineBreaks()](#getPreserveLineBreaks--) | Gets whether to preserve newline characters within table entries. |
| [setPreserveLineBreaks(boolean value)](#setPreserveLineBreaks-boolean-) | Sets whether to preserve newline characters within table entries. |
| [getHideInWebLayout()](#getHideInWebLayout--) | Gets whether to hide tab leader and page numbers in Web layout view. |
| [setHideInWebLayout(boolean value)](#setHideInWebLayout-boolean-) | Sets whether to hide tab leader and page numbers in Web layout view. |
### updatePageNumbers() {#updatePageNumbers--}
```
public boolean updatePageNumbers()
```


Updates the page numbers for items in this table of contents.

**Returns:**
boolean - True if the operation is successful. If any of the related TOC bookmarks was removed, false will be returned.
### getLevelForCustomStyle(Paragraph paragraph, Style style) {#getLevelForCustomStyle-com.aspose.words.Paragraph-com.aspose.words.Style-}
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
### getSkipTables() {#getSkipTables--}
```
public boolean getSkipTables()
```




**Returns:**
boolean
### getIncludeRefDocFields() {#getIncludeRefDocFields--}
```
public boolean getIncludeRefDocFields()
```




**Returns:**
boolean
### getSwitchType(String switchName) {#getSwitchType-java.lang.String-}
```
public int getSwitchType(String switchName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| switchName | java.lang.String |  |

**Returns:**
int
### getIncludeTocEntryFields() {#getIncludeTocEntryFields--}
```
public boolean getIncludeTocEntryFields()
```




**Returns:**
boolean
### getEntryTypeCore() {#getEntryTypeCore--}
```
public int getEntryTypeCore()
```




**Returns:**
int
### isHeadingLevelRangeSpecified() {#isHeadingLevelRangeSpecified--}
```
public boolean isHeadingLevelRangeSpecified()
```




**Returns:**
boolean
### isEntryLevelRangeSpecified() {#isEntryLevelRangeSpecified--}
```
public boolean isEntryLevelRangeSpecified()
```




**Returns:**
boolean
### getAreCustomStylesSpecified() {#getAreCustomStylesSpecified--}
```
public boolean getAreCustomStylesSpecified()
```




**Returns:**
boolean
### isTableOfFigures() {#isTableOfFigures--}
```
public boolean isTableOfFigures()
```




**Returns:**
boolean
### getBookmarkName() {#getBookmarkName--}
```
public String getBookmarkName()
```


Gets the name of the bookmark that marks the portion of the document used to build the table.

**Returns:**
java.lang.String - The name of the bookmark that marks the portion of the document used to build the table.
### setBookmarkName(String value) {#setBookmarkName-java.lang.String-}
```
public void setBookmarkName(String value)
```


Sets the name of the bookmark that marks the portion of the document used to build the table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the bookmark that marks the portion of the document used to build the table. |

### getTableOfFiguresLabel() {#getTableOfFiguresLabel--}
```
public String getTableOfFiguresLabel()
```


Gets the name of the sequence identifier used when building a table of figures.

**Returns:**
java.lang.String - The name of the sequence identifier used when building a table of figures.
### setTableOfFiguresLabel(String value) {#setTableOfFiguresLabel-java.lang.String-}
```
public void setTableOfFiguresLabel(String value)
```


Sets the name of the sequence identifier used when building a table of figures.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the sequence identifier used when building a table of figures. |

### getCaptionlessTableOfFiguresLabel() {#getCaptionlessTableOfFiguresLabel--}
```
public String getCaptionlessTableOfFiguresLabel()
```


Gets the name of the sequence identifier used when building a table of figures that does not include caption's label and number.

**Returns:**
java.lang.String - The name of the sequence identifier used when building a table of figures that does not include caption's label and number.
### setCaptionlessTableOfFiguresLabel(String value) {#setCaptionlessTableOfFiguresLabel-java.lang.String-}
```
public void setCaptionlessTableOfFiguresLabel(String value)
```


Sets the name of the sequence identifier used when building a table of figures that does not include caption's label and number.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the sequence identifier used when building a table of figures that does not include caption's label and number. |

### isBookmarkRangeSpecified() {#isBookmarkRangeSpecified--}
```
public boolean isBookmarkRangeSpecified()
```




**Returns:**
boolean
### getRangeBookmark() {#getRangeBookmark--}
```
public Bookmark getRangeBookmark()
```




**Returns:**
[Bookmark](../../com.aspose.words/bookmark)
### getSequenceSeparator() {#getSequenceSeparator--}
```
public String getSequenceSeparator()
```


Gets the character sequence that is used to separate sequence numbers and page numbers.

**Returns:**
java.lang.String - The character sequence that is used to separate sequence numbers and page numbers.
### setSequenceSeparator(String value) {#setSequenceSeparator-java.lang.String-}
```
public void setSequenceSeparator(String value)
```


Sets the character sequence that is used to separate sequence numbers and page numbers.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The character sequence that is used to separate sequence numbers and page numbers. |

### getEntryIdentifier() {#getEntryIdentifier--}
```
public String getEntryIdentifier()
```


Gets a string that should match type identifiers of TC fields being included.

**Returns:**
java.lang.String - A string that should match type identifiers of TC fields being included.
### setEntryIdentifier(String value) {#setEntryIdentifier-java.lang.String-}
```
public void setEntryIdentifier(String value)
```


Sets a string that should match type identifiers of TC fields being included.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A string that should match type identifiers of TC fields being included. |

### getInsertHyperlinks() {#getInsertHyperlinks--}
```
public boolean getInsertHyperlinks()
```


Gets whether to make the table of contents entries hyperlinks.

**Returns:**
boolean - Whether to make the table of contents entries hyperlinks.
### setInsertHyperlinks(boolean value) {#setInsertHyperlinks-boolean-}
```
public void setInsertHyperlinks(boolean value)
```


Sets whether to make the table of contents entries hyperlinks.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to make the table of contents entries hyperlinks. |

### getEntryLevelRange() {#getEntryLevelRange--}
```
public String getEntryLevelRange()
```


Gets a range of levels of the table of contents entries to be included.

**Returns:**
java.lang.String - A range of levels of the table of contents entries to be included.
### setEntryLevelRange(String value) {#setEntryLevelRange-java.lang.String-}
```
public void setEntryLevelRange(String value)
```


Sets a range of levels of the table of contents entries to be included.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A range of levels of the table of contents entries to be included. |

### getPageNumberOmittingLevelRange() {#getPageNumberOmittingLevelRange--}
```
public String getPageNumberOmittingLevelRange()
```


Gets a range of levels of the table of contents entries from which to omits page numbers.

**Returns:**
java.lang.String - A range of levels of the table of contents entries from which to omits page numbers.
### setPageNumberOmittingLevelRange(String value) {#setPageNumberOmittingLevelRange-java.lang.String-}
```
public void setPageNumberOmittingLevelRange(String value)
```


Sets a range of levels of the table of contents entries from which to omits page numbers.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A range of levels of the table of contents entries from which to omits page numbers. |

### getHeadingLevelRange() {#getHeadingLevelRange--}
```
public String getHeadingLevelRange()
```


Gets a range of heading levels to include.

**Returns:**
java.lang.String - A range of heading levels to include.
### setHeadingLevelRange(String value) {#setHeadingLevelRange-java.lang.String-}
```
public void setHeadingLevelRange(String value)
```


Sets a range of heading levels to include.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A range of heading levels to include. |

### getEntrySeparator() {#getEntrySeparator--}
```
public String getEntrySeparator()
```


Gets a sequence of characters that separate an entry and its page number.

**Returns:**
java.lang.String - A sequence of characters that separate an entry and its page number.
### setEntrySeparator(String value) {#setEntrySeparator-java.lang.String-}
```
public void setEntrySeparator(String value)
```


Sets a sequence of characters that separate an entry and its page number.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A sequence of characters that separate an entry and its page number. |

### getPrefixedSequenceIdentifier() {#getPrefixedSequenceIdentifier--}
```
public String getPrefixedSequenceIdentifier()
```


Gets the identifier of a sequence for which a prefix should be added to the entry's page number.

**Returns:**
java.lang.String - The identifier of a sequence for which a prefix should be added to the entry's page number.
### setPrefixedSequenceIdentifier(String value) {#setPrefixedSequenceIdentifier-java.lang.String-}
```
public void setPrefixedSequenceIdentifier(String value)
```


Sets the identifier of a sequence for which a prefix should be added to the entry's page number.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The identifier of a sequence for which a prefix should be added to the entry's page number. |

### getCustomStyles() {#getCustomStyles--}
```
public String getCustomStyles()
```


Gets a list of styles other than the built-in heading styles to include in the table of contents.

**Returns:**
java.lang.String - A list of styles other than the built-in heading styles to include in the table of contents.
### setCustomStyles(String value) {#setCustomStyles-java.lang.String-}
```
public void setCustomStyles(String value)
```


Sets a list of styles other than the built-in heading styles to include in the table of contents.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A list of styles other than the built-in heading styles to include in the table of contents. |

### getUseParagraphOutlineLevel() {#getUseParagraphOutlineLevel--}
```
public boolean getUseParagraphOutlineLevel()
```


Gets whether to use the applied paragraph outline level.

**Returns:**
boolean - Whether to use the applied paragraph outline level.
### setUseParagraphOutlineLevel(boolean value) {#setUseParagraphOutlineLevel-boolean-}
```
public void setUseParagraphOutlineLevel(boolean value)
```


Sets whether to use the applied paragraph outline level.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to use the applied paragraph outline level. |

### getPreserveTabs() {#getPreserveTabs--}
```
public boolean getPreserveTabs()
```


Gets whether to preserve tab entries within table entries.

**Returns:**
boolean - Whether to preserve tab entries within table entries.
### setPreserveTabs(boolean value) {#setPreserveTabs-boolean-}
```
public void setPreserveTabs(boolean value)
```


Sets whether to preserve tab entries within table entries.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to preserve tab entries within table entries. |

### getPreserveLineBreaks() {#getPreserveLineBreaks--}
```
public boolean getPreserveLineBreaks()
```


Gets whether to preserve newline characters within table entries.

**Returns:**
boolean - Whether to preserve newline characters within table entries.
### setPreserveLineBreaks(boolean value) {#setPreserveLineBreaks-boolean-}
```
public void setPreserveLineBreaks(boolean value)
```


Sets whether to preserve newline characters within table entries.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to preserve newline characters within table entries. |

### getHideInWebLayout() {#getHideInWebLayout--}
```
public boolean getHideInWebLayout()
```


Gets whether to hide tab leader and page numbers in Web layout view.

**Returns:**
boolean - Whether to hide tab leader and page numbers in Web layout view.
### setHideInWebLayout(boolean value) {#setHideInWebLayout-boolean-}
```
public void setHideInWebLayout(boolean value)
```


Sets whether to hide tab leader and page numbers in Web layout view.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to hide tab leader and page numbers in Web layout view. |

