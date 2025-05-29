---
title: FormField.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words pour .NET
description: Découvrez comment gérer facilement la propriété FormField Name pour personnaliser et optimiser vos formulaires pour un meilleur engagement des utilisateurs et une meilleure collecte de données.
type: docs
weight: 130
url: /fr/net/aspose.words.fields/formfield/name/
---
## FormField.Name property

Obtient ou définit le nom du champ de formulaire.

```csharp
public string Name { get; set; }
```

## Remarques

Microsoft Word autorise les chaînes contenant au maximum 20 caractères.

## Exemples

Montre comment insérer une zone de liste déroulante.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Insérer une zone de liste déroulante qui permettra à un utilisateur de choisir une option parmi une collection de chaînes.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// Le champ de formulaire apparaîtra sous la forme d'une balise HTML « select ».
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### Voir également

* class [FormField](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
