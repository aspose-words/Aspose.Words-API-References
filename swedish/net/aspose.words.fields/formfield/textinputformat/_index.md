---
title: FormField.TextInputFormat
linktitle: TextInputFormat
articleTitle: TextInputFormat
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FormField TextInputFormat för att enkelt anpassa textformatering för dina formulär, vilket förbättrar användarupplevelsen och datainsamlingen.
type: docs
weight: 200
url: /sv/net/aspose.words.fields/formfield/textinputformat/
---
## FormField.TextInputFormat property

Returnerar eller anger textformateringen för ett textformulärfält.

```csharp
public string TextInputFormat { get; set; }
```

## Anmärkningar

Om textformulärfältet innehåller vanlig text är giltiga formatsträngar "", "VERSALER", "GEMENER", "VERSALER" och "TITLES". Strängarna är inte skiftlägeskänsliga.

Om textformulärfältet innehåller ett nummer eller ett datum-/tidsvärde, är strängarna av typen valid nummer- eller datum- och tidsformatsträngar.

Microsoft Word tillåter strängar med högst 64 tecken.

## Exempel

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

    // Använd en dokumentbyggare för att infoga textinmatningsfält i formuläret.
    builder.Write("Enter text here: ");
    FormField textInput = builder.InsertTextInput("MyTextInput", TextFormFieldType.Regular, "", "Placeholder text", 50);
    textInput.EntryMacro = "EntryMacro";
    textInput.ExitMacro = "ExitMacro";
    textInput.TextInputDefault = "Regular";
    textInput.TextInputFormat = "FIRST CAPITAL";
    textInput.SetTextInputValue("New placeholder text");
    Assert.AreEqual(TextFormFieldType.Regular, textInput.TextInputType);
    Assert.AreEqual(50, textInput.MaxLength);

    // Denna samling innehåller alla våra formulärfält.
    FormFieldCollection formFields = doc.Range.FormFields;
    Assert.AreEqual(3, formFields.Count);

    // Fält visar våra formulärfält. Vi kan se deras fältkoder genom att öppna det här dokumentet
    // i Microsoft och trycker på Alt + F9. Dessa fält har inga växlar,
    // och medlemmar i FormField-objektet styr helt innehållet i deras formulärfält.
    Assert.AreEqual(3, doc.Range.Fields.Count);
    Assert.AreEqual(" FORMDROPDOWN \u0001", doc.Range.Fields[0].GetFieldCode());
    Assert.AreEqual(" FORMCHECKBOX \u0001", doc.Range.Fields[1].GetFieldCode());
    Assert.AreEqual(" FORMTEXT \u0001", doc.Range.Fields[2].GetFieldCode());

    // Tillåt att varje formulärfält accepterar en dokumentbesökare.
    FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

    using (IEnumerator<FormField> fieldEnumerator = formFields.GetEnumerator())
        while (fieldEnumerator.MoveNext())
            fieldEnumerator.Current.Accept(formFieldVisitor);

    Console.WriteLine(formFieldVisitor.GetText());

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "FormFields.Visitor.html");
}

/// <summary>
 /// Besökarimplementering som skriver ut information om formulärfält som besöks.
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

        // Låt besökaren fortsätta besöka andra noder.
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Lägger till nyradsavslutad text till aktuell utdata.
    /// </summary>
    private void AppendLine(string text)
    {
        mBuilder.Append(text + '\n');
    }

    /// <summary>
    /// Hämtar klartexten från dokumentet som besökaren samlade in.
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
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
