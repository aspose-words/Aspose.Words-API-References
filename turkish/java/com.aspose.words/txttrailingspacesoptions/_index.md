---
title: "TxtTrailingSpacesOptions"
linktitle: "TxtTrailingSpacesOptions"
second_title: "Aspose.Words Java için"
description: "Java'da LoadFormat.TEXT dosyasından içe aktarırken sondaki boşlukların işlenmesi için mevcut seçenekleri belirtir."
type: docs
weight: 697
url: /tr/java/com.aspose.words/txttrailingspacesoptions/
---

**Inheritance:**
java.lang.Object
```
public class TxtTrailingSpacesOptions
```

İçe aktarma sırasında [LoadFormat.TEXT](../../com.aspose.words/loadformat/\#TEXT) dosyasındaki sondaki boşlukların işlenmesi için kullanılabilir seçenekleri belirtir.

 **Examples:** 

Düz metin belgeleri yüklenirken boşlukların nasıl kırpılacağını gösterir.

```

 String textDoc = "      Line 1 \n" +
         "    Line 2   \n" +
         " Line 3       ";

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Preserve"
 // to preserve all whitespace characters at the start of every line.
 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.ConvertToIndent"
 // to remove all whitespace characters from the start of every line,
 // and then apply a left first line indent to the paragraph to simulate the effect of the whitespaces.
 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Trim"
 // to remove all whitespace characters from every line's start.
 loadOptions.setLeadingSpacesOptions(txtLeadingSpacesOptions);

 // Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Preserve"
 // to preserve all whitespace characters at the end of every line.
 // Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Trim" to
 // remove all whitespace characters from the end of every line.
 loadOptions.setTrailingSpacesOptions(txtTrailingSpacesOptions);

 Document doc = new Document(new ByteArrayInputStream(textDoc.getBytes()), loadOptions);
 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 switch (txtLeadingSpacesOptions) {
     case TxtLeadingSpacesOptions.CONVERT_TO_INDENT:
         Assert.assertEquals(37.8d, paragraphs.get(0).getParagraphFormat().getFirstLineIndent());
         Assert.assertEquals(25.2d, paragraphs.get(1).getParagraphFormat().getFirstLineIndent());
         Assert.assertEquals(6.3d, paragraphs.get(2).getParagraphFormat().getFirstLineIndent());

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith("Line 3"));
         break;
     case TxtLeadingSpacesOptions.PRESERVE:
         Assert.assertTrue(IterableUtils.matchesAll(paragraphs, s -> s.getParagraphFormat().getFirstLineIndent() == 0.0d));

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("      Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("    Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith(" Line 3"));
         break;
     case TxtLeadingSpacesOptions.TRIM:
         Assert.assertTrue(IterableUtils.matchesAll(paragraphs, s -> s.getParagraphFormat().getFirstLineIndent() == 0.0d));

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith("Line 3"));
         break;
 }

 switch (txtTrailingSpacesOptions) {
     case TxtTrailingSpacesOptions.PRESERVE:
         Assert.assertTrue(paragraphs.get(0).getText().endsWith("Line 1 \r"));
         Assert.assertTrue(paragraphs.get(1).getText().endsWith("Line 2   \r"));
         Assert.assertTrue(paragraphs.get(2).getText().endsWith("Line 3       \f"));
         break;
     case TxtTrailingSpacesOptions.TRIM:
         Assert.assertTrue(paragraphs.get(0).getText().endsWith("Line 1\r"));
         Assert.assertTrue(paragraphs.get(1).getText().endsWith("Line 2\r"));
         Assert.assertTrue(paragraphs.get(2).getText().endsWith("Line 3\f"));
         break;
 }
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [PRESERVE](#PRESERVE) | Sondaki boşluklar korunur. |
| [TRIM](#TRIM) | Sondaki boşluklar kırpılır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String txtTrailingSpacesOptionsName)](#fromName-java.lang.String) |  |
| [getName(int txtTrailingSpacesOptions)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int txtTrailingSpacesOptions)](#toString-int) |  |
### PRESERVE {#PRESERVE}
```
public static int PRESERVE
```


Sondaki boşluklar korunur.

### TRIM {#TRIM}
```
public static int TRIM
```


Sondaki boşluklar kırpılır.

### length {#length}
```
public static int length
```


### fromName(String txtTrailingSpacesOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String txtTrailingSpacesOptionsName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| txtTrailingSpacesOptionsName | java.lang.String |  |

**Returns:**
int
### getName(int txtTrailingSpacesOptions) {#getName-int}
```
public static String getName(int txtTrailingSpacesOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| txtTrailingSpacesOptions | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int txtTrailingSpacesOptions) {#toString-int}
```
public static String toString(int txtTrailingSpacesOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| txtTrailingSpacesOptions | int |  |

**Returns:**
java.lang.String
