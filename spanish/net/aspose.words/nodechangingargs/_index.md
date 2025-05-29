---
title: NodeChangingArgs Class
linktitle: NodeChangingArgs
articleTitle: NodeChangingArgs
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.NodeChangingArgs, diseñada para optimizar el procesamiento de documentos con una integración fluida con INodeChangingCallback. ¡Optimice su flujo de trabajo hoy mismo!
type: docs
weight: 4880
url: /es/net/aspose.words/nodechangingargs/
---
## NodeChangingArgs class

Proporciona datos para los métodos de la[`INodeChangingCallback`](../inodechangingcallback/) interfaz.

Para obtener más información, visite el[Modelo de objetos de documento (DOM) de Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Artículo de documentación.

```csharp
public class NodeChangingArgs
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Action](../../aspose.words/nodechangingargs/action/) { get; } | Obtiene un valor que indica qué tipo de evento de cambio de nodo está ocurriendo. |
| [NewParent](../../aspose.words/nodechangingargs/newparent/) { get; } | Obtiene el padre del nodo que se establecerá después de que se complete la operación. |
| [Node](../../aspose.words/nodechangingargs/node/) { get; } | Obtiene el[`Node`](./node/) que se está agregando o eliminando. |
| [OldParent](../../aspose.words/nodechangingargs/oldparent/) { get; } | Obtiene el padre del nodo antes de que comenzara la operación. |

## Ejemplos

Muestra cómo personalizar el cambio de nodo con una devolución de llamada.

```csharp
public void FontChangeViaCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Establezca la devolución de llamada de cambio de nodo en una implementación personalizada,
    // luego agrega/elimina nodos para generar un registro.
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
/// Registra la fecha y hora de la inserción y eliminación de cada nodo.
/// Establece un nombre y tamaño de fuente personalizado para el contenido de texto de los nodos Ejecutar.
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

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
