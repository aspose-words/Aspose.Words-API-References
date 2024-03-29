---
title: CompositeNode.CreateNavigator
linktitle: CreateNavigator
articleTitle: CreateNavigator
second_title: Aspose.Words pour .NET
description: CompositeNode CreateNavigator méthode. Crée un navigateur qui peut être utilisé pour parcourir et lire des nœuds en C#.
type: docs
weight: 70
url: /fr/net/aspose.words/compositenode/createnavigator/
---
## CompositeNode.CreateNavigator method

Crée un navigateur qui peut être utilisé pour parcourir et lire des nœuds.

```csharp
[EditorBrowsable(EditorBrowsableState.Never)]
public XPathNavigator CreateNavigator()
```

## Exemples

Montre comment créer un XPathNavigator, puis l'utiliser pour parcourir et lire des nœuds.

```csharp
public void NodeXPathNavigator()
{
    Document doc = new Document();
    XPathNavigator navigator = doc.CreateNavigator();

    if (navigator != null)
    {
        Assert.AreEqual("Document", navigator.Name);
        Assert.AreEqual(false, navigator.MoveToNext());
        Assert.AreEqual(1, navigator.SelectChildren(XPathNodeType.All).Count);

        // L'arborescence du document contient le document, première section,
        // corps et premier paragraphe comme nœuds, chacun étant le seul enfant du précédent.
        // Nous pouvons en ajouter quelques autres pour donner à l'arborescence quelques branches que le navigateur pourra parcourir.
        DocumentBuilder docBuilder = new DocumentBuilder(doc);
        docBuilder.Write("Section 1, Paragraph 1. ");
        docBuilder.InsertParagraph();
        docBuilder.Write("Section 1, Paragraph 2. ");
        doc.AppendChild(new Section(doc));
        docBuilder.MoveToSection(1);
        docBuilder.Write("Section 2, Paragraph 1. ");

        // Utilisez notre navigateur pour imprimer une carte de tous les nœuds du document sur la console.
        StringBuilder stringBuilder = new StringBuilder();
        MapDocument(navigator, stringBuilder, 0);
        Console.Write(stringBuilder.ToString());
    }
}

/// <summary>
/// Parcourt tous les enfants d'un nœud composite et mappe la structure dans le style d'une arborescence de répertoires.
/// La quantité d'indentation spatiale indique la profondeur par rapport au nœud initial.
/// Imprime le contenu du texte du nœud actuel uniquement s'il s'agit d'un Run.
/// </summary>
private static void MapDocument(XPathNavigator navigator, StringBuilder stringBuilder, int depth)
{
    do
    {
        stringBuilder.Append(' ', depth);
        stringBuilder.Append(navigator.Name + ": ");

        if (navigator.Name == "Run")
        {
            stringBuilder.Append(navigator.Value);
        }

        stringBuilder.Append('\n');

        if (navigator.HasChildren)
        {
            navigator.MoveToFirstChild();
            MapDocument(navigator, stringBuilder, depth + 1);
            navigator.MoveToParent();
        }
    } while (navigator.MoveToNext());
}
```

### Voir également

* class [CompositeNode](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
