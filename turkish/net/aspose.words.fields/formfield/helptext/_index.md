---
title: FormField.HelpText
second_title: Aspose.Words for .NET API Referansı
description: FormField mülk. Odak form alanı olduğunda ve kullanıcı F1e bastığında bir mesaj kutusunda görüntülenen metni döndürür veya ayarlar.
type: docs
weight: 100
url: /tr/net/aspose.words.fields/formfield/helptext/
---
## FormField.HelpText property

Odak form alanı olduğunda ve kullanıcı F1'e bastığında bir mesaj kutusunda görüntülenen metni döndürür veya ayarlar.

```csharp
public string HelpText { get; set; }
```

### Notlar

OwnHelp özelliği True olarak ayarlanırsa, HelpText metin dizesi değerini belirtir. OwnHelp False olarak ayarlanırsa, HelpText, form alanı için help metnini içeren bir Otomatik Metin girişinin adını belirtir.

Microsoft Word, en fazla 255 karakterden oluşan dizelere izin verir.

### Örnekler

Bir belgeye farklı türde form alanlarının nasıl ekleneceğini ve bunları bir belge ziyaretçisi uygulaması kullanarak nasıl işlediğini gösterir.

```csharp
public void Visitor()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Birleşik giriş kutusu eklemek için bir belge oluşturucu kullanın.
    builder.Write("Choose a value from this combo box: ");
    FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 0);
    comboBox.CalculateOnExit = true;
    Assert.AreEqual(3, comboBox.DropDownItems.Count);
    Assert.AreEqual(0, comboBox.DropDownSelectedIndex);
    Assert.True(comboBox.Enabled);

    builder.InsertBreak(BreakType.ParagraphBreak);

    // Onay kutusu eklemek için bir belge oluşturucu kullanın.
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

    // Metin giriş formu alanı eklemek için bir belge oluşturucu kullanın.
    builder.Write("Enter text here: ");
    FormField textInput = builder.InsertTextInput("MyTextInput", TextFormFieldType.Regular, "", "Placeholder text", 50);
    textInput.EntryMacro = "EntryMacro";
    textInput.ExitMacro = "ExitMacro";
    textInput.TextInputDefault = "Regular";
    textInput.TextInputFormat = "FIRST CAPITAL";
    textInput.SetTextInputValue("New placeholder text");
    Assert.AreEqual(TextFormFieldType.Regular, textInput.TextInputType);
    Assert.AreEqual(50, textInput.MaxLength);

    // Bu koleksiyon tüm form alanlarımızı içerir.
    FormFieldCollection formFields = doc.Range.FormFields;
    Assert.AreEqual(3, formFields.Count);

    // Alanlar form alanlarımızı görüntüler. Bu belgeyi açarak alan kodlarını görebiliriz.
    // Microsoft'ta ve Alt + F9 tuşlarına basın. Bu alanların anahtarı yoktur,
    // ve FormField nesnesinin üyeleri, form alanlarının içeriğini tamamen yönetir.
    Assert.AreEqual(3, doc.Range.Fields.Count);
    Assert.AreEqual(" FORMDROPDOWN \u0001", doc.Range.Fields[0].GetFieldCode());
    Assert.AreEqual(" FORMCHECKBOX \u0001", doc.Range.Fields[1].GetFieldCode());
    Assert.AreEqual(" FORMTEXT \u0001", doc.Range.Fields[2].GetFieldCode());

    // Her form alanının bir belge ziyaretçisini kabul etmesine izin verin.
    FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

    using (IEnumerator<FormField> fieldEnumerator = formFields.GetEnumerator())
        while (fieldEnumerator.MoveNext())
            fieldEnumerator.Current.Accept(formFieldVisitor);

    Console.WriteLine(formFieldVisitor.GetText());

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "FormFields.Visitor.html");
}

/// <summary>
/// Ziyaret ettiği form alanlarının ayrıntılarını yazdıran ziyaretçi uygulaması. 
/// </summary>
public class FormFieldVisitor : DocumentVisitor
{
    public FormFieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Belgede bir FormField düğümüyle karşılaşıldığında çağrılır.
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

        // Ziyaretçinin diğer düğümleri ziyaret etmesine izin verin.
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Geçerli çıktıya yeni satır karakteriyle sonlandırılmış metin ekler.
    /// </summary>
    private void AppendLine(string text)
    {
        mBuilder.Append(text + '\n');
    }

    /// <summary>
    /// Ziyaretçi tarafından toplanan belgenin düz metnini alır.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### Ayrıca bakınız

* class [FormField](../)
* ad alanı [Aspose.Words.Fields](../../formfield/)
* toplantı [Aspose.Words](../../../)


