---
title: FormFieldCollection Class
linktitle: FormFieldCollection
articleTitle: FormFieldCollection
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fields.FormFieldCollection 类，这是您轻松高效地管理文档中所有表单字段的首选解决方案。
type: docs
weight: 3040
url: /zh/net/aspose.words.fields/formfieldcollection/
---
## FormFieldCollection class

的集合[`FormField`](../formfield/)表示范围内所有表单字段的对象。

要了解更多信息，请访问[使用表单字段](https://docs.aspose.com/words/net/working-with-form-fields/)文档文章。

```csharp
public class FormFieldCollection : IEnumerable<FormField>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.fields/formfieldcollection/count/) { get; } | 返回集合中的表单字段数。 |
| [Item](../../aspose.words.fields/formfieldcollection/item/) { get; } | 返回指定索引处的表单字段。 (2 indexers) |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Clear](../../aspose.words.fields/formfieldcollection/clear/)() | 从此集合和文档中删除所有表单字段。 |
| [GetEnumerator](../../aspose.words.fields/formfieldcollection/getenumerator/)() | 返回一个枚举器对象。 |
| [Remove](../../aspose.words.fields/formfieldcollection/remove/)(*string*) | 删除具有指定名称的表单字段。 |
| [RemoveAt](../../aspose.words.fields/formfieldcollection/removeat/)(*int*) | 删除指定索引处的表单字段。 |

## 例子

展示如何将不同类型的表单字段插入文档，并使用文档访问者实现来处理它们。

```csharp
public void Visitor()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 使用文档生成器插入组合框。
    builder.Write("Choose a value from this combo box: ");
    FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 0);
    comboBox.CalculateOnExit = true;
    Assert.AreEqual(3, comboBox.DropDownItems.Count);
    Assert.AreEqual(0, comboBox.DropDownSelectedIndex);
    Assert.True(comboBox.Enabled);

    builder.InsertBreak(BreakType.ParagraphBreak);

    // 使用文档生成器插入复选框。
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

    // 使用文档构建器插入文本输入表单字段。
    builder.Write("Enter text here: ");
    FormField textInput = builder.InsertTextInput("MyTextInput", TextFormFieldType.Regular, "", "Placeholder text", 50);
    textInput.EntryMacro = "EntryMacro";
    textInput.ExitMacro = "ExitMacro";
    textInput.TextInputDefault = "Regular";
    textInput.TextInputFormat = "FIRST CAPITAL";
    textInput.SetTextInputValue("New placeholder text");
    Assert.AreEqual(TextFormFieldType.Regular, textInput.TextInputType);
    Assert.AreEqual(50, textInput.MaxLength);

    // 此集合包含我们所有的表单字段。
    FormFieldCollection formFields = doc.Range.FormFields;
    Assert.AreEqual(3, formFields.Count);

    // Fields 显示我们的表单字段。我们可以通过打开此文档来查看它们的字段代码
    // 在 Microsoft 中按下 Alt + F9。这些字段没有开关，
    // 并且 FormField 对象的成员完全控制其表单字段的内容。
    Assert.AreEqual(3, doc.Range.Fields.Count);
    Assert.AreEqual(" FORMDROPDOWN \u0001", doc.Range.Fields[0].GetFieldCode());
    Assert.AreEqual(" FORMCHECKBOX \u0001", doc.Range.Fields[1].GetFieldCode());
    Assert.AreEqual(" FORMTEXT \u0001", doc.Range.Fields[2].GetFieldCode());

    // 允许每个表单字段接受一个文档访问者。
    FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

    using (IEnumerator<FormField> fieldEnumerator = formFields.GetEnumerator())
        while (fieldEnumerator.MoveNext())
            fieldEnumerator.Current.Accept(formFieldVisitor);

    Console.WriteLine(formFieldVisitor.GetText());

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "FormFields.Visitor.html");
}

/// <summary>
 /// 访问者实现打印其访问的表单字段的详细信息。
/// </summary>
public class FormFieldVisitor : DocumentVisitor
{
    public FormFieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// 当在文档中遇到 FormField 节点时调用。
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

        // 让访问者继续访问其他节点。
        return VisitorAction.Continue;
    }

    /// <summary>
    /// 将换行符终止的文本添加到当前输出。
    /// </summary>
    private void AppendLine(string text)
    {
        mBuilder.Append(text + '\n');
    }

    /// <summary>
    /// 获取访问者积累的文档的纯文本。
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### 也可以看看

* class [FormField](../formfield/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
