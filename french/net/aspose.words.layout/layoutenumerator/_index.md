---
title: LayoutEnumerator Class
linktitle: LayoutEnumerator
articleTitle: LayoutEnumerator
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Layout.LayoutEnumerator pour une énumération efficace de la mise en page de vos documents. Explorez la géométrie, le texte et la structure des pages sans effort !
type: docs
weight: 3790
url: /fr/net/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class

Énumère les entités de mise en page d'un document. Vous pouvez utiliser cette classe pour parcourir le modèle de mise en page. Les propriétés disponibles sont le type, la géométrie, le texte et l'index de la page où l'entité est rendue, ainsi que la structure globale et les relations. Utilisez une combinaison de[`GetEntity`](../layoutcollector/getentity/) et[`Current`](./current/) déplacer vers l'entité qui correspond à un nœud de document.

Pour en savoir plus, visitez le[Conversion au format de page fixe](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) article de documentation.

```csharp
public class LayoutEnumerator
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [LayoutEnumerator](layoutenumerator/)(*[Document](../../aspose.words/document/)*) | Initialise une nouvelle instance de cette classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [Current](../../aspose.words.layout/layoutenumerator/current/) { get; set; } | Obtient ou définit la position actuelle dans le modèle de mise en page. Cette propriété renvoie un objet opaque qui correspond à l'entité de mise en page actuelle. |
| [Document](../../aspose.words.layout/layoutenumerator/document/) { get; } | Obtient le document que cette instance énumère. |
| [Item](../../aspose.words.layout/layoutenumerator/item/) { get; } | Obtient une propriété nommée de l'entité. |
| [Kind](../../aspose.words.layout/layoutenumerator/kind/) { get; } | Récupère le type de l'entité courante. Il peut s'agir d'une chaîne vide, mais jamais`nul` . |
| [PageIndex](../../aspose.words.layout/layoutenumerator/pageindex/) { get; } | Obtient l'index de base 1 d'une page qui contient l'entité actuelle. |
| [Rectangle](../../aspose.words.layout/layoutenumerator/rectangle/) { get; } | Renvoie le rectangle de délimitation de l'entité actuelle par rapport au coin supérieur gauche de la page (en points). |
| [Text](../../aspose.words.layout/layoutenumerator/text/) { get; } | Récupère le texte de l'entité span actuelle. Lève la requête pour les autres types d'entités. |
| [Type](../../aspose.words.layout/layoutenumerator/type/) { get; } | Obtient le type de l'entité actuelle. |

## Méthodes

| Nom | La description |
| --- | --- |
| [MoveFirstChild](../../aspose.words.layout/layoutenumerator/movefirstchild/)() | Passe à la première entité enfant. |
| [MoveLastChild](../../aspose.words.layout/layoutenumerator/movelastchild/)() | Passe à la dernière entité enfant. |
| [MoveNext](../../aspose.words.layout/layoutenumerator/movenext/)() | Passe à l'entité sœur suivante dans l'ordre visuel. Lors de l'itération des lignes d'un paragraphe réparties sur plusieurs pages, cette méthode ne passera pas à la page suivante mais plutôt à l'entité suivante sur la même page. |
| [MoveNextLogical](../../aspose.words.layout/layoutenumerator/movenextlogical/)() | Passe à l'entité sœur suivante dans un ordre logique. Lors de l'itération des lignes d'un paragraphe réparties sur plusieurs pages, cette méthode passera à la ligne suivante même si elle réside sur une autre page. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent)() | Déplace vers l'entité parent. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent_1)(*[LayoutEntityType](../layoutentitytype/)*) | Déplace vers l'entité parente du type spécifié. |
| [MovePrevious](../../aspose.words.layout/layoutenumerator/moveprevious/)() | Passe à l'entité sœur précédente. |
| [MovePreviousLogical](../../aspose.words.layout/layoutenumerator/movepreviouslogical/)() | Passe à l'entité sœur précédente dans un ordre logique. Lors de l'itération des lignes d'un paragraphe réparties sur plusieurs pages, cette méthode passera à la ligne précédente même si elle réside sur une autre page. |
| [Reset](../../aspose.words.layout/layoutenumerator/reset/)() | Déplace l'énumérateur vers la première page du document. |

## Exemples

Affiche les différentes manières de parcourir les entités de mise en page d'un document.

```csharp
public void LayoutEnumerator()
{
    // Ouvrez un document contenant une variété d’entités de mise en page.
    // Les entités de mise en page sont des pages, des cellules, des lignes, des lignes et d'autres objets inclus dans l'énumération LayoutEntityType.
    // Chaque entité de mise en page dispose d'un espace rectangulaire qu'elle occupe dans le corps du document.
    Document doc = new Document(MyDir + "Layout entities.docx");

    // Créez un énumérateur qui peut parcourir ces entités comme un arbre.
    LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

    Assert.AreEqual(doc, layoutEnumerator.Document);

    layoutEnumerator.MoveParent(LayoutEntityType.Page);

    Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);
    Assert.Throws<InvalidOperationException>(() => Console.WriteLine(layoutEnumerator.Text));

    // Nous pouvons appeler cette méthode pour nous assurer que l'énumérateur sera sur la première entité de mise en page.
    layoutEnumerator.Reset();

    // Il existe deux ordres qui déterminent la manière dont l'énumérateur de mise en page continue de parcourir les entités de mise en page
    // lorsqu'il rencontre des entités qui s'étendent sur plusieurs pages.
    // 1 - Dans l'ordre visuel :
    // Lors du déplacement dans les enfants d'une entité qui s'étendent sur plusieurs pages,
    // la mise en page est prioritaire, et nous passons aux autres éléments enfants de cette page et évitons ceux de la suivante.
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

    // Notre énumérateur est maintenant à la fin de la collection. Nous pouvons parcourir les entités de mise en page en arrière pour revenir au début.
    Console.WriteLine("Traversing from last to first, elements between pages separated:");
    TraverseLayoutBackward(layoutEnumerator, 1);

    // 2 - Dans l'ordre logique :
    // Lors du déplacement dans les enfants d'une entité qui s'étendent sur plusieurs pages,
    // l'énumérateur se déplacera entre les pages pour parcourir toutes les entités enfants.
    Console.WriteLine("Traversing from first to last, elements between pages mixed:");
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    Console.WriteLine("Traversing from last to first, elements between pages mixed:");
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

