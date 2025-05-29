---
title: FormFieldCollection Class
linktitle: FormFieldCollection
articleTitle: FormFieldCollection
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fields.FormFieldCollection, votre solution de référence pour gérer tous les champs de formulaire d'un document avec facilité et efficacité.
type: docs
weight: 3040
url: /fr/net/aspose.words.fields/formfieldcollection/
---
## FormFieldCollection class

Une collection de[`FormField`](../formfield/) objets qui représentent tous les champs de formulaire dans une plage.

Pour en savoir plus, visitez le[Travailler avec les champs de formulaire](https://docs.aspose.com/words/net/working-with-form-fields/) article de documentation.

```csharp
public class FormFieldCollection : IEnumerable<FormField>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.fields/formfieldcollection/count/) { get; } | Renvoie le nombre de champs de formulaire dans la collection. |
| [Item](../../aspose.words.fields/formfieldcollection/item/) { get; } | Renvoie un champ de formulaire à l'index spécifié. (2 indexers) |

## Méthodes

| Nom | La description |
| --- | --- |
| [Clear](../../aspose.words.fields/formfieldcollection/clear/)() | Supprime tous les champs de formulaire de cette collection et du document. |
| [GetEnumerator](../../aspose.words.fields/formfieldcollection/getenumerator/)() | Renvoie un objet énumérateur. |
| [Remove](../../aspose.words.fields/formfieldcollection/remove/)(*string*) | Supprime un champ de formulaire avec le nom spécifié. |
| [RemoveAt](../../aspose.words.fields/formfieldcollection/removeat/)(*int*) | Supprime un champ de formulaire à l'index spécifié. |

## Exemples

Montre comment insérer différents types de champs de formulaire dans un document et les traiter à l'aide d'une implémentation de visiteur de document.

```csharp
public void Visitor()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Utilisez un générateur de documents pour insérer une zone de liste déroulante.
    builder.Write("Choose a value from this combo box: ");
    FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 0);
    comboBox.CalculateOnExit = true;
    Assert.AreEqual(3, comboBox.DropDownItems.Count);
    Assert.AreEqual(0, comboBox.DropDownSelectedIndex);
    Assert.True(comboBox.Enabled);

    builder.InsertBreak(BreakType.ParagraphBreak);

    // Utilisez un générateur de documents pour insérer une case à cocher.
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

    // Utilisez un générateur de documents pour insérer un champ de formulaire de saisie de texte.
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

    // Les champs affichent les champs de notre formulaire. Leurs codes sont visibles en ouvrant ce document.
    // dans Microsoft et en appuyant sur Alt + F9. Ces champs n'ont pas de commutateurs,
    // et les membres de l'objet FormField gouvernent entièrement le contenu de leurs champs de formulaire.
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
 /// Implémentation du visiteur qui imprime les détails des champs de formulaire qu'il visite.
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

        // Laissez le visiteur continuer à visiter d'autres nœuds.
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Ajoute du texte terminé par un caractère de nouvelle ligne à la sortie actuelle.
    /// </summary>
    private void AppendLine(string text)
    {
        mBuilder.Append(text + '\n');
    }

    /// <summary>
    /// Obtient le texte brut du document accumulé par le visiteur.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### Voir également

* class [FormField](../formfield/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
