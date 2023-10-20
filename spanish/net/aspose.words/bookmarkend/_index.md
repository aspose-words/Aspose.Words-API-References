---
title: BookmarkEnd Class
linktitle: BookmarkEnd
articleTitle: BookmarkEnd
second_title: Aspose.Words para .NET
description: Aspose.Words.BookmarkEnd clase. Representa el final de un marcador en un documento de Word en C#.
type: docs
weight: 60
url: /es/net/aspose.words/bookmarkend/
---
## BookmarkEnd class

Representa el final de un marcador en un documento de Word.

Para obtener más información, visite el[Trabajar con marcadores](https://docs.aspose.com/words/net/working-with-bookmarks/) artículo de documentación.

```csharp
public class BookmarkEnd : Node
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [BookmarkEnd](bookmarkend/)(*[DocumentBase](../documentbase/), string*) | Inicializa una nueva instancia del`BookmarkEnd` clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica el identificador de nodo personalizado. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Devoluciones`verdadero` si este nodo puede contener otros nodos. |
| [Name](../../aspose.words/bookmarkend/name/) { get; set; } | Obtiene o establece el nombre del marcador. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| override [NodeType](../../aspose.words/bookmarkend/nodetype/) { get; } | DevolucionesBookmarkEnd . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un[`Range`](../range/) objeto que representa la parte de un documento contenido en este nodo. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words/bookmarkend/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Acepta un visitante. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicado del nodo. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Obtiene el primer ancestro del especificado[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtiene el primer antepasado del tipo de objeto especificado. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Obtiene el siguiente nodo según el algoritmo transversal del árbol de pedidos anticipados. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Obtiene el nodo anterior según el algoritmo transversal del árbol de pedidos anticipados. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina del padre. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |

## Observaciones

Un marcador completo en un documento de Word consta de un[`BookmarkStart`](../bookmarkstart/) y una coincidencia`BookmarkEnd` con el mismo nombre de marcador.

[`BookmarkStart`](../bookmarkstart/) y`BookmarkEnd` son solo marcadores dentro de un document que especifican dónde comienza y termina el marcador.

Utilizar el[`Bookmark`](../bookmark/) clase como "fachada" para trabajar con un bookmark como un solo objeto.

## Ejemplos

Muestra cómo agregar marcadores y actualizar su contenido.

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // Cree un documento con tres marcadores y luego utilice una implementación personalizada de visitante de documentos para imprimir su contenido.
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;
    PrintAllBookmarkInfo(bookmarks);

    // Se puede acceder a los marcadores en la colección de marcadores por índice o nombre, y sus nombres se pueden actualizar.
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // Imprime todos los marcadores nuevamente para ver los valores actualizados.
    PrintAllBookmarkInfo(bookmarks);
}

/// <summary>
/// Crea un documento con un número determinado de marcadores.
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
/// Utilice un iterador y un visitante para imprimir información de cada marcador de la colección.
/// </summary>
private static void PrintAllBookmarkInfo(BookmarkCollection bookmarks)
{
    BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

    // Obtenga cada marcador de la colección para aceptar un visitante que imprimirá su contenido.
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
/// Imprime el contenido de cada marcador visitado en la consola.
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

### Ver también

* class [Node](../node/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
