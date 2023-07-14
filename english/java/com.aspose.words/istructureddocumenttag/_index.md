---
title: IStructuredDocumentTag
linktitle: IStructuredDocumentTag
second_title: Aspose.Words for Java
description: Interface to define a common data for StructuredDocumentTag and StructuredDocumentTagRangeStart in Java.
type: docs
weight: 686
url: /java/com.aspose.words/istructureddocumenttag/
---
```
public interface IStructuredDocumentTag
```

Interface to define a common data for [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) and [StructuredDocumentTagRangeStart](../../com.aspose.words/structureddocumenttagrangestart/).
## Methods

| Method | Description |
| --- | --- |
| [getColor()](#getColor) | Gets the color of the structured document tag. |
| [getId()](#getId) | Specifies a unique read-only persistent numerical Id for this **SDT**. |
| [getLevel()](#getLevel) | Gets the level at which this **SDT** occurs in the document tree. |
| [getLockContentControl()](#getLockContentControl) | When set to true, this property will prohibit a user from deleting this **SDT**. |
| [getLockContents()](#getLockContents) | When set to true, this property will prohibit a user from editing the contents of this **SDT**. |
| [getPlaceholder()](#getPlaceholder) | Gets the [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [getXmlMapping()](../../com.aspose.words/istructureddocumenttag/\#getXmlMapping) element or the [isShowingPlaceholderText()](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText-boolean) element is true. |
| [getPlaceholderName()](#getPlaceholderName) | Gets or sets Name of the [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text. |
| [getSdtType()](#getSdtType) | Gets type of this **Structured document tag**. |
| [getTag()](#getTag) | Specifies a tag associated with the current SDT node. |
| [getTitle()](#getTitle) | Specifies the friendly name associated with this **SDT**. |
| [getWordOpenXML()](#getWordOpenXML) | Gets a string that represents the XML contained within the node in the [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC) format. |
| [getXmlMapping()](#getXmlMapping) | Gets an object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document. |
| [isRanged()](#isRanged) | Returns true if this instance is a ranged structured document tag. |
| [isShowingPlaceholderText()](#isShowingPlaceholderText) | Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). |
| [isShowingPlaceholderText(boolean value)](#isShowingPlaceholderText-boolean) | Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). |
| [setColor(Color value)](#setColor-java.awt.Color) | Sets the color of the structured document tag. |
| [setLockContentControl(boolean value)](#setLockContentControl-boolean) | When set to true, this property will prohibit a user from deleting this **SDT**. |
| [setLockContents(boolean value)](#setLockContents-boolean) | When set to true, this property will prohibit a user from editing the contents of this **SDT**. |
| [setPlaceholderName(String value)](#setPlaceholderName-java.lang.String) | Gets or sets Name of the [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text. |
| [setTag(String value)](#setTag-java.lang.String) | Specifies a tag associated with the current SDT node. |
| [setTitle(String value)](#setTitle-java.lang.String) | Specifies the friendly name associated with this **SDT**. |
| [structuredDocumentTagNode()](#structuredDocumentTagNode) | Returns Node object that implements this interface. |
### getColor() {#getColor}
```
public abstract Color getColor()
```


Gets the color of the structured document tag.

**Returns:**
java.awt.Color - The color of the structured document tag.
### getId() {#getId}
```
public abstract int getId()
```


Specifies a unique read-only persistent numerical Id for this **SDT**.

**Returns:**
int - The corresponding  int  value.
### getLevel() {#getLevel}
```
public abstract int getLevel()
```


Gets the level at which this **SDT** occurs in the document tree.

**Returns:**
int - The level at which this **SDT** occurs in the document tree. The returned value is one of [MarkupLevel](../../com.aspose.words/markuplevel/) constants.
### getLockContentControl() {#getLockContentControl}
```
public abstract boolean getLockContentControl()
```


When set to true, this property will prohibit a user from deleting this **SDT**.

**Returns:**
boolean - The corresponding  boolean  value.
### getLockContents() {#getLockContents}
```
public abstract boolean getLockContents()
```


When set to true, this property will prohibit a user from editing the contents of this **SDT**.

**Returns:**
boolean - The corresponding  boolean  value.
### getPlaceholder() {#getPlaceholder}
```
public abstract BuildingBlock getPlaceholder()
```


Gets the [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [getXmlMapping()](../../com.aspose.words/istructureddocumenttag/\#getXmlMapping) element or the [isShowingPlaceholderText()](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText-boolean) element is true.

 **Remarks:** 

Can be null, meaning that the placeholder is not applicable for this Sdt.

**Returns:**
[BuildingBlock](../../com.aspose.words/buildingblock/) - The [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [getXmlMapping()](../../com.aspose.words/istructureddocumenttag/\#getXmlMapping) element or the [isShowingPlaceholderText()](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText-boolean) element is true.
### getPlaceholderName() {#getPlaceholderName}
```
public abstract String getPlaceholderName()
```


Gets or sets Name of the [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text.

BuildingBlock with this name [BuildingBlock.getName()](../../com.aspose.words/buildingblock/\#getName) / [BuildingBlock.setName(java.lang.String)](../../com.aspose.words/buildingblock/\#setName-java.lang.String) has to be present in the [Document.getGlossaryDocument()](../../com.aspose.words/document/\#getGlossaryDocument) / [Document.setGlossaryDocument(com.aspose.words.GlossaryDocument)](../../com.aspose.words/document/\#setGlossaryDocument-com.aspose.words.GlossaryDocument) otherwise java.lang.IllegalStateException will occur.

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
 System.out.println(sdt.isRanged());
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

**Returns:**
java.lang.String - A string that represents the XML contained within the node in the [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC) format.
### getXmlMapping() {#getXmlMapping}
```
public abstract XmlMapping getXmlMapping()
```


Gets an object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document.

 **Remarks:** 

You can use the [XmlMapping.setMapping(com.aspose.words.CustomXmlPart, java.lang.String, java.lang.String)](../../com.aspose.words/xmlmapping/\#setMapping-com.aspose.words.CustomXmlPart--java.lang.String--java.lang.String) method of this object to map a structured document tag to XML data.

**Returns:**
[XmlMapping](../../com.aspose.words/xmlmapping/) - An object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document.
### isRanged() {#isRanged}
```
public abstract boolean isRanged()
```


Returns true if this instance is a ranged structured document tag.

 **Examples:** 

Shows how to get structured document tag.

```

 Document doc = new Document(getMyDir() + "Structured document tags by id.docx");

 // Get the structured document tag by Id.
 IStructuredDocumentTag sdt = doc.getRange().getStructuredDocumentTags().getById(1160505028);
 System.out.println(sdt.isRanged());
 System.out.println(sdt.getTitle());

 // Get the structured document tag or ranged tag by Title.
 sdt = doc.getRange().getStructuredDocumentTags().getByTitle("Alias4");
 System.out.println(sdt.getId());
 
```

**Returns:**
boolean
### isShowingPlaceholderText() {#isShowingPlaceholderText}
```
public abstract boolean isShowingPlaceholderText()
```


Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT).

if set to true, this state shall be resumed (showing placeholder text) upon opening this document.

**Returns:**
boolean - The corresponding  boolean  value.
### isShowingPlaceholderText(boolean value) {#isShowingPlaceholderText-boolean}
```
public abstract void isShowingPlaceholderText(boolean value)
```


Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT).

if set to true, this state shall be resumed (showing placeholder text) upon opening this document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setColor(Color value) {#setColor-java.awt.Color}
```
public abstract void setColor(Color value)
```


Sets the color of the structured document tag.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The color of the structured document tag. |

### setLockContentControl(boolean value) {#setLockContentControl-boolean}
```
public abstract void setLockContentControl(boolean value)
```


When set to true, this property will prohibit a user from deleting this **SDT**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setLockContents(boolean value) {#setLockContents-boolean}
```
public abstract void setLockContents(boolean value)
```


When set to true, this property will prohibit a user from editing the contents of this **SDT**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setPlaceholderName(String value) {#setPlaceholderName-java.lang.String}
```
public abstract void setPlaceholderName(String value)
```


Gets or sets Name of the [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text.

BuildingBlock with this name [BuildingBlock.getName()](../../com.aspose.words/buildingblock/\#getName) / [BuildingBlock.setName(java.lang.String)](../../com.aspose.words/buildingblock/\#setName-java.lang.String) has to be present in the [Document.getGlossaryDocument()](../../com.aspose.words/document/\#getGlossaryDocument) / [Document.setGlossaryDocument(com.aspose.words.GlossaryDocument)](../../com.aspose.words/document/\#setGlossaryDocument-com.aspose.words.GlossaryDocument) otherwise java.lang.IllegalStateException will occur.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setTag(String value) {#setTag-java.lang.String}
```
public abstract void setTag(String value)
```


Specifies a tag associated with the current SDT node. Can not be null.

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
 System.out.println(sdt.isRanged());
 System.out.println(sdt.getTitle());

 // Get the structured document tag or ranged tag by Title.
 sdt = doc.getRange().getStructuredDocumentTags().getByTitle("Alias4");
 System.out.println(sdt.getId());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### structuredDocumentTagNode() {#structuredDocumentTagNode}
```
public abstract Node structuredDocumentTagNode()
```


Returns Node object that implements this interface.

**Returns:**
[Node](../../com.aspose.words/node/)
