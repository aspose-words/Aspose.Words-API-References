---
title: NodeChangingAction Enum
linktitle: NodeChangingAction
articleTitle: NodeChangingAction
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.NodeChangingAction, um Knotenänderungen in Ihren Dokumenten effizient zu verwalten. Verbessern Sie noch heute Ihre Dokumentverarbeitung!
type: docs
weight: 4870
url: /de/net/aspose.words/nodechangingaction/
---
## NodeChangingAction enumeration

Gibt den Typ der Knotenänderung an.

```csharp
public enum NodeChangingAction
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Insert | `0` | Ein Knoten wird in den Baum eingefügt. |
| Remove | `1` | Ein Knoten wird aus dem Baum entfernt. |

## Beispiele

Zeigt, wie ein NodeChangingCallback verwendet wird, um Änderungen am Dokumentbaum während der Bearbeitung in Echtzeit zu überwachen.

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
/// Druckt jedes Einfügen/Entfernen von Knoten, während es im Dokument stattfindet.
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

### Siehe auch

* class [NodeChangingArgs](../nodechangingargs/)
* property [Action](../nodechangingargs/action/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
