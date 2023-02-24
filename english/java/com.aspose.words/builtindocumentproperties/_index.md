---
title: BuiltInDocumentProperties
linktitle: BuiltInDocumentProperties
second_title: Aspose.Words for Java API Reference
description: A collection of built-in document properties in Java.
type: docs
weight: 46
url: /java/com.aspose.words/builtindocumentproperties/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.DocumentPropertyCollection](../../com.aspose.words/documentpropertycollection/)
```
public class BuiltInDocumentProperties extends DocumentPropertyCollection
```

A collection of built-in document properties.

To learn more, visit the [ Work with Document Properties ][Work with Document Properties] documentation article.

Provides access to [DocumentProperty](../../com.aspose.words/documentproperty/) objects by their names (using an indexer) and via a set of typed properties that return values of appropriate types.

The names of the properties are case-insensitive.

The properties in the collection are sorted alphabetically by name.


[Work with Document Properties]: https://docs.aspose.com/words/java/work-with-document-properties/
## Methods

| Method | Description |
| --- | --- |
| [clear()](#clear) | Removes all properties from the collection. |
| [contains(String name)](#contains-java.lang.String) | Returns  true  if a property with the specified name exists in the collection. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [get(int index)](#get-int) | Returns a [DocumentProperty](../../com.aspose.words/documentproperty/) object by index. |
| [get(String name)](#get-java.lang.String) | Returns a [DocumentProperty](../../com.aspose.words/documentproperty/) object. |
| [getAuthor()](#getAuthor) | Gets the name of the document's author. |
| [getBytes()](#getBytes) | Represents an estimate of the number of bytes in the document. |
| [getCategory()](#getCategory) | Gets the category of the document. |
| [getCharacters()](#getCharacters) | Represents an estimate of the number of characters in the document. |
| [getCharactersWithSpaces()](#getCharactersWithSpaces) | Represents an estimate of the number of characters (including spaces) in the document. |
| [getClass()](#getClass) |  |
| [getComments()](#getComments) | Gets the document comments. |
| [getCompany()](#getCompany) | Gets the company property. |
| [getContentStatus()](#getContentStatus) | Gets the **F:Aspose.Words.Properties.PropertyName.ContentStatus** of the document. |
| [getContentType()](#getContentType) | Gets the **F:Aspose.Words.Properties.PropertyName.ContentType** of the document. |
| [getCount()](#getCount) | Gets number of items in the collection. |
| [getCreatedTime()](#getCreatedTime) | Gets date of the document creation in UTC. |
| [getHeadingPairs()](#getHeadingPairs) | Specifies document headings and their names. |
| [getHyperlinkBase()](#getHyperlinkBase) | Specifies the base string used for evaluating relative hyperlinks in this document. |
| [getKeywords()](#getKeywords) | Gets the document keywords. |
| [getLastPrinted()](#getLastPrinted) | Gets the date when the document was last printed in UTC. |
| [getLastSavedBy()](#getLastSavedBy) | Gets the name of the last author. |
| [getLastSavedTime()](#getLastSavedTime) | Gets the time of the last save in UTC. |
| [getLines()](#getLines) | Represents an estimate of the number of lines in the document. |
| [getLinksUpToDate()](#getLinksUpToDate) | Indicates whether hyperlinks in a document are up-to-date. |
| [getManager()](#getManager) | Gets the manager property. |
| [getNameOfApplication()](#getNameOfApplication) | Gets the name of the application. |
| [getPages()](#getPages) | Represents an estimate of the number of pages in the document. |
| [getParagraphs()](#getParagraphs) | Represents an estimate of the number of paragraphs in the document. |
| [getRevisionNumber()](#getRevisionNumber) | Gets the document revision number. |
| [getSecurity()](#getSecurity) | Specifies the security level of a document as a numeric value. |
| [getSubject()](#getSubject) | Gets the subject of the document. |
| [getTemplate()](#getTemplate) | Gets the informational name of the document template. |
| [getThumbnail()](#getThumbnail) | Gets or sets the thumbnail of the document. |
| [getTitle()](#getTitle) | Gets the title of the document. |
| [getTitlesOfParts()](#getTitlesOfParts) | Each string in the array specifies the name of a part in the document. |
| [getTotalEditingTime()](#getTotalEditingTime) | Gets the total editing time in minutes. |
| [getVersion()](#getVersion) | Represents the version number of the application that created the document. |
| [getWords()](#getWords) | Represents an estimate of the number of words in the document. |
| [hashCode()](#hashCode) |  |
| [indexOf(String name)](#indexOf-java.lang.String) | Gets the index of a property by name. |
| [iterator()](#iterator) | Returns an iterator object that can be used to iterate over all items in the collection. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [remove(String name)](#remove-java.lang.String) | Removes a property with the specified name from the collection. |
| [removeAt(int index)](#removeAt-int) | Removes a property at the specified index. |
| [setAuthor(String value)](#setAuthor-java.lang.String) | Sets the name of the document's author. |
| [setBytes(int value)](#setBytes-int) | Represents an estimate of the number of bytes in the document. |
| [setCategory(String value)](#setCategory-java.lang.String) | Sets the category of the document. |
| [setCharacters(int value)](#setCharacters-int) | Represents an estimate of the number of characters in the document. |
| [setCharactersWithSpaces(int value)](#setCharactersWithSpaces-int) | Represents an estimate of the number of characters (including spaces) in the document. |
| [setComments(String value)](#setComments-java.lang.String) | Sets the document comments. |
| [setCompany(String value)](#setCompany-java.lang.String) | Sets the company property. |
| [setContentStatus(String value)](#setContentStatus-java.lang.String) | Sets the **F:Aspose.Words.Properties.PropertyName.ContentStatus** of the document. |
| [setContentType(String value)](#setContentType-java.lang.String) | Sets the **F:Aspose.Words.Properties.PropertyName.ContentType** of the document. |
| [setCreatedTime(Date value)](#setCreatedTime-java.util.Date) | Sets date of the document creation in UTC. |
| [setHeadingPairs(Object[] value)](#setHeadingPairs-java.lang.Object) | Specifies document headings and their names. |
| [setHyperlinkBase(String value)](#setHyperlinkBase-java.lang.String) | Specifies the base string used for evaluating relative hyperlinks in this document. |
| [setKeywords(String value)](#setKeywords-java.lang.String) | Sets the document keywords. |
| [setLastPrinted(Date value)](#setLastPrinted-java.util.Date) | Sets the date when the document was last printed in UTC. |
| [setLastSavedBy(String value)](#setLastSavedBy-java.lang.String) | Sets the name of the last author. |
| [setLastSavedTime(Date value)](#setLastSavedTime-java.util.Date) | Sets the time of the last save in UTC. |
| [setLines(int value)](#setLines-int) | Represents an estimate of the number of lines in the document. |
| [setLinksUpToDate(boolean value)](#setLinksUpToDate-boolean) | Indicates whether hyperlinks in a document are up-to-date. |
| [setManager(String value)](#setManager-java.lang.String) | Sets the manager property. |
| [setNameOfApplication(String value)](#setNameOfApplication-java.lang.String) | Sets the name of the application. |
| [setPages(int value)](#setPages-int) | Represents an estimate of the number of pages in the document. |
| [setParagraphs(int value)](#setParagraphs-int) | Represents an estimate of the number of paragraphs in the document. |
| [setRevisionNumber(int value)](#setRevisionNumber-int) | Sets the document revision number. |
| [setSecurity(int value)](#setSecurity-int) | Specifies the security level of a document as a numeric value. |
| [setSubject(String value)](#setSubject-java.lang.String) | Sets the subject of the document. |
| [setTemplate(String value)](#setTemplate-java.lang.String) | Sets the informational name of the document template. |
| [setThumbnail(byte[] value)](#setThumbnail-byte) | Gets or sets the thumbnail of the document. |
| [setTitle(String value)](#setTitle-java.lang.String) | Sets the title of the document. |
| [setTitlesOfParts(String[] value)](#setTitlesOfParts-java.lang.String) | Each string in the array specifies the name of a part in the document. |
| [setTotalEditingTime(int value)](#setTotalEditingTime-int) | Sets the total editing time in minutes. |
| [setVersion(int value)](#setVersion-int) | Represents the version number of the application that created the document. |
| [setWords(int value)](#setWords-int) | Represents an estimate of the number of words in the document. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### clear() {#clear}
```
public void clear()
```


Removes all properties from the collection.

### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Returns  true  if a property with the specified name exists in the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-insensitive name of the property. |

**Returns:**
boolean - \{ true  if the property exists in the collection;  false  otherwise.
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
### get(int index) {#get-int}
```
public DocumentProperty get(int index)
```


Returns a [DocumentProperty](../../com.aspose.words/documentproperty/) object by index.

**Note:**  In Java this method is slow because iterates over all nodes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | Zero-based index of the [DocumentProperty](../../com.aspose.words/documentproperty/) to retrieve. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - A [DocumentProperty](../../com.aspose.words/documentproperty/) object by index.
### get(String name) {#get-java.lang.String}
```
public DocumentProperty get(String name)
```


Returns a [DocumentProperty](../../com.aspose.words/documentproperty/) object.  Returns a [DocumentProperty](../../com.aspose.words/documentproperty/) object by the name of the property.

The string names of the properties correspond to the names of the typed properties available from [BuiltInDocumentProperties](../../com.aspose.words/builtindocumentproperties/).

If you request a property that is not present in the document, but the name of the property is recognized as a valid built-in name, a new [DocumentProperty](../../com.aspose.words/documentproperty/) is created, added to the collection and returned. The newly created property is assigned a default value (empty string, zero,  false  or DateTime.MinValue depending on the type of the built-in property).

If you request a property that is not present in the document and the name is not recognized as a built-in name, a  null  is returned.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-insensitive name of the property to retrieve. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - The corresponding [DocumentProperty](../../com.aspose.words/documentproperty/) value.
### getAuthor() {#getAuthor}
```
public String getAuthor()
```


Gets the name of the document's author.

**Returns:**
java.lang.String - The name of the document's author.
### getBytes() {#getBytes}
```
public int getBytes()
```


Represents an estimate of the number of bytes in the document.

Microsoft Word does not always set this property.

Aspose.Words does not update this property.

**Returns:**
int - The corresponding  int  value.
### getCategory() {#getCategory}
```
public String getCategory()
```


Gets the category of the document.

**Returns:**
java.lang.String - The category of the document.
### getCharacters() {#getCharacters}
```
public int getCharacters()
```


Represents an estimate of the number of characters in the document.

Aspose.Words updates this property when you call [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

**Returns:**
int - The corresponding  int  value.
### getCharactersWithSpaces() {#getCharactersWithSpaces}
```
public int getCharactersWithSpaces()
```


Represents an estimate of the number of characters (including spaces) in the document.

Aspose.Words updates this property when you call [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

**Returns:**
int - The corresponding  int  value.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getComments() {#getComments}
```
public String getComments()
```


Gets the document comments.

**Returns:**
java.lang.String - The document comments.
### getCompany() {#getCompany}
```
public String getCompany()
```


Gets the company property.

**Returns:**
java.lang.String - The company property.
### getContentStatus() {#getContentStatus}
```
public String getContentStatus()
```


Gets the **F:Aspose.Words.Properties.PropertyName.ContentStatus** of the document.

**Returns:**
java.lang.String - The **F:Aspose.Words.Properties.PropertyName.ContentStatus** of the document.
### getContentType() {#getContentType}
```
public String getContentType()
```


Gets the **F:Aspose.Words.Properties.PropertyName.ContentType** of the document.

**Returns:**
java.lang.String - The **F:Aspose.Words.Properties.PropertyName.ContentType** of the document.
### getCount() {#getCount}
```
public int getCount()
```


Gets number of items in the collection.

**Returns:**
int - Number of items in the collection.
### getCreatedTime() {#getCreatedTime}
```
public Date getCreatedTime()
```


Gets date of the document creation in UTC.

For documents originated from RTF format this property returns local time of the author's machine at the moment of document creation.

Aspose.Words does not update this property.

**Returns:**
java.util.Date - Date of the document creation in UTC.
### getHeadingPairs() {#getHeadingPairs}
```
public Object[] getHeadingPairs()
```


Specifies document headings and their names.

Every heading pair occupies two elements in this array.

The first element of the pair is a java.lang.String and specifies the heading name. The second element of the pair is an int and specifies the count of document parts for this heading in the [getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties/\#getTitlesOfParts) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties/\#setTitlesOfParts-java.lang.String) property.

The total sum of counts for all heading pairs in this property must be equal to the number of elements in the [getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties/\#getTitlesOfParts) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties/\#setTitlesOfParts-java.lang.String) property.

Aspose.Words does not update this property.

**Returns:**
java.lang.Object[] - The corresponding java.lang.Object[] value.
### getHyperlinkBase() {#getHyperlinkBase}
```
public String getHyperlinkBase()
```


Specifies the base string used for evaluating relative hyperlinks in this document.

Aspose.Words does not use this property.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getKeywords() {#getKeywords}
```
public String getKeywords()
```


Gets the document keywords.

**Returns:**
java.lang.String - The document keywords.
### getLastPrinted() {#getLastPrinted}
```
public Date getLastPrinted()
```


Gets the date when the document was last printed in UTC.

For documents originated from RTF format this property returns the local time of last print operation.

If the document was never printed, this property will return DateTime.MinValue.

Aspose.Words does not update this property.

**Returns:**
java.util.Date - The date when the document was last printed in UTC.
### getLastSavedBy() {#getLastSavedBy}
```
public String getLastSavedBy()
```


Gets the name of the last author.

Aspose.Words does not update this property.

**Returns:**
java.lang.String - The name of the last author.
### getLastSavedTime() {#getLastSavedTime}
```
public Date getLastSavedTime()
```


Gets the time of the last save in UTC.

For documents originated from RTF format this property returns the local time of last save operation.

Aspose.Words does not update this property.

**Returns:**
java.util.Date - The time of the last save in UTC.
### getLines() {#getLines}
```
public int getLines()
```


Represents an estimate of the number of lines in the document.

Aspose.Words updates this property when you call [Document.updateWordCount(boolean)](../../com.aspose.words/document/\#updateWordCount-boolean).

**Returns:**
int - The corresponding  int  value.
### getLinksUpToDate() {#getLinksUpToDate}
```
public boolean getLinksUpToDate()
```


Indicates whether hyperlinks in a document are up-to-date.

Aspose.Words does not update this property.

**Returns:**
boolean - The corresponding  boolean  value.
### getManager() {#getManager}
```
public String getManager()
```


Gets the manager property.

**Returns:**
java.lang.String - The manager property.
### getNameOfApplication() {#getNameOfApplication}
```
public String getNameOfApplication()
```


Gets the name of the application.

**Returns:**
java.lang.String - The name of the application.
### getPages() {#getPages}
```
public int getPages()
```


Represents an estimate of the number of pages in the document.

Aspose.Words updates this property when you call [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout).

**Returns:**
int - The corresponding  int  value.
### getParagraphs() {#getParagraphs}
```
public int getParagraphs()
```


Represents an estimate of the number of paragraphs in the document.

Aspose.Words updates this property when you call [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

**Returns:**
int - The corresponding  int  value.
### getRevisionNumber() {#getRevisionNumber}
```
public int getRevisionNumber()
```


Gets the document revision number.

Aspose.Words does not update this property.

**Returns:**
int - The document revision number.
### getSecurity() {#getSecurity}
```
public int getSecurity()
```


Specifies the security level of a document as a numeric value.

Use this property for informational purposes only because Microsoft Word does not always set this property. This property is available in DOC and OOXML documents only.

To protect or unprotect a document use the **M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)** and [Document.unprotect()](../../com.aspose.words/document/\#unprotect) methods.

Aspose.Words updates this property to a correct value before saving a document.

**Returns:**
int - The corresponding  int  value. The returned value is a bitwise combination of [DocumentSecurity](../../com.aspose.words/documentsecurity/) constants.
### getSubject() {#getSubject}
```
public String getSubject()
```


Gets the subject of the document.

**Returns:**
java.lang.String - The subject of the document.
### getTemplate() {#getTemplate}
```
public String getTemplate()
```


Gets the informational name of the document template.

In Microsoft Word, this property is for informational purposes only and usually contains only the file name of the template without the path.

Empty string means the document is attached to the Normal template.

To get or set the actual name of the attached template, use the [Document.getAttachedTemplate()](../../com.aspose.words/document/\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document/\#setAttachedTemplate-java.lang.String) property.

**Returns:**
java.lang.String - The informational name of the document template.
### getThumbnail() {#getThumbnail}
```
public byte[] getThumbnail()
```


Gets or sets the thumbnail of the document.

For now this property is used only when a document is being exported to ePub, it's not read from and written to other document formats.

Image of arbitrary format can be set to this property, but the format is checked during export. java.lang.IllegalStateException is thrown if the image is invalid or its format is unsupported for specific format of document.

Only gif, jpeg and png images can be used for ePub publication.

**Returns:**
byte[] - The corresponding byte[] value.
### getTitle() {#getTitle}
```
public String getTitle()
```


Gets the title of the document.

**Returns:**
java.lang.String - The title of the document.
### getTitlesOfParts() {#getTitlesOfParts}
```
public String[] getTitlesOfParts()
```


Each string in the array specifies the name of a part in the document.

Aspose.Words does not update this property.

**Returns:**
java.lang.String[] - The corresponding java.lang.String[] value.
### getTotalEditingTime() {#getTotalEditingTime}
```
public int getTotalEditingTime()
```


Gets the total editing time in minutes.

**Returns:**
int - The total editing time in minutes.
### getVersion() {#getVersion}
```
public int getVersion()
```


Represents the version number of the application that created the document.

When a document was created by Microsoft Word, then high 16 bit represent the major version and low 16 bit represent the build number.

**Returns:**
int - The corresponding  int  value.
### getWords() {#getWords}
```
public int getWords()
```


Represents an estimate of the number of words in the document.

Aspose.Words updates this property when you call [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

**Returns:**
int - The corresponding  int  value.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### indexOf(String name) {#indexOf-java.lang.String}
```
public int indexOf(String name)
```


Gets the index of a property by name.

**Note:**  In Java this method is slow because iterates over all nodes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-insensitive name of the property. |

**Returns:**
int - The zero based index. Negative value if not found.
### iterator() {#iterator}
```
public Iterator iterator()
```


Returns an iterator object that can be used to iterate over all items in the collection.

**Returns:**
java.util.Iterator
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### remove(String name) {#remove-java.lang.String}
```
public void remove(String name)
```


Removes a property with the specified name from the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-insensitive name of the property. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Removes a property at the specified index.

**Note:**  In Java this method is slow because iterates over all nodes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero based index. |

### setAuthor(String value) {#setAuthor-java.lang.String}
```
public void setAuthor(String value)
```


Sets the name of the document's author.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the document's author. |

### setBytes(int value) {#setBytes-int}
```
public void setBytes(int value)
```


Represents an estimate of the number of bytes in the document.

Microsoft Word does not always set this property.

Aspose.Words does not update this property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setCategory(String value) {#setCategory-java.lang.String}
```
public void setCategory(String value)
```


Sets the category of the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The category of the document. |

### setCharacters(int value) {#setCharacters-int}
```
public void setCharacters(int value)
```


Represents an estimate of the number of characters in the document.

Aspose.Words updates this property when you call [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setCharactersWithSpaces(int value) {#setCharactersWithSpaces-int}
```
public void setCharactersWithSpaces(int value)
```


Represents an estimate of the number of characters (including spaces) in the document.

Aspose.Words updates this property when you call [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setComments(String value) {#setComments-java.lang.String}
```
public void setComments(String value)
```


Sets the document comments.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The document comments. |

### setCompany(String value) {#setCompany-java.lang.String}
```
public void setCompany(String value)
```


Sets the company property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The company property. |

### setContentStatus(String value) {#setContentStatus-java.lang.String}
```
public void setContentStatus(String value)
```


Sets the **F:Aspose.Words.Properties.PropertyName.ContentStatus** of the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The **F:Aspose.Words.Properties.PropertyName.ContentStatus** of the document. |

### setContentType(String value) {#setContentType-java.lang.String}
```
public void setContentType(String value)
```


Sets the **F:Aspose.Words.Properties.PropertyName.ContentType** of the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The **F:Aspose.Words.Properties.PropertyName.ContentType** of the document. |

### setCreatedTime(Date value) {#setCreatedTime-java.util.Date}
```
public void setCreatedTime(Date value)
```


Sets date of the document creation in UTC.

For documents originated from RTF format this property returns local time of the author's machine at the moment of document creation.

Aspose.Words does not update this property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.util.Date | Date of the document creation in UTC. |

### setHeadingPairs(Object[] value) {#setHeadingPairs-java.lang.Object}
```
public void setHeadingPairs(Object[] value)
```


Specifies document headings and their names.

Every heading pair occupies two elements in this array.

The first element of the pair is a java.lang.String and specifies the heading name. The second element of the pair is an int and specifies the count of document parts for this heading in the [getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties/\#getTitlesOfParts) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties/\#setTitlesOfParts-java.lang.String) property.

The total sum of counts for all heading pairs in this property must be equal to the number of elements in the [getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties/\#getTitlesOfParts) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties/\#setTitlesOfParts-java.lang.String) property.

Aspose.Words does not update this property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.Object[] | The corresponding java.lang.Object[] value. |

### setHyperlinkBase(String value) {#setHyperlinkBase-java.lang.String}
```
public void setHyperlinkBase(String value)
```


Specifies the base string used for evaluating relative hyperlinks in this document.

Aspose.Words does not use this property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setKeywords(String value) {#setKeywords-java.lang.String}
```
public void setKeywords(String value)
```


Sets the document keywords.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The document keywords. |

### setLastPrinted(Date value) {#setLastPrinted-java.util.Date}
```
public void setLastPrinted(Date value)
```


Sets the date when the document was last printed in UTC.

For documents originated from RTF format this property returns the local time of last print operation.

If the document was never printed, this property will return DateTime.MinValue.

Aspose.Words does not update this property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.util.Date | The date when the document was last printed in UTC. |

### setLastSavedBy(String value) {#setLastSavedBy-java.lang.String}
```
public void setLastSavedBy(String value)
```


Sets the name of the last author.

Aspose.Words does not update this property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the last author. |

### setLastSavedTime(Date value) {#setLastSavedTime-java.util.Date}
```
public void setLastSavedTime(Date value)
```


Sets the time of the last save in UTC.

For documents originated from RTF format this property returns the local time of last save operation.

Aspose.Words does not update this property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.util.Date | The time of the last save in UTC. |

### setLines(int value) {#setLines-int}
```
public void setLines(int value)
```


Represents an estimate of the number of lines in the document.

Aspose.Words updates this property when you call [Document.updateWordCount(boolean)](../../com.aspose.words/document/\#updateWordCount-boolean).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setLinksUpToDate(boolean value) {#setLinksUpToDate-boolean}
```
public void setLinksUpToDate(boolean value)
```


Indicates whether hyperlinks in a document are up-to-date.

Aspose.Words does not update this property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setManager(String value) {#setManager-java.lang.String}
```
public void setManager(String value)
```


Sets the manager property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The manager property. |

### setNameOfApplication(String value) {#setNameOfApplication-java.lang.String}
```
public void setNameOfApplication(String value)
```


Sets the name of the application.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the application. |

### setPages(int value) {#setPages-int}
```
public void setPages(int value)
```


Represents an estimate of the number of pages in the document.

Aspose.Words updates this property when you call [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setParagraphs(int value) {#setParagraphs-int}
```
public void setParagraphs(int value)
```


Represents an estimate of the number of paragraphs in the document.

Aspose.Words updates this property when you call [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setRevisionNumber(int value) {#setRevisionNumber-int}
```
public void setRevisionNumber(int value)
```


Sets the document revision number.

Aspose.Words does not update this property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The document revision number. |

### setSecurity(int value) {#setSecurity-int}
```
public void setSecurity(int value)
```


Specifies the security level of a document as a numeric value.

Use this property for informational purposes only because Microsoft Word does not always set this property. This property is available in DOC and OOXML documents only.

To protect or unprotect a document use the **M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)** and [Document.unprotect()](../../com.aspose.words/document/\#unprotect) methods.

Aspose.Words updates this property to a correct value before saving a document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be a bitwise combination of [DocumentSecurity](../../com.aspose.words/documentsecurity/) constants. |

### setSubject(String value) {#setSubject-java.lang.String}
```
public void setSubject(String value)
```


Sets the subject of the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The subject of the document. |

### setTemplate(String value) {#setTemplate-java.lang.String}
```
public void setTemplate(String value)
```


Sets the informational name of the document template.

In Microsoft Word, this property is for informational purposes only and usually contains only the file name of the template without the path.

Empty string means the document is attached to the Normal template.

To get or set the actual name of the attached template, use the [Document.getAttachedTemplate()](../../com.aspose.words/document/\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document/\#setAttachedTemplate-java.lang.String) property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The informational name of the document template. |

### setThumbnail(byte[] value) {#setThumbnail-byte}
```
public void setThumbnail(byte[] value)
```


Gets or sets the thumbnail of the document.

For now this property is used only when a document is being exported to ePub, it's not read from and written to other document formats.

Image of arbitrary format can be set to this property, but the format is checked during export. java.lang.IllegalStateException is thrown if the image is invalid or its format is unsupported for specific format of document.

Only gif, jpeg and png images can be used for ePub publication.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | byte[] | The corresponding byte[] value. |

### setTitle(String value) {#setTitle-java.lang.String}
```
public void setTitle(String value)
```


Sets the title of the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The title of the document. |

### setTitlesOfParts(String[] value) {#setTitlesOfParts-java.lang.String}
```
public void setTitlesOfParts(String[] value)
```


Each string in the array specifies the name of a part in the document.

Aspose.Words does not update this property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String[] | The corresponding java.lang.String[] value. |

### setTotalEditingTime(int value) {#setTotalEditingTime-int}
```
public void setTotalEditingTime(int value)
```


Sets the total editing time in minutes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The total editing time in minutes. |

### setVersion(int value) {#setVersion-int}
```
public void setVersion(int value)
```


Represents the version number of the application that created the document.

When a document was created by Microsoft Word, then high 16 bit represent the major version and low 16 bit represent the build number.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setWords(int value) {#setWords-int}
```
public void setWords(int value)
```


Represents an estimate of the number of words in the document.

Aspose.Words updates this property when you call [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

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

