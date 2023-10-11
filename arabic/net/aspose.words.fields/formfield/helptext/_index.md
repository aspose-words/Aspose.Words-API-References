---
title: FormField.HelpText
second_title: Aspose.Words لمراجع .NET API
description: FormField ملكية. إرجاع أو تعيين النص المعروض في مربع رسالة عندما يكون حقل النموذج هو التركيز ويقوم المستخدم بالضغط على F1.
type: docs
weight: 100
url: /ar/net/aspose.words.fields/formfield/helptext/
---
## FormField.HelpText property

إرجاع أو تعيين النص المعروض في مربع رسالة عندما يكون حقل النموذج هو التركيز ويقوم المستخدم بالضغط على F1.

```csharp
public string HelpText { get; set; }
```

### ملاحظات

إذا[`OwnHelp`](../ownhelp/) تم تعيين الخاصية على`حقيقي` ,`HelpText` يحدد قيمة السلسلة النصية. إذا[`OwnHelp`](../ownhelp/) تم ضبطه على`خطأ شنيع` ,`HelpText`يحدد اسم إدخال النص التلقائي الذي يحتوي على نص help لحقل النموذج.

يسمح Microsoft Word بسلاسل تحتوي على 255 حرفًا على الأكثر.

### أمثلة

يوضح كيفية إدراج أنواع مختلفة من حقول النموذج في المستند ومعالجتها باستخدام تطبيق زائر المستند.

```csharp
public void Visitor()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // استخدم منشئ المستندات لإدراج مربع التحرير والسرد.
    builder.Write("Choose a value from this combo box: ");
    FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 0);
    comboBox.CalculateOnExit = true;
    Assert.AreEqual(3, comboBox.DropDownItems.Count);
    Assert.AreEqual(0, comboBox.DropDownSelectedIndex);
    Assert.True(comboBox.Enabled);

    builder.InsertBreak(BreakType.ParagraphBreak);

    // استخدم منشئ المستندات لإدراج خانة الاختيار.
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

    // تحتوي هذه المجموعة على جميع حقول النموذج لدينا.
    FormFieldCollection formFields = doc.Range.FormFields;
    Assert.AreEqual(3, formFields.Count);

    // تعرض الحقول حقول النموذج الخاصة بنا. يمكننا رؤية رموز الحقول الخاصة بهم عن طريق فتح هذا المستند
    // في مايكروسوفت والضغط على Alt + F9. هذه الحقول ليس لها مفاتيح،
    // وأعضاء كائن FormField يتحكمون بشكل كامل في محتوى حقول النموذج الخاصة بهم.
    Assert.AreEqual(3, doc.Range.Fields.Count);
    Assert.AreEqual(" FORMDROPDOWN \u0001", doc.Range.Fields[0].GetFieldCode());
    Assert.AreEqual(" FORMCHECKBOX \u0001", doc.Range.Fields[1].GetFieldCode());
    Assert.AreEqual(" FORMTEXT \u0001", doc.Range.Fields[2].GetFieldCode());

    // السماح لكل حقل نموذج بقبول زائر المستند.
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
    /// يتم الاتصال به عند مواجهة عقدة FormField في المستند.
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

        // اسمح للزائر بمواصلة زيارة العقد الأخرى.
        return VisitorAction.Continue;
    }

    /// <summary>
    /// يضيف سطرًا جديدًا منتهيًا بالحرف إلى الإخراج الحالي.
    /// </summary>
    private void AppendLine(string text)
    {
        mBuilder.Append(text + '\n');
    }

    /// <summary>
    /// يحصل على النص العادي للمستند الذي قام الزائر بتجميعه.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### أنظر أيضا

* class [FormField](../)
* مساحة الاسم [Aspose.Words.Fields](../../formfield/)
* المجسم [Aspose.Words](../../../)


