---
title: NodeChangingAction Enum
linktitle: NodeChangingAction
articleTitle: NodeChangingAction
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.NodeChangingAction pour gérer efficacement les modifications de nœuds dans vos documents. Améliorez vos capacités de traitement de documents dès aujourd'hui !
type: docs
weight: 4870
url: /fr/net/aspose.words/nodechangingaction/
---
## NodeChangingAction enumeration

Spécifie le type de changement de nœud.

```csharp
public enum NodeChangingAction
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Insert | `0` | Un nœud est en cours d'insertion dans l'arbre. |
| Remove | `1` | Un nœud est en cours de suppression de l'arbre. |

## Exemples

Montre comment utiliser un NodeChangingCallback pour surveiller les modifications apportées à l'arborescence du document en temps réel pendant que nous le modifions.

```csharp
public void NodeChangingCallback()
{
    Document doc = new Document();
    doc.NodeChangingCallback = new NodeChangingPrinter();

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world!");
    builder.StartTable();
    builder.InsertCell();
    builder.Write("Cell 1");
    builder.InsertCell();
    builder.Write("Cell 2");
    builder.EndTable();

    builder.InsertImage(ImageDir + "Logo.jpg");

    builder.CurrentParagraph.ParentNode.RemoveAllChildren();
}

/// <summary>
/// Imprime chaque insertion/suppression de nœud au fur et à mesure qu'elle se produit dans le document.
/// </summary>
private class NodeChangingPrinter : INodeChangingCallback
{
    void INodeChangingCallback.NodeInserting(NodeChangingArgs args)
    {
        Assert.AreEqual(NodeChangingAction.Insert, args.Action);
        Assert.AreEqual(null, args.OldParent);
    }

    void INodeChangingCallback.NodeInserted(NodeChangingArgs args)
    {
        Assert.AreEqual(NodeChangingAction.Insert, args.Action);
        Assert.NotNull(args.NewParent);

        Console.WriteLine("Inserted node:");
        Console.WriteLine($"\tType:\t{args.Node.NodeType}");

        if (args.Node.GetText().Trim() != "")
        {
            Console.WriteLine($"\tText:\t\"{args.Node.GetText().Trim()}\"");
        }

        Console.WriteLine($"\tHash:\t{args.Node.GetHashCode()}");
        Console.WriteLine($"\tParent:\t{args.NewParent.NodeType} ({args.NewParent.GetHashCode()})");
    }

    void INodeChangingCallback.NodeRemoving(NodeChangingArgs args)
    {
        Assert.AreEqual(NodeChangingAction.Remove, args.Action);
    }

    void INodeChangingCallback.NodeRemoved(NodeChangingArgs args)
    {
        Assert.AreEqual(NodeChangingAction.Remove, args.Action);
        Assert.Null(args.NewParent);

        Console.WriteLine($"Removed node: {args.Node.NodeType} ({args.Node.GetHashCode()})");
    }
}
```

### Voir également

* class [NodeChangingArgs](../nodechangingargs/)
* property [Action](../nodechangingargs/action/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
