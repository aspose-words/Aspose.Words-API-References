---
title: WarningType
linktitle: WarningType
second_title: Aspose.Words for Java
description: Specifies the type of a warning that is issued by Aspose.Words during document loading or saving in Java.
type: docs
weight: 677
url: /java/com.aspose.words/warningtype/
---

**Inheritance:**
java.lang.Object
```
public class WarningType
```

Specifies the type of a warning that is issued by Aspose.Words during document loading or saving.

 **Examples:** 

Shows how to set the property for finding the closest match for a missing font from the available font sources.

```

 public void enableFontSubstitution() throws Exception {
     // Open a document that contains text formatted with a font that does not exist in any of our font sources.
     Document doc = new Document(getMyDir() + "Missing font.docx");

     // Assign a callback for handling font substitution warnings.
     HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
     doc.setWarningCallback(substitutionWarningHandler);

     // Set a default font name and enable font substitution.
     FontSettings fontSettings = new FontSettings();
     fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
     fontSettings.getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);

     // Original font metrics should be used after font substitution.
     doc.getLayoutOptions().setKeepOriginalFontMetrics(true);

     // We will get a font substitution warning if we save a document with a missing font.
     doc.setFontSettings(fontSettings);
     doc.save(getArtifactsDir() + "FontSettings.EnableFontSubstitution.pdf");

     Iterator warnings = substitutionWarningHandler.FontWarnings.iterator();

     while (warnings.hasNext())
         System.out.println(warnings.next().getDescription());

     // We can also verify warnings in the collection and clear them.
     Assert.assertEquals(WarningSource.LAYOUT, substitutionWarningHandler.FontWarnings.get(0).getSource());
     Assert.assertEquals("Font '28 Days Later' has not been found. Using 'Calibri' font instead. Reason: alternative name from document.",
             substitutionWarningHandler.FontWarnings.get(0).getDescription());

     substitutionWarningHandler.FontWarnings.clear();

     Assert.assertTrue(substitutionWarningHandler.FontWarnings.getCount() == 0);
 }

 public static class HandleDocumentSubstitutionWarnings implements IWarningCallback {
     /// 
     /// Called every time a warning occurs during loading/saving.
     /// 
     public void warning(WarningInfo info) {
         if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
             FontWarnings.warning(info);
     }

     public WarningInfoCollection FontWarnings = new WarningInfoCollection();
 }
 
```
## Fields

| Field | Description |
| --- | --- |
| [DATA_LOSS](#DATA-LOSS) | Generic data loss, no specific code. |
| [DATA_LOSS_CATEGORY](#DATA-LOSS-CATEGORY) | Some text/char/image or other data will be missing from either the document tree following load, or from the created document following save. |
| [FONT_EMBEDDING](#FONT-EMBEDDING) | Loss of embedded font information during document saving. |
| [FONT_SUBSTITUTION](#FONT-SUBSTITUTION) | Font has been substituted. |
| [HINT](#HINT) | Advises of a potential problem or suggests an improvement. |
| [MAJOR_FORMATTING_LOSS](#MAJOR-FORMATTING-LOSS) | Generic major formatting loss, no specific code. |
| [MAJOR_FORMATTING_LOSS_CATEGORY](#MAJOR-FORMATTING-LOSS-CATEGORY) | The resulting document or a particular location in it might look substantially different compared to the original document. |
| [MINOR_FORMATTING_LOSS](#MINOR-FORMATTING-LOSS) | Generic minor formatting loss, no specific code. |
| [MINOR_FORMATTING_LOSS_CATEGORY](#MINOR-FORMATTING-LOSS-CATEGORY) | The resulting document or a particular location in it might look somewhat different compared to the original document. |
| [UNEXPECTED_CONTENT](#UNEXPECTED-CONTENT) | Generic unexpected content, no specific code. |
| [UNEXPECTED_CONTENT_CATEGORY](#UNEXPECTED-CONTENT-CATEGORY) | Some content in the source document could not be recognized (i.e. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String warningTypeName)](#fromName-java.lang.String) |  |
| [fromNames(Set warningTypeNames)](#fromNames-java.util.Set) |  |
| [getName(int warningType)](#getName-int) |  |
| [getNames(int warningType)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int warningType)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### DATA_LOSS {#DATA-LOSS}
```
public static int DATA_LOSS
```


Generic data loss, no specific code.

### DATA_LOSS_CATEGORY {#DATA-LOSS-CATEGORY}
```
public static int DATA_LOSS_CATEGORY
```


Some text/char/image or other data will be missing from either the document tree following load, or from the created document following save.

### FONT_EMBEDDING {#FONT-EMBEDDING}
```
public static int FONT_EMBEDDING
```


Loss of embedded font information during document saving.

### FONT_SUBSTITUTION {#FONT-SUBSTITUTION}
```
public static int FONT_SUBSTITUTION
```


Font has been substituted.

### HINT {#HINT}
```
public static int HINT
```


Advises of a potential problem or suggests an improvement.

### MAJOR_FORMATTING_LOSS {#MAJOR-FORMATTING-LOSS}
```
public static int MAJOR_FORMATTING_LOSS
```


Generic major formatting loss, no specific code.

### MAJOR_FORMATTING_LOSS_CATEGORY {#MAJOR-FORMATTING-LOSS-CATEGORY}
```
public static int MAJOR_FORMATTING_LOSS_CATEGORY
```


The resulting document or a particular location in it might look substantially different compared to the original document.

### MINOR_FORMATTING_LOSS {#MINOR-FORMATTING-LOSS}
```
public static int MINOR_FORMATTING_LOSS
```


Generic minor formatting loss, no specific code.

### MINOR_FORMATTING_LOSS_CATEGORY {#MINOR-FORMATTING-LOSS-CATEGORY}
```
public static int MINOR_FORMATTING_LOSS_CATEGORY
```


The resulting document or a particular location in it might look somewhat different compared to the original document.

### UNEXPECTED_CONTENT {#UNEXPECTED-CONTENT}
```
public static int UNEXPECTED_CONTENT
```


Generic unexpected content, no specific code.

### UNEXPECTED_CONTENT_CATEGORY {#UNEXPECTED-CONTENT-CATEGORY}
```
public static int UNEXPECTED_CONTENT_CATEGORY
```


Some content in the source document could not be recognized (i.e. is unsupported), this may or may not cause issues or result in data/formatting loss.

### length {#length}
```
public static int length
```


### fromName(String warningTypeName) {#fromName-java.lang.String}
```
public static int fromName(String warningTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| warningTypeName | java.lang.String |  |

**Returns:**
int
### fromNames(Set warningTypeNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set warningTypeNames)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| warningTypeNames | java.util.Set |  |

**Returns:**
int
### getName(int warningType) {#getName-int}
```
public static String getName(int warningType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.lang.String
### getNames(int warningType) {#getNames-int}
```
public static Set getNames(int warningType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int warningType) {#toString-int}
```
public static String toString(int warningType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
