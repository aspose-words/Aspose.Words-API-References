---
title: "IStructuredDocumentTag"
linktitle: "IStructuredDocumentTag"
second_title: "Aspose.Words pour Java"
description: "Interface permettant de définir des données communes pour StructuredDocumentTag et StructuredDocumentTagRangeStart en Java."
type: docs
weight: 785
url: /fr/java/com.aspose.words/istructureddocumenttag/
---
```
public interface IStructuredDocumentTag
```

Interface permettant de définir des données communes pour [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) et [StructuredDocumentTagRangeStart](../../com.aspose.words/structureddocumenttagrangestart/).

 **Examples:** 

Montre comment supprimer la balise de document structuré, tout en conservant le contenu à l'intérieur.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");

 // This collection provides a unified interface for accessing ranged and non-ranged structured tags.
 StructuredDocumentTagCollection sdts = doc.getRange().getStructuredDocumentTags();
 Assert.assertEquals(5, sdts.getCount());

 // Here we can get child nodes from the common interface of ranged and non-ranged structured tags.
 for (IStructuredDocumentTag sdt : sdts)
     if (sdt.getChildNodes(NodeType.ANY, false).getCount() > 0)
         sdt.removeSelfOnly();

 sdts = doc.getRange().getStructuredDocumentTags();
 Assert.assertEquals(0, sdts.getCount());
 
```
## Méthodes

| Méthode | Description |
| --- | --- |
| [getAppearance()](#getAppearance) | Obtient l'apparence de la balise de document structuré. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean) |  |
| [getColor()](#getColor) | Obtient la couleur de la balise de document structuré. |
| [getId()](#getId) | Spécifie un identifiant numérique persistant en lecture seule unique pour ce **SDT**. |
| [getLevel()](#getLevel) | Obtient le niveau auquel ce **SDT** apparaît dans l'arborescence du document. |
| [getLockContentControl()](#getLockContentControl) | Lorsqu'elle est définie sur true, cette propriété empêchera un utilisateur de supprimer ce **SDT**. |
| [getLockContents()](#getLockContents) | Lorsqu'elle est définie sur true, cette propriété empêchera un utilisateur de modifier le contenu de ce **SDT**. |
| [getNode()](#getNode) | Renvoie un objet Node qui implémente cette interface. |
| [getPlaceholder()](#getPlaceholder) | Obtient le [BuildingBlock](../../com.aspose.words/buildingblock/) contenant le texte de substitution qui doit être affiché lorsque le contenu de l'exécution de ce SDT est vide, que l'élément XML mappé associé est vide comme spécifié via l'élément [getXmlMapping()](../../com.aspose.words/istructureddocumenttag/\#getXmlMapping) ou que l'élément [isShowingPlaceholderText()](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText-boolean) est vrai. |
| [getPlaceholderName()](#getPlaceholderName) | Obtient ou définit le nom du [BuildingBlock](../../com.aspose.words/buildingblock/) contenant le texte de substitution. |
| [getSdtType()](#getSdtType) | Obtient le type de cette **Structured document tag**. |
| [getTag()](#getTag) | Spécifie une balise associée au nœud SDT actuel. |
| [getTitle()](#getTitle) | Spécifie le nom convivial associé à ce **SDT**. |
| [getWordOpenXML()](#getWordOpenXML) | Obtient une chaîne qui représente le XML contenu dans le nœud au format [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC). |
| [getXmlMapping()](#getXmlMapping) | Obtient un objet qui représente le mappage de cette balise de document structuré aux données XML dans une partie XML personnalisée du document actuel. |
| [isMultiSection()](#isMultiSection) | Renvoie true si cette instance est une balise de document structuré à portée (multi-section). |
| [isShowingPlaceholderText()](#isShowingPlaceholderText) | Spécifie si le contenu de ce **SDT** doit être interprété comme contenant du texte de substitution (par opposition au texte ordinaire contenu dans le SDT). |
| [isShowingPlaceholderText(boolean value)](#isShowingPlaceholderText-boolean) | Spécifie si le contenu de ce **SDT** doit être interprété comme contenant du texte de substitution (par opposition au texte ordinaire contenu dans le SDT). |
| [removeSelfOnly()](#removeSelfOnly) | Supprime uniquement ce nœud SDT lui-même, tout en conservant son contenu dans l'arborescence du document. |
| [setAppearance(int value)](#setAppearance-int) | Définit l'apparence de la balise de document structuré. |
| [setColor(Color value)](#setColor-java.awt.Color) | Définit la couleur de la balise de document structuré. |
| [setLockContentControl(boolean value)](#setLockContentControl-boolean) | Lorsqu'elle est définie sur true, cette propriété empêchera un utilisateur de supprimer ce **SDT**. |
| [setLockContents(boolean value)](#setLockContents-boolean) | Lorsqu'elle est définie sur true, cette propriété empêchera un utilisateur de modifier le contenu de ce **SDT**. |
| [setPlaceholderName(String value)](#setPlaceholderName-java.lang.String) | Obtient ou définit le nom du [BuildingBlock](../../com.aspose.words/buildingblock/) contenant le texte de substitution. |
| [setTag(String value)](#setTag-java.lang.String) | Spécifie une balise associée au nœud SDT actuel. |
| [setTitle(String value)](#setTitle-java.lang.String) | Spécifie le nom convivial associé à ce **SDT**. |
### getAppearance() {#getAppearance}
```
public abstract int getAppearance()
```


Obtient l'apparence de la balise de document structuré.

 **Examples:** 

Montre comment afficher la balise autour du contenu.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");
 StructuredDocumentTagRangeStart tag = (StructuredDocumentTagRangeStart) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, true);

 if (tag.getAppearance() == SdtAppearance.HIDDEN)
     tag.setAppearance(SdtAppearance.TAGS);
 
```

