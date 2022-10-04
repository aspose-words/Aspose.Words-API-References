---
title: TextInputDefault
second_title: Aspose.Words för .NET API Referens
description: Hämtar eller ställer in standardsträngen eller ett beräkningsuttryck för ett textformulärfält.
type: docs
weight: 190
url: /sv/net/aspose.words.fields/formfield/textinputdefault/
---
## FormField.TextInputDefault property

Hämtar eller ställer in standardsträngen eller ett beräkningsuttryck för ett textformulärfält.

```csharp
public string TextInputDefault { get; set; }
```

### Anmärkningar

Innebörden av denna egenskap beror på värdet av[`TextInputType`](../textinputtype/) fast egendom.

När[`TextInputType`](../textinputtype/) ärRegular or Number, den här strängen anger standardsträngen för textformulärfältet. Denna sträng är innehållet som Microsoft Word kommer att visa i dokumentet när formulärfältet är tomt.

När[`TextInputType`](../textinputtype/) ärCalculated, då innehåller denna sträng uttrycket som ska beräknas. Uttrycket måste vara en formel som är giltig enligt kraven i Microsoft Word-formelfält . När du ställer in ett nytt uttryck med den här egenskapen, beräknar Aspose.Words formeln result automatiskt och infogar den i formulärfältet.

Microsoft Word tillåter strängar med högst 255 tecken.

### Exempel

Visar hur man infogar olika typer av formulärfält i ett dokument och bearbetar dem med hjälp av en dokumentbesökarimplementering.

```csharp
public void Visitor()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Använd en dokumentbyggare för att infoga en kombinationsruta.
    builder.Write("Choose a value from this combo box: ");
    FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 0);
    comboBox.CalculateOnExit = true;
    Assert.AreEqual(3, comboBox.DropDownItems.Count);
    Assert.AreEqual(0, comboBox.DropDownSelectedIndex);
    Assert.True(comboBox.Enabled);

    builder.InsertBreak(BreakType.ParagraphBreak);

    // Använd en dokumentbyggare för att infoga en kryssruta.
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

    // Använd en dokumentbyggare för att infoga textinmatningsformulärfält.
    builder.Write("Enter text here: ");
    FormField textInput = builder.InsertTextInput("MyTextInput", TextFormFieldType.Regular, "", "Placeholder text", 50);
    textInput.EntryMacro = "EntryMacro";
    textInput.ExitMacro = "ExitMacro";
    textInput.TextInputDefault = "Regular";
    textInput.TextInputFormat = "FIRST CAPITAL";
    textInput.SetTextInputValue("New placeholder text");
    Assert.AreEqual(TextFormFieldType.Regular, textInput.TextInputType);
    Assert.AreEqual(50, textInput.MaxLength);

    // Den här samlingen innehåller alla våra formulärfält.
    FormFieldCollection formFields = doc.Range.FormFields;
    Assert.AreEqual(3, formFields.Count);

    // Fält visar våra formulärfält. Vi kan se deras fältkoder genom att öppna detta dokument
    // i Microsoft och tryck på Alt + F9. Dessa fält har inga omkopplare,
    // och medlemmar av FormField-objektet styr helt deras formulärfälts innehåll.
    Assert.AreEqual(3, doc.Range.Fields.Count);
    Assert.AreEqual(" FORMDROPDOWN \u0001", doc.Range.Fields[0].GetFieldCode());
    Assert.AreEqual(" FORMCHECKBOX \u0001", doc.Range.Fields[1].GetFieldCode());
    Assert.AreEqual(" FORMTEXT \u0001", doc.Range.Fields[2].GetFieldCode());

    // Tillåt varje formulärfält att acceptera en dokumentbesökare.
    FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

    using (IEnumerator<FormField> fieldEnumerator = formFields.GetEnumerator())
        while (fieldEnumerator.MoveNext())
            fieldEnumerator.Current.Accept(formFieldVisitor);

    Console.WriteLine(formFieldVisitor.GetText());

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "FormFields.Visitor.html");
}

/// <summary>
/// Besöksimplementering som skriver ut detaljer om formulärfält som den besöker. 
/// </summary>
public class FormFieldVisitor : DocumentVisitor
{
    public FormFieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Anropas när en FormField-nod påträffas i dokumentet.
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

        // Låt besökaren fortsätta att besöka andra noder.
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Lägger till nyrads teckenavslutad text till den aktuella utgången.
    /// </summary>
    private void AppendLine(string text)
    {
        mBuilder.Append(text + '\n');
    }

    /// <summary>
    /// Hämtar vanlig text av dokumentet som samlades av besökaren.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### Se även

* class [FormField](../)
* namnutrymme [Aspose.Words.Fields](../../formfield/)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
