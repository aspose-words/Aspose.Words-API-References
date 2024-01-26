---
title: HyphenationOptions
linktitle: HyphenationOptions
second_title: Aspose.Words for Java
description: Allows to configure document hyphenation options in Java.
type: docs
weight: 353
url: /java/com.aspose.words/hyphenationoptions/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class HyphenationOptions implements Cloneable
```

Allows to configure document hyphenation options.

To learn more, visit the [ Working with Hyphenation ][Working with Hyphenation] documentation article.

 **Examples:** 

Shows how to configure automatic hyphenation.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```


[Working with Hyphenation]: https://docs.aspose.com/words/java/working-with-hyphenation/
## Methods

| Method | Description |
| --- | --- |
| [getAutoHyphenation()](#getAutoHyphenation) | Gets value determining whether automatic hyphenation is turned on for the document. |
| [getConsecutiveHyphenLimit()](#getConsecutiveHyphenLimit) | Gets the maximum number of consecutive lines that can end with hyphens. |
| [getHyphenateCaps()](#getHyphenateCaps) | Gets value determining whether words written in all capital letters are hyphenated. |
| [getHyphenationZone()](#getHyphenationZone) | Gets the distance in 1/20 of a point from the right margin within which you do not want to hyphenate words. |
| [setAutoHyphenation(boolean value)](#setAutoHyphenation-boolean) | Sets value determining whether automatic hyphenation is turned on for the document. |
| [setConsecutiveHyphenLimit(int value)](#setConsecutiveHyphenLimit-int) | Sets the maximum number of consecutive lines that can end with hyphens. |
| [setHyphenateCaps(boolean value)](#setHyphenateCaps-boolean) | Sets value determining whether words written in all capital letters are hyphenated. |
| [setHyphenationZone(int value)](#setHyphenationZone-int) | Sets the distance in 1/20 of a point from the right margin within which you do not want to hyphenate words. |
### getAutoHyphenation() {#getAutoHyphenation}
```
public boolean getAutoHyphenation()
```


Gets value determining whether automatic hyphenation is turned on for the document. Default value for this property is  false .

 **Examples:** 

Shows how to configure automatic hyphenation.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
boolean - Value determining whether automatic hyphenation is turned on for the document.
### getConsecutiveHyphenLimit() {#getConsecutiveHyphenLimit}
```
public int getConsecutiveHyphenLimit()
```


Gets the maximum number of consecutive lines that can end with hyphens. Default value for this property is 0.

 **Remarks:** 

If value of this property is set to 0, any number of consecutive lines can end with hyphens.

The property does not have effect when saving to fixed page formats e.g. PDF.

 **Examples:** 

Shows how to configure automatic hyphenation.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
int - The maximum number of consecutive lines that can end with hyphens.
### getHyphenateCaps() {#getHyphenateCaps}
```
public boolean getHyphenateCaps()
```


Gets value determining whether words written in all capital letters are hyphenated. Default value for this property is  true .

 **Examples:** 

Shows how to configure automatic hyphenation.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
boolean - Value determining whether words written in all capital letters are hyphenated.
### getHyphenationZone() {#getHyphenationZone}
```
public int getHyphenationZone()
```


Gets the distance in 1/20 of a point from the right margin within which you do not want to hyphenate words. Default value for this property is 360 (0.25 inch).

 **Examples:** 

Shows how to configure automatic hyphenation.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
int - The distance in 1/20 of a point from the right margin within which you do not want to hyphenate words.
### setAutoHyphenation(boolean value) {#setAutoHyphenation-boolean}
```
public void setAutoHyphenation(boolean value)
```


Sets value determining whether automatic hyphenation is turned on for the document. Default value for this property is  false .

 **Examples:** 

Shows how to configure automatic hyphenation.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Value determining whether automatic hyphenation is turned on for the document. |

### setConsecutiveHyphenLimit(int value) {#setConsecutiveHyphenLimit-int}
```
public void setConsecutiveHyphenLimit(int value)
```


Sets the maximum number of consecutive lines that can end with hyphens. Default value for this property is 0.

 **Remarks:** 

If value of this property is set to 0, any number of consecutive lines can end with hyphens.

The property does not have effect when saving to fixed page formats e.g. PDF.

 **Examples:** 

Shows how to configure automatic hyphenation.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The maximum number of consecutive lines that can end with hyphens. |

### setHyphenateCaps(boolean value) {#setHyphenateCaps-boolean}
```
public void setHyphenateCaps(boolean value)
```


Sets value determining whether words written in all capital letters are hyphenated. Default value for this property is  true .

 **Examples:** 

Shows how to configure automatic hyphenation.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Value determining whether words written in all capital letters are hyphenated. |

### setHyphenationZone(int value) {#setHyphenationZone-int}
```
public void setHyphenationZone(int value)
```


Sets the distance in 1/20 of a point from the right margin within which you do not want to hyphenate words. Default value for this property is 360 (0.25 inch).

 **Examples:** 

Shows how to configure automatic hyphenation.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The distance in 1/20 of a point from the right margin within which you do not want to hyphenate words. |

