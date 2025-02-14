---
title: BuildingBlockGallery
linktitle: BuildingBlockGallery
second_title: Aspose.Words for Java
description: Specifies the predefined gallery into which a building block is classified in Java.
type: docs
weight: 55
url: /java/com.aspose.words/buildingblockgallery/
---

**Inheritance:**
java.lang.Object
```
public class BuildingBlockGallery
```

Specifies the predefined gallery into which a building block is classified.

 **Remarks:** 

Corresponds to the **ST\_DocPartGallery** type in OOXML.

 **Examples:** 

Shows ways of accessing building blocks in a glossary document.

```

 public void glossaryDocument() throws Exception {
     Document doc = new Document();
     GlossaryDocument glossaryDoc = new GlossaryDocument();

     glossaryDoc.appendChild(createNewBuildingBlock(glossaryDoc, "Block 1"));
     glossaryDoc.appendChild(createNewBuildingBlock(glossaryDoc, "Block 2"));
     glossaryDoc.appendChild(createNewBuildingBlock(glossaryDoc, "Block 3"));
     glossaryDoc.appendChild(createNewBuildingBlock(glossaryDoc, "Block 4"));
     glossaryDoc.appendChild(createNewBuildingBlock(glossaryDoc, "Block 5"));

     Assert.assertEquals(glossaryDoc.getBuildingBlocks().getCount(), 5);

     doc.setGlossaryDocument(glossaryDoc);

     // There are various ways of accessing building blocks.
     // 1 -  Get the first/last building blocks in the collection:
     Assert.assertEquals("Block 1", glossaryDoc.getFirstBuildingBlock().getName());
     Assert.assertEquals("Block 5", glossaryDoc.getLastBuildingBlock().getName());

     // 2 -  Get a building block by index:
     Assert.assertEquals("Block 2", glossaryDoc.getBuildingBlocks().get(1).getName());
     Assert.assertEquals("Block 3", glossaryDoc.getBuildingBlocks().toArray()[2].getName());

     // 3 -  Get the first building block that matches a gallery, name and category:
     Assert.assertEquals("Block 4",
             glossaryDoc.getBuildingBlock(BuildingBlockGallery.ALL, "(Empty Category)", "Block 4").getName());

     // We will do that using a custom visitor,
     // which will give every BuildingBlock in the GlossaryDocument a unique GUID
     GlossaryDocVisitor visitor = new GlossaryDocVisitor();
     // Visit start/end of the Glossary document.
     glossaryDoc.accept(visitor);
     // Visit only start of the Glossary document.
     glossaryDoc.acceptStart(visitor);
     // Visit only end of the Glossary document.
     glossaryDoc.acceptEnd(visitor);
     System.out.println(visitor.getText());

     // In Microsoft Word, we can access the building blocks via "Insert" -> "Quick Parts" -> "Building Blocks Organizer".
     doc.save(getArtifactsDir() + "BuildingBlocks.GlossaryDocument.dotx");
 }

 public static BuildingBlock createNewBuildingBlock(final GlossaryDocument glossaryDoc, final String buildingBlockName) {
     BuildingBlock buildingBlock = new BuildingBlock(glossaryDoc);
     buildingBlock.setName(buildingBlockName);

     return buildingBlock;
 }

 /// 
 /// Gives each building block in a visited glossary document a unique GUID.
 /// Stores the GUID-building block pairs in a dictionary.
 /// 
 public static class GlossaryDocVisitor extends DocumentVisitor {
     public GlossaryDocVisitor() {
         mBlocksByGuid = new HashMap<>();
         mBuilder = new StringBuilder();
     }

     public String getText() {
         return mBuilder.toString();
     }

     public HashMap getDictionary() {
         return mBlocksByGuid;
     }

     public int visitGlossaryDocumentStart(final GlossaryDocument glossary) {
         mBuilder.append("Glossary document found!\n");
         return VisitorAction.CONTINUE;
     }

     public int visitGlossaryDocumentEnd(final GlossaryDocument glossary) {
         mBuilder.append("Reached end of glossary!\n");
         mBuilder.append("BuildingBlocks found: " + mBlocksByGuid.size() + "\r\n");
         return VisitorAction.CONTINUE;
     }

     public int visitBuildingBlockStart(final BuildingBlock block) {
         block.setGuid(UUID.randomUUID());
         mBlocksByGuid.put(block.getGuid(), block);
         return VisitorAction.CONTINUE;
     }

     public int visitBuildingBlockEnd(final BuildingBlock block) {
         mBuilder.append("\tVisited block \"" + block.getName() + "\"" + "\r\n");
         mBuilder.append("\t Type: " + block.getType() + "\r\n");
         mBuilder.append("\t Gallery: " + block.getGallery() + "\r\n");
         mBuilder.append("\t Behavior: " + block.getBehavior() + "\r\n");
         mBuilder.append("\t Description: " + block.getDescription() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     private final HashMap mBlocksByGuid;
     private final StringBuilder mBuilder;
 }
 
```
## Fields

