---
title: Enum NodeChangingAction
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.NodeChangingAction opsomming. Gibt die Art der Knotenänderung an.
type: docs
weight: 4180
url: /de/net/aspose.words/nodechangingaction/
---
## NodeChangingAction enumeration

Gibt die Art der Knotenänderung an.

```csharp
public enum NodeChangingAction
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Insert | `0` | Ein Knoten wird in den Baum eingefügt. |
| Remove | `1` | Ein Knoten wird aus dem Baum entfernt. |

### Beispiele

Zeigt, wie ein NodeChangingCallback verwendet wird, um Änderungen am Dokumentbaum in Echtzeit zu überwachen, während wir ihn bearbeiten.

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

    #if NET48 || JAVA
    builder.InsertImage(Image.FromFile(ImageDir + "Logo.jpg"));
    #elif NET5_0_OR_GREATER || __MOBILE__
    using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
        builder.InsertImage(image);
    #endif

    builder.CurrentParagraph.ParentNode.RemoveAllChildren();
}

/// <summary>
/// Druckt jedes Einfügen/Entfernen eines Knotens, während es im Dokument stattfindet.
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


