---
title: FormField.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words pour .NET
description: FormField Type propriété. Renvoie le type de champ du formulaire en C#.
type: docs
weight: 220
url: /fr/net/aspose.words.fields/formfield/type/
---
## FormField.Type property

Renvoie le type de champ du formulaire.

```csharp
public FieldType Type { get; }
```

## Exemples

Montre comment insérer une zone de liste déroulante.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Insère une zone de liste déroulante qui permettra à un utilisateur de choisir une option parmi une collection de chaînes.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// Le champ du formulaire apparaîtra sous la forme d'une balise html "select".
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### Voir également

* enum [FieldType](../../fieldtype/)
* class [FormField](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
