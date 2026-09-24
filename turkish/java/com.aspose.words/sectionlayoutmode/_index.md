---
title: "SectionLayoutMode"
linktitle: "SectionLayoutMode"
second_title: "Aspose.Words Java için"
description: "Bir bölüm için düzen modunu belirler ve Java'da belge ızgara davranışını tanımlamaya olanak tanır."
type: docs
weight: 607
url: /tr/java/com.aspose.words/sectionlayoutmode/
---

**Inheritance:**
java.lang.Object
```
public class SectionLayoutMode
```

Bir bölüm için belge ızgara davranışını tanımlamaya izin veren yerleşim modunu belirtir.

 **Examples:** 

Her satırın sahip olabileceği karakter sayısı için bir sınır nasıl belirtileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of characters per line in this section.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.GRID);
 builder.getPageSetup().setCharactersPerLine(10);

 // The number of characters also depends on the size of the font.
 doc.getStyles().get("Normal").getFont().setSize(20.0);

 Assert.assertEquals(8, doc.getFirstSection().getPageSetup().getCharactersPerLine());

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "PageSetup.CharactersPerLine.docx");
 
```

Her sayfanın sahip olabileceği satır sayısı için bir sınırın nasıl belirtileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [DEFAULT](#DEFAULT) | Belgedeki ilgili bölümün içeriğine hiçbir belge ızgarasının uygulanmayacağını belirtir. |
| [GRID](#GRID) | İlgili bölümün, sayfa başına belirli bir satır sayısı ve satır başına karakter sayısını korumak için her satır ve karakterine ek satır aralığı ve karakter aralığı ekleyeceğini belirtir. |
| [LINE_GRID](#LINE-GRID) | İlgili bölümün, sayfa başına belirtilen satır sayısını korumak için her satırına ek satır aralığı ekleyeceğini belirtir. |
| [SNAP_TO_CHARS](#SNAP-TO-CHARS) | İlgili bölümün, sayfa başına belirli bir satır sayısı ve satır başına karakter sayısını korumak için her satır ve karakterine ek satır aralığı ve karakter aralığı ekleyeceğini belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String sectionLayoutModeName)](#fromName-java.lang.String) |  |
| [getName(int sectionLayoutMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sectionLayoutMode)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Belgedeki ilgili bölümün içeriğine hiçbir belge ızgarasının uygulanmayacağını belirtir.

### GRID {#GRID}
```
public static int GRID
```


İlgili bölümün, sayfa başına belirli bir satır sayısı ve satır başına karakter sayısını korumak için her satır ve karakterine ek satır aralığı ve karakter aralığı ekleyeceğini belirtir. Karakterler, yazarken ızgara çizgilerine otomatik olarak hizalanmayacaktır.

### LINE_GRID {#LINE-GRID}
```
public static int LINE_GRID
```


İlgili bölümün, sayfa başına belirtilen satır sayısını korumak için her satırına ek satır aralığı ekleyeceğini belirtir.

### SNAP_TO_CHARS {#SNAP-TO-CHARS}
```
public static int SNAP_TO_CHARS
```


İlgili bölümün, sayfa başına belirli bir satır sayısı ve satır başına karakter sayısını korumak için her satır ve karakterine ek satır aralığı ve karakter aralığı ekleyeceğini belirtir. Karakterler, yazarken ızgara çizgilerine otomatik olarak hizalanacaktır.

### length {#length}
```
public static int length
```


### fromName(String sectionLayoutModeName) {#fromName-java.lang.String}
```
public static int fromName(String sectionLayoutModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sectionLayoutModeName | java.lang.String |  |

**Returns:**
int
### getName(int sectionLayoutMode) {#getName-int}
```
public static String getName(int sectionLayoutMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sectionLayoutMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int sectionLayoutMode) {#toString-int}
```
public static String toString(int sectionLayoutMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sectionLayoutMode | int |  |

**Returns:**
java.lang.String
