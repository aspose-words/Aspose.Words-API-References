---
title: SdtListItemCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words pour .NET
description: Découvrez la propriété SdtListItemCollection Count pour récupérer facilement le nombre total d'éléments de votre collection pour une gestion efficace des données.
type: docs
weight: 10
url: /fr/net/aspose.words.markup/sdtlistitemcollection/count/
---
## SdtListItemCollection.Count property

Obtient le nombre d'éléments dans la collection.

```csharp
public int Count { get; }
```

## Exemples

Montre comment travailler avec des balises de document structurées par liste déroulante.

```csharp
Document doc = new Document();
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// Une balise de document structurée de liste déroulante est un formulaire qui permet à l'utilisateur de
// sélectionnez une option dans une liste en cliquant avec le bouton gauche et en ouvrant le formulaire dans Microsoft Word.
// La propriété « ListItems » contient tous les éléments de la liste, et chaque élément de la liste est un « SdtListItem ».
SdtListItemCollection listItems = tag.ListItems;
listItems.Add(new SdtListItem("Value 1"));

Assert.AreEqual(listItems[0].DisplayText, listItems[0].Value);

// Ajouter 3 éléments supplémentaires à la liste. Initialiser ces éléments avec un constructeur différent du premier élément.
// pour afficher les chaînes différentes de leurs valeurs.
listItems.Add(new SdtListItem("Item 2", "Value 2"));
listItems.Add(new SdtListItem("Item 3", "Value 3"));
listItems.Add(new SdtListItem("Item 4", "Value 4"));

Assert.AreEqual(4, listItems.Count);

// La liste déroulante affiche le premier élément. Affectez un autre élément à la valeur sélectionnée pour l'afficher.
listItems.SelectedValue = listItems[3];

Assert.AreEqual("Value 4", listItems.SelectedValue.Value);

// Énumérer la collection et imprimer chaque élément.
using (IEnumerator<SdtListItem> enumerator = listItems.GetEnumerator())
{
    while (enumerator.MoveNext())
        if (enumerator.Current != null)
            Console.WriteLine($"List item: {enumerator.Current.DisplayText}, value: {enumerator.Current.Value}");
}

 // Supprimer le dernier élément de la liste.
listItems.RemoveAt(3);

Assert.AreEqual(3, listItems.Count);

// Étant donné que notre contrôle déroulant est configuré pour afficher l'élément supprimé par défaut, donnez-lui un élément à afficher qui existe.
listItems.SelectedValue = listItems[1];

doc.Save(ArtifactsDir + "StructuredDocumentTag.ListItemCollection.docx");

// Utilisez la méthode « Clear » pour vider toute la collection d’éléments déroulants en une seule fois.
listItems.Clear();

Assert.AreEqual(0, listItems.Count);
```

### Voir également

* class [SdtListItemCollection](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
