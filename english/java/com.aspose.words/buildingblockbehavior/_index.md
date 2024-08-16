---
title: BuildingBlockBehavior
linktitle: BuildingBlockBehavior
second_title: Aspose.Words for Java
description: Specifies the behavior that shall be applied to the contents of the building block when it is inserted into the main document in Java.
type: docs
weight: 50
url: /java/com.aspose.words/buildingblockbehavior/
---

**Inheritance:**
java.lang.Object
```
public class BuildingBlockBehavior
```

Specifies the behavior that shall be applied to the contents of the building block when it is inserted into the main document.

 **Remarks:** 

Corresponds to the **ST\_DocPartBehavior** type in OOXML.

 **Examples:** 

Shows how to add a custom building block to a document.

```

 public void createAndInsert() throws Exception {
     // A document's glossary document stores building blocks.
     Document doc = new Document();
     GlossaryDocument glossaryDoc = new GlossaryDocument();
     doc.setGlossaryDocument(glossaryDoc);

     // Create a building block, name it, and then add it to the glossary document.
     BuildingBlock block = new BuildingBlock(glossaryDoc);
     block.setName("Custom Block");

     glossaryDoc.appendChild(block);

     // All new building block GUIDs have the same zero value by default, and we can give them a new unique value.
     Assert.assertEquals(block.getGuid().toString(), "00000000-0000-0000-0000-000000000000");

     block.setGuid(UUID.randomUUID());

     // The following properties categorize building blocks
     // in the menu we can access in Microsoft Word via "Insert" -> "Quick Parts" -> "Building Blocks Organizer".
     Assert.assertEquals(block.getCategory(), "(Empty Category)");
     Assert.assertEquals(block.getType(), BuildingBlockType.NONE);
     Assert.assertEquals(block.getGallery(), BuildingBlockGallery.ALL);
     Assert.assertEquals(block.getBehavior(), BuildingBlockBehavior.CONTENT);

     // Before we can add this building block to our document, we will need to give it some contents,
     // which we will do using a document visitor. This visitor will also set a category, gallery, and behavior.
     BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
     // Visit start/end of the BuildingBlock.
     block.accept(visitor);

     // We can access the block that we just made from the glossary document.
     BuildingBlock customBlock = glossaryDoc.getBuildingBlock(BuildingBlockGallery.QUICK_PARTS,
             "My custom building blocks", "Custom Block");

     // The block itself is a section that contains the text.
     Assert.assertEquals(MessageFormat.format("Text inside {0}\f", customBlock.getName()), customBlock.getFirstSection().getBody().getFirstParagraph().getText());
     Assert.assertEquals(customBlock.getFirstSection(), customBlock.getLastSection());
     // Now, we can insert it into the document as a new section.
     doc.appendChild(doc.importNode(customBlock.getFirstSection(), true));

     // We can also find it in Microsoft Word's Building Blocks Organizer and place it manually.
     doc.save(getArtifactsDir() + "BuildingBlocks.CreateAndInsert.dotx");
 }

 /// 
 /// Sets up a visited building block to be inserted into the document as a quick part and adds text to its contents.
 /// 
 public static class BuildingBlockVisitor extends DocumentVisitor {
     public BuildingBlockVisitor(final GlossaryDocument ownerGlossaryDoc) {
         mBuilder = new StringBuilder();
         mGlossaryDoc = ownerGlossaryDoc;
     }

     public int visitBuildingBlockStart(final BuildingBlock block) {
         // Configure the building block as a quick part, and add properties used by Building Blocks Organizer.
         block.setBehavior(BuildingBlockBehavior.PARAGRAPH);
         block.setCategory("My custom building blocks");
         block.setDescription("Using this block in the Quick Parts section of word will place its contents at the cursor.");
         block.setGallery(BuildingBlockGallery.QUICK_PARTS);

         // Add a section with text.
         // Inserting the block into the document will append this section with its child nodes at the location.
         Section section = new Section(mGlossaryDoc);
         block.appendChild(section);
         block.getFirstSection().ensureMinimum();

         Run run = new Run(mGlossaryDoc, "Text inside " + block.getName());
         block.getFirstSection().getBody().getFirstParagraph().appendChild(run);

         return VisitorAction.CONTINUE;
     }

     public int visitBuildingBlockEnd(final BuildingBlock block) {
         mBuilder.append("Visited " + block.getName() + "\r\n");
         return VisitorAction.CONTINUE;
     }

     private final StringBuilder mBuilder;
     private final GlossaryDocument mGlossaryDoc;
 }
 
```
## Fields

| Field | Description |
| --- | --- |
| [CONTENT](#CONTENT) | Specifies that the building block shall be inserted as inline content. |
| [DEFAULT](#DEFAULT) | Same as [CONTENT](../../com.aspose.words/buildingblockbehavior/\#CONTENT). |
| [PAGE](#PAGE) | Specifies that the building block shall be added into its own page. |
| [PARAGRAPH](#PARAGRAPH) | Specifies that the building block shall be inserted into its own paragraph. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String buildingBlockBehaviorName)](#fromName-java.lang.String) |  |
| [getName(int buildingBlockBehavior)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int buildingBlockBehavior)](#toString-int) |  |
### CONTENT {#CONTENT}
```
public static int CONTENT
```


Specifies that the building block shall be inserted as inline content.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Same as [CONTENT](../../com.aspose.words/buildingblockbehavior/\#CONTENT).

### PAGE {#PAGE}
```
public static int PAGE
```


Specifies that the building block shall be added into its own page.

### PARAGRAPH {#PARAGRAPH}
```
public static int PARAGRAPH
```


Specifies that the building block shall be inserted into its own paragraph.

### length {#length}
```
public static int length
```


### fromName(String buildingBlockBehaviorName) {#fromName-java.lang.String}
```
public static int fromName(String buildingBlockBehaviorName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| buildingBlockBehaviorName | java.lang.String |  |

**Returns:**
int
### getName(int buildingBlockBehavior) {#getName-int}
```
public static String getName(int buildingBlockBehavior)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| buildingBlockBehavior | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int buildingBlockBehavior) {#toString-int}
```
public static String toString(int buildingBlockBehavior)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| buildingBlockBehavior | int |  |

**Returns:**
java.lang.String
