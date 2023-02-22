---
title: CompositeNode.CreateNavigator
second_title: Référence de l'API Aspose.Words pour .NET
description: CompositeNode méthode. Réservé à lutilisation du système. IXPathNavigable.
type: docs
weight: 80
url: /fr/net/aspose.words/compositenode/createnavigator/
---
## CompositeNode.CreateNavigator method

Réservé à l'utilisation du système. IXPathNavigable.

```csharp
[EditorBrowsable(EditorBrowsableState.Never)]
public XPathNavigator CreateNavigator()
```

### Exemples

Montre comment créer un XPathNavigator, puis l'utiliser pour parcourir et lire des nœuds.

```csharp
{
    Document doc = new Document();
    XPathNavigator navigator = doc.CreateNavigator();

    if (navigator != null)
    {
        Assert.AreEqual("Document", navigator.Name);
        Assert.AreEqual(false, navigator.MoveToNext());
        Assert.AreEqual(1, navigator.SelectChildren(XPathNodeType.All).Count);

        // L'arborescence du document contient le document, première section,
        // corps et premier paragraphe comme nœuds, chacun étant un enfant unique du précédent.
        // Nous pouvons en ajouter quelques autres pour donner à l'arbre des branches que le navigateur doit parcourir.
        DocumentBuilder docBuilder = new DocumentBuilder(doc);
        docBuilder.Write("Section 1, Paragraph 1. ");
        docBuilder.InsertParagraph();
        docBuilder.Write("Section 1, Paragraph 2. ");
        doc.AppendChild(new Section(doc));
        docBuilder.MoveToSection(1);
        docBuilder.Write("Section 2, Paragraph 1. ");

        // Utilisez notre navigateur pour imprimer une carte de tous les nœuds du document vers la console.
        StringBuilder stringBuilder = new StringBuilder();
        MapDocument(navigator, stringBuilder, 0);
        Console.Write(stringBuilder.ToString());
}

/// <summary>
/// Parcourt tous les enfants d'un nœud composite et mappe la structure dans le style d'une arborescence de répertoires.
/// La quantité d'espace d'indentation indique la profondeur par rapport au nœud initial.
/// Imprime le contenu textuel du nœud actuel uniquement s'il s'agit d'un Run.
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
* espace de noms [Aspose.Words](../../compositenode/)
* Assemblée [Aspose.Words](../../../)


