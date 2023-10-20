---
title: SdtListItem Class
linktitle: SdtListItem
articleTitle: SdtListItem
second_title: Aspose.Words pour .NET
description: Aspose.Words.Markup.SdtListItem classe. Cet élément spécifie un seul élément de liste au sein dun parentComboBox ouDropDownList balise de document structuré en C#.
type: docs
weight: 4020
url: /fr/net/aspose.words.markup/sdtlistitem/
---
## SdtListItem class

Cet élément spécifie un seul élément de liste au sein d'un parentComboBox ouDropDownList balise de document structuré.

Pour en savoir plus, visitez le[Balises de documents structurés ou contrôle de contenu](https://docs.aspose.com/words/net/working-with-content-control-sdt/) article documentaire.

```csharp
public class SdtListItem
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [SdtListItem](sdtlistitem/#constructor)(*string*) | Initialise une nouvelle instance de cette classe. |
| [SdtListItem](sdtlistitem/#constructor_1)(*string, string*) | Initialise une nouvelle instance de cette classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [DisplayText](../../aspose.words.markup/sdtlistitem/displaytext/) { get; } | Obtient le texte à afficher dans le contenu de l'exécution à la place du[`Value`](./value/) contenu de l'attribut pour cet élément de liste. |
| [Value](../../aspose.words.markup/sdtlistitem/value/) { get; } | Obtient la valeur de cet élément de liste. |

## Exemples

Montre comment utiliser les balises de documents structurés à liste déroulante.

```csharp
Document doc = new Document();
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// Une balise de document structuré par liste déroulante est un formulaire qui permet à l'utilisateur de
// sélectionnez une option dans une liste en cliquant avec le bouton gauche et en ouvrant le formulaire dans Microsoft Word.
// La propriété "ListItems" contient tous les éléments de la liste, et chaque élément de la liste est un "SdtListItem".
SdtListItemCollection listItems = tag.ListItems;
listItems.Add(new SdtListItem("Value 1"));

Assert.AreEqual(listItems[0].DisplayText, listItems[0].Value);

// Ajoute 3 éléments de liste supplémentaires. Initialisez ces éléments en utilisant un constructeur différent du premier élément
// pour afficher les chaînes différentes de leurs valeurs.
listItems.Add(new SdtListItem("Item 2", "Value 2"));
listItems.Add(new SdtListItem("Item 3", "Value 3"));
listItems.Add(new SdtListItem("Item 4", "Value 4"));

Assert.AreEqual(4, listItems.Count);

// La liste déroulante affiche le premier élément. Attribuez un élément de liste différent à "SelectedValue" pour l'afficher.
listItems.SelectedValue = listItems[3];

Assert.AreEqual("Value 4", listItems.SelectedValue.Value);

// Énumère la collection et imprime chaque élément.
using (IEnumerator<SdtListItem> enumerator = listItems.GetEnumerator())
{
    while (enumerator.MoveNext())
        if (enumerator.Current != null)
            Console.WriteLine($"List item: {enumerator.Current.DisplayText}, value: {enumerator.Current.Value}");
}

 // Supprime le dernier élément de la liste.
listItems.RemoveAt(3);

Assert.AreEqual(3, listItems.Count);

// Puisque notre contrôle déroulant est configuré pour afficher l'élément supprimé par défaut, donnez-lui un élément à afficher qui existe.
listItems.SelectedValue = listItems[1];

doc.Save(ArtifactsDir + "StructuredDocumentTag.ListItemCollection.docx");

// Utilisez la méthode "Clear" pour vider toute la collection d'éléments déroulants en une seule fois.
listItems.Clear();

Assert.AreEqual(0, listItems.Count);
```

### Voir également

* espace de noms [Aspose.Words.Markup](../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../)
