---
title: "BuildingBlockType"
linktitle: "BuildingBlockType"
second_title: "Aspose.Words per Java"
description: "Specifica un tipo di blocco di costruzione in Java."
type: docs
weight: 56
url: /it/java/com.aspose.words/buildingblocktype/
---

**Inheritance:**
java.lang.Object
```
public class BuildingBlockType
```

Specifica un tipo di blocco di costruzione. Il tipo potrebbe influire sulla visibilità e sul comportamento del blocco di costruzione in Microsoft Word.

 **Remarks:** 

Corrisponde al tipo **ST\_DocPartType** in OOXML.

 **Examples:** 

Mostra come aggiungere un blocco di costruzione personalizzato a un documento.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [ALL](#ALL) | Il blocco di costruzione è associato a tutti i tipi. |
| [AUTOMATICALLY_REPLACE_NAME_WITH_CONTENT](#AUTOMATICALLY-REPLACE-NAME-WITH-CONTENT) | Consente al blocco di costruzione di essere inserito automaticamente nel documento ogni volta che il suo nome viene inserito in un'applicazione. |
| [AUTO_CORRECT](#AUTO-CORRECT) | Il blocco di costruzione è associato agli strumenti di ortografia e grammatica. |
| [AUTO_TEXT](#AUTO-TEXT) | Il blocco di costruzione è una voce AutoText. |
| [DEFAULT](#DEFAULT) | Salva come [NONE](../../com.aspose.words/buildingblocktype/\#NONE). |
| [FORM_FIELD_HELP_TEXT](#FORM-FIELD-HELP-TEXT) | Il blocco di costruzione è un testo di aiuto per il campo modulo. |
| [NONE](#NONE) | Non è specificata alcuna informazione sul tipo per il blocco di costruzione. |
| [NORMAL](#NORMAL) | Il blocco di costruzione è normale (ad esempio |
| [STRUCTURED_DOCUMENT_TAG_PLACEHOLDER_TEXT](#STRUCTURED-DOCUMENT-TAG-PLACEHOLDER-TEXT) | Il blocco di costruzione è un testo segnaposto per un tag di documento strutturato. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String buildingBlockTypeName)](#fromName-java.lang.String) |  |
| [getName(int buildingBlockType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int buildingBlockType)](#toString-int) |  |
### ALL {#ALL}
```
public static int ALL
```


Il blocco di costruzione è associato a tutti i tipi.

### AUTOMATICALLY_REPLACE_NAME_WITH_CONTENT {#AUTOMATICALLY-REPLACE-NAME-WITH-CONTENT}
```
public static int AUTOMATICALLY_REPLACE_NAME_WITH_CONTENT
```


Consente al blocco di costruzione di essere inserito automaticamente nel documento ogni volta che il suo nome viene inserito in un'applicazione.

### AUTO_CORRECT {#AUTO-CORRECT}
```
public static int AUTO_CORRECT
```


Il blocco di costruzione è associato agli strumenti di ortografia e grammatica.

### AUTO_TEXT {#AUTO-TEXT}
```
public static int AUTO_TEXT
```


Il blocco di costruzione è una voce AutoText.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Salva come [NONE](../../com.aspose.words/buildingblocktype/\#NONE).

### FORM_FIELD_HELP_TEXT {#FORM-FIELD-HELP-TEXT}
```
public static int FORM_FIELD_HELP_TEXT
```


Il blocco di costruzione è un testo di aiuto per il campo modulo.

### NONE {#NONE}
```
public static int NONE
```


Non è specificata alcuna informazione sul tipo per il blocco di costruzione.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Il blocco di costruzione è una voce di documento glossario normale (cioè regolare).

### STRUCTURED_DOCUMENT_TAG_PLACEHOLDER_TEXT {#STRUCTURED-DOCUMENT-TAG-PLACEHOLDER-TEXT}
```
public static int STRUCTURED_DOCUMENT_TAG_PLACEHOLDER_TEXT
```


Il blocco di costruzione è un testo segnaposto per un tag di documento strutturato.

### length {#length}
```
public static int length
```


### fromName(String buildingBlockTypeName) {#fromName-java.lang.String}
```
public static int fromName(String buildingBlockTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| buildingBlockTypeName | java.lang.String |  |

**Returns:**
int
### getName(int buildingBlockType) {#getName-int}
```
public static String getName(int buildingBlockType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| buildingBlockType | int |  |

**Returns:**
java.lang.String
