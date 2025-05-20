---
title: IStructuredDocumentTag
linktitle: IStructuredDocumentTag
second_title: Aspose.Words for Java
description: Interface to define a common data for StructuredDocumentTag and StructuredDocumentTagRangeStart in Java.
type: docs
weight: 773
url: /java/com.aspose.words/istructureddocumenttag/
---
```
public interface IStructuredDocumentTag
```

Interface to define a common data for [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) and [StructuredDocumentTagRangeStart](../../com.aspose.words/structureddocumenttagrangestart/).

 **Examples:** 

Shows how to remove structured document tag, but keeps content inside.

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
## Methods

| Method | Description |
| --- | --- |
| [getAppearance()](#getAppearance) | Gets the appearance of the structured document tag. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean) |  |
| [getColor()](#getColor) | Gets the color of the structured document tag. |
| [getId()](#getId) | Specifies a unique read-only persistent numerical Id for this **SDT**. |
| [getLevel()](#getLevel) | Gets the level at which this **SDT** occurs in the document tree. |
| [getLockContentControl()](#getLockContentControl) | When set to true, this property will prohibit a user from deleting this **SDT**. |
| [getLockContents()](#getLockContents) | When set to true, this property will prohibit a user from editing the contents of this **SDT**. |
| [getNode()](#getNode) | Returns Node object that implements this interface. |
| [getPlaceholder()](#getPlaceholder) | Gets the [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [getXmlMapping()](../../com.aspose.words/istructureddocumenttag/\#getXmlMapping) element or the [isShowingPlaceholderText()](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText-boolean) element is true. |
| [getPlaceholderName()](#getPlaceholderName) | Gets or sets Name of the [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text. |
| [getSdtType()](#getSdtType) | Gets type of this **Structured document tag**. |
| [getTag()](#getTag) | Specifies a tag associated with the current SDT node. |
| [getTitle()](#getTitle) | Specifies the friendly name associated with this **SDT**. |
| [getWordOpenXML()](#getWordOpenXML) | Gets a string that represents the XML contained within the node in the [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC) format. |
| [getXmlMapping()](#getXmlMapping) | Gets an object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document. |
| [isMultiSection()](#isMultiSection) | Returns true if this instance is a ranged (multi-section) structured document tag. |
| [isShowingPlaceholderText()](#isShowingPlaceholderText) | Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). |
| [isShowingPlaceholderText(boolean value)](#isShowingPlaceholderText-boolean) | Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). |
| [removeSelfOnly()](#removeSelfOnly) | Removes just this SDT node itself, but keeps the content of it inside the document tree. |
| [setAppearance(int value)](#setAppearance-int) | Sets the appearance of the structured document tag. |
| [setColor(Color value)](#setColor-java.awt.Color) | Sets the color of the structured document tag. |
| [setLockContentControl(boolean value)](#setLockContentControl-boolean) | When set to true, this property will prohibit a user from deleting this **SDT**. |
| [setLockContents(boolean value)](#setLockContents-boolean) | When set to true, this property will prohibit a user from editing the contents of this **SDT**. |
| [setPlaceholderName(String value)](#setPlaceholderName-java.lang.String) | Gets or sets Name of the [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text. |
| [setTag(String value)](#setTag-java.lang.String) | Specifies a tag associated with the current SDT node. |
| [setTitle(String value)](#setTitle-java.lang.String) | Specifies the friendly name associated with this **SDT**. |
### getAppearance() {#getAppearance}
```
public abstract int getAppearance()
```


Gets the appearance of the structured document tag.

 **Examples:** 

Shows how to show tag around content.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");
 StructuredDocumentTagRangeStart tag = (StructuredDocumentTagRangeStart) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, true);

 if (tag.getAppearance() == SdtAppearance.HIDDEN)
     tag.setAppearance(SdtAppearance.TAGS);
 
```

**Returns:**
int - The appearance of the structured document tag. The returned value is one of [SdtAppearance](../../com.aspose.words/sdtappearance/) constants.
### getChildNodes(int nodeType, boolean isDeep) {#getChildNodes-int-boolean}
```
public abstract NodeCollection getChildNodes(int nodeType, boolean isDeep)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | int |  |
| isDeep | boolean |  |

**Returns:**
[NodeCollection](../../com.aspose.words/nodecollection/)
### getColor() {#getColor}
```
public abstract Color getColor()
```


Gets the color of the structured document tag.

 **Examples:** 

Shows how to get the properties of multi-section structured document tags.

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
java.awt.Color - The color of the structured document tag.
### getId() {#getId}
```
public abstract int getId()
```


Specifies a unique read-only persistent numerical Id for this **SDT**.

 **Examples:** 

Shows how to get the properties of multi-section structured document tags.

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
int - The corresponding  int  value.
### getLevel() {#getLevel}
```
public abstract int getLevel()
```


Gets the level at which this **SDT** occurs in the document tree.

 **Examples:** 

Shows how to get the properties of multi-section structured document tags.

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
int - The level at which this **SDT** occurs in the document tree. The returned value is one of [MarkupLevel](../../com.aspose.words/markuplevel/) constants.
### getLockContentControl() {#getLockContentControl}
```
public abstract boolean getLockContentControl()
```


When set to true, this property will prohibit a user from deleting this **SDT**.

 **Examples:** 

Shows how to apply editing restrictions to structured document tags.

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
boolean - The corresponding  boolean  value.
### getLockContents() {#getLockContents}
```
public abstract boolean getLockContents()
```


When set to true, this property will prohibit a user from editing the contents of this **SDT**.

 **Examples:** 

Shows how to apply editing restrictions to structured document tags.

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
boolean - The corresponding  boolean  value.
### getNode() {#getNode}
```
public abstract Node getNode()
```


Returns Node object that implements this interface.

**Returns:**
[Node](../../com.aspose.words/node/) - Node object that implements this interface.
### getPlaceholder() {#getPlaceholder}
```
public abstract BuildingBlock getPlaceholder()
```


Gets the [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [getXmlMapping()](../../com.aspose.words/istructureddocumenttag/\#getXmlMapping) element or the [isShowingPlaceholderText()](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText-boolean) element is true.

 **Remarks:** 

Can be null, meaning that the placeholder is not applicable for this Sdt.

 **Examples:** 

Shows how to use a building block's contents as a custom placeholder text for a structured document tag.

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


Gets or sets Name of the [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getSdtType() {#getSdtType}
```
public abstract int getSdtType()
```


Gets type of this **Structured document tag**.

**Returns:**
int - Type of this **Structured document tag**. The returned value is one of [SdtType](../../com.aspose.words/sdttype/) constants.
### getTag() {#getTag}
```
public abstract String getTag()
```


Specifies a tag associated with the current SDT node. Can not be null.

 **Examples:** 

Shows how to create a structured document tag in a plain text box and modify its appearance.

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
java.lang.String - The corresponding java.lang.String value.
### getTitle() {#getTitle}
```
public abstract String getTitle()
```


Specifies the friendly name associated with this **SDT**. Can not be null.

 **Examples:** 

Shows how to get structured document tag.

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
java.lang.String - The corresponding java.lang.String value.
### getWordOpenXML() {#getWordOpenXML}
```
public abstract String getWordOpenXML()
```


Gets a string that represents the XML contained within the node in the [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC) format.

 **Examples:** 

Shows how to get XML contained within the node in the FlatOpc format.

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
java.lang.String - A string that represents the XML contained within the node in the [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC) format.
### getXmlMapping() {#getXmlMapping}
```
public abstract XmlMapping getXmlMapping()
```


Gets an object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document.

 **Remarks:** 

You can use the [XmlMapping.setMapping(com.aspose.words.CustomXmlPart, java.lang.String, java.lang.String)](../../com.aspose.words/xmlmapping/\#setMapping-com.aspose.words.CustomXmlPart--java.lang.String--java.lang.String) method of this object to map a structured document tag to XML data.

 **Examples:** 

Shows how to create a structured document tag with custom XML data.

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


Returns true if this instance is a ranged (multi-section) structured document tag.

 **Examples:** 

Shows how to get structured document tag.

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
boolean - True if this instance is a ranged (multi-section) structured document tag.
### isShowingPlaceholderText() {#isShowingPlaceholderText}
```
public abstract boolean isShowingPlaceholderText()
```


Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT).

if set to true, this state shall be resumed (showing placeholder text) upon opening this document.

 **Examples:** 

Shows how to use a building block's contents as a custom placeholder text for a structured document tag.

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
boolean - The corresponding  boolean  value.
### isShowingPlaceholderText(boolean value) {#isShowingPlaceholderText-boolean}
```
public abstract void isShowingPlaceholderText(boolean value)
```


Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT).

if set to true, this state shall be resumed (showing placeholder text) upon opening this document.

 **Examples:** 

Shows how to use a building block's contents as a custom placeholder text for a structured document tag.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### removeSelfOnly() {#removeSelfOnly}
```
public abstract void removeSelfOnly()
```


Removes just this SDT node itself, but keeps the content of it inside the document tree.

 **Examples:** 

Shows how to remove structured document tag, but keeps content inside.

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


Sets the appearance of the structured document tag.

 **Examples:** 

Shows how to show tag around content.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");
 StructuredDocumentTagRangeStart tag = (StructuredDocumentTagRangeStart) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, true);

 if (tag.getAppearance() == SdtAppearance.HIDDEN)
     tag.setAppearance(SdtAppearance.TAGS);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The appearance of the structured document tag. The value must be one of [SdtAppearance](../../com.aspose.words/sdtappearance/) constants. |

### setColor(Color value) {#setColor-java.awt.Color}
```
public abstract void setColor(Color value)
```


Sets the color of the structured document tag.

 **Examples:** 

Shows how to get the properties of multi-section structured document tags.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The color of the structured document tag. |

### setLockContentControl(boolean value) {#setLockContentControl-boolean}
```
public abstract void setLockContentControl(boolean value)
```


When set to true, this property will prohibit a user from deleting this **SDT**.

 **Examples:** 

Shows how to apply editing restrictions to structured document tags.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setLockContents(boolean value) {#setLockContents-boolean}
```
public abstract void setLockContents(boolean value)
```


When set to true, this property will prohibit a user from editing the contents of this **SDT**.

 **Examples:** 

Shows how to apply editing restrictions to structured document tags.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setPlaceholderName(String value) {#setPlaceholderName-java.lang.String}
```
public abstract void setPlaceholderName(String value)
```


Gets or sets Name of the [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setTag(String value) {#setTag-java.lang.String}
```
public abstract void setTag(String value)
```


Specifies a tag associated with the current SDT node. Can not be null.

 **Examples:** 

Shows how to create a structured document tag in a plain text box and modify its appearance.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setTitle(String value) {#setTitle-java.lang.String}
```
public abstract void setTitle(String value)
```


Specifies the friendly name associated with this **SDT**. Can not be null.

 **Examples:** 

Shows how to get structured document tag.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

