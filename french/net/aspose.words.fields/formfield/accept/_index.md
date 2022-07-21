---
title: Accept
second_title: Référence de l'API Aspose.Words pour .NET
description: Accepte un visiteur.
type: docs
weight: 230
url: /fr/net/aspose.words.fields/formfield/accept/
---
## FormField.Accept method

Accepte un visiteur.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| visitor | DocumentVisitor | Le visiteur qui visitera le nœud. |

### Return_Value

Faux si le visiteur a demandé l'arrêt de l'énumération.

### Remarques

Appelle DocumentVisitor.VisitFormField.

Pour plus d'informations, consultez le modèle de conception Visiteur.

### Exemples

Montre comment insérer différents types de champs de formulaire dans un document et les traiter à l'aide d'une implémentation de visiteur de document.

```csharp
public void Visitor()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Utilise un générateur de document pour insérer une zone de liste déroulante.
    builder.Write("Choose a value from this combo box: ");
    FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 0);
    comboBox.CalculateOnExit = true;
    Assert.AreEqual(3, comboBox.DropDownItems.Count);
    Assert.AreEqual(0, comboBox.DropDownSelectedIndex);
    Assert.True(comboBox.Enabled);

    builder.InsertBreak(BreakType.ParagraphBreak);

    // Utilisez un générateur de document pour insérer une case à cocher.
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

    // Utilisez un générateur de document pour insérer un champ de formulaire de saisie de texte.
    builder.Write("Enter text here: ");
    FormField textInput = builder.InsertTextInput("MyTextInput", TextFormFieldType.Regular, "", "Placeholder text", 50);
    textInput.EntryMacro = "EntryMacro";
    textInput.ExitMacro = "ExitMacro";
    textInput.TextInputDefault = "Regular";
    textInput.TextInputFormat = "FIRST CAPITAL";
    textInput.SetTextInputValue("New placeholder text");
    Assert.AreEqual(TextFormFieldType.Regular, textInput.TextInputType);
    Assert.AreEqual(50, textInput.MaxLength);

    // Cette collection contient tous nos champs de formulaire.
    FormFieldCollection formFields = doc.Range.FormFields;
    Assert.AreEqual(3, formFields.Count);

    // Les champs affichent nos champs de formulaire. Nous pouvons voir leurs codes de champ en ouvrant ce document
    // dans Microsoft et en appuyant sur Alt + F9. Ces champs n'ont pas de commutateurs,
    // et les membres de l'objet FormField régissent entièrement le contenu de leurs champs de formulaire.
    Assert.AreEqual(3, doc.Range.Fields.Count);
    Assert.AreEqual(" FORMDROPDOWN \u0001", doc.Range.Fields[0].GetFieldCode());
    Assert.AreEqual(" FORMCHECKBOX \u0001", doc.Range.Fields[1].GetFieldCode());
    Assert.AreEqual(" FORMTEXT \u0001", doc.Range.Fields[2].GetFieldCode());

    // Autoriser chaque champ de formulaire à accepter un visiteur de document.
    FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

    using (IEnumerator<FormField> fieldEnumerator = formFields.GetEnumerator())
        while (fieldEnumerator.MoveNext())
            fieldEnumerator.Current.Accept(formFieldVisitor);

    Console.WriteLine(formFieldVisitor.GetText());

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "FormFields.Visitor.html");
}

/// <summary>
/// Implémentation de visiteur qui imprime les détails des champs de formulaire qu'il visite. 
/// </summary>
public class FormFieldVisitor : DocumentVisitor
{
    public FormFieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Appelé lorsqu'un nœud FormField est rencontré dans le document.
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

        // Laisser le visiteur continuer à visiter d'autres nœuds.
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Ajoute du texte terminé par un caractère de saut de ligne à la sortie actuelle.
    /// </summary>
    private void AppendLine(string text)
    {
        mBuilder.Append(text + '\n');
    }

    /// <summary>
    /// Obtient le texte brut du document qui a été accumulé par le visiteur.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### Voir également

* class [DocumentVisitor](../../../aspose.words/documentvisitor)
* class [FormField](../../formfield)
* espace de noms [Aspose.Words.Fields](../../formfield)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
