---
title: INodeChangingCallback.NodeRemoved
linktitle: NodeRemoved
articleTitle: NodeRemoved
second_title: Aspose.Words para .NET
description: INodeChangingCallback NodeRemoved método. Se llama cuando un nodo que pertenece a este documento se ha eliminado de su padre en C#.
type: docs
weight: 30
url: /es/net/aspose.words/inodechangingcallback/noderemoved/
---
## INodeChangingCallback.NodeRemoved method

Se llama cuando un nodo que pertenece a este documento se ha eliminado de su padre.

```csharp
public void NodeRemoved(NodeChangingArgs args)
```

## Ejemplos

Muestra cómo personalizar el cambio de nodo con una devolución de llamada.

```csharp
public void FontChangeViaCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Establece la devolución de llamada de cambio de nodo para una implementación personalizada,
    // luego agrega/elimina nodos para que genere un registro.
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
/// Registra la fecha y hora de cada inserción y eliminación de nodos.
/// Establece un nombre/tamaño de fuente personalizado para el contenido del texto de los nodos Ejecutar.
/// </summary>
public class HandleNodeChangingFontChanger : INodeChangingCallback
{
    void INodeChangingCallback.NodeInserted(NodeChangingArgs args)
    {
        mLog.AppendLine($"\tType:\t{args.Node.NodeType}");
        mLog.AppendLine($"\tHash:\t{args.Node.GetHashCode()}");

        if (args.Node.NodeType == NodeType.Run)
        {
            Aspose.Words.Font font = ((Run) args.Node).Font;
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

### Ver también

* class [NodeChangingArgs](../../nodechangingargs/)
* interface [INodeChangingCallback](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