**Returns:**
int - L'apparence de la balise de document structuré. La valeur renvoyée est l'une des constantes [SdtAppearance](../../com.aspose.words/sdtappearance/).
### getChildNodes(int nodeType, boolean isDeep) {#getChildNodes-int-boolean}
```
public abstract NodeCollection getChildNodes(int nodeType, boolean isDeep)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nodeType | int |  |
| isDeep | boolean |  |

**Returns:**
[NodeCollection](../../com.aspose.words/nodecollection/)
### getColor() {#getColor}
```
public abstract Color getColor()
```


Obtient la couleur de la balise de document structuré.

 **Examples:** 

Montre comment obtenir les propriétés des balises de document structuré multi-section.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Returns:**
java.awt.Color - La couleur de la balise de document structuré.
### getId() {#getId}
```
public abstract int getId()
```


Spécifie un identifiant numérique persistant en lecture seule unique pour ce **SDT**.

 **Examples:** 

Montre comment obtenir les propriétés des balises de document structuré multi-section.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Returns:**
int - La valeur int correspondante.
### getLevel() {#getLevel}
```
public abstract int getLevel()
```


Obtient le niveau auquel ce **SDT** apparaît dans l'arborescence du document.

 **Examples:** 

Montre comment obtenir les propriétés des balises de document structuré multi-section.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Returns:**
int - Le niveau auquel ce **SDT** apparaît dans l'arborescence du document. La valeur retournée est l'une des constantes [MarkupLevel](../../com.aspose.words/markuplevel/).
### getLockContentControl() {#getLockContentControl}
```
public abstract boolean getLockContentControl()
```


Lorsqu'elle est définie sur true, cette propriété empêchera un utilisateur de supprimer ce **SDT**.

 **Examples:** 

Montre comment appliquer des restrictions d'édition aux balises de document structuré.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a plain text structured document tag, which acts as a text box that prompts the user to fill it in.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "LockContents" property to "true" to prohibit the user from editing this text box's contents.
 tag.setLockContents(true);
 builder.write("The contents of this structured document tag cannot be edited: ");
 builder.insertNode(tag);

 tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "LockContentControl" property to "true" to prohibit the user from
 // deleting this structured document tag manually in Microsoft Word.
 tag.setLockContentControl(true);

 builder.insertParagraph();
 builder.write("This structured document tag cannot be deleted but its contents can be edited: ");
 builder.insertNode(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Lock.docx");
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getLockContents() {#getLockContents}
```
public abstract boolean getLockContents()
```


Lorsqu'elle est définie sur true, cette propriété empêchera un utilisateur de modifier le contenu de ce **SDT**.

 **Examples:** 

Montre comment appliquer des restrictions d'édition aux balises de document structuré.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a plain text structured document tag, which acts as a text box that prompts the user to fill it in.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "LockContents" property to "true" to prohibit the user from editing this text box's contents.
 tag.setLockContents(true);
 builder.write("The contents of this structured document tag cannot be edited: ");
 builder.insertNode(tag);

 tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "LockContentControl" property to "true" to prohibit the user from
 // deleting this structured document tag manually in Microsoft Word.
 tag.setLockContentControl(true);

 builder.insertParagraph();
 builder.write("This structured document tag cannot be deleted but its contents can be edited: ");
 builder.insertNode(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Lock.docx");
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getNode() {#getNode}
```
public abstract Node getNode()
```


Renvoie un objet Node qui implémente cette interface.

**Returns:**
[Node](../../com.aspose.words/node/) - Node object that implements this interface.
### getPlaceholder() {#getPlaceholder}
```
public abstract BuildingBlock getPlaceholder()
```


Obtient le [BuildingBlock](../../com.aspose.words/buildingblock/) contenant le texte de substitution qui doit être affiché lorsque le contenu de l'exécution de ce SDT est vide, que l'élément XML mappé associé est vide comme spécifié via l'élément [getXmlMapping()](../../com.aspose.words/istructureddocumenttag/\#getXmlMapping) ou que l'élément [isShowingPlaceholderText()](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText-boolean) est vrai.

 **Remarks:** 

Peut être nul, ce qui signifie que l'espace réservé n'est pas applicable pour ce Sdt.

 **Examples:** 

Montre comment utiliser le contenu d'un bloc de construction comme texte d'espace réservé personnalisé pour une balise de document structuré.

```

 Document doc = new Document();

 // Insert a plain text structured document tag of the "PlainText" type, which will function as a text box.
 // The contents that it will display by default are a "Click here to enter text." prompt.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // We can get the tag to display the contents of a building block instead of the default text.
 // First, add a building block with contents to the glossary document.
 GlossaryDocument glossaryDoc = doc.getGlossaryDocument();

 BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
 substituteBlock.setName("Custom Placeholder");
 substituteBlock.appendChild(new Section(glossaryDoc));
 substituteBlock.getFirstSection().appendChild(new Body(glossaryDoc));
 substituteBlock.getFirstSection().getBody().appendParagraph("Custom placeholder text.");

 glossaryDoc.appendChild(substituteBlock);

 // Then, use the structured document tag's "PlaceholderName" property to reference that building block by name.
 tag.setPlaceholderName("Custom Placeholder");

 // If "PlaceholderName" refers to an existing block in the parent document's glossary document,
 // we will be able to verify the building block via the "Placeholder" property.
 Assert.assertEquals(substituteBlock, tag.getPlaceholder());

 // Set the "IsShowingPlaceholderText" property to "true" to treat the
 // structured document tag's current contents as placeholder text.
 // This means that clicking on the text box in Microsoft Word will immediately highlight all the tag's contents.
 // Set the "IsShowingPlaceholderText" property to "false" to get the
 // structured document tag to treat its contents as text that a user has already entered.
 // Clicking on this text in Microsoft Word will place the blinking cursor at the clicked location.
 tag.isShowingPlaceholderText(isShowingPlaceholderText);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
 
