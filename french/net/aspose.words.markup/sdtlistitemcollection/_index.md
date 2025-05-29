---
title: SdtListItemCollection Class
linktitle: SdtListItemCollection
articleTitle: SdtListItemCollection
second_title: Aspose.Words pour .NET
description: Explorez la classe Aspose.Words.Markup.SdtListItemCollection pour un accès transparent aux éléments SdtListItem, améliorant ainsi sans effort la gestion structurée des documents.
type: docs
weight: 4720
url: /fr/net/aspose.words.markup/sdtlistitemcollection/
---
## SdtListItemCollection class

Donne accès à[`SdtListItem`](../sdtlistitem/) éléments d'une balise de document structuré.

Pour en savoir plus, visitez le[Balises de documents structurés ou contrôle de contenu](https://docs.aspose.com/words/net/working-with-content-control-sdt/) article de documentation.

```csharp
public class SdtListItemCollection : IEnumerable<SdtListItem>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.markup/sdtlistitemcollection/count/) { get; } | Obtient le nombre d'éléments dans la collection. |
| [Item](../../aspose.words.markup/sdtlistitemcollection/item/) { get; } | Renvoie un[`SdtListItem`](../sdtlistitem/) objet étant donné son index de base zéro dans la collection. |
| [SelectedValue](../../aspose.words.markup/sdtlistitemcollection/selectedvalue/) { get; set; } | Spécifie la valeur actuellement sélectionnée dans cette liste. Valeur nulle autorisée, ce qui signifie qu'aucune entrée actuellement sélectionnée n'est associée à cette collection d'éléments de liste. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words.markup/sdtlistitemcollection/add/)(*[SdtListItem](../sdtlistitem/)*) | Ajoute un élément à cette collection. |
| [Clear](../../aspose.words.markup/sdtlistitemcollection/clear/)() | Efface tous les éléments de cette collection. |
| [GetEnumerator](../../aspose.words.markup/sdtlistitemcollection/getenumerator/)() | Renvoie un objet énumérateur qui peut être utilisé pour parcourir tous les éléments de la collection. |
| [RemoveAt](../../aspose.words.markup/sdtlistitemcollection/removeat/)(*int*) | Supprime un élément de liste à l'index spécifié. |

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

* class [SdtListItem](../sdtlistitem/)
* espace de noms [Aspose.Words.Markup](../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../)
