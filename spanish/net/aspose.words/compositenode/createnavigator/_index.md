---
title: CompositeNode.CreateNavigator
second_title: Referencia de API de Aspose.Words para .NET
description: CompositeNode método. Reservado para uso del sistema. IXPathNavigable.
type: docs
weight: 80
url: /es/net/aspose.words/compositenode/createnavigator/
---
## CompositeNode.CreateNavigator method

Reservado para uso del sistema. IXPathNavigable.

```csharp
[EditorBrowsable(EditorBrowsableState.Never)]
public XPathNavigator CreateNavigator()
```

### Ejemplos

Muestra cómo crear un XPathNavigator y luego usarlo para atravesar y leer nodos.

```csharp
{
    Document doc = new Document();
    XPathNavigator navigator = doc.CreateNavigator();

    if (navigator != null)
    {
        Assert.AreEqual("Document", navigator.Name);
        Assert.AreEqual(false, navigator.MoveToNext());
        Assert.AreEqual(1, navigator.SelectChildren(XPathNodeType.All).Count);

        // El árbol de documentos tiene el documento, primera sección,
        // cuerpo y primer párrafo como nodos, siendo cada uno hijo único del anterior.
        // Podemos agregar algunas más para darle al árbol algunas ramas para que el navegador las atraviese.
        DocumentBuilder docBuilder = new DocumentBuilder(doc);
        docBuilder.Write("Section 1, Paragraph 1. ");
        docBuilder.InsertParagraph();
        docBuilder.Write("Section 1, Paragraph 2. ");
        doc.AppendChild(new Section(doc));
        docBuilder.MoveToSection(1);
        docBuilder.Write("Section 2, Paragraph 1. ");

        // Usa nuestro navegador para imprimir un mapa de todos los nodos en el documento a la consola.
        StringBuilder stringBuilder = new StringBuilder();
        MapDocument(navigator, stringBuilder, 0);
        Console.Write(stringBuilder.ToString());
}

/// <summary>
/// Atraviesa todos los elementos secundarios de un nodo compuesto y mapea la estructura al estilo de un árbol de directorios.
/// La cantidad de sangría espacial indica la profundidad relativa al nodo inicial.
/// Imprime el contenido de texto del nodo actual solo si es Run.
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


