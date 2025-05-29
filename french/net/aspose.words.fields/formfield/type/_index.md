---
title: FormField.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Type FormField pour identifier et utiliser facilement différents types de champs de formulaire, améliorant ainsi la fonctionnalité et l'expérience utilisateur de vos formulaires Web.
type: docs
weight: 220
url: /fr/net/aspose.words.fields/formfield/type/
---
## FormField.Type property

Renvoie le type de champ de formulaire.

```csharp
public FieldType Type { get; }
```

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

* enum [FieldType](../../fieldtype/)
* class [FormField](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
