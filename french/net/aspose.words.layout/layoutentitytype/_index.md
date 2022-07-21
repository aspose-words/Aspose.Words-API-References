---
title: LayoutEntityType
second_title: Référence de l'API Aspose.Words pour .NET
description: Types des entités de mise en page.
type: docs
weight: 3130
url: /fr/net/aspose.words.layout/layoutentitytype/
---
## LayoutEntityType enumeration

Types des entités de mise en page.

```csharp
[Flags]
public enum LayoutEntityType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Valeur par défaut. |
| Page | `1` | Représente la page d'un document. La page peut avoirColumn ,HeaderFooter etComment entités enfants. |
| Column | `2` | Représente une colonne de texte sur une page. La colonne peut avoir les mêmes entités enfants queCell , plusFootnote ,Endnote etNoteSeparator entités. |
| Row | `8` | Représente une ligne de tableau. La ligne peut avoirCell en tant qu'entités enfants. |
| Cell | `10` | Représente une cellule de tableau. La cellule peut avoirLine etRow entités enfants. |
| Line | `20` | Représente la ligne de caractères du texte et des objets en ligne. La ligne peut avoirSpan entités enfants. |
| Span | `40` | Représente un ou plusieurs caractères dans une ligne. Cela inclut les caractères spéciaux tels que les marqueurs de début/fin de champ, les signets et les commentaires. Span ne peut pas avoir d'entités enfants. |
| Footnote | `100` | Représente un espace réservé pour le contenu de la note de bas de page. La note de bas de page peut avoirNote entités enfants. |
| Endnote | `200` | Représente un espace réservé pour le contenu de la note de fin. La note de fin peut avoirNote entités enfants. |
| Note | `4000` | Représente un espace réservé pour le contenu de la note. La note peut avoirLine etRow entités enfants. |
| HeaderFooter | `400` | Représente un espace réservé pour le contenu d'en-tête/pied de page sur une page. HeaderFooter peut avoirLine etRow entités enfants. |
| TextBox | `800` | Représente la zone de texte à l'intérieur d'une forme. La zone de texte peut avoirLine etRow entités enfants. |
| Comment | `1000` | Représente un espace réservé pour le contenu du commentaire. Le commentaire peut avoirLine etRow entités enfants. |
| NoteSeparator | `2000` | Représente le séparateur de note de bas de page/note de fin. NoteSeparator peut avoirLine etRow entités enfants. |

### Exemples

Montre des manières de parcourir les entités de mise en page d'un document.

```csharp
public void LayoutEnumerator()
{
    // Ouvre un document qui contient une variété d'entités de mise en page.
    // Les entités de mise en page sont des pages, des cellules, des lignes, des lignes et d'autres objets inclus dans l'énumération LayoutEntityType.
    // Chaque entité de mise en page a un espace rectangulaire qu'elle occupe dans le corps du document.
    Document doc = new Document(MyDir + "Layout entities.docx");

    // Crée un énumérateur qui peut traverser ces entités comme un arbre.
    LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

    Assert.AreEqual(doc, layoutEnumerator.Document);

    layoutEnumerator.MoveParent(LayoutEntityType.Page);

    Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);
    Assert.Throws<InvalidOperationException>(() => Console.WriteLine(layoutEnumerator.Text));

    // Nous pouvons appeler cette méthode pour nous assurer que l'énumérateur sera à la première entité de mise en page.
    layoutEnumerator.Reset();

    // Il y a deux ordres qui déterminent comment l'énumérateur de mise en page continue à traverser les entités de mise en page
    // lorsqu'il rencontre des entités qui s'étendent sur plusieurs pages.
    // 1 - Dans l'ordre visuel :
    // Lorsque vous parcourez les enfants d'une entité qui s'étendent sur plusieurs pages,
    // la mise en page est prioritaire, et nous passons aux autres éléments enfants de cette page et évitons ceux de la suivante.
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

    // Notre recenseur est maintenant à la fin de la collecte. Nous pouvons parcourir les entités de mise en page en arrière pour revenir au début.
    Console.WriteLine("Traversing from last to first, elements between pages separated:");
    TraverseLayoutBackward(layoutEnumerator, 1);

    // 2 - Dans l'ordre logique :
    // Lorsque vous parcourez les enfants d'une entité qui s'étendent sur plusieurs pages,
    // l'énumérateur se déplacera entre les pages pour parcourir toutes les entités enfants.
    Console.WriteLine("Traversing from first to last, elements between pages mixed:");
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    Console.WriteLine("Traversing from last to first, elements between pages mixed:");
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

/// <summary>
/// Enumérer à travers la collection d'entités de mise en page de layoutEnumerator d'avant en arrière,
/// en profondeur d'abord, et dans l'ordre "Visuel".
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
/// Enumérer à travers la collection d'entités de mise en page de layoutEnumerator à l'envers,
/// en profondeur d'abord, et dans l'ordre "Visuel".
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
/// Enumérer à travers la collection d'entités de mise en page de layoutEnumerator d'avant en arrière,
/// en profondeur d'abord, et dans l'ordre "logique".
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
/// Enumérer à travers la collection d'entités de mise en page de layoutEnumerator à l'envers,
/// en profondeur d'abord, et dans l'ordre "logique".
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
/// Affiche des informations sur l'entité actuelle de layoutEnumerator dans la console, tout en indentant le texte avec des caractères de tabulation
/// en fonction de sa profondeur par rapport au nœud racine que nous avons fourni dans l'instance du constructeur LayoutEnumerator.
/// Le rectangle que nous traitons à la fin représente la zone et l'emplacement que l'entité occupe dans le document.
/// </summary>
private static void PrintCurrentEntity(LayoutEnumerator layoutEnumerator, int indent)
{
    string tabs = new string('\t', indent);

    Console.WriteLine(layoutEnumerator.Kind == string.Empty
        ? $"{tabs}-> Entity type: {layoutEnumerator.Type}"
        : $"{tabs}-> Entity type & kind: {layoutEnumerator.Type}, {layoutEnumerator.Kind}");

    // Seuls les spans peuvent contenir du texte.
    if (layoutEnumerator.Type == LayoutEntityType.Span)
        Console.WriteLine($"{tabs}   Span contents: \"{layoutEnumerator.Text}\"");

    RectangleF leRect = layoutEnumerator.Rectangle;
    Console.WriteLine($"{tabs}   Rectangle dimensions {leRect.Width}x{leRect.Height}, X={leRect.X} Y={leRect.Y}");
    Console.WriteLine($"{tabs}   Page {layoutEnumerator.PageIndex}");
}
```

### Voir également

* espace de noms [Aspose.Words.Layout](../../aspose.words.layout)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
