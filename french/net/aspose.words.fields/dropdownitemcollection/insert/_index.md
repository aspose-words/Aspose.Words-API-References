---
title: DropDownItemCollection.Insert
linktitle: Insert
articleTitle: Insert
second_title: Aspose.Words pour .NET
description: Insérez facilement des chaînes dans votre DropDownItemCollection à n'importe quel index grâce à notre méthode d'insertion facile à utiliser. Optimisez la gestion de vos données dès aujourd'hui !
type: docs
weight: 80
url: /fr/net/aspose.words.fields/dropdownitemcollection/insert/
---
## DropDownItemCollection.Insert method

Insère une chaîne dans la collection à l'index spécifié.

```csharp
public void Insert(int index, string value)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| index | Int32 | L'index de base zéro auquel la valeur est insérée. |
| value | String | La chaîne à insérer. |

## Exemples

Montre comment insérer un champ de zone de liste déroulante et modifier les éléments de sa collection d'éléments.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérez une zone de liste déroulante, puis vérifiez sa collection d'éléments déroulants.
// Dans Microsoft Word, l'utilisateur cliquera sur la zone de liste déroulante,
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

// 2 - Insérer un élément avant un autre élément à un index spécifié :
dropDownItems.Insert(3, "Three and a half");

Assert.AreEqual(5, dropDownItems.Count);

// Itérer sur la collection et imprimer chaque élément.
using (IEnumerator<string> dropDownCollectionEnumerator = dropDownItems.GetEnumerator())
    while (dropDownCollectionEnumerator.MoveNext())
        Console.WriteLine(dropDownCollectionEnumerator.Current);

// Il existe deux manières de supprimer des éléments d'une collection d'éléments déroulants.
// 1 - Supprime un élément dont le contenu est égal à la chaîne passée :
dropDownItems.Remove("Four");

// 2 - Supprimer un élément à un index :
dropDownItems.RemoveAt(3);

Assert.AreEqual(3, dropDownItems.Count);
Assert.IsFalse(dropDownItems.Contains("Three and a half"));
Assert.IsFalse(dropDownItems.Contains("Four"));

doc.Save(ArtifactsDir + "FormFields.DropDownItemCollection.html");

// Vider toute la collection d'éléments déroulants.
dropDownItems.Clear();
```

### Voir également

* class [DropDownItemCollection](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
