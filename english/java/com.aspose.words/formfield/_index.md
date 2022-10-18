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
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [removeField()](#removeField--) | Removes the complete form field, not just the form field special character. |
| [setTextInputValue(Object newValue)](#setTextInputValue-java.lang.Object-) | Applies the text format specified in [getTextInputFormat()](../../com.aspose.words/formfield\#getTextInputFormat--) / [setTextInputFormat(java.lang.String)](../../com.aspose.words/formfield\#setTextInputFormat-java.lang.String-) and stores the value in [getResult()](../../com.aspose.words/formfield\#getResult--) / [setResult(java.lang.String)](../../com.aspose.words/formfield\#setResult-java.lang.String-). |
| [getNodeType()](#getNodeType--) | Returns **NodeType.FormField**. |
| [getName()](#getName--) | Gets the form field name. |
| [setName(String value)](#setName-java.lang.String-) | Sets the form field name. |
| [getType()](#getType--) | Returns the form field type. |
| [getResult()](#getResult--) | Gets a string that represents the result of this form field. |
| [setResult(String value)](#setResult-java.lang.String-) | Sets a string that represents the result of this form field. |
| [getStatusText()](#getStatusText--) | Gets the text that's displayed in the status bar when a form field has the focus. |
| [setStatusText(String value)](#setStatusText-java.lang.String-) | Sets the text that's displayed in the status bar when a form field has the focus. |
| [getOwnStatus()](#getOwnStatus--) | Specifies the source of the text that's displayed in the status bar when a form field has the focus. |
| [setOwnStatus(boolean value)](#setOwnStatus-boolean-) | Specifies the source of the text that's displayed in the status bar when a form field has the focus. |
| [getHelpText()](#getHelpText--) | Gets the text that's displayed in a message box when the form field has the focus and the user presses F1. |
| [setHelpText(String value)](#setHelpText-java.lang.String-) | Sets the text that's displayed in a message box when the form field has the focus and the user presses F1. |
| [getOwnHelp()](#getOwnHelp--) | Specifies the source of the text that's displayed in a message box when a form field has the focus and the user presses F1. |
| [setOwnHelp(boolean value)](#setOwnHelp-boolean-) | Specifies the source of the text that's displayed in a message box when a form field has the focus and the user presses F1. |
| [getCalculateOnExit()](#getCalculateOnExit--) | True if references to the specified form field are automatically updated whenever the field is exited. |
| [setCalculateOnExit(boolean value)](#setCalculateOnExit-boolean-) | True if references to the specified form field are automatically updated whenever the field is exited. |
| [getEntryMacro()](#getEntryMacro--) | Gets an entry macro name for the form field. |
| [setEntryMacro(String value)](#setEntryMacro-java.lang.String-) | Sets an entry macro name for the form field. |
| [getExitMacro()](#getExitMacro--) | Gets an exit macro name for the form field. |
| [setExitMacro(String value)](#setExitMacro-java.lang.String-) | Sets an exit macro name for the form field. |
| [getEnabled()](#getEnabled--) | True if a form field is enabled. |
| [setEnabled(boolean value)](#setEnabled-boolean-) | True if a form field is enabled. |
| [getTextInputFormat()](#getTextInputFormat--) | Gets the text formatting for a text form field. |
| [setTextInputFormat(String value)](#setTextInputFormat-java.lang.String-) | Sets the text formatting for a text form field. |
| [getTextInputType()](#getTextInputType--) | Gets the type of a text form field. |
| [setTextInputType(int value)](#setTextInputType-int-) | Sets the type of a text form field. |
| [getTextInputDefault()](#getTextInputDefault--) | Gets the default string or a calculation expression of a text form field. |
| [setTextInputDefault(String value)](#setTextInputDefault-java.lang.String-) | Sets the default string or a calculation expression of a text form field. |
| [getMaxLength()](#getMaxLength--) | Maximum length for the text field. |
| [setMaxLength(int value)](#setMaxLength-int-) | Maximum length for the text field. |
| [getDropDownItems()](#getDropDownItems--) | Provides access to the items of a dropdown form field. |
| [getDropDownSelectedIndex()](#getDropDownSelectedIndex--) | Gets the index specifying the currently selected item in a dropdown form field. |
| [setDropDownSelectedIndex(int value)](#setDropDownSelectedIndex-int-) | Sets the index specifying the currently selected item in a dropdown form field. |
| [getChecked()](#getChecked--) | Gets the checked status of the check box form field. |
| [setChecked(boolean value)](#setChecked-boolean-) | Sets the checked status of the check box form field. |
| [getDefault()](#getDefault--) | Gets the default value of the check box form field. |
| [setDefault(boolean value)](#setDefault-boolean-) | Sets the default value of the check box form field. |
| [isCheckBoxExactSize()](#isCheckBoxExactSize--) | Gets the boolean value that indicates whether the size of the textbox is automatic or specified explicitly. |
| [isCheckBoxExactSize(boolean value)](#isCheckBoxExactSize-boolean-) | Sets the boolean value that indicates whether the size of the textbox is automatic or specified explicitly. |
| [getCheckBoxSize()](#getCheckBoxSize--) | Gets the size of the checkbox in points. |
| [setCheckBoxSize(double value)](#setCheckBoxSize-double-) | Sets the size of the checkbox in points. |
### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

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
### removeField() {#removeField--}
```
public void removeField()
```


Removes the complete form field, not just the form field special character. If there is a bookmark associated with the form field, the bookmark is not removed.

### setTextInputValue(Object newValue) {#setTextInputValue-java.lang.Object-}
```
public void setTextInputValue(Object newValue)
```


Applies the text format specified in [getTextInputFormat()](../../com.aspose.words/formfield\#getTextInputFormat--) / [setTextInputFormat(java.lang.String)](../../com.aspose.words/formfield\#setTextInputFormat-java.lang.String-) and stores the value in [getResult()](../../com.aspose.words/formfield\#getResult--) / [setResult(java.lang.String)](../../com.aspose.words/formfield\#setResult-java.lang.String-).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newValue | java.lang.Object | Can be a string, number or a DateTime object. The [getTextInputDefault()](../../com.aspose.words/formfield\#getTextInputDefault--) / [setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield\#setTextInputDefault-java.lang.String-) value is applied if  newValue  is  null . |

### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns **NodeType.FormField**.

**Returns:**
int - **NodeType.FormField**. The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getName() {#getName--}
```
public String getName()
```


Gets the form field name. Microsoft Word allows strings with at most 20 characters.

**Returns:**
java.lang.String - The form field name.
### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


Sets the form field name. Microsoft Word allows strings with at most 20 characters.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The form field name. |

### getType() {#getType--}
```
public int getType()
```


Returns the form field type.

**Returns:**
int - The form field type. The returned value is one of [FieldType](../../com.aspose.words/fieldtype) constants.
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

### getStatusText() {#getStatusText--}
```
public String getStatusText()
```


Gets the text that's displayed in the status bar when a form field has the focus.

If the OwnStatus property is set to true, the StatusText property specifies the status bar text. If the OwnStatus property is set to false, the StatusText property specifies the name of an AutoText entry that contains status bar text for the form field.

Microsoft Word allows strings with at most 138 characters.

**Returns:**
java.lang.String - The text that's displayed in the status bar when a form field has the focus.
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

### getOwnStatus() {#getOwnStatus--}
```
public boolean getOwnStatus()
```


Specifies the source of the text that's displayed in the status bar when a form field has the focus.

If true, the text specified by the StatusText property is displayed. If false, the text of the AutoText entry specified by the StatusText property is displayed.

**Returns:**
boolean - The corresponding  boolean  value.
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

### getHelpText() {#getHelpText--}
```
public String getHelpText()
```


Gets the text that's displayed in a message box when the form field has the focus and the user presses F1.

If the OwnHelp property is set to True, HelpText specifies the text string value. If OwnHelp is set to False, HelpText specifies the name of an AutoText entry that contains help text for the form field.

Microsoft Word allows strings with at most 255 characters.

**Returns:**
java.lang.String - The text that's displayed in a message box when the form field has the focus and the user presses F1.
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

### getOwnHelp() {#getOwnHelp--}
```
public boolean getOwnHelp()
```


Specifies the source of the text that's displayed in a message box when a form field has the focus and the user presses F1.

If True, the text specified by the HelpText property is displayed. If False, the text in the AutoText entry specified by the HelpText property is displayed.

**Returns:**
boolean - The corresponding  boolean  value.
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

### getCalculateOnExit() {#getCalculateOnExit--}
```
public boolean getCalculateOnExit()
```


True if references to the specified form field are automatically updated whenever the field is exited.

Setting **CalculateOnExit** only affects the behavior of the form field when the document is opened in Microsoft Word. Aspose.Words never updates references to the form field.

**Returns:**
boolean - The corresponding  boolean  value.
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

### getEntryMacro() {#getEntryMacro--}
```
public String getEntryMacro()
```


Gets an entry macro name for the form field.

The entry macro runs when the form field gets the focus in Microsoft Word.

Microsoft Word allows strings with at most 32 characters.

**Returns:**
java.lang.String - An entry macro name for the form field.
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

### getExitMacro() {#getExitMacro--}
```
public String getExitMacro()
```


Gets an exit macro name for the form field.

The exit macro runs when the form field loses the focus in Microsoft Word.

Microsoft Word allows strings with at most 32 characters.

**Returns:**
java.lang.String - An exit macro name for the form field.
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

### getEnabled() {#getEnabled--}
```
public boolean getEnabled()
```


True if a form field is enabled.

If a form field is enabled, its contents can be changed as the form is filled in.

**Returns:**
boolean - The corresponding  boolean  value.
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

### getTextInputType() {#getTextInputType--}
```
public int getTextInputType()
```


Gets the type of a text form field.

**Returns:**
int - The type of a text form field. The returned value is one of [TextFormFieldType](../../com.aspose.words/textformfieldtype) constants.
### setTextInputType(int value) {#setTextInputType-int-}
```
public void setTextInputType(int value)
```


Sets the type of a text form field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The type of a text form field. The value must be one of [TextFormFieldType](../../com.aspose.words/textformfieldtype) constants. |

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

### getMaxLength() {#getMaxLength--}
```
public int getMaxLength()
```


Maximum length for the text field. Zero when the length is not limited.

**Returns:**
int - The corresponding  int  value.
### setMaxLength(int value) {#setMaxLength-int-}
```
public void setMaxLength(int value)
```


Maximum length for the text field. Zero when the length is not limited.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

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
### setDropDownSelectedIndex(int value) {#setDropDownSelectedIndex-int-}
```
public void setDropDownSelectedIndex(int value)
```


Sets the index specifying the currently selected item in a dropdown form field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The index specifying the currently selected item in a dropdown form field. |

### getChecked() {#getChecked--}
```
public boolean getChecked()
```


Gets the checked status of the check box form field. Default value for this property is **false**.

Applicable for a check box form field only.

**Returns:**
boolean - The checked status of the check box form field.
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

### getDefault() {#getDefault--}
```
public boolean getDefault()
```


Gets the default value of the check box form field. Default value for this property is **false**.

Applicable for a check box form field only.

**Returns:**
boolean - The default value of the check box form field.
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

### getCheckBoxSize() {#getCheckBoxSize--}
```
public double getCheckBoxSize()
```


Gets the size of the checkbox in points. Has effect only when [isCheckBoxExactSize()](../../com.aspose.words/formfield\#isCheckBoxExactSize--) / [isCheckBoxExactSize(boolean)](../../com.aspose.words/formfield\#isCheckBoxExactSize-boolean-) is true.

Applicable for a check box form field only.

**Returns:**
double - The size of the checkbox in points.
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

