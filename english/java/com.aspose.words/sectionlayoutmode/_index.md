---
title: SectionLayoutMode
linktitle: SectionLayoutMode
second_title: Aspose.Words for Java
description: Specifies the layout mode for a section allowing to define the document grid behavior in Java.
type: docs
weight: 605
url: /java/com.aspose.words/sectionlayoutmode/
---

**Inheritance:**
java.lang.Object
```
public class SectionLayoutMode
```

Specifies the layout mode for a section allowing to define the document grid behavior.

 **Examples:** 

Shows how to specify a limit for the number of lines that each page may have.

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

Shows how to specify a for the number of characters that each line may have.

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
## Fields

| Field | Description |
| --- | --- |
| [DEFAULT](#DEFAULT) | Specifies that no document grid shall be applied to the contents of the corresponding section in the document. |
| [GRID](#GRID) | Specifies that the corresponding section shall have both the additional line pitch and character pitch added to each line and character within it in order to maintain a specific number of lines per page and characters per line. |
| [LINE_GRID](#LINE-GRID) | Specifies that the corresponding section shall have additional line pitch added to each line within it in order to maintain the specified number of lines per page. |
| [SNAP_TO_CHARS](#SNAP-TO-CHARS) | Specifies that the corresponding section shall have both the additional line pitch and character pitch added to each line and character within it in order to maintain a specific number of lines per page and characters per line. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String sectionLayoutModeName)](#fromName-java.lang.String) |  |
| [getName(int sectionLayoutMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sectionLayoutMode)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Specifies that no document grid shall be applied to the contents of the corresponding section in the document.

### GRID {#GRID}
```
public static int GRID
```


Specifies that the corresponding section shall have both the additional line pitch and character pitch added to each line and character within it in order to maintain a specific number of lines per page and characters per line. Characters will not be automatically aligned with gridlines on typing.

### LINE_GRID {#LINE-GRID}
```
public static int LINE_GRID
```


Specifies that the corresponding section shall have additional line pitch added to each line within it in order to maintain the specified number of lines per page.

### SNAP_TO_CHARS {#SNAP-TO-CHARS}
```
public static int SNAP_TO_CHARS
```


Specifies that the corresponding section shall have both the additional line pitch and character pitch added to each line and character within it in order to maintain a specific number of lines per page and characters per line. Characters will be automatically aligned with gridlines on typing.

### length {#length}
```
public static int length
```


### fromName(String sectionLayoutModeName) {#fromName-java.lang.String}
```
public static int fromName(String sectionLayoutModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sectionLayoutModeName | java.lang.String |  |

**Returns:**
int
### getName(int sectionLayoutMode) {#getName-int}
```
public static String getName(int sectionLayoutMode)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| sectionLayoutMode | int |  |

**Returns:**
java.lang.String
