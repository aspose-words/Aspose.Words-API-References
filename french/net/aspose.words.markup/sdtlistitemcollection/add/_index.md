---
title: SdtListItemCollection.Add
second_title: Référence de l'API Aspose.Words pour .NET
description: SdtListItemCollection méthode. Ajoute un élément à cette collection.
type: docs
weight: 40
url: /fr/net/aspose.words.markup/sdtlistitemcollection/add/
---
## SdtListItemCollection.Add method

Ajoute un élément à cette collection.

```csharp
public void Add(SdtListItem item)
```

### Exemples

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

* class [SdtListItem](../../sdtlistitem/)
* class [SdtListItemCollection](../)
* espace de noms [Aspose.Words.Markup](../../sdtlistitemcollection/)
* Assemblée [Aspose.Words](../../../)


