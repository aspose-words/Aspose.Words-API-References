---
title: INodeChangingCallback Interface
linktitle: INodeChangingCallback
articleTitle: INodeChangingCallback
second_title: Aspose.Words pour .NET
description: Implémentez l'interface Aspose.Words.INodeChangingCallback pour obtenir des notifications en temps réel sur les modifications des nœuds de document, améliorant ainsi votre expérience de gestion de documents.
type: docs
weight: 3640
url: /fr/net/aspose.words/inodechangingcallback/
---
## INodeChangingCallback interface

Implémentez cette interface si vous souhaitez recevoir des notifications lorsque des nœuds sont insérés ou supprimés dans le document.

```csharp
public interface INodeChangingCallback
```

## Méthodes

| Nom | La description |
| --- | --- |
| [NodeInserted](../../aspose.words/inodechangingcallback/nodeinserted/)(*[NodeChangingArgs](../nodechangingargs/)*) | Appelé lorsqu'un nœud appartenant à ce document a été inséré dans un autre nœud. |
| [NodeInserting](../../aspose.words/inodechangingcallback/nodeinserting/)(*[NodeChangingArgs](../nodechangingargs/)*) | Appelé juste avant qu'un nœud appartenant à ce document soit sur le point d'être inséré dans un autre nœud. |
| [NodeRemoved](../../aspose.words/inodechangingcallback/noderemoved/)(*[NodeChangingArgs](../nodechangingargs/)*) | Appelé lorsqu'un nœud appartenant à ce document a été supprimé de son parent. |
| [NodeRemoving](../../aspose.words/inodechangingcallback/noderemoving/)(*[NodeChangingArgs](../nodechangingargs/)*) | Appelé juste avant qu'un nœud appartenant à ce document soit sur le point d'être supprimé du document. |

## Exemples

Montre comment personnaliser le changement de nœud avec un rappel.

```csharp
public void FontChangeViaCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Définir le rappel de changement de nœud sur une implémentation personnalisée,
    // puis ajoutez/supprimez des nœuds pour générer un journal.
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
/// Enregistre la date et l'heure de chaque insertion et suppression de nœud.
/// Définit un nom/une taille de police personnalisée pour le contenu texte des nœuds Run.
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

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
