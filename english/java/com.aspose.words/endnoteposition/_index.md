---
title: EndnotePosition
linktitle: EndnotePosition
second_title: Aspose.Words for Java
description: Defines the endnote position in Java.
type: docs
weight: 176
url: /java/com.aspose.words/endnoteposition/
---

**Inheritance:**
java.lang.Object
```
public class EndnotePosition
```

Defines the endnote position.

 **Examples:** 

Shows how to select a different place where the document collects and displays its endnotes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // An endnote is a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting an endnote adds a small superscript reference symbol
 // at the main body text where we insert the endnote.
 // Each endnote also creates an entry at the end of the document, consisting of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertEndnote" method.
 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote contents.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("This is the second section.");

 // We can use the "Position" property to determine where the document will place all its endnotes.
 // If we set the value of the "Position" property to "EndnotePosition.EndOfDocument",
 // every footnote will show up in a collection at the end of the document. This is the default value.
 // If we set the value of the "Position" property to "EndnotePosition.EndOfSection",
 // every footnote will show up in a collection at the end of the section whose text contains the endnote's reference mark.
 doc.getEndnoteOptions().setPosition(endnotePosition);

 doc.save(getArtifactsDir() + "InlineStory.PositionEndnote.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [END_OF_DOCUMENT](#END-OF-DOCUMENT) | Endnotes are output at the end of the document. |
| [END_OF_SECTION](#END-OF-SECTION) | Endnotes are output at the end of the section. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String endnotePositionName)](#fromName-java.lang.String) |  |
| [getName(int endnotePosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int endnotePosition)](#toString-int) |  |
### END_OF_DOCUMENT {#END-OF-DOCUMENT}
```
public static int END_OF_DOCUMENT
```


Endnotes are output at the end of the document.

### END_OF_SECTION {#END-OF-SECTION}
```
public static int END_OF_SECTION
```


Endnotes are output at the end of the section.

### length {#length}
```
public static int length
```


### fromName(String endnotePositionName) {#fromName-java.lang.String}
```
public static int fromName(String endnotePositionName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| endnotePositionName | java.lang.String |  |

**Returns:**
int
### getName(int endnotePosition) {#getName-int}
```
public static String getName(int endnotePosition)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| endnotePosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int endnotePosition) {#toString-int}
```
public static String toString(int endnotePosition)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| endnotePosition | int |  |

**Returns:**
java.lang.String