```

**Returns:**
[BuildingBlock](../../com.aspose.words/buildingblock/) - The [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [getXmlMapping()](../../com.aspose.words/istructureddocumenttag/\#getXmlMapping) element or the [isShowingPlaceholderText()](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText-boolean) element is true.
### getPlaceholderName() {#getPlaceholderName}
```
public abstract String getPlaceholderName()
```


Obtient ou définit le nom du [BuildingBlock](../../com.aspose.words/buildingblock/) contenant le texte de substitution.

**Returns:**
java.lang.String - La valeur java.lang.String correspondante.
### getSdtType() {#getSdtType}
```
public abstract int getSdtType()
```


Obtient le type de cette **Structured document tag**.

**Returns:**
int - Type de cette **Structured document tag**. La valeur retournée est l'une des constantes [SdtType](../../com.aspose.words/sdttype/).
### getTag() {#getTag}
```
public abstract String getTag()
```


Spécifie une balise associée au nœud SDT actuel. Ne peut pas être nul.

 **Examples:** 

Montre comment créer une balise de document structuré dans une zone de texte simple et modifier son apparence.

```

 Document doc = new Document();

 // Create a structured document tag that will contain plain text.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the title and color of the frame that appears when you mouse over the structured document tag in Microsoft Word.
 tag.setTitle("My plain text");
 tag.setColor(Color.MAGENTA);

 // Set a tag for this structured document tag, which is obtainable
 // as an XML element named "tag", with the string below in its "@val" attribute.
 tag.setTag("MyPlainTextSDT");

 // Every structured document tag has a random unique ID.
 Assert.assertTrue(tag.getId() > 0);

 // Set the font for the text inside the structured document tag.
 tag.getContentsFont().setName("Arial");

 // Set the font for the text at the end of the structured document tag.
 // Any text that we type in the document body after moving out of the tag with arrow keys will use this font.
 tag.getEndCharacterFont().setName("Arial Black");

 // By default, this is false and pressing enter while inside a structured document tag does nothing.
 // When set to true, our structured document tag can have multiple lines.

 // Set the "Multiline" property to "false" to only allow the contents
 // of this structured document tag to span a single line.
 // Set the "Multiline" property to "true" to allow the tag to contain multiple lines of content.
 tag.setMultiline(true);

 // Set the "Appearance" property to "SdtAppearance.Tags" to show tags around content.
 // By default structured document tag shows as BoundingBox.
 tag.setAppearance(SdtAppearance.TAGS);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(tag);

 // Insert a clone of our structured document tag in a new paragraph.
 StructuredDocumentTag tagClone = (StructuredDocumentTag) tag.deepClone(true);
 builder.insertParagraph();
 builder.insertNode(tagClone);

 // Use the "RemoveSelfOnly" method to remove a structured document tag, while keeping its contents in the document.
 tagClone.removeSelfOnly();

 doc.save(getArtifactsDir() + "StructuredDocumentTag.PlainText.docx");
 
