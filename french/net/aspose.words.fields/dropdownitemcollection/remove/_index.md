---
title: DropDownItemCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words pour .NET
description: DropDownItemCollection Remove méthode. Supprime la valeur spécifiée de la collection en C#.
type: docs
weight: 90
url: /fr/net/aspose.words.fields/dropdownitemcollection/remove/
---
## DropDownItemCollection.Remove method

Supprime la valeur spécifiée de la collection.

```csharp
public void Remove(string name)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| name | String | La valeur sensible à la casse à supprimer. |

## Exemples

Montre comment insérer un champ de zone de liste déroulante et modifier les éléments de sa collection d'éléments.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère une zone de liste déroulante, puis vérifie sa collection d'éléments déroulants.
// Dans Microsoft Word, l'utilisateur cliquera sur la combo,
// puis choisissez l'un des éléments de texte de la collection à afficher.
string[] items = { "One", "Two", "Three" };
FormField comboBoxField = builder.InsertComboBox("DropDown", items, 0);
DropDownItemCollection dropDownItems = comboBoxField.DropDownItems;

Assert.AreEqual(3, dropDownItems.Count);
Assert.AreEqual("One", dropDownItems[0]);
Assert.AreEqual(1, dropDownItems.IndexOf("Two"));
Assert.IsTrue(dropDownItems.Contains("Three"));

// Il existe deux manières d'ajouter un nouvel élément à une collection existante d'éléments de liste déroulante.
// 1 - Ajouter un élément à la fin de la collection :
dropDownItems.Add("Four");

// 2 - Insère un élément avant un autre élément à un index spécifié :
dropDownItems.Insert(3, "Three and a half");

Assert.AreEqual(5, dropDownItems.Count);

// Parcourez la collection et imprimez chaque élément.
using (IEnumerator<string> dropDownCollectionEnumerator = dropDownItems.GetEnumerator())
    while (dropDownCollectionEnumerator.MoveNext())
        Console.WriteLine(dropDownCollectionEnumerator.Current);

// Il existe deux manières de supprimer des éléments d'une collection d'éléments déroulants.
// 1 - Supprime un élément dont le contenu est égal à la chaîne passée :
dropDownItems.Remove("Four");

// 2 - Supprime un élément à un index :
dropDownItems.RemoveAt(3);

Assert.AreEqual(3, dropDownItems.Count);
Assert.IsFalse(dropDownItems.Contains("Three and a half"));
Assert.IsFalse(dropDownItems.Contains("Four"));

doc.Save(ArtifactsDir + "FormFields.DropDownItemCollection.html");

// Vide toute la collection d'éléments déroulants.
dropDownItems.Clear();
```

### Voir également

* class [DropDownItemCollection](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
