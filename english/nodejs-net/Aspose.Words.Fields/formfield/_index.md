---
title: FormField class
linktitle: FormField class
articleTitle: FormField class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Fields.FormField class. Represents a single form field"
type: docs
weight: 1150
url: /nodejs-net/Aspose.Words.Fields/formfield/
---

## FormField class

Represents a single form field.
To learn more, visit the [Working with Form Fields](https://docs.aspose.com/words/nodejs-net/working-with-form-fields/) documentation article.




### Remarks

Microsoft Word provides the following form fields: checkbox, text input and dropdown (combobox).

[FormField](./) is an inline-node and can only be a child of [Paragraph](../../Aspose.Words/paragraph/).

[FormField](./) is represented in a document by a special character and
positioned as a character within a line of text.

A complete form field in a Word document is a complex structure represented by several
nodes: field start, field code such as FORMTEXT, form field data, field separator,
field result, field end and a bookmark. To programmatically create form fields in a Word document use
[DocumentBuilder.insertCheckBox()](../../Aspose.Words/documentbuilder/insertCheckBox/#string_boolean_number),
[DocumentBuilder.insertTextInput()](../../Aspose.Words/documentbuilder/insertTextInput/#string_textformfieldtype_string_string_number) and
[DocumentBuilder.insertComboBox()](../../Aspose.Words/documentbuilder/insertComboBox/#string_string[]_number) which
make sure all of the form field nodes are created in a correct order and in a suitable state.




**Inheritance:** [FormField](./) → [SpecialChar](../../Aspose.Words/specialchar/) → [Inline](../../Aspose.Words/inline/) → [Node](../../Aspose.Words/node/)

### Properties

| Name | Description |
| --- | --- |
| [calculateOnExit](./calculateOnExit/) | True if references to the specified form field are automatically updated whenever the field is exited. |
| [checkBoxSize](./checkBoxSize/) | Gets or sets the size of the checkbox in points. Has effect only when [FormField.isCheckBoxExactSize](./isCheckBoxExactSize/) is ``True``. |
| [checked](./checked/) | Gets or sets the checked status of the check box form field. Default value for this property is ``False``. |
| [customNodeId](../../Aspose.Words/node/customNodeId/) | Specifies custom node identifier.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [default](./default/) | Gets or sets the default value of the check box form field. Default value for this property is ``False``. |
| [document](../../Aspose.Words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [dropDownItems](./dropDownItems/) | Provides access to the items of a dropdown form field. |
| [dropDownSelectedIndex](./dropDownSelectedIndex/) | Gets or sets the index specifying the currently selected item in a dropdown form field. |
| [enabled](./enabled/) | True if a form field is enabled. |
| [entryMacro](./entryMacro/) | Returns or sets an entry macro name for the form field. |
| [exitMacro](./exitMacro/) | Returns or sets an exit macro name for the form field. |
| [font](../../Aspose.Words/inline/font/) | Provides access to the font formatting of this object.<br>(Inherited from [Inline](../../Aspose.Words/inline/)) |
| [helpText](./helpText/) | Returns or sets the text that's displayed in a message box when the form field has the focus and the user presses F1. |
| [isCheckBoxExactSize](./isCheckBoxExactSize/) | Gets or sets the boolean value that indicates whether the size of the textbox is automatic or specified explicitly. |
| [isComposite](../../Aspose.Words/node/isComposite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [isDeleteRevision](../../Aspose.Words/inline/isDeleteRevision/) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../Aspose.Words/inline/)) |
| [isFormatRevision](../../Aspose.Words/inline/isFormatRevision/) | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../Aspose.Words/inline/)) |
| [isInsertRevision](../../Aspose.Words/inline/isInsertRevision/) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../Aspose.Words/inline/)) |
| [isMoveFromRevision](../../Aspose.Words/inline/isMoveFromRevision/) | Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../Aspose.Words/inline/)) |
| [isMoveToRevision](../../Aspose.Words/inline/isMoveToRevision/) | Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../Aspose.Words/inline/)) |
| [maxLength](./maxLength/) | Maximum length for the text field. Zero when the length is not limited. |
| [name](./name/) | Gets or sets the form field name. |
| [nextSibling](../../Aspose.Words/node/nextSibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [nodeType](./nodeType/) | Returns [NodeType.FormField](../../Aspose.Words/nodetype/#FormField). |
| [ownHelp](./ownHelp/) | Specifies the source of the text that's displayed in a message box when a form field has the focus and the user presses F1. |
| [ownStatus](./ownStatus/) | Specifies the source of the text that's displayed in the status bar when a form field has the focus. |
| [parentNode](../../Aspose.Words/node/parentNode/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [parentParagraph](../../Aspose.Words/inline/parentParagraph/) | Retrieves the parent [Paragraph](../../Aspose.Words/paragraph/) of this node.<br>(Inherited from [Inline](../../Aspose.Words/inline/)) |
| [previousSibling](../../Aspose.Words/node/previousSibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [range](../../Aspose.Words/node/range/) | Returns a [Range](../../Aspose.Words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [result](./result/) | Gets or sets a string that represents the result of this form field. |
| [statusText](./statusText/) | Returns or sets the text that's displayed in the status bar when a form field has the focus. |
| [textInputDefault](./textInputDefault/) | Gets or sets the default string or a calculation expression of a text form field. |
| [textInputFormat](./textInputFormat/) | Returns or sets the text formatting for a text form field. |
| [textInputType](./textInputType/) | Gets or sets the type of a text form field. |
| [type](./type/) | Returns the form field type. |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ asBody()](../../Aspose.Words/node/asBody/#default) | Cast node to [Body](../../Aspose.Words/body/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asBookmarkEnd()](../../Aspose.Words/node/asBookmarkEnd/#default) | Cast node to [BookmarkEnd](../../Aspose.Words/bookmarkend/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asBookmarkStart()](../../Aspose.Words/node/asBookmarkStart/#default) | Cast node to [BookmarkStart](../../Aspose.Words/bookmarkstart/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asBuildingBlock()](../../Aspose.Words/node/asBuildingBlock/#default) | Cast node to [BuildingBlock](../../Aspose.Words/buildingblock/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asCell()](../../Aspose.Words/node/asCell/#default) | Cast node to [Cell](../../Aspose.Words.Tables/cell/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asComment()](../../Aspose.Words/node/asComment/#default) | Cast node to [Comment](../../Aspose.Words/comment/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asCommentRangeEnd()](../../Aspose.Words/node/asCommentRangeEnd/#default) | Cast node to [CommentRangeEnd](../../Aspose.Words/commentrangeend/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asCommentRangeStart()](../../Aspose.Words/node/asCommentRangeStart/#default) | Cast node to [CommentRangeStart](../../Aspose.Words/commentrangestart/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asCompositeNode()](../../Aspose.Words/node/asCompositeNode/#default) | Cast node to [CompositeNode](../../Aspose.Words/compositenode/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asDocument()](../../Aspose.Words/node/asDocument/#default) | Cast node to [Node.document](../../Aspose.Words/node/document/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asEditableRangeEnd()](../../Aspose.Words/node/asEditableRangeEnd/#default) | Cast node to [EditableRangeEnd](../../Aspose.Words/editablerangeend/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asEditableRangeStart()](../../Aspose.Words/node/asEditableRangeStart/#default) | Cast node to [EditableRangeStart](../../Aspose.Words/editablerangestart/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asFieldEnd()](../../Aspose.Words/node/asFieldEnd/#default) | Cast node to [FieldEnd](../fieldend/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asFieldSeparator()](../../Aspose.Words/node/asFieldSeparator/#default) | Cast node to [FieldSeparator](../fieldseparator/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asFieldStart()](../../Aspose.Words/node/asFieldStart/#default) | Cast node to [FieldStart](../fieldstart/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asFootnote()](../../Aspose.Words/node/asFootnote/#default) | Cast node to [Footnote](../../Aspose.Words.Notes/footnote/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asFormField()](../../Aspose.Words/node/asFormField/#default) | Cast node to [FormField](./).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asGlossaryDocument()](../../Aspose.Words/node/asGlossaryDocument/#default) | Cast node to [GlossaryDocument](../../Aspose.Words.BuildingBlocks/glossarydocument/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asGroupShape()](../../Aspose.Words/node/asGroupShape/#default) | Cast node to [GroupShape](../../Aspose.Words.Drawing/groupshape/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asHeaderFooter()](../../Aspose.Words/node/asHeaderFooter/#default) | Cast node to [HeaderFooter](../../Aspose.Words/headerfooter/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asOfficeMath()](../../Aspose.Words/node/asOfficeMath/#default) | Cast node to [OfficeMath](../../Aspose.Words.Math/officemath/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asParagraph()](../../Aspose.Words/node/asParagraph/#default) | Cast node to [Paragraph](../../Aspose.Words/paragraph/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asRow()](../../Aspose.Words/node/asRow/#default) | Cast node to [Row](../../Aspose.Words.Tables/row/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asRun()](../../Aspose.Words/node/asRun/#default) | Cast node to [Run](../../Aspose.Words/run/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSection()](../../Aspose.Words/node/asSection/#default) | Cast node to [Section](../../Aspose.Words/section/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asShape()](../../Aspose.Words/node/asShape/#default) | Cast node to [Shape](../../Aspose.Words.Drawing/shape/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSmartTag()](../../Aspose.Words/node/asSmartTag/#default) | Cast node to [SmartTag](../../Aspose.Words.Markup/smarttag/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSpecialChar()](../../Aspose.Words/node/asSpecialChar/#default) | Cast node to [SpecialChar](../../Aspose.Words/specialchar/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asStructuredDocumentTag()](../../Aspose.Words/node/asStructuredDocumentTag/#default) | Cast node to [StructuredDocumentTag](../../Aspose.Words.Markup/structureddocumenttag/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asStructuredDocumentTagRangeEnd()](../../Aspose.Words/node/asStructuredDocumentTagRangeEnd/#default) | Cast node to [StructuredDocumentTagRangeEnd](../../Aspose.Words.Markup/structureddocumenttagrangeend/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asStructuredDocumentTagRangeStart()](../../Aspose.Words/node/asStructuredDocumentTagRangeStart/#default) | Cast node to [StructuredDocumentTagRangeStart](../../Aspose.Words.Markup/structureddocumenttagrangestart/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSubDocument()](../../Aspose.Words/node/asSubDocument/#default) | Cast node to [SubDocument](../../Aspose.Words/subdocument/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asTable()](../../Aspose.Words/node/asTable/#default) | Cast node to [Table](../../Aspose.Words/table/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ clone(isCloneChildren)](../../Aspose.Words/node/clone/#boolean) | Creates a duplicate of the node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ getAncestor(ancestorType)](../../Aspose.Words/node/getAncestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../Aspose.Words/nodetype/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ getText()](../../Aspose.Words/node/getText/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ nextPreOrder(rootNode)](../../Aspose.Words/node/nextPreOrder/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ nodeTypeToString(nodeType)](../../Aspose.Words/node/nodeTypeToString/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ previousPreOrder(rootNode)](../../Aspose.Words/node/previousPreOrder/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ referenceEquals(other)](../../Aspose.Words/node/referenceEquals/#node) | <br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ remove()](../../Aspose.Words/node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ removeField()](./removeField/#default) | Removes the complete form field, not just the form field special character. |
|[ setTextInputValue(newValue)](./setTextInputValue/#object) | Applies the text format specified in [FormField.textInputFormat](./textInputFormat/) and stores the value in [FormField.result](./result/). |
|[ toString(saveFormat)](../../Aspose.Words/node/toString/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ toString(saveOptions)](../../Aspose.Words/node/toString/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../Aspose.Words/node/)) |

### Examples

Shows how to insert a combo box.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.write("Please select a fruit: ");

// Insert a combo box which will allow a user to choose an option from a collection of strings.
let comboBox = builder.insertComboBox("MyComboBox", ["Apple", "Banana", "Cherry"], 0);

expect(comboBox.name).toEqual("MyComboBox");
expect(comboBox.type).toEqual(aw.Fields.FieldType.FieldFormDropDown);
expect(comboBox.result).toEqual("Apple");

// The form field will appear in the form of a "select" html tag.
doc.save(base.artifactsDir + "FormFields.create.html");
```

Shows how to formatting the entire FormField, including the field value.

```js
let doc = new aw.Document(base.myDir + "Form fields.docx");

let formField = doc.range.formFields.at(0);
formField.font.bold = true;
formField.font.size = 24;
formField.font.color = "#FF0000";

formField.result = "Aspose.formField";

doc = DocumentHelper.saveOpen(doc);

let formFieldRun = doc.firstSection.body.firstParagraph.runs.at(1);

expect(formFieldRun.text).toEqual("Aspose.formField");
expect(formFieldRun.font.bold).toEqual(true);
expect(formFieldRun.font.size).toEqual(24);
expect(formFieldRun.font.color).toEqual("#FF0000");
```

### See Also

* module [Aspose.Words.Fields](../)
* class [SpecialChar](../../Aspose.Words/specialchar/)

