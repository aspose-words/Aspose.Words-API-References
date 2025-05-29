---
title: FormField.TextInputDefault
linktitle: TextInputDefault
articleTitle: TextInputDefault
second_title: Aspose.Words для .NET
description: Откройте для себя свойство TextInputDefault объекта FormField, легко задайте текст или вычисления по умолчанию для ваших форм, улучшив пользовательский интерфейс и точность данных.
type: docs
weight: 190
url: /ru/net/aspose.words.fields/formfield/textinputdefault/
---
## FormField.TextInputDefault property

Возвращает или задает строку по умолчанию или выражение расчета для поля текстовой формы.

```csharp
public string TextInputDefault { get; set; }
```

## Примечания

Значение этого свойства зависит от значения[`TextInputType`](../textinputtype/) свойство.

Когда[`TextInputType`](../textinputtype/) являетсяRegular или Numberэта строка указывает строку по умолчанию для текстового поля формы. Эта строка представляет собой содержимое, которое Microsoft Word отобразит в документе, когда поле формы пустое.

Когда[`TextInputType`](../textinputtype/) являетсяCalculated, то эта строка содержит выражение для вычисления. Выражение должно быть формулой, допустимой в соответствии с требованиями Microsoft Word formula field . Когда вы задаете новое выражение с помощью этого свойства, Aspose.Words автоматически вычисляет формулу result и вставляет ее в поле формы.

Microsoft Word допускает строки длиной не более 255 символов.

## Примеры

Показывает, как вставлять различные виды полей формы в документ и обрабатывать их с помощью реализации посетителя документа.

```csharp
public void Visitor()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Используйте конструктор документов для вставки поля со списком.
    builder.Write("Choose a value from this combo box: ");
    FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 0);
    comboBox.CalculateOnExit = true;
    Assert.AreEqual(3, comboBox.DropDownItems.Count);
    Assert.AreEqual(0, comboBox.DropDownSelectedIndex);
    Assert.True(comboBox.Enabled);

    builder.InsertBreak(BreakType.ParagraphBreak);

    // Используйте конструктор документов для вставки флажка.
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

    // Используйте конструктор документов для вставки поля формы ввода текста.
    builder.Write("Enter text here: ");
    FormField textInput = builder.InsertTextInput("MyTextInput", TextFormFieldType.Regular, "", "Placeholder text", 50);
    textInput.EntryMacro = "EntryMacro";
    textInput.ExitMacro = "ExitMacro";
    textInput.TextInputDefault = "Regular";
    textInput.TextInputFormat = "FIRST CAPITAL";
    textInput.SetTextInputValue("New placeholder text");
    Assert.AreEqual(TextFormFieldType.Regular, textInput.TextInputType);
    Assert.AreEqual(50, textInput.MaxLength);

    // Эта коллекция содержит все поля нашей формы.
    FormFieldCollection formFields = doc.Range.FormFields;
    Assert.AreEqual(3, formFields.Count);

    // Поля отображают наши поля формы. Мы можем увидеть их коды полей, открыв этот документ
    // в Microsoft и нажав Alt + F9. Эти поля не имеют переключателей,
    // и члены объекта FormField полностью управляют содержимым своих полей формы.
    Assert.AreEqual(3, doc.Range.Fields.Count);
    Assert.AreEqual(" FORMDROPDOWN \u0001", doc.Range.Fields[0].GetFieldCode());
    Assert.AreEqual(" FORMCHECKBOX \u0001", doc.Range.Fields[1].GetFieldCode());
    Assert.AreEqual(" FORMTEXT \u0001", doc.Range.Fields[2].GetFieldCode());

    // Разрешить каждому полю формы принимать посетителя документа.
    FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

    using (IEnumerator<FormField> fieldEnumerator = formFields.GetEnumerator())
        while (fieldEnumerator.MoveNext())
            fieldEnumerator.Current.Accept(formFieldVisitor);

    Console.WriteLine(formFieldVisitor.GetText());

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "FormFields.Visitor.html");
}

/// <summary>
 /// Реализация посетителя, которая печатает сведения о полях формы, которые он посещает.
/// </summary>
public class FormFieldVisitor : DocumentVisitor
{
    public FormFieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел FormField.
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

        // Позвольте посетителю продолжить посещение других узлов.
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Добавляет текст, завершающийся символом новой строки, к текущему выводу.
    /// </summary>
    private void AppendLine(string text)
    {
        mBuilder.Append(text + '\n');
    }

    /// <summary>
    /// Получает простой текст документа, накопленный посетителем.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### Смотрите также

* class [FormField](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
