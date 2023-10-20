---
title: FormFieldCollection Class
linktitle: FormFieldCollection
articleTitle: FormFieldCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.FormFieldCollection sınıf. Bir koleksiyonFormField bir aralıktaki tüm form alanlarını temsil eden nesneler C#'da.
type: docs
weight: 2630
url: /tr/net/aspose.words.fields/formfieldcollection/
---
## FormFieldCollection class

Bir koleksiyon[`FormField`](../formfield/) bir aralıktaki tüm form alanlarını temsil eden nesneler.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Form Alanlarıyla Çalışmak](https://docs.aspose.com/words/net/working-with-form-fields/) dokümantasyon makalesi.

```csharp
public class FormFieldCollection : IEnumerable<FormField>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.fields/formfieldcollection/count/) { get; } | Koleksiyondaki form alanlarının sayısını döndürür. |
| [Item](../../aspose.words.fields/formfieldcollection/item/) { get; } | Belirtilen dizindeki bir form alanını döndürür. (2 indexers) |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clear](../../aspose.words.fields/formfieldcollection/clear/)() | Tüm form alanlarını bu koleksiyondan ve belgeden kaldırır. |
| [GetEnumerator](../../aspose.words.fields/formfieldcollection/getenumerator/)() | Bir numaralandırıcı nesnesini döndürür. |
| [Remove](../../aspose.words.fields/formfieldcollection/remove/)(*string*) | Belirtilen ada sahip bir form alanını kaldırır. |
| [RemoveAt](../../aspose.words.fields/formfieldcollection/removeat/)(*int*) | Belirtilen dizindeki bir form alanını kaldırır. |

## Örnekler

Bir belgeye farklı türde form alanlarının nasıl eklendiğini ve bunların bir belge ziyaretçi uygulaması kullanılarak nasıl işlendiğini gösterir.

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

    // Onay kutusu eklemek için belge oluşturucuyu kullanın.
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

    // Metin giriş formu alanını eklemek için bir belge oluşturucu kullanın.
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

    // Alanlar form alanlarımızı gösterir. Bu belgeyi açarak alan kodlarını görebiliriz.
    // Microsoft'ta ve Alt + F9 tuşlarına basıyorum. Bu alanların anahtarları yoktur,
    // ve FormField nesnesinin üyeleri, form alanlarının içeriğini tamamen yönetir.
    Assert.AreEqual(3, doc.Range.Fields.Count);
    Assert.AreEqual(" FORMDROPDOWN \u0001", doc.Range.Fields[0].GetFieldCode());
    Assert.AreEqual(" FORMCHECKBOX \u0001", doc.Range.Fields[1].GetFieldCode());
    Assert.AreEqual(" FORMTEXT \u0001", doc.Range.Fields[2].GetFieldCode());

    // Her form alanının bir belge ziyaretçisini kabul etmesine izin ver.
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

        // Ziyaretçinin diğer düğümleri ziyaret etmeye devam etmesine izin verin.
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Geçerli çıktıya yeni satır karakteriyle sonlandırılmış metni ekler.
    /// </summary>
    private void AppendLine(string text)
    {
        mBuilder.Append(text + '\n');
    }

    /// <summary>
    /// Ziyaretçinin biriktirdiği belgenin düz metnini alır.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### Ayrıca bakınız

* class [FormField](../formfield/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
