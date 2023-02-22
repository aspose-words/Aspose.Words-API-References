---
title: LayoutEnumerator.MoveNextLogical
second_title: Referencia de API de Aspose.Words para .NET
description: LayoutEnumerator método. Se mueve a la siguiente entidad hermana en un orden lógico. Al iterar líneas de un párrafo dividido en páginas este método se moverá a la siguiente línea incluso si reside en otra página.
type: docs
weight: 120
url: /es/net/aspose.words.layout/layoutenumerator/movenextlogical/
---
## LayoutEnumerator.MoveNextLogical method

Se mueve a la siguiente entidad hermana en un orden lógico. Al iterar líneas de un párrafo dividido en páginas, este método se moverá a la siguiente línea incluso si reside en otra página.

```csharp
public bool MoveNextLogical()
```

### Observaciones

Tenga en cuenta que todosSpan las entidades están vinculadas entre sí, por lo que si[`Current`](../current/) la entidad es un intervalo de llamadas repetidas de este método iterará la historia completa del documento.

### Ejemplos

Muestra formas de atravesar las entidades de diseño de un documento.

```csharp
public void LayoutEnumerator()
{
    // Abra un documento que contenga una variedad de entidades de diseño.
    // Las entidades de diseño son páginas, celdas, filas, líneas y otros objetos incluidos en la enumeración LayoutEntityType.
    // Cada entidad de diseño tiene un espacio rectangular que ocupa en el cuerpo del documento.
    Document doc = new Document(MyDir + "Layout entities.docx");

    // Cree un enumerador que pueda atravesar estas entidades como un árbol.
    LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

    Assert.AreEqual(doc, layoutEnumerator.Document);

    layoutEnumerator.MoveParent(LayoutEntityType.Page);

    Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);
    Assert.Throws<InvalidOperationException>(() => Console.WriteLine(layoutEnumerator.Text));

    // Podemos llamar a este método para asegurarnos de que el enumerador estará en la primera entidad de diseño.
    layoutEnumerator.Reset();

    // Hay dos órdenes que determinan cómo el enumerador de diseño continúa atravesando las entidades de diseño
    // cuando encuentra entidades que abarcan varias páginas.
    // 1 - En orden visual:
    // Al moverse a través de los elementos secundarios de una entidad que abarcan varias páginas,
    // el diseño de la página tiene prioridad, y pasamos a otros elementos secundarios en esta página y evitamos los de la siguiente.
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

    // Nuestro enumerador ahora está al final de la colección. Podemos recorrer las entidades de diseño hacia atrás para volver al principio.
    Console.WriteLine("Traversing from last to first, elements between pages separated:");
    TraverseLayoutBackward(layoutEnumerator, 1);

    // 2 - En orden lógico:
    // Al moverse a través de los elementos secundarios de una entidad que abarcan varias páginas,
    // el enumerador se moverá entre las páginas para recorrer todas las entidades secundarias.
    Console.WriteLine("Traversing from first to last, elements between pages mixed:");
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    Console.WriteLine("Traversing from last to first, elements between pages mixed:");
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

/// <summary>
/// Enumerar a través de la colección de entidades de diseño de layoutEnumerator de adelante hacia atrás,
/// primero en profundidad y en el orden "Visual".
/// </summary>
private static void TraverseLayoutForward(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveFirstChild())
        {
            TraverseLayoutForward(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MoveNext());
}

/// <summary>
/// Enumerar a través de la colección de entidades de diseño de layoutEnumerator de atrás hacia adelante,
/// primero en profundidad y en el orden "Visual".
/// </summary>
private static void TraverseLayoutBackward(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveLastChild())
        {
            TraverseLayoutBackward(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MovePrevious());
}

/// <summary>
/// Enumerar a través de la colección de entidades de diseño de layoutEnumerator de adelante hacia atrás,
/// primero en profundidad y en el orden "Lógico".
/// </summary>
private static void TraverseLayoutForwardLogical(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveFirstChild())
        {
            TraverseLayoutForwardLogical(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MoveNextLogical());
}

/// <summary>
/// Enumerar a través de la colección de entidades de diseño de layoutEnumerator de atrás hacia adelante,
/// primero en profundidad y en el orden "Lógico".
/// </summary>
private static void TraverseLayoutBackwardLogical(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveLastChild())
        {
            TraverseLayoutBackwardLogical(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MovePreviousLogical());
}

/// <summary>
/// Imprimir información sobre la entidad actual de layoutEnumerator en la consola, mientras se sangra el texto con caracteres de tabulación
/// según su profundidad relativa al nodo raíz que proporcionamos en la instancia del constructor LayoutEnumerator.
/// El rectángulo que procesamos al final representa el área y la ubicación que ocupa la entidad en el documento.
/// </summary>
private static void PrintCurrentEntity(LayoutEnumerator layoutEnumerator, int indent)
{
    string tabs = new string('\t', indent);

    Console.WriteLine(layoutEnumerator.Kind == string.Empty
        ? $"{tabs}-> Entity type: {layoutEnumerator.Type}"
        : $"{tabs}-> Entity type & kind: {layoutEnumerator.Type}, {layoutEnumerator.Kind}");

    // Solo los intervalos pueden contener texto.
    if (layoutEnumerator.Type == LayoutEntityType.Span)
        Console.WriteLine($"{tabs}   Span contents: \"{layoutEnumerator.Text}\"");

    RectangleF leRect = layoutEnumerator.Rectangle;
    Console.WriteLine($"{tabs}   Rectangle dimensions {leRect.Width}x{leRect.Height}, X={leRect.X} Y={leRect.Y}");
    Console.WriteLine($"{tabs}   Page {layoutEnumerator.PageIndex}");
}
```

### Ver también

* class [LayoutEnumerator](../)
* espacio de nombres [Aspose.Words.Layout](../../layoutenumerator/)
* asamblea [Aspose.Words](../../../)


