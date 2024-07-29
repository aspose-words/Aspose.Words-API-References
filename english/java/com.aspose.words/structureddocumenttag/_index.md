---
title: StructuredDocumentTag
linktitle: StructuredDocumentTag
second_title: Aspose.Words for Java
description: Represents a structured document tag SDT or content control in a document in Java.
type: docs
weight: 584
url: /java/com.aspose.words/structureddocumenttag/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node/), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode/)

**All Implemented Interfaces:**
[com.aspose.words.IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
```
public class StructuredDocumentTag extends CompositeNode implements IStructuredDocumentTag
```

Represents a structured document tag (SDT or content control) in a document.

To learn more, visit the [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control] documentation article.

 **Remarks:** 

Structured document tags (SDTs) allow to embed customer-defined semantics as well as its behavior and appearance into a document.

In this version Aspose.Words provides a number of public methods and properties to manipulate the behavior and content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/). Mapping of SDT nodes to custom XML packages within a document can be performed with using the [getXmlMapping()](../../com.aspose.words/structureddocumenttag/\#getXmlMapping) property.

[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) can occur in a document in the following places:

 *  Block-level - Among paragraphs and tables, as a child of a [Body](../../com.aspose.words/body/), [HeaderFooter](../../com.aspose.words/headerfooter/), [Comment](../../com.aspose.words/comment/), [Footnote](../../com.aspose.words/footnote/) or a [Shape](../../com.aspose.words/shape/) node.
 *  Row-level - Among rows in a table, as a child of a [Table](../../com.aspose.words/table/) node.
 *  Cell-level - Among cells in a table row, as a child of a [Row](../../com.aspose.words/row/) node.
 *  Inline-level - Among inline content inside, as a child of a [Paragraph](../../com.aspose.words/paragraph/).
 *  Nested inside another [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/).

 **Examples:** 

Shows how to work with styles for content control elements.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways to apply a style from the document to a structured document tag.
 // 1 -  Apply a style object from the document's style collection:
 Style quoteStyle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.QUOTE);
 StructuredDocumentTag sdtPlainText = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);
 sdtPlainText.setStyle(quoteStyle);

 // 2 -  Reference a style in the document by name:
 StructuredDocumentTag sdtRichText = new StructuredDocumentTag(doc, SdtType.RICH_TEXT, MarkupLevel.INLINE);
 sdtRichText.setStyleName("Quote");

 builder.insertNode(sdtPlainText);
 builder.insertNode(sdtRichText);

 Assert.assertEquals(NodeType.STRUCTURED_DOCUMENT_TAG, sdtPlainText.getNodeType());

 NodeCollection tags = doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG, true);

 for (StructuredDocumentTag sdt : (Iterable) tags) {
     Assert.assertEquals(StyleIdentifier.QUOTE, sdt.getStyle().getStyleIdentifier());
     Assert.assertEquals("Quote", sdt.getStyleName());
 }
 
```


[Structured Document Tags or Content Control]: https://docs.aspose.com/words/java/working-with-content-control-sdt/
## Constructors

| Constructor | Description |
| --- | --- |
| [StructuredDocumentTag(DocumentBase doc, int type, int level)](#StructuredDocumentTag-com.aspose.words.DocumentBase-int-int) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor) | Accepts a visitor. |
| [acceptEnd(DocumentVisitor visitor)](#acceptEnd-com.aspose.words.DocumentVisitor) | Accepts a visitor for visiting the end of the StructuredDocumentTag. |
| [acceptStart(DocumentVisitor visitor)](#acceptStart-com.aspose.words.DocumentVisitor) | Accepts a visitor for visiting the start of the StructuredDocumentTag. |
| [clear()](#clear) | Clears contents of this structured document tag and displays a placeholder if it is defined. |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [dd()](#dd) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean) | Creates a duplicate of the node. |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int) |  |
| [getAncestor(int ancestorType)](#getAncestor-int) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class) | Gets the first ancestor of the specified object type. |
| [getAppearance()](#getAppearance) | Gets/sets the appearance of a structured document tag. |
| [getBuildingBlockCategory()](#getBuildingBlockCategory) | Specifies category of building block for this **SDT** node. |
| [getBuildingBlockGallery()](#getBuildingBlockGallery) | Specifies type of building block for this **SDT**. |
| [getCalendarType()](#getCalendarType) | Specifies the type of calendar for this **SDT**. |
| [getChecked()](#getChecked) | Gets/Sets current state of the Checkbox **SDT**. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean) |  |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean) |  |
| [getColor()](#getColor) | Gets the color of the structured document tag. |
| [getContainer()](#getContainer) |  |
| [getContentsFont()](#getContentsFont) | Font formatting that will be applied to text entered into **SDT**. |
| [getCount()](#getCount) | Gets the number of immediate children of this node. |
| [getCurrentNode()](#getCurrentNode) |  |
| [getCustomNodeId()](#getCustomNodeId) | Specifies custom node identifier. |
| [getDateDisplayFormat()](#getDateDisplayFormat) | String that represents the format in which dates are displayed. |
| [getDateDisplayLocale()](#getDateDisplayLocale) | Allows to set/get the language format for the date displayed in this **SDT**. |
| [getDateStorageFormat()](#getDateStorageFormat) | Gets/sets format in which the date for a date SDT is stored when the **SDT** is bound to an XML node in the document's data store. |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getDocument()](#getDocument) | Gets the document to which this node belongs. |
| [getEndCharacterFont()](#getEndCharacterFont) | Font formatting that will be applied to the last character of text entered into **SDT**. |
| [getFirstChild()](#getFirstChild) | Gets the first child of the node. |
| [getFullDate()](#getFullDate) | Specifies the full date and time last entered into this **SDT**. |
| [getId()](#getId) | Specifies a unique read-only persistent numerical Id for this **SDT**. |
| [getLastChild()](#getLastChild) | Gets the last child of the node. |
| [getLevel()](#getLevel) | Gets the level at which this **SDT** occurs in the document tree. |
| [getLevel_IMarkupNode()](#getLevel-IMarkupNode) |  |
| [getListItems()](#getListItems) | Gets [SdtListItemCollection](../../com.aspose.words/sdtlistitemcollection/) associated with this **SDT**. |
| [getLockContentControl()](#getLockContentControl) | When set to  true , this property will prohibit a user from deleting this **SDT**. |
| [getLockContents()](#getLockContents) | When set to  true , this property will prohibit a user from editing the contents of this **SDT**. |
| [getMultiline()](#getMultiline) | Specifies whether this **SDT** allows multiple lines of text. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node) |  |
| [getNextSibling()](#getNextSibling) | Gets the node immediately following this node. |
| [getNode()](#getNode) |  |
| [getNodeType()](#getNodeType) | Returns [NodeType.STRUCTURED\_DOCUMENT\_TAG](../../com.aspose.words/nodetype/\#STRUCTURED-DOCUMENT-TAG). |
| [getParentNode()](#getParentNode) | Gets the immediate parent of this node. |
| [getPlaceholder()](#getPlaceholder) | Gets the [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [getXmlMapping()](../../com.aspose.words/structureddocumenttag/\#getXmlMapping) element or the [isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttag/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttag/\#isShowingPlaceholderText-boolean) element is  true . |
| [getPlaceholderName()](#getPlaceholderName) | Gets or sets Name of the [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text. |
| [getPreviousSibling()](#getPreviousSibling) | Gets the node immediately preceding this node. |
| [getRange()](#getRange) | Returns a [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node. |
| [getSdtType()](#getSdtType) | Gets type of this **Structured document tag**. |
| [getStyle()](#getStyle) | Gets the Style of the structured document tag. |
| [getStyleName()](#getStyleName) | Gets the name of the style applied to the structured document tag. |
| [getTag()](#getTag) | Specifies a tag associated with the current SDT node. |
| [getText()](#getText) | Gets the text of this node and of all its children. |
| [getTitle()](#getTitle) | Specifies the friendly name associated with this **SDT**. |
| [getWordOpenXML()](#getWordOpenXML) | Gets a string that represents the XML contained within the node in the [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC) format. |
| [getWordOpenXMLMinimal()](#getWordOpenXMLMinimal) | Gets a string that represents the XML contained within the node in the [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC) format. |
| [getXmlMapping()](#getXmlMapping) | Gets an object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document. |
| [hasChildNodes()](#hasChildNodes) | Returns  true  if this node has any child nodes. |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node) | Returns the index of the specified child node in the child node array. |
| [isComposite()](#isComposite) | Returns  true  as this node can have child nodes. |
| [isMultiSection()](#isMultiSection) |  |
| [isRanged()](#isRanged) |  |
| [isShowingPlaceholderText()](#isShowingPlaceholderText) | Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). |
| [isShowingPlaceholderText(boolean value)](#isShowingPlaceholderText-boolean) | Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). |
| [isTemporary()](#isTemporary) | Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents are modified. |
| [isTemporary(boolean value)](#isTemporary-boolean) | Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents are modified. |
| [iterator()](#iterator) | Provides support for the for each style iteration over the child nodes of this node. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node) | Gets next node according to the pre-order tree traversal algorithm. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int) |  |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [remove()](#remove) | Removes itself from the parent. |
| [removeAllChildren()](#removeAllChildren) | Removes all the child nodes of the current node. |
| [removeMoveRevisions()](#removeMoveRevisions) |  |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [removeSelfOnly()](#removeSelfOnly) | Removes just this SDT node itself, but keeps the content of it inside the document tree. |
| [removeSmartTags()](#removeSmartTags) | Removes all [SmartTag](../../com.aspose.words/smarttag/) descendant nodes of the current node. |
| [selectNodes(String xpath)](#selectNodes-java.lang.String) | Selects a list of nodes matching the XPath expression. |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String) | Selects the first [Node](../../com.aspose.words/node/) that matches the XPath expression. |
| [setAppearance(int value)](#setAppearance-int) | Gets/sets the appearance of a structured document tag. |
| [setBuildingBlockCategory(String value)](#setBuildingBlockCategory-java.lang.String) | Specifies category of building block for this **SDT** node. |
| [setBuildingBlockGallery(String value)](#setBuildingBlockGallery-java.lang.String) | Specifies type of building block for this **SDT**. |
| [setCalendarType(int value)](#setCalendarType-int) | Specifies the type of calendar for this **SDT**. |
| [setChecked(boolean value)](#setChecked-boolean) | Gets/Sets current state of the Checkbox **SDT**. |
| [setCheckedSymbol(int characterCode, String fontName)](#setCheckedSymbol-int-java.lang.String) | Sets the symbol used to represent the checked state of a check box content control. |
| [setColor(Color value)](#setColor-java.awt.Color) | Sets the color of the structured document tag. |
| [setCustomNodeId(int value)](#setCustomNodeId-int) | Specifies custom node identifier. |
| [setDateDisplayFormat(String value)](#setDateDisplayFormat-java.lang.String) | String that represents the format in which dates are displayed. |
| [setDateDisplayLocale(int value)](#setDateDisplayLocale-int) | Allows to set/get the language format for the date displayed in this **SDT**. |
| [setDateStorageFormat(int value)](#setDateStorageFormat-int) | Gets/sets format in which the date for a date SDT is stored when the **SDT** is bound to an XML node in the document's data store. |
| [setFullDate(Date value)](#setFullDate-java.util.Date) | Specifies the full date and time last entered into this **SDT**. |
| [setLockContentControl(boolean value)](#setLockContentControl-boolean) | When set to  true , this property will prohibit a user from deleting this **SDT**. |
| [setLockContents(boolean value)](#setLockContents-boolean) | When set to  true , this property will prohibit a user from editing the contents of this **SDT**. |
| [setMultiline(boolean value)](#setMultiline-boolean) | Specifies whether this **SDT** allows multiple lines of text. |
| [setPlaceholderName(String value)](#setPlaceholderName-java.lang.String) | Gets or sets Name of the [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text. |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style) | Sets the Style of the structured document tag. |
| [setStyleName(String value)](#setStyleName-java.lang.String) | Sets the name of the style applied to the structured document tag. |
| [setTag(String value)](#setTag-java.lang.String) | Specifies a tag associated with the current SDT node. |
| [setTitle(String value)](#setTitle-java.lang.String) | Specifies the friendly name associated with this **SDT**. |
| [setUncheckedSymbol(int characterCode, String fontName)](#setUncheckedSymbol-int-java.lang.String) | Sets the symbol used to represent the unchecked state of a check box content control. |
| [structuredDocumentTagNode()](#structuredDocumentTagNode) |  |
| [toString()](#toString) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions) | Exports the content of the node into a string using the specified save options. |
| [toString(int saveFormat)](#toString-int) |  |
### StructuredDocumentTag(DocumentBase doc, int type, int level) {#StructuredDocumentTag-com.aspose.words.DocumentBase-int-int}
```
public StructuredDocumentTag(DocumentBase doc, int type, int level)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| type | int |  |
| level | int |  |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

 **Remarks:** 

Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../com.aspose.words/documentvisitor/).

