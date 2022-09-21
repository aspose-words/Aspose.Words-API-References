---
title: FormField
second_title: Aspose.Words for .NET API Reference
description: Represents a single form field.
type: docs
weight: 2460
url: /net/aspose.words.fields/formfield/
---
## FormField class

Represents a single form field.

```csharp
public class FormField : SpecialChar
```

## Properties

| Name | Description |
| --- | --- |
| [CalculateOnExit](../../aspose.words.fields/formfield/calculateonexit) { get; set; } | True if references to the specified form field are automatically updated whenever the field is exited. |
| [CheckBoxSize](../../aspose.words.fields/formfield/checkboxsize) { get; set; } | Gets or sets the size of the checkbox in points. Has effect only when [`IsCheckBoxExactSize`](./ischeckboxexactsize/) is true. |
| [Checked](../../aspose.words.fields/formfield/checked) { get; set; } | Gets or sets the checked status of the check box form field. Default value for this property is **false**. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Specifies custom node identifier. |
| [Default](../../aspose.words.fields/formfield/default) { get; set; } | Gets or sets the default value of the check box form field. Default value for this property is **false**. |
| virtual [Document](../../aspose.words/node/document) { get; } | Gets the document to which this node belongs. |
| [DropDownItems](../../aspose.words.fields/formfield/dropdownitems) { get; } | Provides access to the items of a dropdown form field. |
| [DropDownSelectedIndex](../../aspose.words.fields/formfield/dropdownselectedindex) { get; set; } | Gets or sets the index specifying the currently selected item in a dropdown form field. |
| [Enabled](../../aspose.words.fields/formfield/enabled) { get; set; } | True if a form field is enabled. |
| [EntryMacro](../../aspose.words.fields/formfield/entrymacro) { get; set; } | Returns or sets an entry macro name for the form field. |
| [ExitMacro](../../aspose.words.fields/formfield/exitmacro) { get; set; } | Returns or sets an exit macro name for the form field. |
| [Font](../../aspose.words/inline/font) { get; } | Provides access to the font formatting of this object. |
| [HelpText](../../aspose.words.fields/formfield/helptext) { get; set; } | Returns or sets the text that's displayed in a message box when the form field has the focus and the user presses F1. |
| [IsCheckBoxExactSize](../../aspose.words.fields/formfield/ischeckboxexactsize) { get; set; } | Gets or sets the boolean value that indicates whether the size of the textbox is automatic or specified explicitly. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | Returns true if this node can contain other nodes. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision) { get; } | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision) { get; } | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision) { get; } | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision) { get; } | Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision) { get; } | Returns **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [MaxLength](../../aspose.words.fields/formfield/maxlength) { get; set; } | Maximum length for the text field. Zero when the length is not limited. |
| [Name](../../aspose.words.fields/formfield/name) { get; set; } | Gets or sets the form field name. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Gets the node immediately following this node. |
| override [NodeType](../../aspose.words.fields/formfield/nodetype) { get; } | Returns **NodeType.FormField**. |
| [OwnHelp](../../aspose.words.fields/formfield/ownhelp) { get; set; } | Specifies the source of the text that's displayed in a message box when a form field has the focus and the user presses F1. |
| [OwnStatus](../../aspose.words.fields/formfield/ownstatus) { get; set; } | Specifies the source of the text that's displayed in the status bar when a form field has the focus. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Gets the immediate parent of this node. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph) { get; } | Retrieves the parent [`Paragraph`](../../aspose.words/paragraph/) of this node. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Gets the node immediately preceding this node. |
| [Range](../../aspose.words/node/range) { get; } | Returns a **Range** object that represents the portion of a document that is contained in this node. |
| [Result](../../aspose.words.fields/formfield/result) { get; set; } | Gets or sets a string that represents the result of this form field. |
| [StatusText](../../aspose.words.fields/formfield/statustext) { get; set; } | Returns or sets the text that's displayed in the status bar when a form field has the focus. |
| [TextInputDefault](../../aspose.words.fields/formfield/textinputdefault) { get; set; } | Gets or sets the default string or a calculation expression of a text form field. |
| [TextInputFormat](../../aspose.words.fields/formfield/textinputformat) { get; set; } | Returns or sets the text formatting for a text form field. |
| [TextInputType](../../aspose.words.fields/formfield/textinputtype) { get; set; } | Gets or sets the type of a text form field. |
| [Type](../../aspose.words.fields/formfield/type) { get; } | Returns the form field type. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](../../aspose.words.fields/formfield/accept)(DocumentVisitor) | Accepts a visitor. |
| [Clone](../../aspose.words/node/clone)(bool) | Creates a duplicate of the node. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Gets the first ancestor of the specified [`NodeType`](../../aspose.words/nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Gets the first ancestor of the specified object type. |
| override [GetText](../../aspose.words/specialchar/gettext)() | Gets the special character that this node represents. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Gets next node according to the pre-order tree traversal algorithm. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove)() | Removes itself from the parent. |
| [RemoveField](../../aspose.words.fields/formfield/removefield)() | Removes the complete form field, not just the form field special character. |
| [SetTextInputValue](../../aspose.words.fields/formfield/settextinputvalue)(object) | Applies the text format specified in [`TextInputFormat`](./textinputformat/) and stores the value in [`Result`](./result/). |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exports the content of the node into a string using the specified save options. |

## Remarks

Microsoft Word provides the following form fields: checkbox, text input and dropdown (combobox).

**FormField** is an inline-node and can only be a child of **Paragraph**.

**FormField** is represented in a document by a special character and positioned as a character within a line of text.

A complete form field in a Word document is a complex structure represented by several nodes: field start, field code such as FORMTEXT, form field data, field separator, field result, field end and a bookmark. To programmatically create form fields in a Word document use [`DocumentBuilder.InsertCheckBox`](../../aspose.words/documentbuilder/insertcheckbox/), [`DocumentBuilder.InsertTextInput`](../../aspose.words/documentbuilder/inserttextinput/) and [`DocumentBuilder.InsertComboBox`](../../aspose.words/documentbuilder/insertcombobox/) which make sure all of the form field nodes are created in a correct order and in a suitable state.

## Examples

Shows how to formatting the entire FormField, including the field value.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

FormField formField = doc.Range.FormFields[0];
formField.Font.Bold = true;
formField.Font.Size = 24;
formField.Font.Color = Color.Red;

formField.Result = "Aspose.FormField";

doc = DocumentHelper.SaveOpen(doc);

Run formFieldRun = doc.FirstSection.Body.FirstParagraph.Runs[1];

Assert.AreEqual("Aspose.FormField", formFieldRun.Text);
Assert.AreEqual(true, formFieldRun.Font.Bold);
Assert.AreEqual(24, formFieldRun.Font.Size);
Assert.AreEqual(Color.Red.ToArgb(), formFieldRun.Font.Color.ToArgb());
```

Shows how to insert a combo box.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Insert a combo box which will allow a user to choose an option from a collection of strings.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// The form field will appear in the form of a "select" html tag.
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### See Also

* class [SpecialChar](../../aspose.words/specialchar/)
* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
