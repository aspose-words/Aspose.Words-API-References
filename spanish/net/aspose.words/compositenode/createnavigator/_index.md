---
title: CompositeNode.CreateNavigator
second_title: Referencia de API de Aspose.Words para .NET
description: CompositeNode método. Crea un navegador que se puede utilizar para atravesar y leer nodos.
type: docs
weight: 90
url: /es/net/aspose.words/compositenode/createnavigator/
---
## CompositeNode.CreateNavigator method

Crea un navegador que se puede utilizar para atravesar y leer nodos.

```csharp
[EditorBrowsable(EditorBrowsableState.Never)]
public XPathNavigator CreateNavigator()
```

### Ejemplos

Muestra cómo crear un XPathNavigator y luego usarlo para recorrer y leer nodos.

```csharp
public void NodeXPathNavigator()
{
    Document doc = new Document();
    XPathNavigator navigator = doc.CreateNavigator();

    if (navigator != null)
    {
        Assert.AreEqual("Document", navigator.Name);
        Assert.AreEqual(false, navigator.MoveToNext());
        Assert.AreEqual(1, navigator.SelectChildren(XPathNodeType.All).Count);

        // El árbol del documento tiene el documento, primera sección,
        // cuerpo y primer párrafo como nodos, siendo cada uno hijo único del anterior.
        // Podemos agregar algunas más para darle al árbol algunas ramas para que las recorra el navegador.
        DocumentBuilder docBuilder = new DocumentBuilder(doc);
        docBuilder.Write("Section 1, Paragraph 1. ");
        docBuilder.InsertParagraph();
        docBuilder.Write("Section 1, Paragraph 2. ");
        doc.AppendChild(new Section(doc));
        docBuilder.MoveToSection(1);
        docBuilder.Write("Section 2, Paragraph 1. ");

        // Utilice nuestro navegador para imprimir un mapa de todos los nodos del documento en la consola.
        StringBuilder stringBuilder = new StringBuilder();
        MapDocument(navigator, stringBuilder, 0);
        Console.Write(stringBuilder.ToString());
    }
}

/// <summary>
/// Atraviesa todos los hijos de un nodo compuesto y asigna la estructura al estilo de un árbol de directorios.
/// La cantidad de sangría espacial indica la profundidad relativa al nodo inicial.
/// Imprime el contenido del texto del nodo actual solo si es una Ejecución.
/// </summary>
private static void MapDocument(XPathNavigator navigator, StringBuilder stringBuilder, int depth)
{
    do
    {
        stringBuilder.Append(' ', depth);
        stringBuilder.Append(navigator.Name + ": ");

        if (navigator.Name == "Run")
        {
            stringBuilder.Append(navigator.Value);
        }

        stringBuilder.Append('\n');

        if (navigator.HasChildren)
        {
            navigator.MoveToFirstChild();
            MapDocument(navigator, stringBuilder, depth + 1);
            navigator.MoveToParent();
        }
    } while (navigator.MoveToNext());
}
```

### Ver también

* class [CompositeNode](../)
* espacio de nombres [Aspose.Words](../../compositenode/)
* asamblea [Aspose.Words](../../../)


