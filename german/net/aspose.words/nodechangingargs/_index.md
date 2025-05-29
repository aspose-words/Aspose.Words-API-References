---
title: NodeChangingArgs Class
linktitle: NodeChangingArgs
articleTitle: NodeChangingArgs
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.NodeChangingArgs, die Ihre Dokumentenverarbeitung durch die nahtlose Integration von INodeChangingCallback verbessert. Optimieren Sie Ihren Workflow noch heute!
type: docs
weight: 4880
url: /de/net/aspose.words/nodechangingargs/
---
## NodeChangingArgs class

Stellt Daten für Methoden der[`INodeChangingCallback`](../inodechangingcallback/) Schnittstelle.

Um mehr zu erfahren, besuchen Sie die[Aspose.Words Dokumentobjektmodell (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Dokumentationsartikel.

```csharp
public class NodeChangingArgs
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Action](../../aspose.words/nodechangingargs/action/) { get; } | Ruft einen Wert ab, der angibt, welche Art von Knotenänderungsereignis auftritt. |
| [NewParent](../../aspose.words/nodechangingargs/newparent/) { get; } | Ruft das übergeordnete Element des Knotens ab, das nach Abschluss des Vorgangs festgelegt wird. |
| [Node](../../aspose.words/nodechangingargs/node/) { get; } | Ruft die[`Node`](./node/) das hinzugefügt oder entfernt wird. |
| [OldParent](../../aspose.words/nodechangingargs/oldparent/) { get; } | Ruft den übergeordneten Knoten vor Beginn der Operation ab. |

## Beispiele

Zeigt, wie Sie Knotenänderungen mit einem Rückruf anpassen.

```csharp
public void FontChangeViaCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Den Rückruf zum Ändern des Knotens auf eine benutzerdefinierte Implementierung setzen,
    // dann Knoten hinzufügen/entfernen, um ein Protokoll zu generieren.
    HandleNodeChangingFontChanger callback = new HandleNodeChangingFontChanger();
    doc.NodeChangingCallback = callback;

    builder.Writeln("Hello world!");
    builder.Writeln("Hello again!");
    builder.InsertField(" HYPERLINK \"https://www.google.com/\" ");
    builder.InsertShape(ShapeType.Rectangle, 300, 300);

    doc.Range.Fields[0].Remove();

    Console.WriteLine(callback.GetLog());
}

/// <summary>
/// Protokolliert Datum und Uhrzeit jedes Einfügens und Entfernens eines Knotens.
/// Legt einen benutzerdefinierten Schriftnamen/eine benutzerdefinierte Schriftgröße für den Textinhalt von Run-Knoten fest.
/// </summary>
public class HandleNodeChangingFontChanger : INodeChangingCallback
{
    void INodeChangingCallback.NodeInserted(NodeChangingArgs args)
    {
        mLog.AppendLine($"\tType:\t{args.Node.NodeType}");
        mLog.AppendLine($"\tHash:\t{args.Node.GetHashCode()}");

        if (args.Node.NodeType == NodeType.Run)
        {
            Aspose.Words.Font font = ((Run)args.Node).Font;
            mLog.Append($"\tFont:\tChanged from \"{font.Name}\" {font.Size}pt");

            font.Size = 24;
            font.Name = "Arial";

            mLog.AppendLine($" to \"{font.Name}\" {font.Size}pt");
            mLog.AppendLine($"\tContents:\n\t\t\"{args.Node.GetText()}\"");
        }
    }

    void INodeChangingCallback.NodeInserting(NodeChangingArgs args)
    {
        mLog.AppendLine($"\n{DateTime.Now:dd/MM/yyyy HH:mm:ss:fff}\tNode insertion:");
    }

    void INodeChangingCallback.NodeRemoved(NodeChangingArgs args)
    {
        mLog.AppendLine($"\tType:\t{args.Node.NodeType}");
        mLog.AppendLine($"\tHash code:\t{args.Node.GetHashCode()}");
    }

    void INodeChangingCallback.NodeRemoving(NodeChangingArgs args)
    {
        mLog.AppendLine($"\n{DateTime.Now:dd/MM/yyyy HH:mm:ss:fff}\tNode removal:");
    }

    public string GetLog()
    {
        return mLog.ToString();
    }

    private readonly StringBuilder mLog = new StringBuilder();
}
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