For more info see the Visitor design pattern.

Calls [DocumentVisitor.visitStructuredDocumentTagStart(com.aspose.words.StructuredDocumentTag)](../../com.aspose.words/documentvisitor/\#visitStructuredDocumentTagStart-com.aspose.words.StructuredDocumentTag), then calls [Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node/\#accept-com.aspose.words.DocumentVisitor) for all child nodes of the smart tag and calls [DocumentVisitor.visitStructuredDocumentTagEnd(com.aspose.words.StructuredDocumentTag)](../../com.aspose.words/documentvisitor/\#visitStructuredDocumentTagEnd-com.aspose.words.StructuredDocumentTag) at the end.

 **Examples:** 

Shows how to print the node structure of every structured document tag in a document.

```

 public void structuredDocumentTagToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     StructuredDocumentTagNodePrinter visitor = new StructuredDocumentTagNodePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered StructuredDocumentTag nodes and their children.
 /// 
 public static class StructuredDocumentTagNodePrinter extends DocumentVisitor {
     public StructuredDocumentTagNodePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideStructuredDocumentTag = false;
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         if (mVisitorIsInsideStructuredDocumentTag) {
             indentAndAppendLine("[Run] \"" + run.getText() + "\"");
         }

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a StructuredDocumentTag node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagStart(final StructuredDocumentTag sdt) {
         indentAndAppendLine("[StructuredDocumentTag start] Title: " + sdt.getTitle());
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a StructuredDocumentTag node have been visited.
     /// 
     public int visitStructuredDocumentTagEnd(final StructuredDocumentTag sdt) {
         mDocTraversalDepth--;
         indentAndAppendLine("[StructuredDocumentTag end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private final boolean mVisitorIsInsideStructuredDocumentTag;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | The visitor that will visit the nodes. |

**Returns:**
boolean - True if all nodes were visited; false if [DocumentVisitor](../../com.aspose.words/documentvisitor/) stopped the operation before visiting all nodes.
### acceptEnd(DocumentVisitor visitor) {#acceptEnd-com.aspose.words.DocumentVisitor}
```
public int acceptEnd(DocumentVisitor visitor)
```


Accepts a visitor for visiting the end of the StructuredDocumentTag.

 **Examples:** 

Shows how to print the node structure of every structured document tag in a document.

```

 public void structuredDocumentTagToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     StructuredDocumentTagNodePrinter visitor = new StructuredDocumentTagNodePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered StructuredDocumentTag nodes and their children.
 /// 
 public static class StructuredDocumentTagNodePrinter extends DocumentVisitor {
     public StructuredDocumentTagNodePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideStructuredDocumentTag = false;
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         if (mVisitorIsInsideStructuredDocumentTag) {
             indentAndAppendLine("[Run] \"" + run.getText() + "\"");
         }

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a StructuredDocumentTag node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagStart(final StructuredDocumentTag sdt) {
         indentAndAppendLine("[StructuredDocumentTag start] Title: " + sdt.getTitle());
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a StructuredDocumentTag node have been visited.
     /// 
     public int visitStructuredDocumentTagEnd(final StructuredDocumentTag sdt) {
         mDocTraversalDepth--;
         indentAndAppendLine("[StructuredDocumentTag end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private final boolean mVisitorIsInsideStructuredDocumentTag;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | The document visitor. |

**Returns:**
int - The action to be taken by the visitor. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction/) constants.
### acceptStart(DocumentVisitor visitor) {#acceptStart-com.aspose.words.DocumentVisitor}
```
public int acceptStart(DocumentVisitor visitor)
```


Accepts a visitor for visiting the start of the StructuredDocumentTag.

 **Examples:** 

Shows how to print the node structure of every structured document tag in a document.

```

 public void structuredDocumentTagToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     StructuredDocumentTagNodePrinter visitor = new StructuredDocumentTagNodePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered StructuredDocumentTag nodes and their children.
 /// 
 public static class StructuredDocumentTagNodePrinter extends DocumentVisitor {
     public StructuredDocumentTagNodePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideStructuredDocumentTag = false;
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         if (mVisitorIsInsideStructuredDocumentTag) {
             indentAndAppendLine("[Run] \"" + run.getText() + "\"");
         }

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a StructuredDocumentTag node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagStart(final StructuredDocumentTag sdt) {
         indentAndAppendLine("[StructuredDocumentTag start] Title: " + sdt.getTitle());
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a StructuredDocumentTag node have been visited.
     /// 
     public int visitStructuredDocumentTagEnd(final StructuredDocumentTag sdt) {
         mDocTraversalDepth--;
         indentAndAppendLine("[StructuredDocumentTag end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private final boolean mVisitorIsInsideStructuredDocumentTag;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | The document visitor. |

**Returns:**
int - The action to be taken by the visitor. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction/) constants.
### clear() {#clear}
```
public void clear()
```


Clears contents of this structured document tag and displays a placeholder if it is defined.

 **Remarks:** 

It is not possible to clear contents of a structured document tag if it has revisions.

If this structured document tag is mapped to custom XML (with using the [getXmlMapping()](../../com.aspose.words/structureddocumenttag/\#getXmlMapping) property), the referenced XML node is cleared.

 **Examples:** 

Shows how to delete contents of structured document tag elements.

```

 Document doc = new Document();

 // Create a plain text structured document tag, and then append it to the document.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.BLOCK);
 doc.getFirstSection().getBody().appendChild(tag);

 // This structured document tag, which is in the form of a text box, already displays placeholder text.
 Assert.assertEquals("Click here to enter text.", tag.getText().trim());
 Assert.assertTrue(tag.isShowingPlaceholderText());

 // Create a building block with text contents.
 GlossaryDocument glossaryDoc = doc.getGlossaryDocument();
 BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
 substituteBlock.setName("My placeholder");
 substituteBlock.appendChild(new Section(glossaryDoc));
 substituteBlock.getFirstSection().ensureMinimum();
 substituteBlock.getFirstSection().getBody().getFirstParagraph().appendChild(new Run(glossaryDoc, "Custom placeholder text."));
 glossaryDoc.appendChild(substituteBlock);

 // Set the structured document tag's "PlaceholderName" property to our building block's name to get
 // the structured document tag to display the contents of the building block in place of the original default text.
 tag.setPlaceholderName("My placeholder");

 Assert.assertEquals("Custom placeholder text.", tag.getText().trim());
 Assert.assertTrue(tag.isShowingPlaceholderText());

 // Edit the text of the structured document tag and hide the placeholder text.
 Run run = (Run) tag.getChild(NodeType.RUN, 0, true);
 run.setText("New text.");
 tag.isShowingPlaceholderText(false);

 Assert.assertEquals("New text.", tag.getText().trim());

 // Use the "Clear" method to clear this structured document tag's contents and display the placeholder again.
 tag.clear();

 Assert.assertTrue(tag.isShowingPlaceholderText());
 Assert.assertEquals("Custom placeholder text.", tag.getText().trim());
 
```

### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




### dd() {#dd}
```
public void dd()
```




### deepClone(boolean isCloneChildren) {#deepClone-boolean}
```
public Node deepClone(boolean isCloneChildren)
```


Creates a duplicate of the node.

 **Remarks:** 

This method serves as a copy constructor for nodes. The cloned node has no parent, but belongs to the same document as the original node.

This method always performs a deep copy of the node. The  isCloneChildren  parameter specifies whether to perform copy all child nodes as well.

 **Examples:** 

Shows how to clone a composite node.

```

 Document doc = new Document();
 Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();
 para.appendChild(new Run(doc, "Hello world!"));

 // Below are two ways of cloning a composite node.
 // 1 -  Create a clone of a node, and create a clone of each of its child nodes as well.
 Node cloneWithChildren = para.deepClone(true);

 Assert.assertTrue(((CompositeNode) cloneWithChildren).hasChildNodes());
 Assert.assertEquals("Hello world!", cloneWithChildren.getText().trim());

 // 2 -  Create a clone of a node just by itself without any children.
 Node cloneWithoutChildren = para.deepClone(false);

 Assert.assertFalse(((CompositeNode) cloneWithoutChildren).hasChildNodes());
 Assert.assertEquals("", cloneWithoutChildren.getText().trim());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| isCloneChildren | boolean | True to recursively clone the subtree under the specified node; false to clone only the node itself. |

**Returns:**
[Node](../../com.aspose.words/node/) - The cloned node.
### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getAncestor(int ancestorType) {#getAncestor-int}
```
public CompositeNode getAncestor(int ancestorType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ancestorType | int |  |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/)
### getAncestor(Class ancestorType) {#getAncestor-java.lang.Class}
```
public CompositeNode getAncestor(Class ancestorType)
```


Gets the first ancestor of the specified object type.

 **Remarks:** 

The ancestor type matches if it is equal to  ancestorType  or derived from  ancestorType .

 **Examples:** 

Shows how to find out if a tables are nested.

```

 public void calculateDepthOfNestedTables() throws Exception {
     Document doc = new Document(getMyDir() + "Nested tables.docx");
     NodeCollection tables = doc.getChildNodes(NodeType.TABLE, true);
     for (int i = 0; i < tables.getCount(); i++) {
         Table table = (Table) tables.get(i);

         // Find out if any cells in the table have other tables as children.
         int count = getChildTableCount(table);
         System.out.print(MessageFormat.format("Table #{0} has {1} tables directly within its cells", i, count));

         // Find out if the table is nested inside another table, and, if so, at what depth.
         int tableDepth = getNestedDepthOfTable(table);

         if (tableDepth > 0)
             System.out.println(MessageFormat.format("Table #{0} is nested inside another table at depth of {1}", i, tableDepth));
         else
             System.out.println(MessageFormat.format("Table #{0} is a non nested table (is not a child of another table)", i));
     }
 }

 // Calculates what level a table is nested inside other tables.
 //
 // Returns An integer containing the level the table is nested at.
 // 0 = Table is not nested inside any other table
 // 1 = Table is nested within one parent table
 // 2 = Table is nested within two parent tables etc..
 private static int getNestedDepthOfTable(final Table table) {
     int depth = 0;
     Node parent = table.getAncestor(table.getNodeType());

     while (parent != null) {
         depth++;
         parent = parent.getAncestor(Table.class);
     }

     return depth;
 }

 // Determines if a table contains any immediate child table within its cells.
 // Does not recursively traverse through those tables to check for further tables.
 //
 // Returns true if at least one child cell contains a table.
 // Returns false if no cells in the table contains a table.
 private static int getChildTableCount(final Table table) {
     int childTableCount = 0;

     for (Row row : table.getRows()) {
         for (Cell cell : row.getCells()) {
             TableCollection childTables = cell.getTables();

             if (childTables.getCount() > 0) childTableCount++;
         }
     }

     return childTableCount;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ancestorType | java.lang.Class | The object type of the ancestor to retrieve. |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The ancestor of the specified type or  null  if no ancestor of this type was found.
### getAppearance() {#getAppearance}
```
public int getAppearance()
```


Gets/sets the appearance of a structured document tag.

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
int - The corresponding  int  value. The returned value is one of [SdtAppearance](../../com.aspose.words/sdtappearance/) constants.
### getBuildingBlockCategory() {#getBuildingBlockCategory}
```
public String getBuildingBlockCategory()
```


Specifies category of building block for this **SDT** node. Can not be  null .

 **Remarks:** 

Accessing this property will only work for [SdtType.BUILDING\_BLOCK\_GALLERY](../../com.aspose.words/sdttype/\#BUILDING-BLOCK-GALLERY) and [SdtType.DOC\_PART\_OBJ](../../com.aspose.words/sdttype/\#DOC-PART-OBJ) SDT types. It is read-only for **SDT** of the document part type.

For all other SDT types exception will occur.

 **Examples:** 

Shows how to insert a structured document tag as a building block, and set its category and gallery.

```

 Document doc = new Document();

 StructuredDocumentTag buildingBlockSdt =
         new StructuredDocumentTag(doc, SdtType.BUILDING_BLOCK_GALLERY, MarkupLevel.BLOCK);
 buildingBlockSdt.setBuildingBlockCategory("Built-in");
 buildingBlockSdt.setBuildingBlockGallery("Table of Contents");

 doc.getFirstSection().getBody().appendChild(buildingBlockSdt);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.BuildingBlockCategories.docx");
 
```

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getBuildingBlockGallery() {#getBuildingBlockGallery}
```
public String getBuildingBlockGallery()
```


Specifies type of building block for this **SDT**. Can not be  null .

 **Remarks:** 

Accessing this property will only work for [SdtType.BUILDING\_BLOCK\_GALLERY](../../com.aspose.words/sdttype/\#BUILDING-BLOCK-GALLERY) and [SdtType.DOC\_PART\_OBJ](../../com.aspose.words/sdttype/\#DOC-PART-OBJ) SDT types. It is read-only for **SDT** of the document part type.

For all other SDT types exception will occur.

 **Examples:** 

Shows how to insert a structured document tag as a building block, and set its category and gallery.

```

 Document doc = new Document();

 StructuredDocumentTag buildingBlockSdt =
         new StructuredDocumentTag(doc, SdtType.BUILDING_BLOCK_GALLERY, MarkupLevel.BLOCK);
 buildingBlockSdt.setBuildingBlockCategory("Built-in");
 buildingBlockSdt.setBuildingBlockGallery("Table of Contents");

 doc.getFirstSection().getBody().appendChild(buildingBlockSdt);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.BuildingBlockCategories.docx");
 
```

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getCalendarType() {#getCalendarType}
```
public int getCalendarType()
```


Specifies the type of calendar for this **SDT**. Default is [SdtCalendarType.DEFAULT](../../com.aspose.words/sdtcalendartype/\#DEFAULT)

 **Remarks:** 

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype/\#DATE) SDT type.

For all other SDT types exception will occur.

 **Examples:** 

Shows how to prompt the user to enter a date with a structured document tag.

```

 Document doc = new Document();

 // Insert a structured document tag that prompts the user to enter a date.
 // In Microsoft Word, this element is known as a "Date picker content control".
 // When we click on the arrow on the right end of this tag in Microsoft Word,
 // we will see a pop up in the form of a clickable calendar.
 // We can use that popup to select a date that the tag will display.
 StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.DATE, MarkupLevel.INLINE);

 // Display the date, according to the Saudi Arabian Arabic locale.
 sdtDate.setDateDisplayLocale(1025);

 // Set the format with which to display the date.
 sdtDate.setDateDisplayFormat("dd MMMM, yyyy");
 sdtDate.setDateStorageFormat(SdtDateStorageFormat.DATE_TIME);

 // Display the date according to the Hijri calendar.
 sdtDate.setCalendarType(SdtCalendarType.HIJRI);

 // Before the user chooses a date in Microsoft Word, the tag will display the text "Click here to enter a date.".
 // According to the tag's calendar, set the "FullDate" property to get the tag to display a default date.
 Calendar cal = Calendar.getInstance();
 cal.set(1440, 10, 20);
 sdtDate.setFullDate(cal.getTime());

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(sdtDate);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Date.docx");
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [SdtCalendarType](../../com.aspose.words/sdtcalendartype/) constants.
### getChecked() {#getChecked}
```
public boolean getChecked()
```


Gets/Sets current state of the Checkbox **SDT**. Default value for this property is  false .

 **Remarks:** 

Accessing this property will only work for [SdtType.CHECKBOX](../../com.aspose.words/sdttype/\#CHECKBOX) SDT types.

For all other SDT types exception will occur.

 **Examples:** 

Show how to create a structured document tag in the form of a check box.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 StructuredDocumentTag sdtCheckBox = new StructuredDocumentTag(doc, SdtType.CHECKBOX, MarkupLevel.INLINE);
 sdtCheckBox.setChecked(true);
 sdtCheckBox.setCheckedSymbol(0x00A9, "Times New Roman");
 sdtCheckBox.setUncheckedSymbol(0x00AE, "Times New Roman");

 builder.insertNode(sdtCheckBox);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.CheckBox.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getChild(int nodeType, int index, boolean isDeep) {#getChild-int-int-boolean}
```
public Node getChild(int nodeType, int index, boolean isDeep)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | int |  |
| index | int |  |
| isDeep | boolean |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### getChildNodes(int nodeType, boolean isDeep) {#getChildNodes-int-boolean}
```
public NodeCollection getChildNodes(int nodeType, boolean isDeep)
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
public Color getColor()
```


Gets the color of the structured document tag.

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
java.awt.Color - The color of the structured document tag.
### getContainer() {#getContainer}
```
public CompositeNode getContainer()
```




**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/)
### getContentsFont() {#getContentsFont}
```
public Font getContentsFont()
```


Font formatting that will be applied to text entered into **SDT**.

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
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of immediate children of this node.

 **Examples:** 

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```

 Document doc = new Document();

 // An empty document, by default, has one paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getParagraphs().getCount());

 // Composite nodes such as our paragraph can contain other composite and inline nodes as children.
 Paragraph paragraph = doc.getFirstSection().getBody().getFirstParagraph();
 Run paragraphText = new Run(doc, "Initial text. ");
 paragraph.appendChild(paragraphText);

 // Create three more run nodes.
 Run run1 = new Run(doc, "Run 1. ");
 Run run2 = new Run(doc, "Run 2. ");
 Run run3 = new Run(doc, "Run 3. ");

 // The document body will not display these runs until we insert them into a composite node
 // that itself is a part of the document's node tree, as we did with the first run.
 // We can determine where the text contents of nodes that we insert
 // appears in the document by specifying an insertion location relative to another node in the paragraph.
 Assert.assertEquals("Initial text.", paragraph.getText().trim());

 // Insert the second run into the paragraph in front of the initial run.
 paragraph.insertBefore(run2, paragraphText);

 Assert.assertEquals("Run 2. Initial text.", paragraph.getText().trim());

 // Insert the third run after the initial run.
 paragraph.insertAfter(run3, paragraphText);

 Assert.assertEquals("Run 2. Initial text. Run 3.", paragraph.getText().trim());

 // Insert the first run to the start of the paragraph's child nodes collection.
 paragraph.prependChild(run1);

 Assert.assertEquals("Run 1. Run 2. Initial text. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(4, paragraph.getChildNodes(NodeType.ANY, true).getCount());

 // We can modify the contents of the run by editing and deleting existing child nodes.
 ((Run) paragraph.getChildNodes(NodeType.RUN, true).get(1)).setText("Updated run 2. ");
 paragraph.getChildNodes(NodeType.RUN, true).remove(paragraphText);

 Assert.assertEquals("Run 1. Updated run 2. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, true).getCount());
 
```

**Returns:**
int - The number of immediate children of this node.
### getCurrentNode() {#getCurrentNode}
```
public Node getCurrentNode()
```




**Returns:**
[Node](../../com.aspose.words/node/)
### getCustomNodeId() {#getCustomNodeId}
```
public int getCustomNodeId()
```


Specifies custom node identifier.

 **Remarks:** 

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

 **Examples:** 

Shows how to traverse through a composite node's collection of child nodes.

```

 Document doc = new Document();

 // Add two runs and one shape as child nodes to the first paragraph of this document.
 Paragraph paragraph = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);
 paragraph.appendChild(new Run(doc, "Hello world! "));

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 shape.setWidth(200.0);
 shape.setHeight(200.0);
 // Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
 shape.setCustomNodeId(100);
 shape.setWrapType(WrapType.INLINE);
 paragraph.appendChild(shape);

 paragraph.appendChild(new Run(doc, "Hello again!"));

 // Iterate through the paragraph's collection of immediate children,
 // and print any runs or shapes that we find within.
 NodeCollection children = paragraph.getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, false).getCount());

 for (Node child : (Iterable) children)
     switch (child.getNodeType()) {
         case NodeType.RUN:
             System.out.println("Run contents:");
             System.out.println(MessageFormat.format("\t\"{0}\"", child.getText().trim()));
             break;
         case NodeType.SHAPE:
             Shape childShape = (Shape)child;
             System.out.println("Shape:");
             System.out.println(MessageFormat.format("\t{0}, {1}x{2}", childShape.getShapeType(), childShape.getWidth(), childShape.getHeight()));
             break;
     }
 
```

**Returns:**
int - The corresponding  int  value.
### getDateDisplayFormat() {#getDateDisplayFormat}
```
public String getDateDisplayFormat()
```


String that represents the format in which dates are displayed.

 **Remarks:** 

Can not be  null .

The dates for English (U.S.) is "mm/dd/yyyy"

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype/\#DATE) SDT type.

For all other SDT types exception will occur.

 **Examples:** 

Shows how to prompt the user to enter a date with a structured document tag.

```

 Document doc = new Document();

 // Insert a structured document tag that prompts the user to enter a date.
 // In Microsoft Word, this element is known as a "Date picker content control".
 // When we click on the arrow on the right end of this tag in Microsoft Word,
 // we will see a pop up in the form of a clickable calendar.
 // We can use that popup to select a date that the tag will display.
 StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.DATE, MarkupLevel.INLINE);

 // Display the date, according to the Saudi Arabian Arabic locale.
 sdtDate.setDateDisplayLocale(1025);

 // Set the format with which to display the date.
 sdtDate.setDateDisplayFormat("dd MMMM, yyyy");
 sdtDate.setDateStorageFormat(SdtDateStorageFormat.DATE_TIME);

 // Display the date according to the Hijri calendar.
 sdtDate.setCalendarType(SdtCalendarType.HIJRI);

 // Before the user chooses a date in Microsoft Word, the tag will display the text "Click here to enter a date.".
 // According to the tag's calendar, set the "FullDate" property to get the tag to display a default date.
 Calendar cal = Calendar.getInstance();
 cal.set(1440, 10, 20);
 sdtDate.setFullDate(cal.getTime());

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(sdtDate);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Date.docx");
 
```

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getDateDisplayLocale() {#getDateDisplayLocale}
```
public int getDateDisplayLocale()
```


Allows to set/get the language format for the date displayed in this **SDT**.

 **Remarks:** 

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype/\#DATE) SDT type.

For all other SDT types exception will occur.

 **Examples:** 

Shows how to prompt the user to enter a date with a structured document tag.

```

 Document doc = new Document();

 // Insert a structured document tag that prompts the user to enter a date.
 // In Microsoft Word, this element is known as a "Date picker content control".
 // When we click on the arrow on the right end of this tag in Microsoft Word,
 // we will see a pop up in the form of a clickable calendar.
 // We can use that popup to select a date that the tag will display.
 StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.DATE, MarkupLevel.INLINE);

 // Display the date, according to the Saudi Arabian Arabic locale.
 sdtDate.setDateDisplayLocale(1025);

 // Set the format with which to display the date.
 sdtDate.setDateDisplayFormat("dd MMMM, yyyy");
 sdtDate.setDateStorageFormat(SdtDateStorageFormat.DATE_TIME);

 // Display the date according to the Hijri calendar.
 sdtDate.setCalendarType(SdtCalendarType.HIJRI);

 // Before the user chooses a date in Microsoft Word, the tag will display the text "Click here to enter a date.".
 // According to the tag's calendar, set the "FullDate" property to get the tag to display a default date.
 Calendar cal = Calendar.getInstance();
 cal.set(1440, 10, 20);
 sdtDate.setFullDate(cal.getTime());

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(sdtDate);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Date.docx");
 
```

**Returns:**
int - The corresponding  int  value.
### getDateStorageFormat() {#getDateStorageFormat}
```
public int getDateStorageFormat()
```


Gets/sets format in which the date for a date SDT is stored when the **SDT** is bound to an XML node in the document's data store. Default value is [SdtDateStorageFormat.DATE\_TIME](../../com.aspose.words/sdtdatestorageformat/\#DATE-TIME)

 **Remarks:** 

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype/\#DATE) SDT type.

For all other SDT types exception will occur.

 **Examples:** 

Shows how to prompt the user to enter a date with a structured document tag.

```

 Document doc = new Document();

 // Insert a structured document tag that prompts the user to enter a date.
 // In Microsoft Word, this element is known as a "Date picker content control".
 // When we click on the arrow on the right end of this tag in Microsoft Word,
 // we will see a pop up in the form of a clickable calendar.
 // We can use that popup to select a date that the tag will display.
 StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.DATE, MarkupLevel.INLINE);

 // Display the date, according to the Saudi Arabian Arabic locale.
 sdtDate.setDateDisplayLocale(1025);

 // Set the format with which to display the date.
 sdtDate.setDateDisplayFormat("dd MMMM, yyyy");
 sdtDate.setDateStorageFormat(SdtDateStorageFormat.DATE_TIME);

 // Display the date according to the Hijri calendar.
 sdtDate.setCalendarType(SdtCalendarType.HIJRI);

 // Before the user chooses a date in Microsoft Word, the tag will display the text "Click here to enter a date.".
 // According to the tag's calendar, set the "FullDate" property to get the tag to display a default date.
 Calendar cal = Calendar.getInstance();
 cal.set(1440, 10, 20);
 sdtDate.setFullDate(cal.getTime());

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(sdtDate);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Date.docx");
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [SdtDateStorageFormat](../../com.aspose.words/sdtdatestorageformat/) constants.
### getDirectRunAttr(int key) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Gets the document to which this node belongs.

 **Remarks:** 

The node always belongs to a document even if it has just been created and not yet added to the tree, or if it has been removed from the tree.

 **Examples:** 

Shows how to create a node and set its owning document.

```

 Document doc = new Document();
 Paragraph para = new Paragraph(doc);
 para.appendChild(new Run(doc, "Hello world!"));

 // We have not yet appended this paragraph as a child to any composite node.
 Assert.assertNull(para.getParentNode());

 // If a node is an appropriate child node type of another composite node,
 // we can attach it as a child only if both nodes have the same owner document.
 // The owner document is the document we passed to the node's constructor.
 // We have not attached this paragraph to the document, so the document does not contain its text.
 Assert.assertEquals(para.getDocument(), doc);
 Assert.assertEquals("", doc.getText().trim());

 // Since the document owns this paragraph, we can apply one of its styles to the paragraph's contents.
 para.getParagraphFormat().setStyleName("Heading 1");

 // Add this node to the document, and then verify its contents.
 doc.getFirstSection().getBody().appendChild(para);

 Assert.assertEquals(doc.getFirstSection().getBody(), para.getParentNode());
 Assert.assertEquals("Hello world!", doc.getText().trim());
 
```

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/) - The document to which this node belongs.
### getEndCharacterFont() {#getEndCharacterFont}
```
public Font getEndCharacterFont()
```


Font formatting that will be applied to the last character of text entered into **SDT**.

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
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getFirstChild() {#getFirstChild}
```
public Node getFirstChild()
```


Gets the first child of the node.

 **Remarks:** 

If there is no first child node, a  null  is returned.

 **Examples:** 

Shows how to use a node's NextSibling property to enumerate through its immediate children.

```

 Document doc = new Document(getMyDir() + "Paragraphs.docx");

 for (Node node = doc.getFirstSection().getBody().getFirstChild(); node != null; node = node.getNextSibling()) {
     System.out.println(Node.nodeTypeToString(node.getNodeType()));
 }
 
```

Shows how to traverse a composite node's tree of child nodes.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(MessageFormat.format(" - \"{0}\"", childNode.getText().trim()));
         } else {
             System.out.println();
         }
     }
 }
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The first child of the node.
### getFullDate() {#getFullDate}
```
public Date getFullDate()
```


Specifies the full date and time last entered into this **SDT**.

 **Remarks:** 

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype/\#DATE) SDT type.

For all other SDT types exception will occur.

 **Examples:** 

Shows how to prompt the user to enter a date with a structured document tag.

```

 Document doc = new Document();

 // Insert a structured document tag that prompts the user to enter a date.
 // In Microsoft Word, this element is known as a "Date picker content control".
 // When we click on the arrow on the right end of this tag in Microsoft Word,
 // we will see a pop up in the form of a clickable calendar.
 // We can use that popup to select a date that the tag will display.
 StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.DATE, MarkupLevel.INLINE);

 // Display the date, according to the Saudi Arabian Arabic locale.
 sdtDate.setDateDisplayLocale(1025);

 // Set the format with which to display the date.
 sdtDate.setDateDisplayFormat("dd MMMM, yyyy");
 sdtDate.setDateStorageFormat(SdtDateStorageFormat.DATE_TIME);

 // Display the date according to the Hijri calendar.
 sdtDate.setCalendarType(SdtCalendarType.HIJRI);

 // Before the user chooses a date in Microsoft Word, the tag will display the text "Click here to enter a date.".
 // According to the tag's calendar, set the "FullDate" property to get the tag to display a default date.
 Calendar cal = Calendar.getInstance();
 cal.set(1440, 10, 20);
 sdtDate.setFullDate(cal.getTime());

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(sdtDate);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Date.docx");
 
```

**Returns:**
java.util.Date - The corresponding java.util.Date value.
### getId() {#getId}
```
public int getId()
```


Specifies a unique read-only persistent numerical Id for this **SDT**.

 **Remarks:** 

Id attribute shall follow these rules:

 *  The document shall retain SDT ids only if the whole document is cloned [Document.deepClone()](../../com.aspose.words/document/\#deepClone).
 *  During [DocumentBase.importNode(com.aspose.words.Node, boolean)](../../com.aspose.words/documentbase/\#importNode-com.aspose.words.Node--boolean) Id shall be retained if import does not cause conflicts with other SDT Ids in the target document.
 *  If multiple SDT nodes specify the same decimal number value for the Id attribute, then the first SDT in the document shall maintain this original Id, and all subsequent SDT nodes shall have new identifiers assigned to them when the document is loaded.
 *  During standalone SDT **M:Aspose.Words.Markup.StructuredDocumentTag.Clone(System.Boolean,Aspose.Words.INodeCloningListener)** operation new unique ID will be generated for the cloned SDT node.
 *  If Id is not specified in the source document, then the SDT node shall have a new unique identifier assigned to it when the document is loaded.

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
int - The corresponding  int  value.
### getLastChild() {#getLastChild}
```
public Node getLastChild()
```


Gets the last child of the node.

 **Remarks:** 

If there is no last child node, a  null  is returned.

 **Examples:** 

Shows how to use of methods of Node and CompositeNode to remove a section before the last section in the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1 text.");
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("Section 2 text.");

 // Both sections are siblings of each other.
 Section lastSection = (Section) doc.getLastChild();
 Section firstSection = (Section) lastSection.getPreviousSibling();

 // Remove a section based on its sibling relationship with another section.
 if (lastSection.getPreviousSibling() != null)
     doc.removeChild(firstSection);

 // The section we removed was the first one, leaving the document with only the second.
 Assert.assertEquals("Section 2 text.", doc.getText().trim());
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The last child of the node.
### getLevel() {#getLevel}
```
public int getLevel()
```


Gets the level at which this **SDT** occurs in the document tree.

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
int - The level at which this **SDT** occurs in the document tree. The returned value is one of [MarkupLevel](../../com.aspose.words/markuplevel/) constants.
### getLevel_IMarkupNode() {#getLevel-IMarkupNode}
```
public int getLevel_IMarkupNode()
```




**Returns:**
int
### getListItems() {#getListItems}
```
public SdtListItemCollection getListItems()
```


Gets [SdtListItemCollection](../../com.aspose.words/sdtlistitemcollection/) associated with this **SDT**.

 **Remarks:** 

Accessing this property will only work for [SdtType.COMBO\_BOX](../../com.aspose.words/sdttype/\#COMBO-BOX) or [SdtType.DROP\_DOWN\_LIST](../../com.aspose.words/sdttype/\#DROP-DOWN-LIST) SDT types.

For all other SDT types exception will occur.

 **Examples:** 

Shows how to work with drop down-list structured document tags.

```

 Document doc = new Document();
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DROP_DOWN_LIST, MarkupLevel.BLOCK);
 doc.getFirstSection().getBody().appendChild(tag);

 // A drop-down list structured document tag is a form that allows the user to
 // select an option from a list by left-clicking and opening the form in Microsoft Word.
 // The "ListItems" property contains all list items, and each list item is an "SdtListItem".
 SdtListItemCollection listItems = tag.getListItems();
 listItems.add(new SdtListItem("Value 1"));

 Assert.assertEquals(listItems.get(0).getDisplayText(), listItems.get(0).getValue());

 // Add 3 more list items. Initialize these items using a different constructor to the first item
 // to display strings that are different from their values.
 listItems.add(new SdtListItem("Item 2", "Value 2"));
 listItems.add(new SdtListItem("Item 3", "Value 3"));
 listItems.add(new SdtListItem("Item 4", "Value 4"));

 Assert.assertEquals(4, listItems.getCount());

 // The drop-down list is displaying the first item. Assign a different list item to the "SelectedValue" to display it.
 listItems.setSelectedValue(listItems.get(3));

 Assert.assertEquals(listItems.getSelectedValue().getValue(), "Value 4");

 // Enumerate over the collection and print each element.
 Iterator enumerator = listItems.iterator();
 while (enumerator.hasNext()) {
     SdtListItem sdtListItem = enumerator.next();
     System.out.println(MessageFormat.format("List item: {0}, value: {1}", sdtListItem.getDisplayText(), sdtListItem.getValue()));
 }

 // Remove the last list item.
 listItems.removeAt(3);

 Assert.assertEquals(3, listItems.getCount());

 // Since our drop-down control is set to display the removed item by default, give it an item to display which exists.
 listItems.setSelectedValue(listItems.get(1));

 doc.save(getArtifactsDir() + "StructuredDocumentTag.ListItemCollection.docx");

 // Use the "Clear" method to empty the entire drop-down item collection at once.
 listItems.clear();

 Assert.assertEquals(0, listItems.getCount());
 
```

**Returns:**
[SdtListItemCollection](../../com.aspose.words/sdtlistitemcollection/) - [SdtListItemCollection](../../com.aspose.words/sdtlistitemcollection/) associated with this **SDT**.
### getLockContentControl() {#getLockContentControl}
```
public boolean getLockContentControl()
```


When set to  true , this property will prohibit a user from deleting this **SDT**.

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
public boolean getLockContents()
```


When set to  true , this property will prohibit a user from editing the contents of this **SDT**.

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
### getMultiline() {#getMultiline}
```
public boolean getMultiline()
```


Specifies whether this **SDT** allows multiple lines of text.

 **Remarks:** 

Accessing this property will only work for [SdtType.RICH\_TEXT](../../com.aspose.words/sdttype/\#RICH-TEXT) and [SdtType.PLAIN\_TEXT](../../com.aspose.words/sdttype/\#PLAIN-TEXT) SDT type.

For all other SDT types exception will occur.

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
boolean - The corresponding  boolean  value.
### getNextMatchingNode(Node curNode) {#getNextMatchingNode-com.aspose.words.Node}
```
public Node getNextMatchingNode(Node curNode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node/) |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### getNextSibling() {#getNextSibling}
```
public Node getNextSibling()
```


Gets the node immediately following this node.

 **Remarks:** 

If there is no next node, a  null  is returned.

 **Examples:** 

Shows how to use a node's NextSibling property to enumerate through its immediate children.

```

 Document doc = new Document(getMyDir() + "Paragraphs.docx");

 for (Node node = doc.getFirstSection().getBody().getFirstChild(); node != null; node = node.getNextSibling()) {
     System.out.println(Node.nodeTypeToString(node.getNodeType()));
 }
 
```

Shows how to traverse a composite node's tree of child nodes.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(MessageFormat.format(" - \"{0}\"", childNode.getText().trim()));
         } else {
             System.out.println();
         }
     }
 }
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The node immediately following this node.
### getNode() {#getNode}
```
public Node getNode()
```


Returns Node object that implements this interface.

**Returns:**
[Node](../../com.aspose.words/node/)
### getNodeType() {#getNodeType}
```
public int getNodeType()
```


Returns [NodeType.STRUCTURED\_DOCUMENT\_TAG](../../com.aspose.words/nodetype/\#STRUCTURED-DOCUMENT-TAG).

 **Examples:** 

Shows how to work with styles for content control elements.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways to apply a style from the document to a structured document tag.
 // 1 -  Apply a style object from the document's style collection:
 Style quoteStyle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.QUOTE);
 StructuredDocumentTag sdtPlainText = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);
 sdtPlainText.setStyle(quoteStyle);

 // 2 -  Reference a style in the document by name:
 StructuredDocumentTag sdtRichText = new StructuredDocumentTag(doc, SdtType.RICH_TEXT, MarkupLevel.INLINE);
 sdtRichText.setStyleName("Quote");

 builder.insertNode(sdtPlainText);
 builder.insertNode(sdtRichText);

 Assert.assertEquals(NodeType.STRUCTURED_DOCUMENT_TAG, sdtPlainText.getNodeType());

 NodeCollection tags = doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG, true);

 for (StructuredDocumentTag sdt : (Iterable) tags) {
     Assert.assertEquals(StyleIdentifier.QUOTE, sdt.getStyle().getStyleIdentifier());
     Assert.assertEquals("Quote", sdt.getStyleName());
 }
 
```

**Returns:**
int - [NodeType.STRUCTURED\_DOCUMENT\_TAG](../../com.aspose.words/nodetype/\#STRUCTURED-DOCUMENT-TAG). The returned value is one of [NodeType](../../com.aspose.words/nodetype/) constants.
### getParentNode() {#getParentNode}
```
public CompositeNode getParentNode()
```


Gets the immediate parent of this node.

 **Remarks:** 

If a node has just been created and not yet added to the tree, or if it has been removed from the tree, the parent is  null .

 **Examples:** 

Shows how to access a node's parent node.

```

 Document doc = new Document();
 Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();

 // Append a child Run node to the document's first paragraph.
 Run run = new Run(doc, "Hello world!");
 para.appendChild(run);

 // The paragraph is the parent node of the run node. We can trace this lineage
 // all the way to the document node, which is the root of the document's node tree.
 Assert.assertEquals(para, run.getParentNode());
 Assert.assertEquals(doc.getFirstSection().getBody(), para.getParentNode());
 Assert.assertEquals(doc.getFirstSection(), doc.getFirstSection().getBody().getParentNode());
 Assert.assertEquals(doc, doc.getFirstSection().getParentNode());
 
```

Shows how to create a node and set its owning document.

```

 Document doc = new Document();
 Paragraph para = new Paragraph(doc);
 para.appendChild(new Run(doc, "Hello world!"));

 // We have not yet appended this paragraph as a child to any composite node.
 Assert.assertNull(para.getParentNode());

 // If a node is an appropriate child node type of another composite node,
 // we can attach it as a child only if both nodes have the same owner document.
 // The owner document is the document we passed to the node's constructor.
 // We have not attached this paragraph to the document, so the document does not contain its text.
 Assert.assertEquals(para.getDocument(), doc);
 Assert.assertEquals("", doc.getText().trim());

 // Since the document owns this paragraph, we can apply one of its styles to the paragraph's contents.
 para.getParagraphFormat().setStyleName("Heading 1");

 // Add this node to the document, and then verify its contents.
 doc.getFirstSection().getBody().appendChild(para);

 Assert.assertEquals(doc.getFirstSection().getBody(), para.getParentNode());
 Assert.assertEquals("Hello world!", doc.getText().trim());
 
```

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The immediate parent of this node.
### getPlaceholder() {#getPlaceholder}
```
public BuildingBlock getPlaceholder()
```


Gets the [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [getXmlMapping()](../../com.aspose.words/structureddocumenttag/\#getXmlMapping) element or the [isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttag/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttag/\#isShowingPlaceholderText-boolean) element is  true .

 **Remarks:** 

Can be  null , meaning that the placeholder is not applicable for this Sdt.

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
[BuildingBlock](../../com.aspose.words/buildingblock/) - The [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [getXmlMapping()](../../com.aspose.words/structureddocumenttag/\#getXmlMapping) element or the [isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttag/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttag/\#isShowingPlaceholderText-boolean) element is  true .
### getPlaceholderName() {#getPlaceholderName}
```
public String getPlaceholderName()
```


Gets or sets Name of the [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getPreviousSibling() {#getPreviousSibling}
```
public Node getPreviousSibling()
```


Gets the node immediately preceding this node.

 **Remarks:** 

If there is no preceding node, a  null  is returned.

 **Examples:** 

Shows how to use of methods of Node and CompositeNode to remove a section before the last section in the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1 text.");
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("Section 2 text.");

 // Both sections are siblings of each other.
 Section lastSection = (Section) doc.getLastChild();
 Section firstSection = (Section) lastSection.getPreviousSibling();

 // Remove a section based on its sibling relationship with another section.
 if (lastSection.getPreviousSibling() != null)
     doc.removeChild(firstSection);

 // The section we removed was the first one, leaving the document with only the second.
 Assert.assertEquals("Section 2 text.", doc.getText().trim());
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The node immediately preceding this node.
### getRange() {#getRange}
```
public Range getRange()
```


Returns a [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node.

 **Examples:** 

Shows how to delete all the nodes from a range.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add text to the first section in the document, and then add another section.
 builder.write("Section 1. ");
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.write("Section 2.");

 Assert.assertEquals("Section 1. \fSection 2.", doc.getText().trim());

 // Remove the first section entirely by removing all the nodes
 // within its range, including the section itself.
 doc.getSections().get(0).getRange().delete();

 Assert.assertEquals(1, doc.getSections().getCount());
 Assert.assertEquals("Section 2.", doc.getText().trim());
 
```

**Returns:**
[Range](../../com.aspose.words/range/) - A [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node.
### getSdtType() {#getSdtType}
```
public int getSdtType()
```


Gets type of this **Structured document tag**.

 **Examples:** 

Shows how to get the type of a structured document tag.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");

 List tags = Arrays.stream(doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG, true).toArray())
         .filter(StructuredDocumentTag.class::isInstance)
         .map(StructuredDocumentTag.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(SdtType.REPEATING_SECTION, tags.get(0).getSdtType());
 Assert.assertEquals(SdtType.REPEATING_SECTION_ITEM, tags.get(1).getSdtType());
 Assert.assertEquals(SdtType.RICH_TEXT, tags.get(2).getSdtType());
 
```

**Returns:**
int - Type of this **Structured document tag**. The returned value is one of [SdtType](../../com.aspose.words/sdttype/) constants.
### getStyle() {#getStyle}
```
public Style getStyle()
```


Gets the Style of the structured document tag.

 **Remarks:** 

Only [StyleType.CHARACTER](../../com.aspose.words/styletype/\#CHARACTER) style or [StyleType.PARAGRAPH](../../com.aspose.words/styletype/\#PARAGRAPH) style with linked character style can be set.

 **Examples:** 

Shows how to work with styles for content control elements.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways to apply a style from the document to a structured document tag.
 // 1 -  Apply a style object from the document's style collection:
 Style quoteStyle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.QUOTE);
 StructuredDocumentTag sdtPlainText = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);
 sdtPlainText.setStyle(quoteStyle);

 // 2 -  Reference a style in the document by name:
 StructuredDocumentTag sdtRichText = new StructuredDocumentTag(doc, SdtType.RICH_TEXT, MarkupLevel.INLINE);
 sdtRichText.setStyleName("Quote");

 builder.insertNode(sdtPlainText);
 builder.insertNode(sdtRichText);

 Assert.assertEquals(NodeType.STRUCTURED_DOCUMENT_TAG, sdtPlainText.getNodeType());

 NodeCollection tags = doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG, true);

 for (StructuredDocumentTag sdt : (Iterable) tags) {
     Assert.assertEquals(StyleIdentifier.QUOTE, sdt.getStyle().getStyleIdentifier());
     Assert.assertEquals("Quote", sdt.getStyleName());
 }
 
```

**Returns:**
[Style](../../com.aspose.words/style/) - The Style of the structured document tag.
### getStyleName() {#getStyleName}
```
public String getStyleName()
```


Gets the name of the style applied to the structured document tag.

 **Examples:** 

Shows how to work with styles for content control elements.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways to apply a style from the document to a structured document tag.
 // 1 -  Apply a style object from the document's style collection:
 Style quoteStyle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.QUOTE);
 StructuredDocumentTag sdtPlainText = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);
 sdtPlainText.setStyle(quoteStyle);

 // 2 -  Reference a style in the document by name:
 StructuredDocumentTag sdtRichText = new StructuredDocumentTag(doc, SdtType.RICH_TEXT, MarkupLevel.INLINE);
 sdtRichText.setStyleName("Quote");

 builder.insertNode(sdtPlainText);
 builder.insertNode(sdtRichText);

 Assert.assertEquals(NodeType.STRUCTURED_DOCUMENT_TAG, sdtPlainText.getNodeType());

 NodeCollection tags = doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG, true);

 for (StructuredDocumentTag sdt : (Iterable) tags) {
     Assert.assertEquals(StyleIdentifier.QUOTE, sdt.getStyle().getStyleIdentifier());
     Assert.assertEquals("Quote", sdt.getStyleName());
 }
 
```

**Returns:**
java.lang.String - The name of the style applied to the structured document tag.
### getTag() {#getTag}
```
public String getTag()
```


Specifies a tag associated with the current SDT node. Can not be  null .

 **Remarks:** 

A tag is an arbitrary string which applications can associate with SDT in order to identify it without providing a visible friendly name.

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
### getText() {#getText}
```
public String getText()
```


Gets the text of this node and of all its children.

 **Remarks:** 

The returned string includes all control and special characters as described in [ControlChar](../../com.aspose.words/controlchar/).

 **Examples:** 

Shows the difference between calling the GetText and ToString methods on a node.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertField("MERGEFIELD Field");

 // GetText will retrieve the visible text as well as field codes and special characters.
 Assert.assertEquals("MERGEFIELD Field«Field»\f", doc.getText());

 // ToString will give us the document's appearance if saved to a passed save format.
 Assert.assertEquals("«Field»\r\n", doc.toString(SaveFormat.TEXT));
 
```

Shows how to output all paragraphs in a document that are list items.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getListFormat().applyNumberDefault();
 builder.writeln("Numbered list item 1");
 builder.writeln("Numbered list item 2");
 builder.writeln("Numbered list item 3");
 builder.getListFormat().removeNumbers();

 builder.getListFormat().applyBulletDefault();
 builder.writeln("Bulleted list item 1");
 builder.writeln("Bulleted list item 2");
 builder.writeln("Bulleted list item 3");
 builder.getListFormat().removeNumbers();

 NodeCollection paras = doc.getChildNodes(NodeType.PARAGRAPH, true);
 for (Paragraph para : (Iterable) paras) {
     if (para.getListFormat().isListItem()) {
         System.out.println(java.text.MessageFormat.format("*** A paragraph belongs to list {0}", para.getListFormat().getList().getListId()));
         System.out.println(para.getText());
     }
 }
 
```

**Returns:**
java.lang.String
### getTitle() {#getTitle}
```
public String getTitle()
```


Specifies the friendly name associated with this **SDT**. Can not be  null .

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
### getWordOpenXML() {#getWordOpenXML}
```
public String getWordOpenXML()
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
### getWordOpenXMLMinimal() {#getWordOpenXMLMinimal}
```
public String getWordOpenXMLMinimal()
```


Gets a string that represents the XML contained within the node in the [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC) format. Unlike the [getWordOpenXML()](../../com.aspose.words/structureddocumenttag/\#getWordOpenXML) property, this method generates a stripped-down document that excludes any non-content-related parts.

 **Examples:** 

Shows how to work with styles for content control elements.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways to apply a style from the document to a structured document tag.
 // 1 -  Apply a style object from the document's style collection:
 Style quoteStyle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.QUOTE);
 StructuredDocumentTag sdtPlainText = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);
 sdtPlainText.setStyle(quoteStyle);

 // 2 -  Reference a style in the document by name:
 StructuredDocumentTag sdtRichText = new StructuredDocumentTag(doc, SdtType.RICH_TEXT, MarkupLevel.INLINE);
 sdtRichText.setStyleName("Quote");

 builder.insertNode(sdtPlainText);
 builder.insertNode(sdtRichText);

 Assert.assertEquals(NodeType.STRUCTURED_DOCUMENT_TAG, sdtPlainText.getNodeType());

 NodeCollection tags = doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG, true);

 for (StructuredDocumentTag sdt : (Iterable) tags) {
     Assert.assertEquals(StyleIdentifier.QUOTE, sdt.getStyle().getStyleIdentifier());
     Assert.assertEquals("Quote", sdt.getStyleName());
 }
 
```

**Returns:**
java.lang.String - A string that represents the XML contained within the node in the [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC) format.
### getXmlMapping() {#getXmlMapping}
```
public XmlMapping getXmlMapping()
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
### hasChildNodes() {#hasChildNodes}
```
public boolean hasChildNodes()
```


Returns  true  if this node has any child nodes.

 **Examples:** 

Shows how to combine the rows from two tables into one.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 // Below are two ways of getting a table from a document.
 // 1 -  From the "Tables" collection of a Body node:
 Table firstTable = doc.getFirstSection().getBody().getTables().get(0);

 // 2 -  Using the "GetChild" method:
 Table secondTable = (Table) doc.getChild(NodeType.TABLE, 1, true);

 // Append all rows from the current table to the next.
 while (secondTable.hasChildNodes())
     firstTable.getRows().add(secondTable.getFirstRow());

 // Remove the empty table container.
 secondTable.remove();

 doc.save(getArtifactsDir() + "Table.CombineTables.docx");
 
```

**Returns:**
boolean -  true  if this node has any child nodes.
### indexOf(Node child) {#indexOf-com.aspose.words.Node}
```
public int indexOf(Node child)
```


Returns the index of the specified child node in the child node array.

 **Remarks:** 

Returns -1 if the node is not found in the child nodes.

 **Examples:** 

Shows how to get the index of a given child node from its parent.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 Body body = doc.getFirstSection().getBody();

 // Retrieve the index of the last paragraph in the body of the first section.
 Assert.assertEquals(24, body.getChildNodes(NodeType.ANY, false).indexOf(body.getLastParagraph()));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| child | [Node](../../com.aspose.words/node/) |  |

**Returns:**
int
### isComposite() {#isComposite}
```
public boolean isComposite()
```


Returns  true  as this node can have child nodes.

 **Examples:** 

Shows how to traverse a composite node's tree of child nodes.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(MessageFormat.format(" - \"{0}\"", childNode.getText().trim()));
         } else {
             System.out.println();
         }
     }
 }
 
```

**Returns:**
boolean -  true  as this node can have child nodes.
### isMultiSection() {#isMultiSection}
```
public boolean isMultiSection()
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
boolean
### isRanged() {#isRanged}
```
public boolean isRanged()
```


Returns true if this instance is a ranged structured document tag.

**Returns:**
boolean
### isShowingPlaceholderText() {#isShowingPlaceholderText}
```
public boolean isShowingPlaceholderText()
```


Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT).

if set to  true , this state shall be resumed (showing placeholder text) upon opening this document.

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
public void isShowingPlaceholderText(boolean value)
```


Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT).

if set to  true , this state shall be resumed (showing placeholder text) upon opening this document.

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

### isTemporary() {#isTemporary}
```
public boolean isTemporary()
```


Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents are modified.

 **Examples:** 

Shows how to make single-use controls.

```

 Document doc = new Document();

 // Insert a plain text structured document tag,
 // which will act as a plain text form that the user may enter text into.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "IsTemporary" property to "true" to make the structured document tag disappear and
 // assimilate its contents into the document after the user edits it once in Microsoft Word.
 // Set the "IsTemporary" property to "false" to allow the user to edit the contents
 // of the structured document tag any number of times.
 tag.isTemporary(isTemporary);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("Please enter text: ");
 builder.insertNode(tag);

 // Insert another structured document tag in the form of a check box and set its default state to "checked".
 tag = new StructuredDocumentTag(doc, SdtType.CHECKBOX, MarkupLevel.INLINE);
 tag.setChecked(true);

 // Set the "IsTemporary" property to "true" to make the check box become a symbol
 // once the user clicks on it in Microsoft Word.
 // Set the "IsTemporary" property to "false" to allow the user to click on the check box any number of times.
 tag.isTemporary(isTemporary);

 builder.write("\nPlease click the check box: ");
 builder.insertNode(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.IsTemporary.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### isTemporary(boolean value) {#isTemporary-boolean}
```
public void isTemporary(boolean value)
```


Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents are modified.

 **Examples:** 

Shows how to make single-use controls.

```

 Document doc = new Document();

 // Insert a plain text structured document tag,
 // which will act as a plain text form that the user may enter text into.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "IsTemporary" property to "true" to make the structured document tag disappear and
 // assimilate its contents into the document after the user edits it once in Microsoft Word.
 // Set the "IsTemporary" property to "false" to allow the user to edit the contents
 // of the structured document tag any number of times.
 tag.isTemporary(isTemporary);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("Please enter text: ");
 builder.insertNode(tag);

 // Insert another structured document tag in the form of a check box and set its default state to "checked".
 tag = new StructuredDocumentTag(doc, SdtType.CHECKBOX, MarkupLevel.INLINE);
 tag.setChecked(true);

 // Set the "IsTemporary" property to "true" to make the check box become a symbol
 // once the user clicks on it in Microsoft Word.
 // Set the "IsTemporary" property to "false" to allow the user to click on the check box any number of times.
 tag.isTemporary(isTemporary);

 builder.write("\nPlease click the check box: ");
 builder.insertNode(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.IsTemporary.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### iterator() {#iterator}
```
public Iterator iterator()
```


Provides support for the for each style iteration over the child nodes of this node.

 **Examples:** 

Shows how to print all of a document's comments and their replies.

```

 Document doc = new Document(getMyDir() + "Comments.docx");

 NodeCollection comments = doc.getChildNodes(NodeType.COMMENT, true);
 // If a comment has no ancestor, it is a "top-level" comment as opposed to a reply-type comment.
 // Print all top-level comments along with any replies they may have.
 for (Comment comment : (Iterable) comments) {
     if (comment.getAncestor() == null) {
         System.out.println("Top-level comment:");
         System.out.println("\t\"{comment.GetText().Trim()}\", by {comment.Author}");
         System.out.println("Has {comment.Replies.Count} replies");
         for (Comment commentReply : comment.getReplies()) {
             System.out.println("\t\"{commentReply.GetText().Trim()}\", by {commentReply.Author}");
         }
         System.out.println();
     }
 }
 
```

**Returns:**
java.util.Iterator
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node}
```
public Node nextPreOrder(Node rootNode)
```


Gets next node according to the pre-order tree traversal algorithm.

 **Examples:** 

Shows how to traverse the document's node tree using the pre-order traversal algorithm, and delete any encountered shape with an image.

```

 Document doc = new Document(getMyDir() + "Images.docx");
 ArrayList shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(9, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));

 Node curNode = doc;
 while (curNode != null) {
     Node nextNode = curNode.nextPreOrder(doc);

     if (curNode.previousPreOrder(doc) != null && nextNode != null)
         Assert.assertEquals(curNode, nextNode.previousPreOrder(doc));

     if (curNode.getNodeType() == NodeType.SHAPE && ((Shape) curNode).hasImage())
         curNode.remove();

     curNode = nextNode;
 }

 shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(0, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | The top node (limit) of traversal. |

**Returns:**
[Node](../../com.aspose.words/node/) - Next node in pre-order order. Null if reached the  rootNode .
### nodeTypeToString(int nodeType) {#nodeTypeToString-int}
```
public static String nodeTypeToString(int nodeType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node}
```
public Node previousPreOrder(Node rootNode)
```


Gets the previous node according to the pre-order tree traversal algorithm.

 **Examples:** 

Shows how to traverse the document's node tree using the pre-order traversal algorithm, and delete any encountered shape with an image.

```

 Document doc = new Document(getMyDir() + "Images.docx");
 ArrayList shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(9, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));

 Node curNode = doc;
 while (curNode != null) {
     Node nextNode = curNode.nextPreOrder(doc);

     if (curNode.previousPreOrder(doc) != null && nextNode != null)
         Assert.assertEquals(curNode, nextNode.previousPreOrder(doc));

     if (curNode.getNodeType() == NodeType.SHAPE && ((Shape) curNode).hasImage())
         curNode.remove();

     curNode = nextNode;
 }

 shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(0, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | The top node (limit) of traversal. |

**Returns:**
[Node](../../com.aspose.words/node/) - Previous node in pre-order order. Null if reached the  rootNode .
### remove() {#remove}
```
public void remove()
```


Removes itself from the parent.

 **Examples:** 

Shows how to remove all child nodes of a specific type from a composite node.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Assert.assertEquals(2, doc.getChildNodes(NodeType.TABLE, true).getCount());

 Node curNode = doc.getFirstSection().getBody().getFirstChild();

 while (curNode != null) {
     // Save the next sibling node as a variable in case we want to move to it after deleting this node.
     Node nextNode = curNode.getNextSibling();

     // A section body can contain Paragraph and Table nodes.
     // If the node is a Table, remove it from the parent.
     if (curNode.getNodeType() == NodeType.TABLE) {
         curNode.remove();
     }

     curNode = nextNode;
 }

 Assert.assertEquals(0, doc.getChildNodes(NodeType.TABLE, true).getCount());
 
```

Shows how to delete all shapes with images from a document.

```

 Document doc = new Document(getMyDir() + "Images.docx");
 ArrayList shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(9, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));

 for (Shape shape : shapes)
     if (shape.hasImage())
         shape.remove();

 shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(0, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));
 
```

### removeAllChildren() {#removeAllChildren}
```
public void removeAllChildren()
```


Removes all the child nodes of the current node.

 **Examples:** 

Shows how to construct an Aspose.Words document by hand.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

### removeMoveRevisions() {#removeMoveRevisions}
```
public void removeMoveRevisions()
```




### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### removeSelfOnly() {#removeSelfOnly}
```
public void removeSelfOnly()
```


Removes just this SDT node itself, but keeps the content of it inside the document tree.

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

### removeSmartTags() {#removeSmartTags}
```
public void removeSmartTags()
```


Removes all [SmartTag](../../com.aspose.words/smarttag/) descendant nodes of the current node.

 **Remarks:** 

This method does not remove the content of the smart tags.

 **Examples:** 

Removes all smart tags from descendant nodes of a composite node.

```

 Document doc = new Document(getMyDir() + "Smart tags.doc");

 Assert.assertEquals(8, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());

 doc.removeSmartTags();

 Assert.assertEquals(0, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());
 
```

Shows how to create smart tags.

```

 public void create() throws Exception {
     Document doc = new Document();

     // A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
     // such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
     SmartTag smartTag = new SmartTag(doc);

     // Smart tags are composite nodes that contain their recognized text in its entirety.
     // Add contents to this smart tag manually.
     smartTag.appendChild(new Run(doc, "May 29, 2019"));

     // Microsoft Word may recognize the above contents as being a date.
     // Smart tags use the "Element" property to reflect the type of data they contain.
     smartTag.setElement("date");

     // Some smart tag types process their contents further into custom XML properties.
     smartTag.getProperties().add(new CustomXmlProperty("Day", "", "29"));
     smartTag.getProperties().add(new CustomXmlProperty("Month", "", "5"));
     smartTag.getProperties().add(new CustomXmlProperty("Year", "", "2019"));

     // Set the smart tag's URI to the default value.
     smartTag.setUri("urn:schemas-microsoft-com:office:smarttags");

     doc.getFirstSection().getBody().getFirstParagraph().appendChild(smartTag);
     doc.getFirstSection().getBody().getFirstParagraph().appendChild(new Run(doc, " is a date. "));

     // Create another smart tag for a stock ticker.
     smartTag = new SmartTag(doc);
     smartTag.setElement("stockticker");
     smartTag.setUri("urn:schemas-microsoft-com:office:smarttags");

     smartTag.appendChild(new Run(doc, "MSFT"));

     doc.getFirstSection().getBody().getFirstParagraph().appendChild(smartTag);
     doc.getFirstSection().getBody().getFirstParagraph().appendChild(new Run(doc, " is a stock ticker."));

     // Print all the smart tags in our document using a document visitor.
     doc.accept(new SmartTagPrinter());

     // Older versions of Microsoft Word support smart tags.
     doc.save(getArtifactsDir() + "SmartTag.Create.doc");

     // Use the "RemoveSmartTags" method to remove all smart tags from a document.
     Assert.assertEquals(2, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());

     doc.removeSmartTags();

     Assert.assertEquals(0, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());
 }

 /// 
 /// Prints visited smart tags and their contents.
 /// 
 private static class SmartTagPrinter extends DocumentVisitor {
     /// 
     /// Called when a SmartTag node is encountered in the document.
     /// 
     public int visitSmartTagStart(SmartTag smartTag) {
         System.out.println("Smart tag type: {smartTag.Element}");
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when the visiting of a SmartTag node is ended.
     /// 
     public int visitSmartTagEnd(SmartTag smartTag) {
         System.out.println("\tContents: \"{smartTag.ToString(SaveFormat.Text)}\"");

         if (smartTag.getProperties().getCount() == 0) {
             System.out.println("\tContains no properties");
         } else {
             System.out.println("\tProperties: ");
             String[] properties = new String[smartTag.getProperties().getCount()];
             int index = 0;

             for (CustomXmlProperty cxp : smartTag.getProperties())
                 properties[index++] = MessageFormat.format("\"{0}\" = \"{1}\"", cxp.getName(), cxp.getValue());

             System.out.println(StringUtils.join(properties, ", "));
         }

         return VisitorAction.CONTINUE;
     }
 }
 
```

### selectNodes(String xpath) {#selectNodes-java.lang.String}
```
public NodeList selectNodes(String xpath)
```


Selects a list of nodes matching the XPath expression.

 **Remarks:** 

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

 **Examples:** 

Shows how to use an XPath expression to test whether a node is inside a field.

```

 Document doc = new Document(getMyDir() + "Mail merge destination - Northwind employees.docx");

 // The NodeList that results from this XPath expression will contain all nodes we find inside a field.
 // However, FieldStart and FieldEnd nodes can be on the list if there are nested fields in the path.
 // Currently does not find rare fields in which the FieldCode or FieldResult spans across multiple paragraphs.
 NodeList resultList =
         doc.selectNodes("//FieldStart/following-sibling::node()[following-sibling::FieldEnd]");
 Run[] runs = Arrays.stream(resultList.toArray()).filter(n -> n.getNodeType() == NodeType.RUN).toArray(Run[]::new);
 Run run = runs[0];

 // Check if the specified run is one of the nodes that are inside the field.
 System.out.println(MessageFormat.format("Contents of the first Run node that''s part of a field: {0}", run.getText().trim()));
 
```

Shows how to select certain nodes by using an XPath expression.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 // This expression will extract all paragraph nodes,
 // which are descendants of any table node in the document.
 NodeList nodeList = doc.selectNodes("//Table//Paragraph");

 // Iterate through the list with an enumerator and print the contents of every paragraph in each cell of the table.
 int index = 0;

 Iterator e = nodeList.iterator();
 while (e.hasNext()) {
     Node currentNode = e.next();
     System.out.println(MessageFormat.format("Table paragraph index {0}, contents: \"{1}\"", index++, currentNode.getText().trim()));
 }

 // This expression will select any paragraphs that are direct children of any Body node in the document.
 nodeList = doc.selectNodes("//Body/Paragraph");

 // We can treat the list as an array.
 Assert.assertEquals(nodeList.toArray().length, 4);

 // Use SelectSingleNode to select the first result of the same expression as above.
 Node node = doc.selectSingleNode("//Body/Paragraph");

 Assert.assertEquals(Paragraph.class, node.getClass());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xpath | java.lang.String | The XPath expression. |

**Returns:**
[NodeList](../../com.aspose.words/nodelist/) - A list of nodes matching the XPath query.
### selectSingleNode(String xpath) {#selectSingleNode-java.lang.String}
```
public Node selectSingleNode(String xpath)
```


Selects the first [Node](../../com.aspose.words/node/) that matches the XPath expression.

 **Remarks:** 

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

 **Examples:** 

Shows how to select certain nodes by using an XPath expression.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 // This expression will extract all paragraph nodes,
 // which are descendants of any table node in the document.
 NodeList nodeList = doc.selectNodes("//Table//Paragraph");

 // Iterate through the list with an enumerator and print the contents of every paragraph in each cell of the table.
 int index = 0;

 Iterator e = nodeList.iterator();
 while (e.hasNext()) {
     Node currentNode = e.next();
     System.out.println(MessageFormat.format("Table paragraph index {0}, contents: \"{1}\"", index++, currentNode.getText().trim()));
 }

 // This expression will select any paragraphs that are direct children of any Body node in the document.
 nodeList = doc.selectNodes("//Body/Paragraph");

 // We can treat the list as an array.
 Assert.assertEquals(nodeList.toArray().length, 4);

 // Use SelectSingleNode to select the first result of the same expression as above.
 Node node = doc.selectSingleNode("//Body/Paragraph");

 Assert.assertEquals(Paragraph.class, node.getClass());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xpath | java.lang.String | The XPath expression. |

**Returns:**
[Node](../../com.aspose.words/node/) - The first [Node](../../com.aspose.words/node/) that matches the XPath query or  null  if no matching node is found.
### setAppearance(int value) {#setAppearance-int}
```
public void setAppearance(int value)
```


Gets/sets the appearance of a structured document tag.

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
| value | int | The corresponding  int  value. The value must be one of [SdtAppearance](../../com.aspose.words/sdtappearance/) constants. |

### setBuildingBlockCategory(String value) {#setBuildingBlockCategory-java.lang.String}
```
public void setBuildingBlockCategory(String value)
```


Specifies category of building block for this **SDT** node. Can not be  null .

 **Remarks:** 

Accessing this property will only work for [SdtType.BUILDING\_BLOCK\_GALLERY](../../com.aspose.words/sdttype/\#BUILDING-BLOCK-GALLERY) and [SdtType.DOC\_PART\_OBJ](../../com.aspose.words/sdttype/\#DOC-PART-OBJ) SDT types. It is read-only for **SDT** of the document part type.

For all other SDT types exception will occur.

 **Examples:** 

Shows how to insert a structured document tag as a building block, and set its category and gallery.

```

 Document doc = new Document();

 StructuredDocumentTag buildingBlockSdt =
         new StructuredDocumentTag(doc, SdtType.BUILDING_BLOCK_GALLERY, MarkupLevel.BLOCK);
 buildingBlockSdt.setBuildingBlockCategory("Built-in");
 buildingBlockSdt.setBuildingBlockGallery("Table of Contents");

 doc.getFirstSection().getBody().appendChild(buildingBlockSdt);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.BuildingBlockCategories.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setBuildingBlockGallery(String value) {#setBuildingBlockGallery-java.lang.String}
```
public void setBuildingBlockGallery(String value)
```


Specifies type of building block for this **SDT**. Can not be  null .

 **Remarks:** 

Accessing this property will only work for [SdtType.BUILDING\_BLOCK\_GALLERY](../../com.aspose.words/sdttype/\#BUILDING-BLOCK-GALLERY) and [SdtType.DOC\_PART\_OBJ](../../com.aspose.words/sdttype/\#DOC-PART-OBJ) SDT types. It is read-only for **SDT** of the document part type.

For all other SDT types exception will occur.

 **Examples:** 

Shows how to insert a structured document tag as a building block, and set its category and gallery.

```

 Document doc = new Document();

 StructuredDocumentTag buildingBlockSdt =
         new StructuredDocumentTag(doc, SdtType.BUILDING_BLOCK_GALLERY, MarkupLevel.BLOCK);
 buildingBlockSdt.setBuildingBlockCategory("Built-in");
 buildingBlockSdt.setBuildingBlockGallery("Table of Contents");

 doc.getFirstSection().getBody().appendChild(buildingBlockSdt);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.BuildingBlockCategories.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setCalendarType(int value) {#setCalendarType-int}
```
public void setCalendarType(int value)
```


Specifies the type of calendar for this **SDT**. Default is [SdtCalendarType.DEFAULT](../../com.aspose.words/sdtcalendartype/\#DEFAULT)

 **Remarks:** 

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype/\#DATE) SDT type.

For all other SDT types exception will occur.

 **Examples:** 

Shows how to prompt the user to enter a date with a structured document tag.

```

 Document doc = new Document();

 // Insert a structured document tag that prompts the user to enter a date.
 // In Microsoft Word, this element is known as a "Date picker content control".
 // When we click on the arrow on the right end of this tag in Microsoft Word,
 // we will see a pop up in the form of a clickable calendar.
 // We can use that popup to select a date that the tag will display.
 StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.DATE, MarkupLevel.INLINE);

 // Display the date, according to the Saudi Arabian Arabic locale.
 sdtDate.setDateDisplayLocale(1025);

 // Set the format with which to display the date.
 sdtDate.setDateDisplayFormat("dd MMMM, yyyy");
 sdtDate.setDateStorageFormat(SdtDateStorageFormat.DATE_TIME);

 // Display the date according to the Hijri calendar.
 sdtDate.setCalendarType(SdtCalendarType.HIJRI);

 // Before the user chooses a date in Microsoft Word, the tag will display the text "Click here to enter a date.".
 // According to the tag's calendar, set the "FullDate" property to get the tag to display a default date.
 Calendar cal = Calendar.getInstance();
 cal.set(1440, 10, 20);
 sdtDate.setFullDate(cal.getTime());

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(sdtDate);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Date.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SdtCalendarType](../../com.aspose.words/sdtcalendartype/) constants. |

### setChecked(boolean value) {#setChecked-boolean}
```
public void setChecked(boolean value)
```


Gets/Sets current state of the Checkbox **SDT**. Default value for this property is  false .

 **Remarks:** 

Accessing this property will only work for [SdtType.CHECKBOX](../../com.aspose.words/sdttype/\#CHECKBOX) SDT types.

For all other SDT types exception will occur.

 **Examples:** 

Show how to create a structured document tag in the form of a check box.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 StructuredDocumentTag sdtCheckBox = new StructuredDocumentTag(doc, SdtType.CHECKBOX, MarkupLevel.INLINE);
 sdtCheckBox.setChecked(true);
 sdtCheckBox.setCheckedSymbol(0x00A9, "Times New Roman");
 sdtCheckBox.setUncheckedSymbol(0x00AE, "Times New Roman");

 builder.insertNode(sdtCheckBox);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.CheckBox.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setCheckedSymbol(int characterCode, String fontName) {#setCheckedSymbol-int-java.lang.String}
```
public void setCheckedSymbol(int characterCode, String fontName)
```


Sets the symbol used to represent the checked state of a check box content control.

 **Remarks:** 

Accessing this method will only work for [SdtType.CHECKBOX](../../com.aspose.words/sdttype/\#CHECKBOX) SDT types.

For all other SDT types exception will occur.

 **Examples:** 

Show how to create a structured document tag in the form of a check box.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 StructuredDocumentTag sdtCheckBox = new StructuredDocumentTag(doc, SdtType.CHECKBOX, MarkupLevel.INLINE);
 sdtCheckBox.setChecked(true);
 sdtCheckBox.setCheckedSymbol(0x00A9, "Times New Roman");
 sdtCheckBox.setUncheckedSymbol(0x00AE, "Times New Roman");

 builder.insertNode(sdtCheckBox);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.CheckBox.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| characterCode | int | The character code for the specified symbol. |
| fontName | java.lang.String | The name of the font that contains the symbol. |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Sets the color of the structured document tag.

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
| value | java.awt.Color | The color of the structured document tag. |

### setCustomNodeId(int value) {#setCustomNodeId-int}
```
public void setCustomNodeId(int value)
```


Specifies custom node identifier.

 **Remarks:** 

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

 **Examples:** 

Shows how to traverse through a composite node's collection of child nodes.

```

 Document doc = new Document();

 // Add two runs and one shape as child nodes to the first paragraph of this document.
 Paragraph paragraph = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);
 paragraph.appendChild(new Run(doc, "Hello world! "));

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 shape.setWidth(200.0);
 shape.setHeight(200.0);
 // Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
 shape.setCustomNodeId(100);
 shape.setWrapType(WrapType.INLINE);
 paragraph.appendChild(shape);

 paragraph.appendChild(new Run(doc, "Hello again!"));

 // Iterate through the paragraph's collection of immediate children,
 // and print any runs or shapes that we find within.
 NodeCollection children = paragraph.getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, false).getCount());

 for (Node child : (Iterable) children)
     switch (child.getNodeType()) {
         case NodeType.RUN:
             System.out.println("Run contents:");
             System.out.println(MessageFormat.format("\t\"{0}\"", child.getText().trim()));
             break;
         case NodeType.SHAPE:
             Shape childShape = (Shape)child;
             System.out.println("Shape:");
             System.out.println(MessageFormat.format("\t{0}, {1}x{2}", childShape.getShapeType(), childShape.getWidth(), childShape.getHeight()));
             break;
     }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setDateDisplayFormat(String value) {#setDateDisplayFormat-java.lang.String}
```
public void setDateDisplayFormat(String value)
```


String that represents the format in which dates are displayed.

 **Remarks:** 

Can not be  null .

The dates for English (U.S.) is "mm/dd/yyyy"

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype/\#DATE) SDT type.

For all other SDT types exception will occur.

 **Examples:** 

Shows how to prompt the user to enter a date with a structured document tag.

```

 Document doc = new Document();

 // Insert a structured document tag that prompts the user to enter a date.
 // In Microsoft Word, this element is known as a "Date picker content control".
 // When we click on the arrow on the right end of this tag in Microsoft Word,
 // we will see a pop up in the form of a clickable calendar.
 // We can use that popup to select a date that the tag will display.
 StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.DATE, MarkupLevel.INLINE);

 // Display the date, according to the Saudi Arabian Arabic locale.
 sdtDate.setDateDisplayLocale(1025);

 // Set the format with which to display the date.
 sdtDate.setDateDisplayFormat("dd MMMM, yyyy");
 sdtDate.setDateStorageFormat(SdtDateStorageFormat.DATE_TIME);

 // Display the date according to the Hijri calendar.
 sdtDate.setCalendarType(SdtCalendarType.HIJRI);

 // Before the user chooses a date in Microsoft Word, the tag will display the text "Click here to enter a date.".
 // According to the tag's calendar, set the "FullDate" property to get the tag to display a default date.
 Calendar cal = Calendar.getInstance();
 cal.set(1440, 10, 20);
 sdtDate.setFullDate(cal.getTime());

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(sdtDate);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Date.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setDateDisplayLocale(int value) {#setDateDisplayLocale-int}
```
public void setDateDisplayLocale(int value)
```


Allows to set/get the language format for the date displayed in this **SDT**.

 **Remarks:** 

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype/\#DATE) SDT type.

For all other SDT types exception will occur.

 **Examples:** 

Shows how to prompt the user to enter a date with a structured document tag.

```

 Document doc = new Document();

 // Insert a structured document tag that prompts the user to enter a date.
 // In Microsoft Word, this element is known as a "Date picker content control".
 // When we click on the arrow on the right end of this tag in Microsoft Word,
 // we will see a pop up in the form of a clickable calendar.
 // We can use that popup to select a date that the tag will display.
 StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.DATE, MarkupLevel.INLINE);

 // Display the date, according to the Saudi Arabian Arabic locale.
 sdtDate.setDateDisplayLocale(1025);

 // Set the format with which to display the date.
 sdtDate.setDateDisplayFormat("dd MMMM, yyyy");
 sdtDate.setDateStorageFormat(SdtDateStorageFormat.DATE_TIME);

 // Display the date according to the Hijri calendar.
 sdtDate.setCalendarType(SdtCalendarType.HIJRI);

 // Before the user chooses a date in Microsoft Word, the tag will display the text "Click here to enter a date.".
 // According to the tag's calendar, set the "FullDate" property to get the tag to display a default date.
 Calendar cal = Calendar.getInstance();
 cal.set(1440, 10, 20);
 sdtDate.setFullDate(cal.getTime());

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(sdtDate);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Date.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setDateStorageFormat(int value) {#setDateStorageFormat-int}
```
public void setDateStorageFormat(int value)
```


Gets/sets format in which the date for a date SDT is stored when the **SDT** is bound to an XML node in the document's data store. Default value is [SdtDateStorageFormat.DATE\_TIME](../../com.aspose.words/sdtdatestorageformat/\#DATE-TIME)

 **Remarks:** 

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype/\#DATE) SDT type.

For all other SDT types exception will occur.

 **Examples:** 

Shows how to prompt the user to enter a date with a structured document tag.

```

 Document doc = new Document();

 // Insert a structured document tag that prompts the user to enter a date.
 // In Microsoft Word, this element is known as a "Date picker content control".
 // When we click on the arrow on the right end of this tag in Microsoft Word,
 // we will see a pop up in the form of a clickable calendar.
 // We can use that popup to select a date that the tag will display.
 StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.DATE, MarkupLevel.INLINE);

 // Display the date, according to the Saudi Arabian Arabic locale.
 sdtDate.setDateDisplayLocale(1025);

 // Set the format with which to display the date.
 sdtDate.setDateDisplayFormat("dd MMMM, yyyy");
 sdtDate.setDateStorageFormat(SdtDateStorageFormat.DATE_TIME);

 // Display the date according to the Hijri calendar.
 sdtDate.setCalendarType(SdtCalendarType.HIJRI);

 // Before the user chooses a date in Microsoft Word, the tag will display the text "Click here to enter a date.".
 // According to the tag's calendar, set the "FullDate" property to get the tag to display a default date.
 Calendar cal = Calendar.getInstance();
 cal.set(1440, 10, 20);
 sdtDate.setFullDate(cal.getTime());

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(sdtDate);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Date.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SdtDateStorageFormat](../../com.aspose.words/sdtdatestorageformat/) constants. |

### setFullDate(Date value) {#setFullDate-java.util.Date}
```
public void setFullDate(Date value)
```


Specifies the full date and time last entered into this **SDT**.

 **Remarks:** 

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype/\#DATE) SDT type.

For all other SDT types exception will occur.

 **Examples:** 

Shows how to prompt the user to enter a date with a structured document tag.

```

 Document doc = new Document();

 // Insert a structured document tag that prompts the user to enter a date.
 // In Microsoft Word, this element is known as a "Date picker content control".
 // When we click on the arrow on the right end of this tag in Microsoft Word,
 // we will see a pop up in the form of a clickable calendar.
 // We can use that popup to select a date that the tag will display.
 StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.DATE, MarkupLevel.INLINE);

 // Display the date, according to the Saudi Arabian Arabic locale.
 sdtDate.setDateDisplayLocale(1025);

 // Set the format with which to display the date.
 sdtDate.setDateDisplayFormat("dd MMMM, yyyy");
 sdtDate.setDateStorageFormat(SdtDateStorageFormat.DATE_TIME);

 // Display the date according to the Hijri calendar.
 sdtDate.setCalendarType(SdtCalendarType.HIJRI);

 // Before the user chooses a date in Microsoft Word, the tag will display the text "Click here to enter a date.".
 // According to the tag's calendar, set the "FullDate" property to get the tag to display a default date.
 Calendar cal = Calendar.getInstance();
 cal.set(1440, 10, 20);
 sdtDate.setFullDate(cal.getTime());

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(sdtDate);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Date.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.util.Date | The corresponding java.util.Date value. |

### setLockContentControl(boolean value) {#setLockContentControl-boolean}
```
public void setLockContentControl(boolean value)
```


When set to  true , this property will prohibit a user from deleting this **SDT**.

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
public void setLockContents(boolean value)
```


When set to  true , this property will prohibit a user from editing the contents of this **SDT**.

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

### setMultiline(boolean value) {#setMultiline-boolean}
```
public void setMultiline(boolean value)
```


Specifies whether this **SDT** allows multiple lines of text.

 **Remarks:** 

Accessing this property will only work for [SdtType.RICH\_TEXT](../../com.aspose.words/sdttype/\#RICH-TEXT) and [SdtType.PLAIN\_TEXT](../../com.aspose.words/sdttype/\#PLAIN-TEXT) SDT type.

For all other SDT types exception will occur.

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
| value | boolean | The corresponding  boolean  value. |

### setPlaceholderName(String value) {#setPlaceholderName-java.lang.String}
```
public void setPlaceholderName(String value)
```


Gets or sets Name of the [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setStyle(Style value) {#setStyle-com.aspose.words.Style}
```
public void setStyle(Style value)
```


Sets the Style of the structured document tag.

 **Remarks:** 

Only [StyleType.CHARACTER](../../com.aspose.words/styletype/\#CHARACTER) style or [StyleType.PARAGRAPH](../../com.aspose.words/styletype/\#PARAGRAPH) style with linked character style can be set.

 **Examples:** 

Shows how to work with styles for content control elements.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways to apply a style from the document to a structured document tag.
 // 1 -  Apply a style object from the document's style collection:
 Style quoteStyle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.QUOTE);
 StructuredDocumentTag sdtPlainText = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);
 sdtPlainText.setStyle(quoteStyle);

 // 2 -  Reference a style in the document by name:
 StructuredDocumentTag sdtRichText = new StructuredDocumentTag(doc, SdtType.RICH_TEXT, MarkupLevel.INLINE);
 sdtRichText.setStyleName("Quote");

 builder.insertNode(sdtPlainText);
 builder.insertNode(sdtRichText);

 Assert.assertEquals(NodeType.STRUCTURED_DOCUMENT_TAG, sdtPlainText.getNodeType());

 NodeCollection tags = doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG, true);

 for (StructuredDocumentTag sdt : (Iterable) tags) {
     Assert.assertEquals(StyleIdentifier.QUOTE, sdt.getStyle().getStyleIdentifier());
     Assert.assertEquals("Quote", sdt.getStyleName());
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style/) | The Style of the structured document tag. |

### setStyleName(String value) {#setStyleName-java.lang.String}
```
public void setStyleName(String value)
```


Sets the name of the style applied to the structured document tag.

 **Examples:** 

Shows how to work with styles for content control elements.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways to apply a style from the document to a structured document tag.
 // 1 -  Apply a style object from the document's style collection:
 Style quoteStyle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.QUOTE);
 StructuredDocumentTag sdtPlainText = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);
 sdtPlainText.setStyle(quoteStyle);

 // 2 -  Reference a style in the document by name:
 StructuredDocumentTag sdtRichText = new StructuredDocumentTag(doc, SdtType.RICH_TEXT, MarkupLevel.INLINE);
 sdtRichText.setStyleName("Quote");

 builder.insertNode(sdtPlainText);
 builder.insertNode(sdtRichText);

 Assert.assertEquals(NodeType.STRUCTURED_DOCUMENT_TAG, sdtPlainText.getNodeType());

 NodeCollection tags = doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG, true);

 for (StructuredDocumentTag sdt : (Iterable) tags) {
     Assert.assertEquals(StyleIdentifier.QUOTE, sdt.getStyle().getStyleIdentifier());
     Assert.assertEquals("Quote", sdt.getStyleName());
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the style applied to the structured document tag. |

### setTag(String value) {#setTag-java.lang.String}
```
public void setTag(String value)
```


Specifies a tag associated with the current SDT node. Can not be  null .

 **Remarks:** 

A tag is an arbitrary string which applications can associate with SDT in order to identify it without providing a visible friendly name.

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
public void setTitle(String value)
```


Specifies the friendly name associated with this **SDT**. Can not be  null .

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

### setUncheckedSymbol(int characterCode, String fontName) {#setUncheckedSymbol-int-java.lang.String}
```
public void setUncheckedSymbol(int characterCode, String fontName)
```


Sets the symbol used to represent the unchecked state of a check box content control.

 **Remarks:** 

Accessing this method will only work for [SdtType.CHECKBOX](../../com.aspose.words/sdttype/\#CHECKBOX) SDT types.

For all other SDT types exception will occur.

 **Examples:** 

Show how to create a structured document tag in the form of a check box.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 StructuredDocumentTag sdtCheckBox = new StructuredDocumentTag(doc, SdtType.CHECKBOX, MarkupLevel.INLINE);
 sdtCheckBox.setChecked(true);
 sdtCheckBox.setCheckedSymbol(0x00A9, "Times New Roman");
 sdtCheckBox.setUncheckedSymbol(0x00AE, "Times New Roman");

 builder.insertNode(sdtCheckBox);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.CheckBox.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| characterCode | int | The character code for the specified symbol. |
| fontName | java.lang.String | The name of the font that contains the symbol. |

### structuredDocumentTagNode() {#structuredDocumentTagNode}
```
public Node structuredDocumentTagNode()
```


Returns Node object that implements this interface.

**Returns:**
[Node](../../com.aspose.words/node/)
### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(SaveOptions saveOptions) {#toString-com.aspose.words.SaveOptions}
```
public String toString(SaveOptions saveOptions)
```


Exports the content of the node into a string using the specified save options.

 **Examples:** 

Exports the content of a node to String in HTML format.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 Node node = doc.getLastSection().getBody().getLastParagraph();

 // When we call the ToString method using the html SaveFormat overload,
 // it converts the node's contents to their raw html representation.
 Assert.assertEquals(" " +
         "Hello World!" +
         "", node.toString(SaveFormat.HTML));

 // We can also modify the result of this conversion using a SaveOptions object.
 HtmlSaveOptions saveOptions = new HtmlSaveOptions();
 saveOptions.setExportRelativeFontSize(true);

 Assert.assertEquals(" " +
         "Hello World!" +
         "", node.toString(saveOptions));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Specifies the options that control how the node is saved. |

**Returns:**
java.lang.String - The content of the node in the specified format.
### toString(int saveFormat) {#toString-int}
```
public String toString(int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