| Field | Description |
| --- | --- |
| [ALL](#ALL) | Specifies that this glossary document entry shall be associated with all possible gallery classification values. |
| [AUTO_TEXT](#AUTO-TEXT) |  |
| [BIBLIOGRAPHY](#BIBLIOGRAPHY) |  |
| [COVER_PAGE](#COVER-PAGE) |  |
| [CUSTOM_1](#CUSTOM-1) |  |
| [CUSTOM_2](#CUSTOM-2) |  |
| [CUSTOM_3](#CUSTOM-3) |  |
| [CUSTOM_4](#CUSTOM-4) |  |
| [CUSTOM_5](#CUSTOM-5) |  |
| [CUSTOM_AUTO_TEXT](#CUSTOM-AUTO-TEXT) |  |
| [CUSTOM_BIBLIOGRAPHY](#CUSTOM-BIBLIOGRAPHY) |  |
| [CUSTOM_COVER_PAGE](#CUSTOM-COVER-PAGE) |  |
| [CUSTOM_EQUATIONS](#CUSTOM-EQUATIONS) |  |
| [CUSTOM_FOOTERS](#CUSTOM-FOOTERS) |  |
| [CUSTOM_HEADERS](#CUSTOM-HEADERS) |  |
| [CUSTOM_PAGE_NUMBER](#CUSTOM-PAGE-NUMBER) |  |
| [CUSTOM_PAGE_NUMBER_AT_BOTTOM](#CUSTOM-PAGE-NUMBER-AT-BOTTOM) |  |
| [CUSTOM_PAGE_NUMBER_AT_MARGIN](#CUSTOM-PAGE-NUMBER-AT-MARGIN) |  |
| [CUSTOM_PAGE_NUMBER_AT_TOP](#CUSTOM-PAGE-NUMBER-AT-TOP) |  |
| [CUSTOM_QUICK_PARTS](#CUSTOM-QUICK-PARTS) |  |
| [CUSTOM_TABLES](#CUSTOM-TABLES) |  |
| [CUSTOM_TABLE_OF_CONTENTS](#CUSTOM-TABLE-OF-CONTENTS) |  |
| [CUSTOM_TEXT_BOX](#CUSTOM-TEXT-BOX) |  |
| [CUSTOM_WATERMARKS](#CUSTOM-WATERMARKS) |  |
| [DEFAULT](#DEFAULT) | Same as [ALL](../../com.aspose.words/buildingblockgallery/\#ALL). |
| [EQUATIONS](#EQUATIONS) |  |
| [FOOTERS](#FOOTERS) |  |
| [HEADERS](#HEADERS) |  |
| [NO_GALLERY](#NO-GALLERY) |  |
| [PAGE_NUMBER](#PAGE-NUMBER) |  |
| [PAGE_NUMBER_AT_BOTTOM](#PAGE-NUMBER-AT-BOTTOM) |  |
| [PAGE_NUMBER_AT_MARGIN](#PAGE-NUMBER-AT-MARGIN) |  |
| [PAGE_NUMBER_AT_TOP](#PAGE-NUMBER-AT-TOP) |  |
| [QUICK_PARTS](#QUICK-PARTS) |  |
| [STRUCTURED_DOCUMENT_TAG_PLACEHOLDER_TEXT](#STRUCTURED-DOCUMENT-TAG-PLACEHOLDER-TEXT) |  |
| [TABLES](#TABLES) |  |
| [TABLE_OF_CONTENTS](#TABLE-OF-CONTENTS) |  |
| [TEXT_BOX](#TEXT-BOX) |  |
| [WATERMARKS](#WATERMARKS) |  |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String buildingBlockGalleryName)](#fromName-java.lang.String) |  |
| [getName(int buildingBlockGallery)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int buildingBlockGallery)](#toString-int) |  |
### ALL {#ALL}
```
public static int ALL
```


Specifies that this glossary document entry shall be associated with all possible gallery classification values.

### AUTO_TEXT {#AUTO-TEXT}
```
public static int AUTO_TEXT
```




### BIBLIOGRAPHY {#BIBLIOGRAPHY}
```
public static int BIBLIOGRAPHY
```




### COVER_PAGE {#COVER-PAGE}
```
public static int COVER_PAGE
```




### CUSTOM_1 {#CUSTOM-1}
```
public static int CUSTOM_1
```




### CUSTOM_2 {#CUSTOM-2}
```
public static int CUSTOM_2
```




### CUSTOM_3 {#CUSTOM-3}
```
public static int CUSTOM_3
```




### CUSTOM_4 {#CUSTOM-4}
```
public static int CUSTOM_4
```




### CUSTOM_5 {#CUSTOM-5}
```
public static int CUSTOM_5
```




### CUSTOM_AUTO_TEXT {#CUSTOM-AUTO-TEXT}
```
public static int CUSTOM_AUTO_TEXT
```




### CUSTOM_BIBLIOGRAPHY {#CUSTOM-BIBLIOGRAPHY}
```
public static int CUSTOM_BIBLIOGRAPHY
```




### CUSTOM_COVER_PAGE {#CUSTOM-COVER-PAGE}
```
public static int CUSTOM_COVER_PAGE
```




### CUSTOM_EQUATIONS {#CUSTOM-EQUATIONS}
```
public static int CUSTOM_EQUATIONS
```




### CUSTOM_FOOTERS {#CUSTOM-FOOTERS}
```
public static int CUSTOM_FOOTERS
```




### CUSTOM_HEADERS {#CUSTOM-HEADERS}
```
public static int CUSTOM_HEADERS
```




### CUSTOM_PAGE_NUMBER {#CUSTOM-PAGE-NUMBER}
```
public static int CUSTOM_PAGE_NUMBER
```




### CUSTOM_PAGE_NUMBER_AT_BOTTOM {#CUSTOM-PAGE-NUMBER-AT-BOTTOM}
```
public static int CUSTOM_PAGE_NUMBER_AT_BOTTOM
```




### CUSTOM_PAGE_NUMBER_AT_MARGIN {#CUSTOM-PAGE-NUMBER-AT-MARGIN}
```
public static int CUSTOM_PAGE_NUMBER_AT_MARGIN
```




### CUSTOM_PAGE_NUMBER_AT_TOP {#CUSTOM-PAGE-NUMBER-AT-TOP}
```
public static int CUSTOM_PAGE_NUMBER_AT_TOP
```




### CUSTOM_QUICK_PARTS {#CUSTOM-QUICK-PARTS}
```
public static int CUSTOM_QUICK_PARTS
```




### CUSTOM_TABLES {#CUSTOM-TABLES}
```
public static int CUSTOM_TABLES
```




### CUSTOM_TABLE_OF_CONTENTS {#CUSTOM-TABLE-OF-CONTENTS}
```
public static int CUSTOM_TABLE_OF_CONTENTS
```




### CUSTOM_TEXT_BOX {#CUSTOM-TEXT-BOX}
```
public static int CUSTOM_TEXT_BOX
```




### CUSTOM_WATERMARKS {#CUSTOM-WATERMARKS}
```
public static int CUSTOM_WATERMARKS
```




### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Same as [ALL](../../com.aspose.words/buildingblockgallery/\#ALL).

### EQUATIONS {#EQUATIONS}
```
public static int EQUATIONS
```




### FOOTERS {#FOOTERS}
```
public static int FOOTERS
```




### HEADERS {#HEADERS}
```
public static int HEADERS
```




### NO_GALLERY {#NO-GALLERY}
```
public static int NO_GALLERY
```




### PAGE_NUMBER {#PAGE-NUMBER}
```
public static int PAGE_NUMBER
```




### PAGE_NUMBER_AT_BOTTOM {#PAGE-NUMBER-AT-BOTTOM}
```
public static int PAGE_NUMBER_AT_BOTTOM
```




### PAGE_NUMBER_AT_MARGIN {#PAGE-NUMBER-AT-MARGIN}
```
public static int PAGE_NUMBER_AT_MARGIN
```




### PAGE_NUMBER_AT_TOP {#PAGE-NUMBER-AT-TOP}
```
public static int PAGE_NUMBER_AT_TOP
```




### QUICK_PARTS {#QUICK-PARTS}
```
public static int QUICK_PARTS
```




### STRUCTURED_DOCUMENT_TAG_PLACEHOLDER_TEXT {#STRUCTURED-DOCUMENT-TAG-PLACEHOLDER-TEXT}
```
public static int STRUCTURED_DOCUMENT_TAG_PLACEHOLDER_TEXT
```




### TABLES {#TABLES}
```
public static int TABLES
```




### TABLE_OF_CONTENTS {#TABLE-OF-CONTENTS}
```
public static int TABLE_OF_CONTENTS
```




### TEXT_BOX {#TEXT-BOX}
```
public static int TEXT_BOX
```




### WATERMARKS {#WATERMARKS}
```
public static int WATERMARKS
```




### length {#length}
```
public static int length
```


### fromName(String buildingBlockGalleryName) {#fromName-java.lang.String}
```
public static int fromName(String buildingBlockGalleryName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| buildingBlockGalleryName | java.lang.String |  |

**Returns:**
int
### getName(int buildingBlockGallery) {#getName-int}
```
public static String getName(int buildingBlockGallery)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| buildingBlockGallery | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int buildingBlockGallery) {#toString-int}
```
public static String toString(int buildingBlockGallery)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| buildingBlockGallery | int |  |

**Returns:**
java.lang.String
