---
title: FormFieldCollection Class
linktitle: FormFieldCollection
articleTitle: FormFieldCollection
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fields.FormFieldCollection، الحل الأمثل لإدارة كافة حقول النماذج في المستند بسهولة وكفاءة.
type: docs
weight: 3040
url: /ar/net/aspose.words.fields/formfieldcollection/
---
## FormFieldCollection class

مجموعة من[`FormField`](../formfield/) الكائنات التي تمثل جميع حقول النموذج في نطاق.

لمعرفة المزيد، قم بزيارة[العمل مع حقول النموذج](https://docs.aspose.com/words/net/working-with-form-fields/) مقالة توثيقية.

```csharp
public class FormFieldCollection : IEnumerable<FormField>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.fields/formfieldcollection/count/) { get; } | إرجاع عدد حقول النموذج في المجموعة. |
| [Item](../../aspose.words.fields/formfieldcollection/item/) { get; } | يعيد حقل نموذج عند الفهرس المحدد. (2 indexers) |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clear](../../aspose.words.fields/formfieldcollection/clear/)() | يزيل جميع حقول النموذج من هذه المجموعة ومن المستند. |
| [GetEnumerator](../../aspose.words.fields/formfieldcollection/getenumerator/)() | يعيد كائن المعداد. |
| [Remove](../../aspose.words.fields/formfieldcollection/remove/)(*string*) | يزيل حقل النموذج بالاسم المحدد. |
| [RemoveAt](../../aspose.words.fields/formfieldcollection/removeat/)(*int*) | يزيل حقل النموذج عند الفهرس المحدد. |

## أمثلة

يوضح كيفية إدراج أنواع مختلفة من حقول النموذج في مستند، ومعالجتها باستخدام تنفيذ زائر المستند.

```csharp
public void Visitor()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    //استخدم منشئ المستندات لإدراج مربع المجموعة.
    builder.Write("Choose a value from this combo box: ");
    FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 0);
    comboBox.CalculateOnExit = true;
    Assert.AreEqual(3, comboBox.DropDownItems.Count);
    Assert.AreEqual(0, comboBox.DropDownSelectedIndex);
    Assert.True(comboBox.Enabled);

    builder.InsertBreak(BreakType.ParagraphBreak);

    // استخدم منشئ المستندات لإدراج مربع الاختيار.
    builder.Write("Click this check box to tick/untick it: ");
    FormField checkBox = builder.InsertCheckBox("MyCheckBox", false, 50);
    checkBox.IsCheckBoxExactSize = true;
    checkBox.HelpText = "Right click to check this box";
    checkBox.OwnHelp = true;
    checkBox.StatusText = "Checkbox status text";
    checkBox.OwnStatus = true;
    Assert.AreEqual(50.0d, checkBox.CheckBoxSize);
    Assert.False(checkBox.Checked);
    Assert.False(checkBox.Default);

    builder.InsertBreak(BreakType.ParagraphBreak);

    // استخدم منشئ المستندات لإدراج حقل نموذج إدخال النص.
    builder.Write("Enter text here: ");
    FormField textInput = builder.InsertTextInput("MyTextInput", TextFormFieldType.Regular, "", "Placeholder text", 50);
    textInput.EntryMacro = "EntryMacro";
    textInput.ExitMacro = "ExitMacro";
    textInput.TextInputDefault = "Regular";
    textInput.TextInputFormat = "FIRST CAPITAL";
    textInput.SetTextInputValue("New placeholder text");
    Assert.AreEqual(TextFormFieldType.Regular, textInput.TextInputType);
    Assert.AreEqual(50, textInput.MaxLength);

    //تحتوي هذه المجموعة على جميع حقول النماذج الخاصة بنا.
    FormFieldCollection formFields = doc.Range.FormFields;
    Assert.AreEqual(3, formFields.Count);

    // تعرض الحقول حقول النموذج. يمكننا رؤية رموزها بفتح هذا المستند.
    // في مايكروسوفت، اضغط على Alt + F9. هذه الحقول لا تحتوي على مفاتيح.
    // ويتحكم أعضاء كائن FormField بشكل كامل في محتوى حقول النموذج الخاصة بهم.
    Assert.AreEqual(3, doc.Range.Fields.Count);
    Assert.AreEqual(" FORMDROPDOWN \u0001", doc.Range.Fields[0].GetFieldCode());
    Assert.AreEqual(" FORMCHECKBOX \u0001", doc.Range.Fields[1].GetFieldCode());
    Assert.AreEqual(" FORMTEXT \u0001", doc.Range.Fields[2].GetFieldCode());

    //السماح لكل حقل نموذج بقبول زائر المستند.
    FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

    using (IEnumerator<FormField> fieldEnumerator = formFields.GetEnumerator())
        while (fieldEnumerator.MoveNext())
            fieldEnumerator.Current.Accept(formFieldVisitor);

    Console.WriteLine(formFieldVisitor.GetText());

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "FormFields.Visitor.html");
}

/// <summary>
 /// تنفيذ الزائر الذي يطبع تفاصيل حقول النموذج التي يزورها.
/// </summary>
public class FormFieldVisitor : DocumentVisitor
{
    public FormFieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة FormField في المستند.
    /// </summary>
    public override VisitorAction VisitFormField(FormField formField)
    {
        AppendLine(formField.Type + ": \"" + formField.Name + "\"");
        AppendLine("\tStatus: " + (formField.Enabled ? "Enabled" : "Disabled"));
        AppendLine("\tHelp Text:  " + formField.HelpText);
        AppendLine("\tEntry macro name: " + formField.EntryMacro);
        AppendLine("\tExit macro name: " + formField.ExitMacro);

        switch (formField.Type)
        {
            case FieldType.FieldFormDropDown:
                AppendLine("\tDrop-down items count: " + formField.DropDownItems.Count + ", default selected item index: " + formField.DropDownSelectedIndex);
                AppendLine("\tDrop-down items: " + string.Join(", ", formField.DropDownItems.ToArray()));
                break;
            case FieldType.FieldFormCheckBox:
                AppendLine("\tCheckbox size: " + formField.CheckBoxSize);
                AppendLine("\t" + "Checkbox is currently: " + (formField.Checked ? "checked, " : "unchecked, ") + "by default: " + (formField.Default ? "checked" : "unchecked"));
                break;
            case FieldType.FieldFormTextInput:
                AppendLine("\tInput format: " + formField.TextInputFormat);
                AppendLine("\tCurrent contents: " + formField.Result);
                break;
        }

        // دع الزائر يواصل زيارة العقد الأخرى.
        return VisitorAction.Continue;
    }

    /// <summary>
    /// يضيف نصًا منتهيًا بحرف سطر جديد إلى الإخراج الحالي.
    /// </summary>
    private void AppendLine(string text)
    {
        mBuilder.Append(text + '\n');
    }

    /// <summary>
    /// يحصل على النص العادي للمستند الذي جمعه الزائر.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### أنظر أيضا

* class [FormField](../formfield/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
