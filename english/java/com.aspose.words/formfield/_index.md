---
title: FormField
second_title: Aspose.Words for Java API Reference
description: Represents a single form field.
type: docs
weight: 296
url: /java/com.aspose.words/formfield/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.Inline](../../com.aspose.words/inline), [com.aspose.words.SpecialChar](../../com.aspose.words/specialchar)
```
public class FormField extends SpecialChar
```

Represents a single form field.

To learn more, visit the **Working with Form Fields** documentation article.

Microsoft Word provides the following form fields: checkbox, text input and dropdown (combobox).

**FormField** is an inline-node and can only be a child of **Paragraph**.

**FormField** is represented in a document by a special character and positioned as a character within a line of text.

A complete form field in a Word document is a complex structure represented by several nodes: field start, field code such as FORMTEXT, form field data, field separator, field result, field end and a bookmark. To programmatically create form fields in a Word document use [DocumentBuilder.insertCheckBox(java.lang.String, boolean, int)](../../com.aspose.words/documentbuilder\#insertCheckBox-java.lang.String--boolean--int-), **M:Aspose.Words.DocumentBuilder.InsertTextInput(System.String,Aspose.Words.Fields.TextFormFieldType,System.String,System.String,System.Int32)** and [DocumentBuilder.insertComboBox(java.lang.String, java.lang.String[], int)](../../com.aspose.words/documentbuilder\#insertComboBox-java.lang.String--java.lang.String----int-) which make sure all of the form field nodes are created in a correct order and in a suitable state.
## Methods

| Method | Description |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | Creates a duplicate of the node. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int-) |  |
| [getAncestor(int ancestorType)](#getAncestor-int-) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class-) | Gets the first ancestor of the specified object type. |
| [getCalculateOnExit()](#getCalculateOnExit--) | True if references to the specified form field are automatically updated whenever the field is exited. |
| [getCheckBoxSize()](#getCheckBoxSize--) | Gets the size of the checkbox in points. |
| [getChecked()](#getChecked--) | Gets the checked status of the check box form field. |
| [getClass()](#getClass--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | Specifies custom node identifier. |
| [getDefault()](#getDefault--) | Gets the default value of the check box form field. |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int-) |  |
| [getDocument()](#getDocument--) | Gets the document to which this node belongs. |
| [getDocument_IInline()](#getDocument-IInline--) |  |
| [getDropDownItems()](#getDropDownItems--) | Provides access to the items of a dropdown form field. |
| [getDropDownSelectedIndex()](#getDropDownSelectedIndex--) | Gets the index specifying the currently selected item in a dropdown form field. |
| [getEnabled()](#getEnabled--) | True if a form field is enabled. |
| [getEntryMacro()](#getEntryMacro--) | Gets an entry macro name for the form field. |
| [getExitMacro()](#getExitMacro--) | Gets an exit macro name for the form field. |
| [getFont()](#getFont--) | Provides access to the font formatting of this object. |
| [getHelpText()](#getHelpText--) | Gets the text that's displayed in a message box when the form field has the focus and the user presses F1. |
| [getMaxLength()](#getMaxLength--) | Maximum length for the text field. |
| [getName()](#getName--) | Gets the form field name. |
| [getNextSibling()](#getNextSibling--) | Gets the node immediately following this node. |
| [getNodeType()](#getNodeType--) | Returns **NodeType.FormField**. |
| [getOwnHelp()](#getOwnHelp--) | Specifies the source of the text that's displayed in a message box when a form field has the focus and the user presses F1. |
| [getOwnStatus()](#getOwnStatus--) | Specifies the source of the text that's displayed in the status bar when a form field has the focus. |
| [getParentNode()](#getParentNode--) | Gets the immediate parent of this node. |
| [getParentParagraph()](#getParentParagraph--) | Retrieves the parent [Paragraph](../../com.aspose.words/paragraph) of this node. |
| [getParentParagraph_IInline()](#getParentParagraph-IInline--) |  |
| [getPreviousSibling()](#getPreviousSibling--) | Gets the node immediately preceding this node. |
| [getRange()](#getRange--) | Returns a **Range** object that represents the portion of a document that is contained in this node. |
| [getResult()](#getResult--) | Gets a string that represents the result of this form field. |
| [getStatusText()](#getStatusText--) | Gets the text that's displayed in the status bar when a form field has the focus. |
| [getText()](#getText--) | Gets the special character that this node represents. |
| [getTextInputDefault()](#getTextInputDefault--) | Gets the default string or a calculation expression of a text form field. |
| [getTextInputFormat()](#getTextInputFormat--) | Gets the text formatting for a text form field. |
| [getTextInputType()](#getTextInputType--) | Gets the type of a text form field. |
| [getType()](#getType--) | Returns the form field type. |
| [hashCode()](#hashCode--) |  |
| [isCheckBoxExactSize()](#isCheckBoxExactSize--) | Gets the boolean value that indicates whether the size of the textbox is automatic or specified explicitly. |
| [isCheckBoxExactSize(boolean value)](#isCheckBoxExactSize-boolean-) | Sets the boolean value that indicates whether the size of the textbox is automatic or specified explicitly. |
| [isComposite()](#isComposite--) | Returns true if this node can contain other nodes. |
| [isDeleteRevision()](#isDeleteRevision--) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [isFormatRevision()](#isFormatRevision--) | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled. |
| [isInsertRevision()](#isInsertRevision--) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [isMoveFromRevision()](#isMoveFromRevision--) | Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [isMoveToRevision()](#isMoveToRevision--) | Returns **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node-) | Gets next node according to the pre-order tree traversal algorithm. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int-) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node-) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [remove()](#remove--) | Removes itself from the parent. |
| [removeField()](#removeField--) | Removes the complete form field, not just the form field special character. |
| [removeMoveRevisions()](#removeMoveRevisions--) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [setCalculateOnExit(boolean value)](#setCalculateOnExit-boolean-) | True if references to the specified form field are automatically updated whenever the field is exited. |
| [setCheckBoxSize(double value)](#setCheckBoxSize-double-) | Sets the size of the checkbox in points. |
| [setChecked(boolean value)](#setChecked-boolean-) | Sets the checked status of the check box form field. |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | Specifies custom node identifier. |
| [setDefault(boolean value)](#setDefault-boolean-) | Sets the default value of the check box form field. |
| [setDropDownSelectedIndex(int value)](#setDropDownSelectedIndex-int-) | Sets the index specifying the currently selected item in a dropdown form field. |
| [setEnabled(boolean value)](#setEnabled-boolean-) | True if a form field is enabled. |
| [setEntryMacro(String value)](#setEntryMacro-java.lang.String-) | Sets an entry macro name for the form field. |
| [setExitMacro(String value)](#setExitMacro-java.lang.String-) | Sets an exit macro name for the form field. |
| [setHelpText(String value)](#setHelpText-java.lang.String-) | Sets the text that's displayed in a message box when the form field has the focus and the user presses F1. |
| [setMaxLength(int value)](#setMaxLength-int-) | Maximum length for the text field. |
| [setName(String value)](#setName-java.lang.String-) | Sets the form field name. |
| [setOwnHelp(boolean value)](#setOwnHelp-boolean-) | Specifies the source of the text that's displayed in a message box when a form field has the focus and the user presses F1. |
| [setOwnStatus(boolean value)](#setOwnStatus-boolean-) | Specifies the source of the text that's displayed in the status bar when a form field has the focus. |
| [setResult(String value)](#setResult-java.lang.String-) | Sets a string that represents the result of this form field. |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [setStatusText(String value)](#setStatusText-java.lang.String-) | Sets the text that's displayed in the status bar when a form field has the focus. |
| [setTextInputDefault(String value)](#setTextInputDefault-java.lang.String-) | Sets the default string or a calculation expression of a text form field. |
| [setTextInputFormat(String value)](#setTextInputFormat-java.lang.String-) | Sets the text formatting for a text form field. |
| [setTextInputType(int value)](#setTextInputType-int-) | Sets the type of a text form field. |
| [setTextInputValue(Object newValue)](#setTextInputValue-java.lang.Object-) | Applies the text format specified in [getTextInputFormat()](../../com.aspose.words/formfield\#getTextInputFormat--) / [setTextInputFormat(java.lang.String)](../../com.aspose.words/formfield\#setTextInputFormat-java.lang.String-) and stores the value in [getResult()](../../com.aspose.words/formfield\#getResult--) / [setResult(java.lang.String)](../../com.aspose.words/formfield\#setResult-java.lang.String-). |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | Exports the content of the node into a string using the specified save options. |
| [toString(int saveFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

Calls DocumentVisitor.VisitFormField.

For more info see the Visitor design pattern.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | The visitor that will visit the node. |

**Returns:**
boolean - False if the visitor requested the enumeration to stop.
### clearRunAttrs() {#clearRunAttrs--}
```
public void clearRunAttrs()
```




### dd() {#dd--}
```
public void dd()
```




### deepClone(boolean isCloneChildren) {#deepClone-boolean-}
```
public Node deepClone(boolean isCloneChildren)
```


Creates a duplicate of the node.

This method serves as a copy constructor for nodes. The cloned node has no parent, but belongs to the same document as the original node.

This method always performs a deep copy of the node. The *isCloneChildren* parameter specifies whether to perform copy all child nodes as well.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| isCloneChildren | boolean | True to recursively clone the subtree under the specified node; false to clone only the node itself. |

**Returns:**
[Node](../../com.aspose.words/node) - The cloned node.
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### fetchInheritedRunAttr(int fontAttr) {#fetchInheritedRunAttr-int-}
```
public Object fetchInheritedRunAttr(int fontAttr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### getAncestor(int ancestorType) {#getAncestor-int-}
```
public CompositeNode getAncestor(int ancestorType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ancestorType | int |  |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode)
### getAncestor(Class ancestorType) {#getAncestor-java.lang.Class-}
```
public CompositeNode getAncestor(Class ancestorType)
```


Gets the first ancestor of the specified object type.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ancestorType | java.lang.Class | The object type of the ancestor to retrieve. |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode) - The ancestor of the specified type or null if no ancestor of this type was found.

The ancestor type matches if it is equal to ancestorType or derived from ancestorType.
### getCalculateOnExit() {#getCalculateOnExit--}
```
public boolean getCalculateOnExit()
```


True if references to the specified form field are automatically updated whenever the field is exited.

Setting **CalculateOnExit** only affects the behavior of the form field when the document is opened in Microsoft Word. Aspose.Words never updates references to the form field.

**Returns:**
boolean - The corresponding  boolean  value.
### getCheckBoxSize() {#getCheckBoxSize--}
```
public double getCheckBoxSize()
```


Gets the size of the checkbox in points. Has effect only when [isCheckBoxExactSize()](../../com.aspose.words/formfield\#isCheckBoxExactSize--) / [isCheckBoxExactSize(boolean)](../../com.aspose.words/formfield\#isCheckBoxExactSize-boolean-) is true.

Applicable for a check box form field only.

**Returns:**
double - The size of the checkbox in points.
### getChecked() {#getChecked--}
```
public boolean getChecked()
```


Gets the checked status of the check box form field. Default value for this property is **false**.

Applicable for a check box form field only.

**Returns:**
boolean - The checked status of the check box form field.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getCustomNodeId() {#getCustomNodeId--}
```
public int getCustomNodeId()
```


Specifies custom node identifier.

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

**Returns:**
int - The corresponding  int  value.
### getDefault() {#getDefault--}
```
public boolean getDefault()
```


Gets the default value of the check box form field. Default value for this property is **false**.

Applicable for a check box form field only.

**Returns:**
boolean - The default value of the check box form field.
### getDirectRunAttr(int fontAttr) {#getDirectRunAttr-int-}
```
public Object getDirectRunAttr(int fontAttr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


Gets the document to which this node belongs.

The node always belongs to a document even if it has just been created and not yet added to the tree, or if it has been removed from the tree.

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase) - The document to which this node belongs.
### getDocument_IInline() {#getDocument-IInline--}
```
public DocumentBase getDocument_IInline()
```




**Returns:**
[DocumentBase](../../com.aspose.words/documentbase)
### getDropDownItems() {#getDropDownItems--}
```
public DropDownItemCollection getDropDownItems()
```


Provides access to the items of a dropdown form field.

Microsoft Word allows maximum 25 items in a dropdown form field.

**Returns:**
[DropDownItemCollection](../../com.aspose.words/dropdownitemcollection) - The corresponding [DropDownItemCollection](../../com.aspose.words/dropdownitemcollection) value.
### getDropDownSelectedIndex() {#getDropDownSelectedIndex--}
```
public int getDropDownSelectedIndex()
```


Gets the index specifying the currently selected item in a dropdown form field.

**Returns:**
int - The index specifying the currently selected item in a dropdown form field.
### getEnabled() {#getEnabled--}
```
public boolean getEnabled()
```


True if a form field is enabled.

If a form field is enabled, its contents can be changed as the form is filled in.

**Returns:**
boolean - The corresponding  boolean  value.
### getEntryMacro() {#getEntryMacro--}
```
public String getEntryMacro()
```


Gets an entry macro name for the form field.

The entry macro runs when the form field gets the focus in Microsoft Word.

Microsoft Word allows strings with at most 32 characters.

**Returns:**
java.lang.String - An entry macro name for the form field.
### getExitMacro() {#getExitMacro--}
```
public String getExitMacro()
```


Gets an exit macro name for the form field.

The exit macro runs when the form field loses the focus in Microsoft Word.

Microsoft Word allows strings with at most 32 characters.

**Returns:**
java.lang.String - An exit macro name for the form field.
### getFont() {#getFont--}
```
public Font getFont()
```


Provides access to the font formatting of this object.

**Returns:**
[Font](../../com.aspose.words/font) - The corresponding [Font](../../com.aspose.words/font) value.
### getHelpText() {#getHelpText--}
```
public String getHelpText()
```


Gets the text that's displayed in a message box when the form field has the focus and the user presses F1.

If the OwnHelp property is set to True, HelpText specifies the text string value. If OwnHelp is set to False, HelpText specifies the name of an AutoText entry that contains help text for the form field.

Microsoft Word allows strings with at most 255 characters.

**Returns:**
java.lang.String - The text that's displayed in a message box when the form field has the focus and the user presses F1.
### getMaxLength() {#getMaxLength--}
```
public int getMaxLength()
```


Maximum length for the text field. Zero when the length is not limited.

**Returns:**
int - The corresponding  int  value.
### getName() {#getName--}
```
public String getName()
```


Gets the form field name. Microsoft Word allows strings with at most 20 characters.

**Returns:**
java.lang.String - The form field name.
### getNextSibling() {#getNextSibling--}
```
public Node getNextSibling()
```


Gets the node immediately following this node. If there is no next node, a null is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The node immediately following this node.
### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns **NodeType.FormField**.

**Returns:**
int - **NodeType.FormField**. The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getOwnHelp() {#getOwnHelp--}
```
public boolean getOwnHelp()
```


Specifies the source of the text that's displayed in a message box when a form field has the focus and the user presses F1.

If True, the text specified by the HelpText property is displayed. If False, the text in the AutoText entry specified by the HelpText property is displayed.

**Returns:**
boolean - The corresponding  boolean  value.
### getOwnStatus() {#getOwnStatus--}
```
public boolean getOwnStatus()
```


Specifies the source of the text that's displayed in the status bar when a form field has the focus.

If true, the text specified by the StatusText property is displayed. If false, the text of the AutoText entry specified by the StatusText property is displayed.

**Returns:**
boolean - The corresponding  boolean  value.
### getParentNode() {#getParentNode--}
```
public CompositeNode getParentNode()
```


Gets the immediate parent of this node.

If a node has just been created and not yet added to the tree, or if it has been removed from the tree, the parent is null.

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode) - The immediate parent of this node.
### getParentParagraph() {#getParentParagraph--}
```
public Paragraph getParentParagraph()
```


Retrieves the parent [Paragraph](../../com.aspose.words/paragraph) of this node.

**Returns:**
[Paragraph](../../com.aspose.words/paragraph) - The corresponding [Paragraph](../../com.aspose.words/paragraph) value.
### getParentParagraph_IInline() {#getParentParagraph-IInline--}
```
public Paragraph getParentParagraph_IInline()
```




**Returns:**
[Paragraph](../../com.aspose.words/paragraph)
### getPreviousSibling() {#getPreviousSibling--}
```
public Node getPreviousSibling()
```


Gets the node immediately preceding this node. If there is no preceding node, a null is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The node immediately preceding this node.
### getRange() {#getRange--}
```
public Range getRange()
```


Returns a **Range** object that represents the portion of a document that is contained in this node.

**Returns:**
[Range](../../com.aspose.words/range) - A **Range** object that represents the portion of a document that is contained in this node.
### getResult() {#getResult--}
```
public String getResult()
```


Gets a string that represents the result of this form field.

For a text form field the result is the text that is in the field.

For a checkbox form field the result can be "1" or "0" to indicate checked or unchecked.

For a dropdown form field the result is the string selected in the dropdown.

Setting [getResult()](../../com.aspose.words/formfield\#getResult--) / [setResult(java.lang.String)](../../com.aspose.words/formfield\#setResult-java.lang.String-) for a text form field does not apply the text format specified in [getTextInputFormat()](../../com.aspose.words/formfield\#getTextInputFormat--) / [setTextInputFormat(java.lang.String)](../../com.aspose.words/formfield\#setTextInputFormat-java.lang.String-). If you want to set a value and apply the format, use the [setTextInputValue(java.lang.Object)](../../com.aspose.words/formfield\#setTextInputValue-java.lang.Object-) method.

For a text form field the [getTextInputDefault()](../../com.aspose.words/formfield\#getTextInputDefault--) / [setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield\#setTextInputDefault-java.lang.String-) value is applied if  value  is  null .

**Returns:**
java.lang.String - A string that represents the result of this form field.
### getStatusText() {#getStatusText--}
```
public String getStatusText()
```


Gets the text that's displayed in the status bar when a form field has the focus.

If the OwnStatus property is set to true, the StatusText property specifies the status bar text. If the OwnStatus property is set to false, the StatusText property specifies the name of an AutoText entry that contains status bar text for the form field.

Microsoft Word allows strings with at most 138 characters.

**Returns:**
java.lang.String - The text that's displayed in the status bar when a form field has the focus.
### getText() {#getText--}
```
public String getText()
```


Gets the special character that this node represents.

**Returns:**
java.lang.String - The string that contains the character that this node represents.
### getTextInputDefault() {#getTextInputDefault--}
```
public String getTextInputDefault()
```


Gets the default string or a calculation expression of a text form field.

The meaning of this property depends on the value of the [getTextInputType()](../../com.aspose.words/formfield\#getTextInputType--) / [setTextInputType(int)](../../com.aspose.words/formfield\#setTextInputType-int-) property.

When [getTextInputType()](../../com.aspose.words/formfield\#getTextInputType--) / [setTextInputType(int)](../../com.aspose.words/formfield\#setTextInputType-int-) is [TextFormFieldType.REGULAR](../../com.aspose.words/textformfieldtype\#REGULAR) or [TextFormFieldType.NUMBER](../../com.aspose.words/textformfieldtype\#NUMBER), this string specifies the default string for the text form field. This string is the content that Microsoft Word will display in the document when the form field is empty.

When [getTextInputType()](../../com.aspose.words/formfield\#getTextInputType--) / [setTextInputType(int)](../../com.aspose.words/formfield\#setTextInputType-int-) is [TextFormFieldType.CALCULATED](../../com.aspose.words/textformfieldtype\#CALCULATED), then this string holds the expression to be calculated. The expression needs to be a formula valid according to Microsoft Word formula field requirements. When you set a new expression using this property, Aspose.Words calculates the formula result automatically and inserts it into the form field.

Microsoft Word allows strings with at most 255 characters.

**Returns:**
java.lang.String - The default string or a calculation expression of a text form field.
### getTextInputFormat() {#getTextInputFormat--}
```
public String getTextInputFormat()
```


Gets the text formatting for a text form field.

If the text form field contains regular text, then valid format strings are "", "UPPERCASE", "LOWERCASE", "FIRST CAPITAL" and "TITLE CASE". The strings are case-insensitive.

If the text form field contains a number or a date/time value, then valid format strings are number or date and time format strings.

Microsoft Word allows strings with at most 64 characters.

**Returns:**
java.lang.String - The text formatting for a text form field.
### getTextInputType() {#getTextInputType--}
```
public int getTextInputType()
```


Gets the type of a text form field.

**Returns:**
int - The type of a text form field. The returned value is one of [TextFormFieldType](../../com.aspose.words/textformfieldtype) constants.
### getType() {#getType--}
```
public int getType()
```


Returns the form field type.

**Returns:**
int - The form field type. The returned value is one of [FieldType](../../com.aspose.words/fieldtype) constants.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### isCheckBoxExactSize() {#isCheckBoxExactSize--}
```
public boolean isCheckBoxExactSize()
```


Gets the boolean value that indicates whether the size of the textbox is automatic or specified explicitly.

Applicable for a check box form field only.

**Returns:**
boolean - The boolean value that indicates whether the size of the textbox is automatic or specified explicitly.
### isCheckBoxExactSize(boolean value) {#isCheckBoxExactSize-boolean-}
```
public void isCheckBoxExactSize(boolean value)
```


Sets the boolean value that indicates whether the size of the textbox is automatic or specified explicitly.

Applicable for a check box form field only.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The boolean value that indicates whether the size of the textbox is automatic or specified explicitly. |

### isComposite() {#isComposite--}
```
public boolean isComposite()
```


Returns true if this node can contain other nodes. (31110,6)

**Returns:**
boolean - True if this node can contain other nodes.
### isDeleteRevision() {#isDeleteRevision--}
```
public boolean isDeleteRevision()
```


Returns true if this object was deleted in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - True if this object was deleted in Microsoft Word while change tracking was enabled.
### isFormatRevision() {#isFormatRevision--}
```
public boolean isFormatRevision()
```


Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - True if formatting of the object was changed in Microsoft Word while change tracking was enabled.
### isInsertRevision() {#isInsertRevision--}
```
public boolean isInsertRevision()
```


Returns true if this object was inserted in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - True if this object was inserted in Microsoft Word while change tracking was enabled.
### isMoveFromRevision() {#isMoveFromRevision--}
```
public boolean isMoveFromRevision()
```


Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled.
### isMoveToRevision() {#isMoveToRevision--}
```
public boolean isMoveToRevision()
```


Returns **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled.
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node-}
```
public Node nextPreOrder(Node rootNode)
```


Gets next node according to the pre-order tree traversal algorithm.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | The top node (limit) of traversal. |

**Returns:**
[Node](../../com.aspose.words/node) - Next node in pre-order order. Null if reached the rootNode.
### nodeTypeToString(int nodeType) {#nodeTypeToString-int-}
```
public static String nodeTypeToString(int nodeType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node-}
```
public Node previousPreOrder(Node rootNode)
```


Gets the previous node according to the pre-order tree traversal algorithm.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | The top node (limit) of traversal. |

**Returns:**
[Node](../../com.aspose.words/node) - Previous node in pre-order order. Null if reached the rootNode.
### remove() {#remove--}
```
public void remove()
```


Removes itself from the parent.

### removeField() {#removeField--}
```
public void removeField()
```


Removes the complete form field, not just the form field special character. If there is a bookmark associated with the form field, the bookmark is not removed.

### removeMoveRevisions() {#removeMoveRevisions--}
```
public void removeMoveRevisions()
```




### removeRunAttr(int key) {#removeRunAttr-int-}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### setCalculateOnExit(boolean value) {#setCalculateOnExit-boolean-}
```
public void setCalculateOnExit(boolean value)
```


True if references to the specified form field are automatically updated whenever the field is exited.

Setting **CalculateOnExit** only affects the behavior of the form field when the document is opened in Microsoft Word. Aspose.Words never updates references to the form field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setCheckBoxSize(double value) {#setCheckBoxSize-double-}
```
public void setCheckBoxSize(double value)
```


Sets the size of the checkbox in points. Has effect only when [isCheckBoxExactSize()](../../com.aspose.words/formfield\#isCheckBoxExactSize--) / [isCheckBoxExactSize(boolean)](../../com.aspose.words/formfield\#isCheckBoxExactSize-boolean-) is true.

Applicable for a check box form field only.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The size of the checkbox in points. |

### setChecked(boolean value) {#setChecked-boolean-}
```
public void setChecked(boolean value)
```


Sets the checked status of the check box form field. Default value for this property is **false**.

Applicable for a check box form field only.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The checked status of the check box form field. |

### setCustomNodeId(int value) {#setCustomNodeId-int-}
```
public void setCustomNodeId(int value)
```


Specifies custom node identifier.

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setDefault(boolean value) {#setDefault-boolean-}
```
public void setDefault(boolean value)
```


Sets the default value of the check box form field. Default value for this property is **false**.

Applicable for a check box form field only.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The default value of the check box form field. |

### setDropDownSelectedIndex(int value) {#setDropDownSelectedIndex-int-}
```
public void setDropDownSelectedIndex(int value)
```


Sets the index specifying the currently selected item in a dropdown form field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The index specifying the currently selected item in a dropdown form field. |

### setEnabled(boolean value) {#setEnabled-boolean-}
```
public void setEnabled(boolean value)
```


True if a form field is enabled.

If a form field is enabled, its contents can be changed as the form is filled in.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setEntryMacro(String value) {#setEntryMacro-java.lang.String-}
```
public void setEntryMacro(String value)
```


Sets an entry macro name for the form field.

The entry macro runs when the form field gets the focus in Microsoft Word.

Microsoft Word allows strings with at most 32 characters.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | An entry macro name for the form field. |

### setExitMacro(String value) {#setExitMacro-java.lang.String-}
```
public void setExitMacro(String value)
```


Sets an exit macro name for the form field.

The exit macro runs when the form field loses the focus in Microsoft Word.

Microsoft Word allows strings with at most 32 characters.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | An exit macro name for the form field. |

### setHelpText(String value) {#setHelpText-java.lang.String-}
```
public void setHelpText(String value)
```


Sets the text that's displayed in a message box when the form field has the focus and the user presses F1.

If the OwnHelp property is set to True, HelpText specifies the text string value. If OwnHelp is set to False, HelpText specifies the name of an AutoText entry that contains help text for the form field.

Microsoft Word allows strings with at most 255 characters.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The text that's displayed in a message box when the form field has the focus and the user presses F1. |

### setMaxLength(int value) {#setMaxLength-int-}
```
public void setMaxLength(int value)
```


Maximum length for the text field. Zero when the length is not limited.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


Sets the form field name. Microsoft Word allows strings with at most 20 characters.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The form field name. |

### setOwnHelp(boolean value) {#setOwnHelp-boolean-}
```
public void setOwnHelp(boolean value)
```


Specifies the source of the text that's displayed in a message box when a form field has the focus and the user presses F1.

If True, the text specified by the HelpText property is displayed. If False, the text in the AutoText entry specified by the HelpText property is displayed.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setOwnStatus(boolean value) {#setOwnStatus-boolean-}
```
public void setOwnStatus(boolean value)
```


Specifies the source of the text that's displayed in the status bar when a form field has the focus.

If true, the text specified by the StatusText property is displayed. If false, the text of the AutoText entry specified by the StatusText property is displayed.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


Sets a string that represents the result of this form field.

For a text form field the result is the text that is in the field.

For a checkbox form field the result can be "1" or "0" to indicate checked or unchecked.

For a dropdown form field the result is the string selected in the dropdown.

Setting [getResult()](../../com.aspose.words/formfield\#getResult--) / [setResult(java.lang.String)](../../com.aspose.words/formfield\#setResult-java.lang.String-) for a text form field does not apply the text format specified in [getTextInputFormat()](../../com.aspose.words/formfield\#getTextInputFormat--) / [setTextInputFormat(java.lang.String)](../../com.aspose.words/formfield\#setTextInputFormat-java.lang.String-). If you want to set a value and apply the format, use the [setTextInputValue(java.lang.Object)](../../com.aspose.words/formfield\#setTextInputValue-java.lang.Object-) method.

For a text form field the [getTextInputDefault()](../../com.aspose.words/formfield\#getTextInputDefault--) / [setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield\#setTextInputDefault-java.lang.String-) value is applied if  value  is  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A string that represents the result of this form field. |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setStatusText(String value) {#setStatusText-java.lang.String-}
```
public void setStatusText(String value)
```


Sets the text that's displayed in the status bar when a form field has the focus.

If the OwnStatus property is set to true, the StatusText property specifies the status bar text. If the OwnStatus property is set to false, the StatusText property specifies the name of an AutoText entry that contains status bar text for the form field.

Microsoft Word allows strings with at most 138 characters.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The text that's displayed in the status bar when a form field has the focus. |

### setTextInputDefault(String value) {#setTextInputDefault-java.lang.String-}
```
public void setTextInputDefault(String value)
```


Sets the default string or a calculation expression of a text form field.

The meaning of this property depends on the value of the [getTextInputType()](../../com.aspose.words/formfield\#getTextInputType--) / [setTextInputType(int)](../../com.aspose.words/formfield\#setTextInputType-int-) property.

When [getTextInputType()](../../com.aspose.words/formfield\#getTextInputType--) / [setTextInputType(int)](../../com.aspose.words/formfield\#setTextInputType-int-) is [TextFormFieldType.REGULAR](../../com.aspose.words/textformfieldtype\#REGULAR) or [TextFormFieldType.NUMBER](../../com.aspose.words/textformfieldtype\#NUMBER), this string specifies the default string for the text form field. This string is the content that Microsoft Word will display in the document when the form field is empty.

When [getTextInputType()](../../com.aspose.words/formfield\#getTextInputType--) / [setTextInputType(int)](../../com.aspose.words/formfield\#setTextInputType-int-) is [TextFormFieldType.CALCULATED](../../com.aspose.words/textformfieldtype\#CALCULATED), then this string holds the expression to be calculated. The expression needs to be a formula valid according to Microsoft Word formula field requirements. When you set a new expression using this property, Aspose.Words calculates the formula result automatically and inserts it into the form field.

Microsoft Word allows strings with at most 255 characters.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The default string or a calculation expression of a text form field. |

### setTextInputFormat(String value) {#setTextInputFormat-java.lang.String-}
```
public void setTextInputFormat(String value)
```


Sets the text formatting for a text form field.

If the text form field contains regular text, then valid format strings are "", "UPPERCASE", "LOWERCASE", "FIRST CAPITAL" and "TITLE CASE". The strings are case-insensitive.

If the text form field contains a number or a date/time value, then valid format strings are number or date and time format strings.

Microsoft Word allows strings with at most 64 characters.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The text formatting for a text form field. |

### setTextInputType(int value) {#setTextInputType-int-}
```
public void setTextInputType(int value)
```


Sets the type of a text form field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The type of a text form field. The value must be one of [TextFormFieldType](../../com.aspose.words/textformfieldtype) constants. |

### setTextInputValue(Object newValue) {#setTextInputValue-java.lang.Object-}
```
public void setTextInputValue(Object newValue)
```


Applies the text format specified in [getTextInputFormat()](../../com.aspose.words/formfield\#getTextInputFormat--) / [setTextInputFormat(java.lang.String)](../../com.aspose.words/formfield\#setTextInputFormat-java.lang.String-) and stores the value in [getResult()](../../com.aspose.words/formfield\#getResult--) / [setResult(java.lang.String)](../../com.aspose.words/formfield\#setResult-java.lang.String-).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newValue | java.lang.Object | Can be a string, number or a DateTime object. The [getTextInputDefault()](../../com.aspose.words/formfield\#getTextInputDefault--) / [setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield\#setTextInputDefault-java.lang.String-) value is applied if  newValue  is  null . |

### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(SaveOptions saveOptions) {#toString-com.aspose.words.SaveOptions-}
```
public String toString(SaveOptions saveOptions)
```


Exports the content of the node into a string using the specified save options.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions) | Specifies the options that control how the node is saved. |

**Returns:**
java.lang.String - The content of the node in the specified format.
### toString(int saveFormat) {#toString-int-}
```
public String toString(int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