```

**Returns:**
java.lang.String - La valeur java.lang.String correspondante.
### getTitle() {#getTitle}
```
public abstract String getTitle()
```


Spécifie le nom convivial associé à ce **SDT**. Ne peut pas être nul.

 **Examples:** 

Montre comment obtenir une balise de document structuré.

```

 Document doc = new Document(getMyDir() + "Structured document tags by id.docx");

 // Get the structured document tag by Id.
 IStructuredDocumentTag sdt = doc.getRange().getStructuredDocumentTags().getById(1160505028);
 System.out.println(sdt.isMultiSection());
 System.out.println(sdt.getTitle());

 // Get the structured document tag or ranged tag by Title.
 sdt = doc.getRange().getStructuredDocumentTags().getByTitle("Alias4");
 System.out.println(sdt.getId());
 
```

**Returns:**
java.lang.String - La valeur java.lang.String correspondante.
### getWordOpenXML() {#getWordOpenXML}
```
public abstract String getWordOpenXML()
```


Obtient une chaîne qui représente le XML contenu dans le nœud au format [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC).

 **Examples:** 

Montre comment obtenir le XML contenu dans le nœud au format FlatOpc.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");

 List tags = Arrays.stream(doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG, true).toArray())
         .filter(StructuredDocumentTag.class::isInstance)
         .map(StructuredDocumentTag.class::cast)
         .collect(Collectors.toList());

 Assert.assertTrue(tags.get(0).getWordOpenXML()
         .contains(
                 ""));
 
```

