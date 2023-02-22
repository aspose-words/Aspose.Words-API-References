---
title: Class DropDownItemCollection
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Fields.DropDownItemCollection classe. Une collection de chaînes qui représentent tous les éléments dans un champ de formulaire déroulant.
type: docs
weight: 1350
url: /fr/net/aspose.words.fields/dropdownitemcollection/
---
## DropDownItemCollection class

Une collection de chaînes qui représentent tous les éléments dans un champ de formulaire déroulant.

```csharp
public class DropDownItemCollection : IEnumerable<string>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.fields/dropdownitemcollection/count/) { get; } | Obtient le nombre d'éléments contenus dans la collection. |
| [Item](../../aspose.words.fields/dropdownitemcollection/item/) { get; set; } | Obtient ou définit l'élément à l'index spécifié. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words.fields/dropdownitemcollection/add/)(string) | Ajoute une chaîne à la fin de la collection. |
| [Clear](../../aspose.words.fields/dropdownitemcollection/clear/)() | Supprime tous les éléments de la collection. |
| [Contains](../../aspose.words.fields/dropdownitemcollection/contains/)(string) | Détermine si la collection contient la valeur spécifiée. |
| [GetEnumerator](../../aspose.words.fields/dropdownitemcollection/getenumerator/)() | Renvoie un objet énumérateur qui peut être utilisé pour itérer sur tous les éléments de la collection. |
| [IndexOf](../../aspose.words.fields/dropdownitemcollection/indexof/)(string) | Renvoie l'index de base zéro de la valeur spécifiée dans la collection. |
| [Insert](../../aspose.words.fields/dropdownitemcollection/insert/)(int, string) | Insère une chaîne dans la collection à l'index spécifié. |
| [Remove](../../aspose.words.fields/dropdownitemcollection/remove/)(string) | Supprime la valeur spécifiée de la collection. |
| [RemoveAt](../../aspose.words.fields/dropdownitemcollection/removeat/)(int) | Supprime une valeur à l'index spécifié. |

### Exemples

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

// Il existe deux manières d'ajouter un nouvel élément à une collection existante d'éléments de la liste déroulante.
// 1 - Ajoute un élément à la fin de la collection :
dropDownItems.Add("Four");

// 2 - Insère un élément avant un autre élément à un index spécifié :
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

// Vide toute la collection d'éléments déroulants.
dropDownItems.Clear();
```

### Voir également

* class [FormField](../formfield/)
* property [DropDownItems](../formfield/dropdownitems/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)


