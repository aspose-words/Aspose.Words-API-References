---
title: BookmarkStart
second_title: Référence de l'API Aspose.Words pour .NET
description: Représente le début dun signet dans un document Word.
type: docs
weight: 60
url: /fr/net/aspose.words/bookmarkstart/
---
## BookmarkStart class

Représente le début d'un signet dans un document Word.

```csharp
public class BookmarkStart : Node
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [BookmarkStart](bookmarkstart/)(DocumentBase, string) | Initialise une nouvelle instance du`BookmarkStart` classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [Bookmark](../../aspose.words/bookmarkstart/bookmark/) { get; } | Obtient l'objet façade qui encapsule le début et la fin de ce signet. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel ce nœud appartient. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Renvoie true si ce nœud peut contenir d'autres nœuds. |
| [Name](../../aspose.words/bookmarkstart/name/) { get; set; } | Obtient ou définit le nom du signet. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| override [NodeType](../../aspose.words/bookmarkstart/nodetype/) { get; } | RetoursBookmarkStart . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un **Intervalle** objet qui représente la partie d'un document contenue dans ce nœud. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words/bookmarkstart/accept/)(DocumentVisitor) | Accepte un visiteur. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crée un doublon du nœud. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtient le premier ancêtre du spécifié[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtient le premier ancêtre du type d'objet spécifié. |
| override [GetText](../../aspose.words/bookmarkstart/gettext/)() | Renvoie une chaîne vide. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtient le nœud suivant selon l'algorithme de traversée de l'arbre de pré-ordre. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtient le nœud précédent selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporte le contenu du nœud dans une chaîne à l'aide des options d'enregistrement spécifiées. |

### Remarques

Un signet complet dans un document Word consiste en un`BookmarkStart` et une correspondance[`BookmarkEnd`](../bookmarkend/) avec le même nom de signet.

`BookmarkStart` et[`BookmarkEnd`](../bookmarkend/) ne sont que des marqueurs à l'intérieur d'un document qui spécifient où le signet commence et se termine.

Utilisez le[`Bookmark`](./bookmark/) classe comme une "façade" pour travailler avec un bookmark comme un seul objet.

### Exemples

Montre comment ajouter des signets et mettre à jour leur contenu.

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // Créez un document avec trois signets, puis utilisez une implémentation de visiteur de document personnalisée pour imprimer leur contenu.
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;

    PrintAllBookmarkInfo(bookmarks);

    // Les signets sont accessibles dans la collection de signets par index ou nom, et leurs noms peuvent être mis à jour.
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // Imprimez à nouveau tous les signets pour voir les valeurs mises à jour.
    PrintAllBookmarkInfo(bookmarks);
}

/// <summary>
/// Crée un document avec un nombre donné de signets.
/// </summary>
private static Document CreateDocumentWithBookmarks(int numberOfBookmarks)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    for (int i = 1; i <= numberOfBookmarks; i++)
    {
        string bookmarkName = "MyBookmark_" + i;

        builder.Write("Text before bookmark.");
        builder.StartBookmark(bookmarkName);
        builder.Write($"Text inside {bookmarkName}.");
        builder.EndBookmark(bookmarkName);
        builder.Writeln("Text after bookmark.");
    }

    return doc;
}

/// <summary>
/// Utilisez un itérateur et un visiteur pour imprimer les informations de chaque signet de la collection.
/// </summary>
private static void PrintAllBookmarkInfo(BookmarkCollection bookmarks)
{
    BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

    // Obtient chaque signet de la collection pour accepter un visiteur qui imprimera son contenu.
    using (IEnumerator<Bookmark> enumerator = bookmarks.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Bookmark currentBookmark = enumerator.Current;

            if (currentBookmark != null)
            {
                currentBookmark.BookmarkStart.Accept(bookmarkVisitor);
                currentBookmark.BookmarkEnd.Accept(bookmarkVisitor);

                Console.WriteLine(currentBookmark.BookmarkStart.GetText());
            }
        }
    }
}

/// <summary>
/// Imprime le contenu de chaque signet visité sur la console.
/// </summary>
public class BookmarkInfoPrinter : DocumentVisitor
{
    public override VisitorAction VisitBookmarkStart(BookmarkStart bookmarkStart)
    {
        Console.WriteLine($"BookmarkStart name: \"{bookmarkStart.Name}\", Contents: \"{bookmarkStart.Bookmark.Text}\"");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBookmarkEnd(BookmarkEnd bookmarkEnd)
    {
        Console.WriteLine($"BookmarkEnd name: \"{bookmarkEnd.Name}\"");
        return VisitorAction.Continue;
    }
}
```

### Voir également

* class [Node](../node/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
