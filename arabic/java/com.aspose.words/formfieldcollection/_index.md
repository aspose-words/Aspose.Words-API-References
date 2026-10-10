---
title: "FormFieldCollection"
linktitle: "FormFieldCollection"
second_title: "Aspose.Words لـ Java"
description: "A collection of FormField objects that represent all the form fields in a range in Java."
type: docs
weight: 348
url: /ar/java/com.aspose.words/formfieldcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class FormFieldCollection implements Iterable
```

A collection of [FormField](../../com.aspose.words/formfield/) objects that represent all the form fields in a range.

لمزيد من المعلومات، زر مقالة التوثيق [ Working with Form Fields ][Working with Form Fields].

 **Examples:** 

يظهر كيفية إدراج أنواع مختلفة من حقول النموذج في مستند، ومعالجتها باستخدام تنفيذ زائر المستند.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```


[Working with Form Fields]: https://docs.aspose.com/words/java/working-with-form-fields/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [clear()](#clear) | Removes all form fields from this collection and from the document. |
| [get(int index)](#get-int) | Returns a form field at the specified index. |
| [get(String bookmarkName)](#get-java.lang.String) | Returns a form field by bookmark name. |
| [getCount()](#getCount) | Returns the number of form fields in the collection. |
| [iterator()](#iterator) | يرجع كائن عداد. |
| [remove(String formField)](#remove-java.lang.String) | Removes a form field with the specified name. |
| [removeAt(int index)](#removeAt-int) | Removes a form field at the specified index. |
### clear() {#clear}
```
public void clear()
```


Removes all form fields from this collection and from the document.

 **Examples:** 

يظهر كيفية إدراج أنواع مختلفة من حقول النموذج في مستند، ومعالجتها باستخدام تنفيذ زائر المستند.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

### get(int index) {#get-int}
```
public FormField get(int index)
```


Returns a form field at the specified index.

 **Remarks:** 

الفهرس يبدأ من الصفر.

يسمح بالمؤشرات السلبية وتدل على الوصول من نهاية المجموعة. على سبيل المثال -1 يعني العنصر الأخير، -2 يعني العنصر قبل الأخير الثاني وهكذا.

إذا كان الفهرس أكبر من أو يساوي عدد العناصر في القائمة، فإن هذا يُعيد إشارة فارغة.

إذا كان الفهرس سالبًا وكانت قيمته المطلقة أكبر من عدد العناصر في القائمة، فإن هذا يُعيد إشارة فارغة.

 **Examples:** 

يظهر كيفية إدراج أنواع مختلفة من حقول النموذج في مستند، ومعالجتها باستخدام تنفيذ زائر المستند.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int | فهرس داخل المجموعة. |

**Returns:**
[FormField](../../com.aspose.words/formfield/) - A form field at the specified index.
### get(String bookmarkName) {#get-java.lang.String}
```
public FormField get(String bookmarkName)
```


Returns a form field by bookmark name.

 **Remarks:** 

Returns null if the form field with the specified bookmark name cannot be found.

 **Examples:** 

يظهر كيفية إدراج أنواع مختلفة من حقول النموذج في مستند، ومعالجتها باستخدام تنفيذ زائر المستند.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| bookmarkName | java.lang.String | Case-insensitive bookmark name. |

**Returns:**
[FormField](../../com.aspose.words/formfield/) - A form field by bookmark name.
### getCount() {#getCount}
```
public int getCount()
```


Returns the number of form fields in the collection.

 **Examples:** 

يظهر كيفية إدراج أنواع مختلفة من حقول النموذج في مستند، ومعالجتها باستخدام تنفيذ زائر المستند.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
int - The number of form fields in the collection.
### iterator() {#iterator}
```
public Iterator iterator()
```


يرجع كائن عداد.

 **Examples:** 

يظهر كيفية إدراج أنواع مختلفة من حقول النموذج في مستند، ومعالجتها باستخدام تنفيذ زائر المستند.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
java.util.Iterator
### remove(String formField) {#remove-java.lang.String}
```
public void remove(String formField)
```


Removes a form field with the specified name.

 **Remarks:** 

إذا كان هناك إشارة مرجعية مرتبطة بالحقل، فإن الإشارة المرجعية لا تُحذف.

 **Examples:** 

يظهر كيفية إدراج أنواع مختلفة من حقول النموذج في مستند، ومعالجتها باستخدام تنفيذ زائر المستند.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| formField | java.lang.String | The case-insensitive name of the form field to remove. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Removes a form field at the specified index.

 **Remarks:** 

إذا كان هناك إشارة مرجعية مرتبطة بالحقل، فإن الإشارة المرجعية لا تُحذف.

 **Examples:** 

يظهر كيفية إدراج أنواع مختلفة من حقول النموذج في مستند، ومعالجتها باستخدام تنفيذ زائر المستند.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int | The zero-based index of the form field to remove. |

