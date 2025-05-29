---
title: SdtListItem.DisplayText
linktitle: DisplayText
articleTitle: DisplayText
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété DisplayText SdtListItem améliore votre contenu en personnalisant le texte affiché, en améliorant l'engagement et la clarté des utilisateurs.
type: docs
weight: 20
url: /fr/net/aspose.words.markup/sdtlistitem/displaytext/
---
## SdtListItem.DisplayText property

Obtient le texte à afficher dans le contenu de l'exécution à la place du[`Value`](../value/) contenu de l'attribut pour cet élément de liste.

```csharp
public string DisplayText { get; }
```

## Remarques

Ne peut pas être`nul` et ne peut pas être une chaîne vide.

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

* class [SdtListItem](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
