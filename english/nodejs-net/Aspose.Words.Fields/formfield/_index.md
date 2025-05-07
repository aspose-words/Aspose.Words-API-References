---
title: FormField class
linktitle: FormField class
articleTitle: FormField class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Fields.FormField class. Represents a single form field"
type: docs
weight: 1150
url: /nodejs-net/aspose.words.fields/formfield/
---

## FormField class

Represents a single form field.
To learn more, visit the [Working with Form Fields](https://docs.aspose.com/words/nodejs-net/working-with-form-fields/) documentation article.




### Remarks

Microsoft Word provides the following form fields: checkbox, text input and dropdown (combobox).

[FormField](./) is an inline-node and can only be a child of [Paragraph](../../aspose.words/paragraph/).

[FormField](./) is represented in a document by a special character and
positioned as a character within a line of text.

A complete form field in a Word document is a complex structure represented by several
nodes: field start, field code such as FORMTEXT, form field data, field separator,
field result, field end and a bookmark. To programmatically create form fields in a Word document use
[DocumentBuilder.insertCheckBox()](../../aspose.words/documentbuilder/insertCheckBox/#string_boolean_number),
[DocumentBuilder.insertTextInput()](../../aspose.words/documentbuilder/insertTextInput/#string_textformfieldtype_string_string_number) and
[DocumentBuilder.insertComboBox()](../../aspose.words/documentbuilder/insertComboBox/#string_string[]_number) which
make sure all of the form field nodes are created in a correct order and in a suitable state.




**Inheritance:** [FormField](./) → [SpecialChar](../../aspose.words/specialchar/) → [Inline](../../aspose.words/inline/) → [Node](../../aspose.words/node/)

### Properties

| Name | Description |
| --- | --- |
| [calculateOnExit](./calculateOnExit/) | True if references to the specified form field are automatically updated whenever the field is exited. |
| [checkBoxSize](./checkBoxSize/) | Gets or sets the size of the checkbox in points. Has effect only when [FormField.isCheckBoxExactSize](./isCheckBoxExactSize/) is ``true``. |
| [checked](./checked/) | Gets or sets the checked status of the check box form field. Default value for this property is ``false``. |
| [customNodeId](../../aspose.words/node/customNodeId/) | Specifies custom node identifier.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [default](./default/) | Gets or sets the default value of the check box form field. Default value for this property is ``false``. |
| [document](../../aspose.words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [dropDownItems](./dropDownItems/) | Provides access to the items of a dropdown form field. |
| [dropDownSelectedIndex](./dropDownSelectedIndex/) | Gets or sets the index specifying the currently selected item in a dropdown form field. |
| [enabled](./enabled/) | True if a form field is enabled. |
| [entryMacro](./entryMacro/) | Returns or sets an entry macro name for the form field. |
| [exitMacro](./exitMacro/) | Returns or sets an exit macro name for the form field. |
| [font](../../aspose.words/inline/font/) | Provides access to the font formatting of this object.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [helpText](./helpText/) | Returns or sets the text that's displayed in a message box when the form field has the focus and the user presses F1. |
| [isCheckBoxExactSize](./isCheckBoxExactSize/) | Gets or sets the boolean value that indicates whether the size of the textbox is automatic or specified explicitly. |
| [isComposite](../../aspose.words/node/isComposite/) | Returns ``true`` if this node can contain other nodes.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [isDeleteRevision](../../aspose.words/inline/isDeleteRevision/) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [isFormatRevision](../../aspose.words/inline/isFormatRevision/) | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [isInsertRevision](../../aspose.words/inline/isInsertRevision/) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [isMoveFromRevision](../../aspose.words/inline/isMoveFromRevision/) | Returns ``true`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [isMoveToRevision](../../aspose.words/inline/isMoveToRevision/) | Returns ``true`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [maxLength](./maxLength/) | Maximum length for the text field. Zero when the length is not limited. |
| [name](./name/) | Gets or sets the form field name. |
| [nextSibling](../../aspose.words/node/nextSibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [nodeType](./nodeType/) | Returns [NodeType.FormField](../../aspose.words/nodetype/#FormField). |
| [ownHelp](./ownHelp/) | Specifies the source of the text that's displayed in a message box when a form field has the focus and the user presses F1. |
| [ownStatus](./ownStatus/) | Specifies the source of the text that's displayed in the status bar when a form field has the focus. |
| [parentNode](../../aspose.words/node/parentNode/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [parentParagraph](../../aspose.words/inline/parentParagraph/) | Retrieves the parent [Paragraph](../../aspose.words/paragraph/) of this node.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [previousSibling](../../aspose.words/node/previousSibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [range](../../aspose.words/node/range/) | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
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
|[ asBody()](../../aspose.words/node/asBody/#default) | Cast node to [Body](../../aspose.words/body/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asBookmarkEnd()](../../aspose.words/node/asBookmarkEnd/#default) | Cast node to [BookmarkEnd](../../aspose.words/bookmarkend/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asBookmarkStart()](../../aspose.words/node/asBookmarkStart/#default) | Cast node to [BookmarkStart](../../aspose.words/bookmarkstart/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asBuildingBlock()](../../aspose.words/node/asBuildingBlock/#default) | Cast node to [BuildingBlock](../../aspose.words/buildingblock/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asCell()](../../aspose.words/node/asCell/#default) | Cast node to [Cell](../../aspose.words.tables/cell/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asComment()](../../aspose.words/node/asComment/#default) | Cast node to [Comment](../../aspose.words/comment/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asCommentRangeEnd()](../../aspose.words/node/asCommentRangeEnd/#default) | Cast node to [CommentRangeEnd](../../aspose.words/commentrangeend/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asCommentRangeStart()](../../aspose.words/node/asCommentRangeStart/#default) | Cast node to [CommentRangeStart](../../aspose.words/commentrangestart/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asCompositeNode()](../../aspose.words/node/asCompositeNode/#default) | Cast node to [CompositeNode](../../aspose.words/compositenode/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asDocument()](../../aspose.words/node/asDocument/#default) | Cast node to [Node.document](../../aspose.words/node/document/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asEditableRangeEnd()](../../aspose.words/node/asEditableRangeEnd/#default) | Cast node to [EditableRangeEnd](../../aspose.words/editablerangeend/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asEditableRangeStart()](../../aspose.words/node/asEditableRangeStart/#default) | Cast node to [EditableRangeStart](../../aspose.words/editablerangestart/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFieldEnd()](../../aspose.words/node/asFieldEnd/#default) | Cast node to [FieldEnd](../fieldend/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFieldSeparator()](../../aspose.words/node/asFieldSeparator/#default) | Cast node to [FieldSeparator](../fieldseparator/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFieldStart()](../../aspose.words/node/asFieldStart/#default) | Cast node to [FieldStart](../fieldstart/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFootnote()](../../aspose.words/node/asFootnote/#default) | Cast node to [Footnote](../../aspose.words.notes/footnote/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFormField()](../../aspose.words/node/asFormField/#default) | Cast node to [FormField](./).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asGlossaryDocument()](../../aspose.words/node/asGlossaryDocument/#default) | Cast node to [GlossaryDocument](../../aspose.words.buildingblocks/glossarydocument/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asGroupShape()](../../aspose.words/node/asGroupShape/#default) | Cast node to [GroupShape](../../aspose.words.drawing/groupshape/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asHeaderFooter()](../../aspose.words/node/asHeaderFooter/#default) | Cast node to [HeaderFooter](../../aspose.words/headerfooter/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asOfficeMath()](../../aspose.words/node/asOfficeMath/#default) | Cast node to [OfficeMath](../../aspose.words.math/officemath/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asParagraph()](../../aspose.words/node/asParagraph/#default) | Cast node to [Paragraph](../../aspose.words/paragraph/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asRow()](../../aspose.words/node/asRow/#default) | Cast node to [Row](../../aspose.words.tables/row/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asRun()](../../aspose.words/node/asRun/#default) | Cast node to [Run](../../aspose.words/run/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSection()](../../aspose.words/node/asSection/#default) | Cast node to [Section](../../aspose.words/section/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asShape()](../../aspose.words/node/asShape/#default) | Cast node to [Shape](../../aspose.words.drawing/shape/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSmartTag()](../../aspose.words/node/asSmartTag/#default) | Cast node to [SmartTag](../../aspose.words.markup/smarttag/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSpecialChar()](../../aspose.words/node/asSpecialChar/#default) | Cast node to [SpecialChar](../../aspose.words/specialchar/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asStructuredDocumentTag()](../../aspose.words/node/asStructuredDocumentTag/#default) | Cast node to [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asStructuredDocumentTagRangeEnd()](../../aspose.words/node/asStructuredDocumentTagRangeEnd/#default) | Cast node to [StructuredDocumentTagRangeEnd](../../aspose.words.markup/structureddocumenttagrangeend/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asStructuredDocumentTagRangeStart()](../../aspose.words/node/asStructuredDocumentTagRangeStart/#default) | Cast node to [StructuredDocumentTagRangeStart](../../aspose.words.markup/structureddocumenttagrangestart/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSubDocument()](../../aspose.words/node/asSubDocument/#default) | Cast node to [SubDocument](../../aspose.words/subdocument/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asTable()](../../aspose.words/node/asTable/#default) | Cast node to [Table](../../aspose.words/table/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ clone(isCloneChildren)](../../aspose.words/node/clone/#boolean) | Creates a duplicate of the node.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ getAncestor(ancestorType)](../../aspose.words/node/getAncestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ getText()](../../aspose.words/node/getText/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ nextPreOrder(rootNode)](../../aspose.words/node/nextPreOrder/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ nodeTypeToString(nodeType)](../../aspose.words/node/nodeTypeToString/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ previousPreOrder(rootNode)](../../aspose.words/node/previousPreOrder/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ referenceEquals(other)](../../aspose.words/node/referenceEquals/#node) | <br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove()](../../aspose.words/node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ removeField()](./removeField/#default) | Removes the complete form field, not just the form field special character. |
|[ setTextInputValue(newValue)](./setTextInputValue/#object) | Applies the text format specified in [FormField.textInputFormat](./textInputFormat/) and stores the value in [FormField.result](./result/). |
|[ toString(saveFormat)](../../aspose.words/node/toString/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ toString(saveOptions)](../../aspose.words/node/toString/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../aspose.words/node/)) |

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
* class [SpecialChar](../../aspose.words/specialchar/)

