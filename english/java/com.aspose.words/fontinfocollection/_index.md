---
title: FontInfoCollection
linktitle: FontInfoCollection
second_title: Aspose.Words for Java
description: Represents a collection of fonts used in a document in Java.
type: docs
weight: 327
url: /java/com.aspose.words/fontinfocollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class FontInfoCollection implements Iterable
```

Represents a collection of fonts used in a document.

To learn more, visit the [ Working with Fonts ][Working with Fonts] documentation article.

 **Remarks:** 

Items are [FontInfo](../../com.aspose.words/fontinfo/) objects.

You do not create instances of this class directly. Use the [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos) property to access the collection of fonts defined in the document.

 **Examples:** 

Shows how to save a document with embedded TrueType fonts.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

Shows how to print the details of what fonts are present in a document.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfoCollection allFonts = doc.getFontInfos();
 // Print all the used and unused fonts in the document.
 for (int i = 0; i < allFonts.getCount(); i++) {
     System.out.println("Font index #{i}");
     System.out.println("\tName: {allFonts[i].Name}");
 }
 
```


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Methods

| Method | Description |
| --- | --- |
| [contains(String name)](#contains-java.lang.String) | Determines whether the collection contains a font with the given name. |
| [get(int index)](#get-int) | Gets a font at the specified index. |
| [get(String name)](#get-java.lang.String) | Provides access to the collection items. |
| [getCount()](#getCount) | Gets the number of elements contained in the collection. |
| [getEmbedSystemFonts()](#getEmbedSystemFonts) | Specifies whether or not to embed System fonts into the document. |
| [getEmbedTrueTypeFonts()](#getEmbedTrueTypeFonts) | Specifies whether or not to embed TrueType fonts in a document when it is saved. |
| [getSaveSubsetFonts()](#getSaveSubsetFonts) | Specifies whether or not to save a subset of the embedded TrueType fonts with the document. |
| [iterator()](#iterator) | Returns an iterator object that can be used to iterate over all items in the collection. |
| [setEmbedSystemFonts(boolean value)](#setEmbedSystemFonts-boolean) | Specifies whether or not to embed System fonts into the document. |
| [setEmbedTrueTypeFonts(boolean value)](#setEmbedTrueTypeFonts-boolean) | Specifies whether or not to embed TrueType fonts in a document when it is saved. |
| [setSaveSubsetFonts(boolean value)](#setSaveSubsetFonts-boolean) | Specifies whether or not to save a subset of the embedded TrueType fonts with the document. |
### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Determines whether the collection contains a font with the given name.

 **Examples:** 

Shows info about the fonts that are present in the blank document.

```

 Document doc = new Document();

 // A blank document contains 3 default fonts. Each font in the document
 // will have a corresponding FontInfo object which contains details about that font.
 Assert.assertEquals(3, doc.getFontInfos().getCount());

 Assert.assertTrue(doc.getFontInfos().contains("Times New Roman"));
 Assert.assertEquals(204, doc.getFontInfos().get("Times New Roman").getCharset());

 Assert.assertTrue(doc.getFontInfos().contains("Symbol"));
 Assert.assertTrue(doc.getFontInfos().contains("Arial"));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | Case-insensitive name of the font to locate. |

**Returns:**
boolean -  true  if the item is found in the collection; otherwise,  false .
### get(int index) {#get-int}
```
public FontInfo get(int index)
```


Gets a font at the specified index.

 **Examples:** 

Shows how to extract an embedded font from a document, and save it to the local file system.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfo embeddedFont = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift");
 byte[] embeddedFontBytes = embeddedFont.getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR);
 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.ttf"), embeddedFontBytes);

 // Embedded font formats may be different in other formats such as .doc.
 // We need to know the correct format before we can extract the font.
 doc = new Document(getMyDir() + "Embedded font.doc");

 Assert.assertNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR));
 Assert.assertNotNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.EMBEDDED_OPEN_TYPE, EmbeddedFontStyle.REGULAR));

 // Also, we can convert embedded OpenType format, which comes from .doc documents, to OpenType.
 embeddedFontBytes = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFontAsOpenType(EmbeddedFontStyle.REGULAR);

 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.otf"), embeddedFontBytes);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | Zero-based index of the font. |

**Returns:**
[FontInfo](../../com.aspose.words/fontinfo/) - A font at the specified index.
### get(String name) {#get-java.lang.String}
```
public FontInfo get(String name)
```


Provides access to the collection items.  Gets a font with the specified name.

 **Examples:** 

Shows how to extract an embedded font from a document, and save it to the local file system.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfo embeddedFont = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift");
 byte[] embeddedFontBytes = embeddedFont.getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR);
 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.ttf"), embeddedFontBytes);

 // Embedded font formats may be different in other formats such as .doc.
 // We need to know the correct format before we can extract the font.
 doc = new Document(getMyDir() + "Embedded font.doc");

 Assert.assertNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR));
 Assert.assertNotNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.EMBEDDED_OPEN_TYPE, EmbeddedFontStyle.REGULAR));

 // Also, we can convert embedded OpenType format, which comes from .doc documents, to OpenType.
 embeddedFontBytes = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFontAsOpenType(EmbeddedFontStyle.REGULAR);

 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.otf"), embeddedFontBytes);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | Case-insensitive name of the font to locate. |

**Returns:**
[FontInfo](../../com.aspose.words/fontinfo/) - The corresponding [FontInfo](../../com.aspose.words/fontinfo/) value.
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of elements contained in the collection.

 **Examples:** 

Shows info about the fonts that are present in the blank document.

```

 Document doc = new Document();

 // A blank document contains 3 default fonts. Each font in the document
 // will have a corresponding FontInfo object which contains details about that font.
 Assert.assertEquals(3, doc.getFontInfos().getCount());

 Assert.assertTrue(doc.getFontInfos().contains("Times New Roman"));
 Assert.assertEquals(204, doc.getFontInfos().get("Times New Roman").getCharset());

 Assert.assertTrue(doc.getFontInfos().contains("Symbol"));
 Assert.assertTrue(doc.getFontInfos().contains("Arial"));
 
```

**Returns:**
int - The number of elements contained in the collection.
### getEmbedSystemFonts() {#getEmbedSystemFonts}
```
public boolean getEmbedSystemFonts()
```


Specifies whether or not to embed System fonts into the document. Default value for this property is  false .

This option works only when [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) option is set to  true .

 **Remarks:** 

Setting this property to  true  is useful if the user is on an East Asian system and wants to create a document that is readable by others who do not have fonts for that language on their system. For example, a user on a Japanese system could choose to embed the fonts in a document so that the Japanese document would be readable on all systems.

This option works for DOC, DOCX and RTF formats only.

 **Examples:** 

Shows how to save a document with embedded TrueType fonts.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getEmbedTrueTypeFonts() {#getEmbedTrueTypeFonts}
```
public boolean getEmbedTrueTypeFonts()
```


Specifies whether or not to embed TrueType fonts in a document when it is saved. Default value for this property is  false .

 **Remarks:** 

Embedding TrueType fonts allows others to view the document with the same fonts that were used to create it, but may substantially increase the document size.

This option works for DOC, DOCX and RTF formats only.

 **Examples:** 

Shows how to save a document with embedded TrueType fonts.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getSaveSubsetFonts() {#getSaveSubsetFonts}
```
public boolean getSaveSubsetFonts()
```


Specifies whether or not to save a subset of the embedded TrueType fonts with the document. Default value for this property is  false .

This option works only when [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) property is set to  true .

 **Remarks:** 

This option works for DOC, DOCX and RTF formats only.

 **Examples:** 

Shows how to save a document with embedded TrueType fonts.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### iterator() {#iterator}
```
public Iterator iterator()
```


Returns an iterator object that can be used to iterate over all items in the collection.

 **Examples:** 

Shows how to access and print details of each font in a document.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 Iterator fontCollectionEnumerator = doc.getFontInfos().iterator();
 while (fontCollectionEnumerator.hasNext()) {
     FontInfo fontInfo = fontCollectionEnumerator.next();
     if (fontInfo != null) {
         System.out.println("Font name: " + fontInfo.getName());

         // Alt names are usually blank.
         System.out.println("Alt name: " + fontInfo.getAltName());
         System.out.println("\t- Family: " + fontInfo.getFamily());
         System.out.println("\t- " + (fontInfo.isTrueType() ? "Is TrueType" : "Is not TrueType"));
         System.out.println("\t- Pitch: " + fontInfo.getPitch());
         System.out.println("\t- Charset: " + fontInfo.getCharset());
         System.out.println("\t- Panose:");
         System.out.println("\t\tFamily Kind: " + (fontInfo.getPanose()[0] & 0xFF));
         System.out.println("\t\tSerif Style: " + (fontInfo.getPanose()[1] & 0xFF));
         System.out.println("\t\tWeight: " + (fontInfo.getPanose()[2] & 0xFF));
         System.out.println("\t\tProportion: " + (fontInfo.getPanose()[3] & 0xFF));
         System.out.println("\t\tContrast: " + (fontInfo.getPanose()[4] & 0xFF));
         System.out.println("\t\tStroke Variation: " + (fontInfo.getPanose()[5] & 0xFF));
         System.out.println("\t\tArm Style: " + (fontInfo.getPanose()[6] & 0xFF));
         System.out.println("\t\tLetterform: " + (fontInfo.getPanose()[7] & 0xFF));
         System.out.println("\t\tMidline: " + (fontInfo.getPanose()[8] & 0xFF));
         System.out.println("\t\tX-Height: " + (fontInfo.getPanose()[9] & 0xFF));
     }
 }
 
```

**Returns:**
java.util.Iterator
### setEmbedSystemFonts(boolean value) {#setEmbedSystemFonts-boolean}
```
public void setEmbedSystemFonts(boolean value)
```


Specifies whether or not to embed System fonts into the document. Default value for this property is  false .

This option works only when [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) option is set to  true .

 **Remarks:** 

Setting this property to  true  is useful if the user is on an East Asian system and wants to create a document that is readable by others who do not have fonts for that language on their system. For example, a user on a Japanese system could choose to embed the fonts in a document so that the Japanese document would be readable on all systems.

This option works for DOC, DOCX and RTF formats only.

 **Examples:** 

Shows how to save a document with embedded TrueType fonts.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setEmbedTrueTypeFonts(boolean value) {#setEmbedTrueTypeFonts-boolean}
```
public void setEmbedTrueTypeFonts(boolean value)
```


Specifies whether or not to embed TrueType fonts in a document when it is saved. Default value for this property is  false .

 **Remarks:** 

Embedding TrueType fonts allows others to view the document with the same fonts that were used to create it, but may substantially increase the document size.

This option works for DOC, DOCX and RTF formats only.

 **Examples:** 

Shows how to save a document with embedded TrueType fonts.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setSaveSubsetFonts(boolean value) {#setSaveSubsetFonts-boolean}
```
public void setSaveSubsetFonts(boolean value)
```


Specifies whether or not to save a subset of the embedded TrueType fonts with the document. Default value for this property is  false .

This option works only when [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) property is set to  true .

 **Remarks:** 

This option works for DOC, DOCX and RTF formats only.

 **Examples:** 

Shows how to save a document with embedded TrueType fonts.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

