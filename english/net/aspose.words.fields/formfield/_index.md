---
title: "FormField"
second_title: Aspose.Words for .NET API Reference
description: ""
type: docs
weight: 2410
url: /net/aspose.words.fields/formfield/
---
## FormField class

Represents a single form field.

```csharp
public class FormField : SpecialChar
```

## Public Members

| Name | Description |
| --- | --- |
| [CalculateOnExit](calculateonexit) { get; set; } | True if references to the specified form field are automatically updated whenever the field is exited. |
| [CheckBoxSize](checkboxsize) { get; set; } | Gets or sets the size of the checkbox in points. Has effect only when [`IsCheckBoxExactSize`](./ischeckboxexactsize) is true. |
| [Checked](checked) { get; set; } | Gets or sets the checked status of the check box form field. Default value for this property is false. |
| [Default](default) { get; set; } | Gets or sets the default value of the check box form field. Default value for this property is false. |
| [DropDownItems](dropdownitems) { get; } | Provides access to the items of a dropdown form field. |
| [DropDownSelectedIndex](dropdownselectedindex) { get; set; } | Gets or sets the index specifying the currently selected item in a dropdown form field. |
| [Enabled](enabled) { get; set; } | True if a form field is enabled. |
| [EntryMacro](entrymacro) { get; set; } | Returns or sets an entry macro name for the form field. |
| [ExitMacro](exitmacro) { get; set; } | Returns or sets an exit macro name for the form field. |
| [HelpText](helptext) { get; set; } | Returns or sets the text that's displayed in a message box when the form field has the focus and the user presses F1. |
| [IsCheckBoxExactSize](ischeckboxexactsize) { get; set; } | Gets or sets the boolean value that indicates whether the size of the textbox is automatic or specified explicitly. |
| [MaxLength](maxlength) { get; set; } | Maximum length for the text field. Zero when the length is not limited. |
| [Name](name) { get; set; } | Gets or sets the form field name. |
| override [NodeType](nodetype) { get; } | Returns NodeType.FormField. |
| [OwnHelp](ownhelp) { get; set; } | Specifies the source of the text that's displayed in a message box when a form field has the focus and the user presses F1. |
| [OwnStatus](ownstatus) { get; set; } | Specifies the source of the text that's displayed in the status bar when a form field has the focus. |
| [Result](result) { get; set; } | Gets or sets a string that represents the result of this form field. |
| [StatusText](statustext) { get; set; } | Returns or sets the text that's displayed in the status bar when a form field has the focus. |
| [TextInputDefault](textinputdefault) { get; set; } | Gets or sets the default string or a calculation expression of a text form field. |
| [TextInputFormat](textinputformat) { get; set; } | Returns or sets the text formatting for a text form field. |
| [TextInputType](textinputtype) { get; set; } | Gets or sets the type of a text form field. |
| [Type](type) { get; } | Returns the form field type. |
| override [Accept](accept)(…) | Accepts a visitor. |
| [RemoveField](removefield)() | Removes the complete form field, not just the form field special character. |
| [SetTextInputValue](settextinputvalue)(…) | Applies the text format specified in [`TextInputFormat`](./textinputformat) and stores the value in [`Result`](./result). |

### Remarks

Microsoft Word provides the following form fields: checkbox, text input and dropdown (combobox).FormField is an inline-node and can only be a child of Paragraph.FormField is represented in a document by a special character and positioned as a character within a line of text.A complete form field in a Word document is a complex structure represented by several nodes: field start, field code such as FORMTEXT, form field data, field separator, field result, field end and a bookmark. To programmatically create form fields in a Word document use [`DocumentBuilder.InsertCheckBox`](../../aspose.words/documentbuilder/insertcheckbox), [`DocumentBuilder.InsertTextInput`](../../aspose.words/documentbuilder/inserttextinput) and [`DocumentBuilder.InsertComboBox`](../../aspose.words/documentbuilder/insertcombobox) which make sure all of the form field nodes are created in a correct order and in a suitable state.

### Examples

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

* class [SpecialChar](../../aspose.words/specialchar)
* namespace [Aspose.Words.Fields](../../aspose.words.fields)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