/// <summary>
/// Énumérer la collection d'entités de mise en page de layoutEnumerator de l'avant vers l'arrière,
/// de manière approfondie d'abord, et dans l'ordre « Visuel ».
/// </summary>
private static void TraverseLayoutForward(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveFirstChild())
        {
            TraverseLayoutForward(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MoveNext());
}

/// <summary>
/// Énumérer la collection d'entités de mise en page de layoutEnumerator de l'arrière vers l'avant,
/// de manière approfondie d'abord, et dans l'ordre « Visuel ».
/// </summary>
private static void TraverseLayoutBackward(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveLastChild())
        {
            TraverseLayoutBackward(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MovePrevious());
}

/// <summary>
/// Énumérer la collection d'entités de mise en page de layoutEnumerator de l'avant vers l'arrière,
/// de manière approfondie d'abord, et dans l'ordre « logique ».
/// </summary>
private static void TraverseLayoutForwardLogical(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveFirstChild())
        {
            TraverseLayoutForwardLogical(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MoveNextLogical());
}

/// <summary>
/// Énumérer la collection d'entités de mise en page de layoutEnumerator de l'arrière vers l'avant,
/// de manière approfondie d'abord, et dans l'ordre « logique ».
/// </summary>
private static void TraverseLayoutBackwardLogical(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveLastChild())
        {
            TraverseLayoutBackwardLogical(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MovePreviousLogical());
}

/// <summary>
/// Imprimez des informations sur l'entité actuelle de layoutEnumerator sur la console, tout en indentant le texte avec des caractères de tabulation
/// en fonction de sa profondeur par rapport au nœud racine que nous avons fourni dans l'instance du constructeur LayoutEnumerator.
/// Le rectangle que nous traitons à la fin représente la zone et l'emplacement que l'entité occupe dans le document.
/// </summary>
private static void PrintCurrentEntity(LayoutEnumerator layoutEnumerator, int indent)
{
    string tabs = new string('\t', indent);

    Console.WriteLine(layoutEnumerator.Kind == string.Empty
        ? $"{tabs}-> Entity type: {layoutEnumerator.Type}"
        : $"{tabs}-> Entity type & kind: {layoutEnumerator.Type}, {layoutEnumerator.Kind}");

    // Seules les étendues peuvent contenir du texte.
    if (layoutEnumerator.Type == LayoutEntityType.Span)
        Console.WriteLine($"{tabs}   Span contents: \"{layoutEnumerator.Text}\"");

    RectangleF leRect = layoutEnumerator.Rectangle;
    Console.WriteLine($"{tabs}   Rectangle dimensions {leRect.Width}x{leRect.Height}, X={leRect.X} Y={leRect.Y}");
    Console.WriteLine($"{tabs}   Page {layoutEnumerator.PageIndex}");
}
```

### Voir également

* espace de noms [Aspose.Words.Layout](../../aspose.words.layout/)
* Assemblée [Aspose.Words](../../)
