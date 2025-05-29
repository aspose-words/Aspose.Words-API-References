---
title: INodeChangingCallback Interface
linktitle: INodeChangingCallback
articleTitle: INodeChangingCallback
second_title: Aspose.Words para .NET
description: Implemente la interfaz Aspose.Words.INodeChangingCallback para recibir notificaciones en tiempo real sobre los cambios en los nodos del documento, mejorando su experiencia de gestión de documentos.
type: docs
weight: 3640
url: /es/net/aspose.words/inodechangingcallback/
---
## INodeChangingCallback interface

Implemente esta interfaz si desea recibir notificaciones cuando se inserten o eliminen nodos en el documento.

```csharp
public interface INodeChangingCallback
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| [NodeInserted](../../aspose.words/inodechangingcallback/nodeinserted/)(*[NodeChangingArgs](../nodechangingargs/)*) | Se llama cuando un nodo que pertenece a este documento se ha insertado en otro nodo. |
| [NodeInserting](../../aspose.words/inodechangingcallback/nodeinserting/)(*[NodeChangingArgs](../nodechangingargs/)*) | Se llama justo antes de que un nodo que pertenece a este documento esté a punto de insertarse en otro nodo. |
| [NodeRemoved](../../aspose.words/inodechangingcallback/noderemoved/)(*[NodeChangingArgs](../nodechangingargs/)*) | Se llama cuando un nodo que pertenece a este documento ha sido eliminado de su padre. |
| [NodeRemoving](../../aspose.words/inodechangingcallback/noderemoving/)(*[NodeChangingArgs](../nodechangingargs/)*) | Se llama justo antes de que un nodo que pertenece a este documento esté a punto de ser eliminado del documento. |

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
