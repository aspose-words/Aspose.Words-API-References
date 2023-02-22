---
title: Enum NodeChangingAction
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.NodeChangingAction énumération. Spécifie le type de changement de nœud.
type: docs
weight: 3940
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
| Insert | `0` | Un nœud est en cours d'insertion dans l'arborescence. |
| Remove | `1` | Un nœud est en cours de suppression de l'arborescence. |

### Exemples

Montre comment utiliser un NodeChangingCallback pour surveiller les modifications apportées à l'arborescence du document en temps réel au fur et à mesure que nous le modifions.

```csharp
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

    #if NET48 || JAVA
    builder.InsertImage(Image.FromFile(ImageDir + "Logo.jpg"));
    #elif NET5_0_OR_GREATER || __MOBILE__
    using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
        builder.InsertImage(image);
    #endif

    builder.CurrentParagraph.ParentNode.RemoveAllChildren();
}

/// <summary>
/// Imprime chaque insertion/suppression de nœud telle qu'elle a lieu dans le document.
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


