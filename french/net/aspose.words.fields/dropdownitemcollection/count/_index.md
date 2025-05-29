---
title: DropDownItemCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words pour .NET
description: Découvrez la propriété DropDownItemCollection Count, qui récupère efficacement le nombre total d'éléments de votre collection pour une gestion simplifiée des données.
type: docs
weight: 10
url: /fr/net/aspose.words.fields/dropdownitemcollection/count/
---
## DropDownItemCollection.Count property

Obtient le nombre d'éléments contenus dans la collection.

```csharp
public int Count { get; }
```

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
