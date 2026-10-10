---
title: "BuildingBlockType"
linktitle: "BuildingBlockType"
second_title: "Aspose.Words für Java"
description: "Gibt einen Building‑Block‑Typ in Java an."
type: docs
weight: 56
url: /de/java/com.aspose.words/buildingblocktype/
---

**Inheritance:**
java.lang.Object
```
public class BuildingBlockType
```

Gibt einen Bausteintyp an. Der Typ kann die Sichtbarkeit und das Verhalten des Bausteins in Microsoft Word beeinflussen.

 **Remarks:** 

Entspricht dem Typ **ST\_DocPartType** in OOXML.

 **Examples:** 

Zeigt, wie ein benutzerdefinierter Baustein zu einem Dokument hinzugefügt wird.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [ALL](#ALL) | Der Baustein ist mit allen Typen verknüpft. |
| [AUTOMATICALLY_REPLACE_NAME_WITH_CONTENT](#AUTOMATICALLY-REPLACE-NAME-WITH-CONTENT) | Ermöglicht, dass der Baustein automatisch in das Dokument eingefügt wird, sobald sein Name in einer Anwendung eingegeben wird. |
| [AUTO_CORRECT](#AUTO-CORRECT) | Der Baustein ist mit den Rechtschreib- und Grammatikwerkzeugen verknüpft. |
| [AUTO_TEXT](#AUTO-TEXT) | Der Baustein ist ein AutoText-Eintrag. |
| [DEFAULT](#DEFAULT) | Speichern als [NONE](../../com.aspose.words/buildingblocktype/\#NONE). |
| [FORM_FIELD_HELP_TEXT](#FORM-FIELD-HELP-TEXT) | Der Baustein ist ein Hilfetext für ein Formularfeld. |
| [NONE](#NONE) | Für den Baustein ist keine Typinformation angegeben. |
| [NORMAL](#NORMAL) | Der Baustein ist ein normaler (d.h. |
| [STRUCTURED_DOCUMENT_TAG_PLACEHOLDER_TEXT](#STRUCTURED-DOCUMENT-TAG-PLACEHOLDER-TEXT) | Der Baustein ist ein Platzhaltertext für ein strukturiertes Dokument-Tag. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String buildingBlockTypeName)](#fromName-java.lang.String) |  |
| [getName(int buildingBlockType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int buildingBlockType)](#toString-int) |  |
### ALL {#ALL}
```
public static int ALL
```


Der Baustein ist mit allen Typen verknüpft.

### AUTOMATICALLY_REPLACE_NAME_WITH_CONTENT {#AUTOMATICALLY-REPLACE-NAME-WITH-CONTENT}
```
public static int AUTOMATICALLY_REPLACE_NAME_WITH_CONTENT
```


Ermöglicht, dass der Baustein automatisch in das Dokument eingefügt wird, sobald sein Name in einer Anwendung eingegeben wird.

### AUTO_CORRECT {#AUTO-CORRECT}
```
public static int AUTO_CORRECT
```


Der Baustein ist mit den Rechtschreib- und Grammatikwerkzeugen verknüpft.

### AUTO_TEXT {#AUTO-TEXT}
```
public static int AUTO_TEXT
```


Der Baustein ist ein AutoText-Eintrag.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Speichern als [NONE](../../com.aspose.words/buildingblocktype/\#NONE).

### FORM_FIELD_HELP_TEXT {#FORM-FIELD-HELP-TEXT}
```
public static int FORM_FIELD_HELP_TEXT
```


Der Baustein ist ein Hilfetext für ein Formularfeld.

### NONE {#NONE}
```
public static int NONE
```


Für den Baustein ist keine Typinformation angegeben.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Der Baustein ist ein normaler (d.h. regulärer) Glossareintrags-Dokument.

### STRUCTURED_DOCUMENT_TAG_PLACEHOLDER_TEXT {#STRUCTURED-DOCUMENT-TAG-PLACEHOLDER-TEXT}
```
public static int STRUCTURED_DOCUMENT_TAG_PLACEHOLDER_TEXT
```


Der Baustein ist ein Platzhaltertext für ein strukturiertes Dokument-Tag.

### length {#length}
```
public static int length
```


### fromName(String buildingBlockTypeName) {#fromName-java.lang.String}
```
public static int fromName(String buildingBlockTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| buildingBlockTypeName | java.lang.String |  |

**Returns:**
int
### getName(int buildingBlockType) {#getName-int}
```
public static String getName(int buildingBlockType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| buildingBlockType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int buildingBlockType) {#toString-int}
```
public static String toString(int buildingBlockType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| buildingBlockType | int |  |

**Returns:**
java.lang.String