**Returns:**
java.lang.String - Une chaîne qui représente le XML contenu dans le nœud au format [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC).
### getXmlMapping() {#getXmlMapping}
```
public abstract XmlMapping getXmlMapping()
```


Obtient un objet qui représente le mappage de cette balise de document structuré aux données XML dans une partie XML personnalisée du document actuel.

 **Remarks:** 

Vous pouvez utiliser la méthode [XmlMapping.setMapping(com.aspose.words.CustomXmlPart, java.lang.String, java.lang.String)](../../com.aspose.words/xmlmapping/\#setMapping-com.aspose.words.CustomXmlPart--java.lang.String--java.lang.String) de cet objet pour associer une balise de document structuré à des données XML.

 **Examples:** 

Montre comment créer une balise de document structuré avec des données XML personnalisées.

```

 Document doc = new Document();

 // Construct an XML part that contains data and add it to the document's collection.
 // If we enable the "Developer" tab in Microsoft Word,
 // we can find elements from this collection in the "XML Mapping Pane", along with a few default elements.
 String xmlPartId = UUID.randomUUID().toString();
 String xmlPartContent = "Hello, World!";
 CustomXmlPart xmlPart = doc.getCustomXmlParts().add(xmlPartId, xmlPartContent);

 Assert.assertEquals(xmlPart.getData(), xmlPartContent.getBytes());
 Assert.assertEquals(xmlPart.getId(), xmlPartId);

 // Below are two ways to refer to XML parts.
 // 1 -  By an index in the custom XML part collection:
 Assert.assertEquals(xmlPart, doc.getCustomXmlParts().get(0));

 // 2 -  By GUID:
 Assert.assertEquals(xmlPart, doc.getCustomXmlParts().getById(xmlPartId));

 // Add an XML schema association.
 xmlPart.getSchemas().add("http://www.w3.org/2001/XMLSchema");

 // Clone a part, and then insert it into the collection.
 CustomXmlPart xmlPartClone = xmlPart.deepClone();
 xmlPartClone.setId(UUID.randomUUID().toString());
 doc.getCustomXmlParts().add(xmlPartClone);

 Assert.assertEquals(doc.getCustomXmlParts().getCount(), 2);

 // Iterate through the collection and print the contents of each part.
 Iterator enumerator = doc.getCustomXmlParts().iterator();
 int index = 0;
 while (enumerator.hasNext()) {
     CustomXmlPart customXmlPart = enumerator.next();
     System.out.println(MessageFormat.format("XML part index {0}, ID: {1}", index, customXmlPart.getId()));
     System.out.println(MessageFormat.format("\tContent: {0}", customXmlPart.getData()));
     index++;
 }

 // Use the "RemoveAt" method to remove the cloned part by index.
 doc.getCustomXmlParts().removeAt(1);

 Assert.assertEquals(doc.getCustomXmlParts().getCount(), 1);

 // Clone the XML parts collection, and then use the "Clear" method to remove all its elements at once.
 CustomXmlPartCollection customXmlParts = doc.getCustomXmlParts().deepClone();
 customXmlParts.clear();

 // Create a structured document tag that will display our part's contents and insert it into the document body.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.BLOCK);
 tag.getXmlMapping().setMapping(xmlPart, "/root[1]/text[1]", "");

 doc.getFirstSection().getBody().appendChild(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.CustomXml.docx");
 
```

**Returns:**
[XmlMapping](../../com.aspose.words/xmlmapping/) - An object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document.
### isMultiSection() {#isMultiSection}
```
public abstract boolean isMultiSection()
```


Renvoie true si cette instance est une balise de document structuré à portée (multi-section).

 **Examples:** 

Montre comment obtenir une balise de document structuré.

```

 Document doc = new Document(getMyDir() + "Structured document tags by id.docx");

 // Get the structured document tag by Id.
 IStructuredDocumentTag sdt = doc.getRange().getStructuredDocumentTags().getById(1160505028);
 System.out.println(sdt.isMultiSection());
 System.out.println(sdt.getTitle());

 // Get the structured document tag or ranged tag by Title.
 sdt = doc.getRange().getStructuredDocumentTags().getByTitle("Alias4");
 System.out.println(sdt.getId());
 
```

**Returns:**
boolean - Vrai si cette instance est une balise de document structuré à portée (multi-section).
### isShowingPlaceholderText() {#isShowingPlaceholderText}
```
public abstract boolean isShowingPlaceholderText()
```


Spécifie si le contenu de ce **SDT** doit être interprété comme contenant du texte de substitution (par opposition au texte ordinaire contenu dans le SDT).

si réglé sur vrai, cet état sera repris (affichage du texte d'espace réservé) à l'ouverture de ce document.

 **Examples:** 

Montre comment utiliser le contenu d'un bloc de construction comme texte d'espace réservé personnalisé pour une balise de document structuré.

```

 Document doc = new Document();

 // Insert a plain text structured document tag of the "PlainText" type, which will function as a text box.
 // The contents that it will display by default are a "Click here to enter text." prompt.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // We can get the tag to display the contents of a building block instead of the default text.
 // First, add a building block with contents to the glossary document.
 GlossaryDocument glossaryDoc = doc.getGlossaryDocument();

 BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
 substituteBlock.setName("Custom Placeholder");
 substituteBlock.appendChild(new Section(glossaryDoc));
 substituteBlock.getFirstSection().appendChild(new Body(glossaryDoc));
 substituteBlock.getFirstSection().getBody().appendParagraph("Custom placeholder text.");

 glossaryDoc.appendChild(substituteBlock);

 // Then, use the structured document tag's "PlaceholderName" property to reference that building block by name.
 tag.setPlaceholderName("Custom Placeholder");

 // If "PlaceholderName" refers to an existing block in the parent document's glossary document,
 // we will be able to verify the building block via the "Placeholder" property.
 Assert.assertEquals(substituteBlock, tag.getPlaceholder());

 // Set the "IsShowingPlaceholderText" property to "true" to treat the
 // structured document tag's current contents as placeholder text.
 // This means that clicking on the text box in Microsoft Word will immediately highlight all the tag's contents.
 // Set the "IsShowingPlaceholderText" property to "false" to get the
 // structured document tag to treat its contents as text that a user has already entered.
 // Clicking on this text in Microsoft Word will place the blinking cursor at the clicked location.
 tag.isShowingPlaceholderText(isShowingPlaceholderText);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### isShowingPlaceholderText(boolean value) {#isShowingPlaceholderText-boolean}
```
public abstract void isShowingPlaceholderText(boolean value)
```


Spécifie si le contenu de ce **SDT** doit être interprété comme contenant du texte de substitution (par opposition au texte ordinaire contenu dans le SDT).

si réglé sur vrai, cet état sera repris (affichage du texte d'espace réservé) à l'ouverture de ce document.

 **Examples:** 

Montre comment utiliser le contenu d'un bloc de construction comme texte d'espace réservé personnalisé pour une balise de document structuré.

```

 Document doc = new Document();

 // Insert a plain text structured document tag of the "PlainText" type, which will function as a text box.
 // The contents that it will display by default are a "Click here to enter text." prompt.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // We can get the tag to display the contents of a building block instead of the default text.
 // First, add a building block with contents to the glossary document.
 GlossaryDocument glossaryDoc = doc.getGlossaryDocument();

 BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
 substituteBlock.setName("Custom Placeholder");
 substituteBlock.appendChild(new Section(glossaryDoc));
 substituteBlock.getFirstSection().appendChild(new Body(glossaryDoc));
 substituteBlock.getFirstSection().getBody().appendParagraph("Custom placeholder text.");

 glossaryDoc.appendChild(substituteBlock);

 // Then, use the structured document tag's "PlaceholderName" property to reference that building block by name.
 tag.setPlaceholderName("Custom Placeholder");

 // If "PlaceholderName" refers to an existing block in the parent document's glossary document,
 // we will be able to verify the building block via the "Placeholder" property.
 Assert.assertEquals(substituteBlock, tag.getPlaceholder());

 // Set the "IsShowingPlaceholderText" property to "true" to treat the
 // structured document tag's current contents as placeholder text.
 // This means that clicking on the text box in Microsoft Word will immediately highlight all the tag's contents.
 // Set the "IsShowingPlaceholderText" property to "false" to get the
 // structured document tag to treat its contents as text that a user has already entered.
 // Clicking on this text in Microsoft Word will place the blinking cursor at the clicked location.
 tag.isShowingPlaceholderText(isShowingPlaceholderText);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### removeSelfOnly() {#removeSelfOnly}
```
public abstract void removeSelfOnly()
```


Supprime uniquement ce nœud SDT lui-même, tout en conservant son contenu dans l'arborescence du document.

 **Examples:** 

Montre comment supprimer la balise de document structuré, tout en conservant le contenu à l'intérieur.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");

 // This collection provides a unified interface for accessing ranged and non-ranged structured tags.
 StructuredDocumentTagCollection sdts = doc.getRange().getStructuredDocumentTags();
 Assert.assertEquals(5, sdts.getCount());

 // Here we can get child nodes from the common interface of ranged and non-ranged structured tags.
 for (IStructuredDocumentTag sdt : sdts)
     if (sdt.getChildNodes(NodeType.ANY, false).getCount() > 0)
         sdt.removeSelfOnly();

 sdts = doc.getRange().getStructuredDocumentTags();
 Assert.assertEquals(0, sdts.getCount());
 
```

### setAppearance(int value) {#setAppearance-int}
```
public abstract void setAppearance(int value)
```


Définit l'apparence de la balise de document structuré.

 **Examples:** 

Montre comment afficher la balise autour du contenu.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");
 StructuredDocumentTagRangeStart tag = (StructuredDocumentTagRangeStart) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, true);

 if (tag.getAppearance() == SdtAppearance.HIDDEN)
     tag.setAppearance(SdtAppearance.TAGS);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | L'apparence de la balise de document structuré. La valeur doit être l'une des constantes [SdtAppearance](../../com.aspose.words/sdtappearance/). |

### setColor(Color value) {#setColor-java.awt.Color}
```
public abstract void setColor(Color value)
```


Définit la couleur de la balise de document structuré.

 **Examples:** 

Montre comment obtenir les propriétés des balises de document structuré multi-section.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.awt.Color | La couleur de la balise de document structuré. |

### setLockContentControl(boolean value) {#setLockContentControl-boolean}
```
public abstract void setLockContentControl(boolean value)
```


Lorsqu'elle est définie sur true, cette propriété empêchera un utilisateur de supprimer ce **SDT**.

 **Examples:** 

Montre comment appliquer des restrictions d'édition aux balises de document structuré.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a plain text structured document tag, which acts as a text box that prompts the user to fill it in.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "LockContents" property to "true" to prohibit the user from editing this text box's contents.
 tag.setLockContents(true);
 builder.write("The contents of this structured document tag cannot be edited: ");
 builder.insertNode(tag);

 tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "LockContentControl" property to "true" to prohibit the user from
 // deleting this structured document tag manually in Microsoft Word.
 tag.setLockContentControl(true);

 builder.insertParagraph();
 builder.write("This structured document tag cannot be deleted but its contents can be edited: ");
 builder.insertNode(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Lock.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setLockContents(boolean value) {#setLockContents-boolean}
```
public abstract void setLockContents(boolean value)
```


Lorsqu'elle est définie sur true, cette propriété empêchera un utilisateur de modifier le contenu de ce **SDT**.

 **Examples:** 

Montre comment appliquer des restrictions d'édition aux balises de document structuré.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a plain text structured document tag, which acts as a text box that prompts the user to fill it in.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "LockContents" property to "true" to prohibit the user from editing this text box's contents.
 tag.setLockContents(true);
 builder.write("The contents of this structured document tag cannot be edited: ");
 builder.insertNode(tag);

 tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "LockContentControl" property to "true" to prohibit the user from
 // deleting this structured document tag manually in Microsoft Word.
 tag.setLockContentControl(true);

 builder.insertParagraph();
 builder.write("This structured document tag cannot be deleted but its contents can be edited: ");
 builder.insertNode(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Lock.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setPlaceholderName(String value) {#setPlaceholderName-java.lang.String}
```
public abstract void setPlaceholderName(String value)
```


Obtient ou définit le nom du [BuildingBlock](../../com.aspose.words/buildingblock/) contenant le texte de substitution.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

### setTag(String value) {#setTag-java.lang.String}
```
public abstract void setTag(String value)
```


Spécifie une balise associée au nœud SDT actuel. Ne peut pas être nul.

 **Examples:** 

Montre comment créer une balise de document structuré dans une zone de texte simple et modifier son apparence.

```

 Document doc = new Document();

 // Create a structured document tag that will contain plain text.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the title and color of the frame that appears when you mouse over the structured document tag in Microsoft Word.
 tag.setTitle("My plain text");
 tag.setColor(Color.MAGENTA);

 // Set a tag for this structured document tag, which is obtainable
 // as an XML element named "tag", with the string below in its "@val" attribute.
 tag.setTag("MyPlainTextSDT");

 // Every structured document tag has a random unique ID.
 Assert.assertTrue(tag.getId() > 0);

 // Set the font for the text inside the structured document tag.
 tag.getContentsFont().setName("Arial");

 // Set the font for the text at the end of the structured document tag.
 // Any text that we type in the document body after moving out of the tag with arrow keys will use this font.
 tag.getEndCharacterFont().setName("Arial Black");

 // By default, this is false and pressing enter while inside a structured document tag does nothing.
 // When set to true, our structured document tag can have multiple lines.

 // Set the "Multiline" property to "false" to only allow the contents
 // of this structured document tag to span a single line.
 // Set the "Multiline" property to "true" to allow the tag to contain multiple lines of content.
 tag.setMultiline(true);

 // Set the "Appearance" property to "SdtAppearance.Tags" to show tags around content.
 // By default structured document tag shows as BoundingBox.
 tag.setAppearance(SdtAppearance.TAGS);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(tag);

 // Insert a clone of our structured document tag in a new paragraph.
 StructuredDocumentTag tagClone = (StructuredDocumentTag) tag.deepClone(true);
 builder.insertParagraph();
 builder.insertNode(tagClone);

 // Use the "RemoveSelfOnly" method to remove a structured document tag, while keeping its contents in the document.
 tagClone.removeSelfOnly();

 doc.save(getArtifactsDir() + "StructuredDocumentTag.PlainText.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

### setTitle(String value) {#setTitle-java.lang.String}
```
public abstract void setTitle(String value)
```


Spécifie le nom convivial associé à ce **SDT**. Ne peut pas être nul.

 **Examples:** 

Montre comment obtenir une balise de document structuré.

```

 Document doc = new Document(getMyDir() + "Structured document tags by id.docx");

 // Get the structured document tag by Id.
 IStructuredDocumentTag sdt = doc.getRange().getStructuredDocumentTags().getById(1160505028);
 System.out.println(sdt.isMultiSection());
 System.out.println(sdt.getTitle());

 // Get the structured document tag or ranged tag by Title.
 sdt = doc.getRange().getStructuredDocumentTags().getByTitle("Alias4");
 System.out.println(sdt.getId());
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

