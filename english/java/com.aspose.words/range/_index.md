---
title: Range
second_title: Aspose.Words for Java API Reference
description: Represents a contiguous area in a document.
type: docs
weight: 472
url: /java/com.aspose.words/range/
---

**Inheritance:**
java.lang.Object
```
public class Range
```

Represents a contiguous area in a document.

To learn more, visit the **Working with Ranges** documentation article.

The document is represented by a tree of nodes and the nodes provide operations to work with the tree, but some operations are easier to perform if the document is treated as a contiguous sequence of text.

**Range** is a "facade" interface that provide methods that treat the document or portions of the document as "flat" text regardless of the fact that the document nodes are stored in a tree-like object model.

**Range** does not contain any text or nodes, it is merely a view or "window" over a fragment of a document.
## Methods

| Method | Description |
| --- | --- |
| [delete()](#delete--) | Deletes all characters of the range. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBookmarks()](#getBookmarks--) | Returns a [getBookmarks()](../../com.aspose.words/range\#getBookmarks--) collection that represents all bookmarks in the range. |
| [getClass()](#getClass--) |  |
| [getFields()](#getFields--) | Returns a [getFields()](../../com.aspose.words/range\#getFields--) collection that represents all fields in the range. |
| [getFormFields()](#getFormFields--) | Returns a [getFormFields()](../../com.aspose.words/range\#getFormFields--) collection that represents all form fields in the range. |
| [getStructuredDocumentTags()](#getStructuredDocumentTags--) | Returns a [getStructuredDocumentTags()](../../com.aspose.words/range\#getStructuredDocumentTags--) collection that represents all structured document tags in the range. |
| [getText()](#getText--) | Gets the text of the range. |
| [hashCode()](#hashCode--) |  |
| [normalizeFieldTypes()](#normalizeFieldTypes--) | Changes field type values [FieldChar.getFieldType()](../../com.aspose.words/fieldchar\#getFieldType--) of [FieldStart](../../com.aspose.words/fieldstart), [FieldSeparator](../../com.aspose.words/fieldseparator), [FieldEnd](../../com.aspose.words/fieldend) in this range so that they correspond to the field types contained in the field codes. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [replace(String pattern, String replacement)](#replace-java.lang.String-java.lang.String-) | Replaces all occurrences of a specified character string pattern with a replacement string. |
| [replace(String pattern, String replacement, FindReplaceOptions options)](#replace-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions-) | Replaces all occurrences of a specified character string pattern with a replacement string. |
| [replace(Pattern pattern, String replacement)](#replace-java.util.regex.Pattern-java.lang.String-) | Replaces all occurrences of a character pattern specified by a regular expression with another string. |
| [replace(Pattern pattern, String replacement, FindReplaceOptions options)](#replace-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions-) | Replaces all occurrences of a character pattern specified by a regular expression with another string. |
| [toDocument()](#toDocument--) | Constructs a new fully formed document that contains the range. |
| [toString()](#toString--) |  |
| [unlinkFields()](#unlinkFields--) | Unlinks fields in this range. |
| [updateFields()](#updateFields--) | Updates the values of document fields in this range. |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### delete() {#delete--}
```
public void delete()
```


Deletes all characters of the range.

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
### getBookmarks() {#getBookmarks--}
```
public BookmarkCollection getBookmarks()
```


Returns a [getBookmarks()](../../com.aspose.words/range\#getBookmarks--) collection that represents all bookmarks in the range.

**Returns:**
[BookmarkCollection](../../com.aspose.words/bookmarkcollection) - A [getBookmarks()](../../com.aspose.words/range\#getBookmarks--) collection that represents all bookmarks in the range.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getFields() {#getFields--}
```
public FieldCollection getFields()
```


Returns a [getFields()](../../com.aspose.words/range\#getFields--) collection that represents all fields in the range.

**Returns:**
[FieldCollection](../../com.aspose.words/fieldcollection) - A [getFields()](../../com.aspose.words/range\#getFields--) collection that represents all fields in the range.
### getFormFields() {#getFormFields--}
```
public FormFieldCollection getFormFields()
```


Returns a [getFormFields()](../../com.aspose.words/range\#getFormFields--) collection that represents all form fields in the range.

**Returns:**
[FormFieldCollection](../../com.aspose.words/formfieldcollection) - A [getFormFields()](../../com.aspose.words/range\#getFormFields--) collection that represents all form fields in the range.
### getStructuredDocumentTags() {#getStructuredDocumentTags--}
```
public StructuredDocumentTagCollection getStructuredDocumentTags()
```


Returns a [getStructuredDocumentTags()](../../com.aspose.words/range\#getStructuredDocumentTags--) collection that represents all structured document tags in the range.

**Returns:**
[StructuredDocumentTagCollection](../../com.aspose.words/structureddocumenttagcollection) - A [getStructuredDocumentTags()](../../com.aspose.words/range\#getStructuredDocumentTags--) collection that represents all structured document tags in the range.
### getText() {#getText--}
```
public String getText()
```


Gets the text of the range.

The returned string includes all control and special characters as described in [ControlChar](../../com.aspose.words/controlchar).

**Returns:**
java.lang.String - The text of the range.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### normalizeFieldTypes() {#normalizeFieldTypes--}
```
public void normalizeFieldTypes()
```


Changes field type values [FieldChar.getFieldType()](../../com.aspose.words/fieldchar\#getFieldType--) of [FieldStart](../../com.aspose.words/fieldstart), [FieldSeparator](../../com.aspose.words/fieldseparator), [FieldEnd](../../com.aspose.words/fieldend) in this range so that they correspond to the field types contained in the field codes.

Use this method after document changes that affect field types.

To change field type values in the whole document use [Document.normalizeFieldTypes()](../../com.aspose.words/document\#normalizeFieldTypes--).

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### replace(String pattern, String replacement) {#replace-java.lang.String-java.lang.String-}
```
public int replace(String pattern, String replacement)
```


Replaces all occurrences of a specified character string pattern with a replacement string.

The pattern will not be used as regular expression. Please use [replace(java.util.regex.Pattern, java.lang.String)](../../com.aspose.words/range\#replace-java.util.regex.Pattern--java.lang.String-) if you need regular expressions.

Used case-insensitive comparison.

Method is able to process breaks in both pattern and replacement strings.

You should use special meta-characters if you need to work with breaks:

 *  **&p** \- paragraph break
 *  **&b** \- section break
 *  **&m** \- page break
 *  **&l** \- manual line break

Use method [replace(java.lang.String, java.lang.String, com.aspose.words.FindReplaceOptions)](../../com.aspose.words/range\#replace-java.lang.String--java.lang.String--com.aspose.words.FindReplaceOptions-) to have more flexible customization.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pattern | java.lang.String | A string to be replaced. |
| replacement | java.lang.String | A string to replace all occurrences of pattern. |

**Returns:**
int - The number of replacements made.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.Writeln("Numbers 1, 2, 3");

 // Inserts paragraph break after Numbers.
 doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
 
```
### replace(String pattern, String replacement, FindReplaceOptions options) {#replace-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions-}
```
public int replace(String pattern, String replacement, FindReplaceOptions options)
```


Replaces all occurrences of a specified character string pattern with a replacement string.

The pattern will not be used as regular expression. Please use [replace(java.util.regex.Pattern, java.lang.String, com.aspose.words.FindReplaceOptions)](../../com.aspose.words/range\#replace-java.util.regex.Pattern--java.lang.String--com.aspose.words.FindReplaceOptions-) if you need regular expressions.

Method is able to process breaks in both pattern and replacement strings.

You should use special meta-characters if you need to work with breaks:

 *  **&p** \- paragraph break
 *  **&b** \- section break
 *  **&m** \- page break
 *  **&l** \- manual line break
 *  **&&** \- & character

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pattern | java.lang.String | A string to be replaced. |
| replacement | java.lang.String | A string to replace all occurrences of pattern. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions) | \{[FindReplaceOptions](../../com.aspose.words/findreplaceoptions) object to specify additional options. |

**Returns:**
int - The number of replacements made.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.Writeln("Numbers 1, 2, 3");

 // Inserts paragraph break after Numbers.
 doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
 
```
### replace(Pattern pattern, String replacement) {#replace-java.util.regex.Pattern-java.lang.String-}
```
public int replace(Pattern pattern, String replacement)
```


Replaces all occurrences of a character pattern specified by a regular expression with another string.

Replaces the whole match captured by the regular expression.

Method is able to process breaks in both pattern and replacement strings.

You should use special meta-characters if you need to work with breaks:

 *  **&p** \- paragraph break
 *  **&b** \- section break
 *  **&m** \- page break
 *  **&l** \- manual line break

Use method [replace(java.util.regex.Pattern, java.lang.String, com.aspose.words.FindReplaceOptions)](../../com.aspose.words/range\#replace-java.util.regex.Pattern--java.lang.String--com.aspose.words.FindReplaceOptions-) to have more flexible customization.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pattern | java.util.regex.Pattern | A regular expression pattern used to find matches. |
| replacement | java.lang.String | A string to replace all occurrences of pattern. |

**Returns:**
int - The number of replacements made.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.Writeln("a1, b2, c3");

 // Replaces each number with paragraph break.
 doc.Range.Replace(new Regex(@"\d+"), "&p");
 
```
### replace(Pattern pattern, String replacement, FindReplaceOptions options) {#replace-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions-}
```
public int replace(Pattern pattern, String replacement, FindReplaceOptions options)
```


Replaces all occurrences of a character pattern specified by a regular expression with another string.

Replaces the whole match captured by the regular expression.

Method is able to process breaks in both pattern and replacement strings.

You should use special meta-characters if you need to work with breaks:

 *  **&p** \- paragraph break
 *  **&b** \- section break
 *  **&m** \- page break
 *  **&l** \- manual line break
 *  **&&** \- & character

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pattern | java.util.regex.Pattern | A regular expression pattern used to find matches. |
| replacement | java.lang.String | A string to replace all occurrences of pattern. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions) | \{[FindReplaceOptions](../../com.aspose.words/findreplaceoptions) object to specify additional options. |

**Returns:**
int - The number of replacements made.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.Writeln("a1, b2, c3");

 // Replaces each number with paragraph break.
 doc.Range.Replace(new Regex(@"\d+"), "&p", new FindReplaceOptions());
 
```
### toDocument() {#toDocument--}
```
public Document toDocument()
```


Constructs a new fully formed document that contains the range.

**Returns:**
[Document](../../com.aspose.words/document)
### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### unlinkFields() {#unlinkFields--}
```
public void unlinkFields()
```


Unlinks fields in this range.

Replaces all the fields in this range with their most recent results.

To unlink fields in the whole document use [unlinkFields()](../../com.aspose.words/range\#unlinkFields--).

### updateFields() {#updateFields--}
```
public void updateFields()
```


Updates the values of document fields in this range.

When you open, modify and then save a document, Aspose.Words does not update fields automatically, it keeps them intact. Therefore, you would usually want to call this method before saving if you have modified the document programmatically and want to make sure the proper (calculated) field values appear in the saved document.

There is no need to update fields after executing a mail merge because mail merge is a kind of field update and automatically updates all fields in the document.

This method does not update all field types. For the detailed list of supported field types, see the Programmers Guide.

This method does not update fields that are related to the page layout algorithms (e.g. PAGE, PAGES, PAGEREF). The page layout-related fields are updated when you render a document or call [Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--).

To update fields in the whole document use [Document.updateFields()](../../com.aspose.words/document\#updateFields--).

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

