---
title: "FootnoteType"
linktitle: "FootnoteType"
second_title: "Aspose.Words para Java"
description: "Especifica si esto es una nota al pie o una nota final en Java."
type: docs
weight: 346
url: /es/java/com.aspose.words/footnotetype/
---

**Inheritance:**
java.lang.Object
```
public class FootnoteType
```

Especifica si se trata de una nota al pie o de una nota al final.

 **Remarks:** 

Tanto las notas al pie como las notas finales están representadas por objetos de la clase [FOOTNOTE](../../com.aspose.words/footnotetype/#FOOTNOTE). Use [Footnote.getFootnoteType()](../../com.aspose.words/footnote/#getFootnoteType) para distinguir entre notas al pie y notas finales.

 **Examples:** 

Muestra cómo referenciar texto con una nota al pie y una nota final.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some text and mark it with a footnote with the IsAuto property set to "true" by default,
 // so the marker seen in the body text will be auto-numbered at "1",
 // and the footnote will appear at the bottom of the page.
 builder.write("This text will be referenced by a footnote.");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote comment regarding referenced text.");

 // Insert more text and mark it with an endnote with a custom reference mark,
 // which will be used in place of the number "2" and set "IsAuto" to false.
 builder.write("This text will be referenced by an endnote.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote comment regarding referenced text.", "CustomMark");

 // Footnotes always appear at the bottom of their referenced text,
 // so this page break will not affect the footnote.
 // On the other hand, endnotes are always at the end of the document
 // so that this page break will push the endnote down to the next page.
 builder.insertBreak(BreakType.PAGE_BREAK);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertFootnote.docx");
 
```

Muestra cómo insertar y personalizar notas al pie.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add text, and reference it with a footnote. This footnote will place a small superscript reference
 // mark after the text that it references and create an entry below the main body text at the bottom of the page.
 // This entry will contain the footnote's reference mark and the reference text,
 // which we will pass to the document builder's "InsertFootnote" method.
 builder.write("Main body text.");
 Footnote footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 // If this property is set to "true", then our footnote's reference mark
 // will be its index among all the section's footnotes.
 // This is the first footnote, so the reference mark will be "1".
 Assert.assertTrue(footnote.isAuto());

 // We can move the document builder inside the footnote to edit its reference text.
 builder.moveTo(footnote.getFirstParagraph());
 builder.write(" More text added by a DocumentBuilder.");
 builder.moveToDocumentEnd();

 Assert.assertEquals(footnote.getParagraphs().get(0).toString(SaveFormat.TEXT).trim(), "Footnote text. More text added by a DocumentBuilder.");

 builder.write(" More main body text.");
 footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 // We can set a custom reference mark which the footnote will use instead of its index number.
 footnote.setReferenceMark("RefMark");

 Assert.assertFalse(footnote.isAuto());

 // A bookmark with the "IsAuto" flag set to true will still show its real index
 // even if previous bookmarks display custom reference marks, so this bookmark's reference mark will be a "3".
 builder.write(" More main body text.");
 footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 Assert.assertTrue(footnote.isAuto());

 doc.save(getArtifactsDir() + "InlineStory.AddFootnote.docx");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [ENDNOTE](#ENDNOTE) | El objeto es una nota final. |
| [FOOTNOTE](#FOOTNOTE) | El objeto es una nota al pie. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String footnoteTypeName)](#fromName-java.lang.String) |  |
| [getName(int footnoteType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int footnoteType)](#toString-int) |  |
### ENDNOTE {#ENDNOTE}
```
public static int ENDNOTE
```


El objeto es una nota final.

### FOOTNOTE {#FOOTNOTE}
```
public static int FOOTNOTE
```


El objeto es una nota al pie.

### length {#length}
```
public static int length
```


### fromName(String footnoteTypeName) {#fromName-java.lang.String}
```
public static int fromName(String footnoteTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| footnoteTypeName | java.lang.String |  |

**Returns:**
int
### getName(int footnoteType) {#getName-int}
```
public static String getName(int footnoteType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| footnoteType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int footnoteType) {#toString-int}
```
public static String toString(int footnoteType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| footnoteType | int |  |

**Returns:**
java.lang.String
