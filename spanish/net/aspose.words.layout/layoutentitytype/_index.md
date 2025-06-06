---
title: LayoutEntityType Enum
linktitle: LayoutEntityType
articleTitle: LayoutEntityType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Layout.LayoutEntityType, que incluye diversos tipos de entidades de diseño para un formato de documento mejorado y una integración perfecta.
type: docs
weight: 3780
url: /es/net/aspose.words.layout/layoutentitytype/
---
## LayoutEntityType enumeration

Tipos de entidades de diseño.

```csharp
[Flags]
public enum LayoutEntityType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | Valor predeterminado. |
| Page | `1` | Representa la página de un documento. La página puede tenerColumn ,HeaderFooter yComment entidades secundarias. |
| Column | `2` | Representa una columna de texto en una página. La columna puede tener las mismas entidades secundarias queCell , másFootnote ,Endnote yNoteSeparator entidades. |
| Row | `8` | Representa una fila de la tabla. La fila puede tenerCell como entidades secundarias. |
| Cell | `10` | Representa una celda de tabla. La celda puede tenerLine yRow entidades secundarias. |
| Line | `20` | Representa una línea de caracteres de texto y objetos en línea. La línea puede tenerSpan entidades secundarias. |
| Span | `40` | Representa uno o más caracteres en una línea. Esto incluye caracteres especiales como marcadores de inicio/fin de campo, marcadores y comentarios. El intervalo no puede tener entidades secundarias. |
| Footnote | `100` | Representa un marcador de posición para el contenido de la nota al pie. La nota al pie puede tenerNote entidades secundarias. |
| Endnote | `200` | Representa un marcador de posición para el contenido de la nota final. La nota final puede tenerNote entidades secundarias. |
| Note | `4000` | Representa un marcador de posición para el contenido de la nota. La nota puede tenerLine yRow entidades secundarias. |
| HeaderFooter | `400` | Representa un marcador de posición para el contenido del encabezado/pie de página en una página. HeaderFooter puede tenerLine yRow entidades secundarias. |
| TextBox | `800` | Representa el área de texto dentro de una forma. El cuadro de texto puede tenerLine yRow entidades secundarias. |
| Comment | `1000` | Representa un marcador de posición para el contenido del comentario. El comentario puede tenerLine yRow entidades secundarias. |
| NoteSeparator | `2000` | Representa el separador de notas al pie/notas finales. El separador de notas puede tenerLine yRow entidades secundarias. |

## Ejemplos

Muestra formas de recorrer las entidades de diseño de un documento.

```csharp
public void LayoutEnumerator()
{
    //Abre un documento que contiene una variedad de entidades de diseño.
    // Las entidades de diseño son páginas, celdas, filas, líneas y otros objetos incluidos en la enumeración LayoutEntityType.
    // Cada entidad de diseño tiene un espacio rectangular que ocupa en el cuerpo del documento.
    Document doc = new Document(MyDir + "Layout entities.docx");

    // Cree un enumerador que pueda recorrer estas entidades como un árbol.
    LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

    Assert.AreEqual(doc, layoutEnumerator.Document);

    layoutEnumerator.MoveParent(LayoutEntityType.Page);

    Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);
    Assert.Throws<InvalidOperationException>(() => Console.WriteLine(layoutEnumerator.Text));

    //Podemos llamar a este método para asegurarnos de que el enumerador estará en la primera entidad de diseño.
    layoutEnumerator.Reset();

    // Hay dos órdenes que determinan cómo el enumerador de diseño continúa recorriendo las entidades de diseño
    // cuando encuentra entidades que abarcan varias páginas.
    // 1 - En orden visual:
    // Al moverse a través de los hijos de una entidad que abarcan varias páginas,
    // el diseño de la página tiene prioridad y pasamos a otros elementos secundarios en esta página y evitamos los de la siguiente.
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

    Nuestro enumerador está ahora al final de la colección. Podemos recorrer las entidades de diseño hacia atrás para volver al principio.
    Console.WriteLine("Traversing from last to first, elements between pages separated:");
    TraverseLayoutBackward(layoutEnumerator, 1);

    // 2 - En orden lógico:
    // Al moverse a través de los hijos de una entidad que abarcan varias páginas,
    // el enumerador se moverá entre páginas para recorrer todas las entidades secundarias.
    Console.WriteLine("Traversing from first to last, elements between pages mixed:");
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    Console.WriteLine("Traversing from last to first, elements between pages mixed:");
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

/// <summary>
/// Enumerar a través de la colección de entidades de diseño de layoutEnumerator de adelante hacia atrás,
/// de manera profunda y en el orden "Visual".
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
/// de manera profunda y en el orden "Visual".
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
/// de manera profunda y en el orden "lógico".
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
/// de manera profunda y en el orden "lógico".
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
/// Imprime información sobre la entidad actual de layoutEnumerator en la consola, mientras sangras el texto con caracteres de tabulación
/// basado en su profundidad relativa al nodo raíz que proporcionamos en la instancia del constructor LayoutEnumerator.
/// El rectángulo que procesamos al final representa el área y ubicación que ocupa la entidad en el documento.
/// </summary>
private static void PrintCurrentEntity(LayoutEnumerator layoutEnumerator, int indent)
{
    string tabs = new string('\t', indent);

    Console.WriteLine(layoutEnumerator.Kind == string.Empty
        ? $"{tabs}-> Entity type: {layoutEnumerator.Type}"
        : $"{tabs}-> Entity type & kind: {layoutEnumerator.Type}, {layoutEnumerator.Kind}");

    //Solo los espacios pueden contener texto.
    if (layoutEnumerator.Type == LayoutEntityType.Span)
        Console.WriteLine($"{tabs}   Span contents: \"{layoutEnumerator.Text}\"");

    RectangleF leRect = layoutEnumerator.Rectangle;
    Console.WriteLine($"{tabs}   Rectangle dimensions {leRect.Width}x{leRect.Height}, X={leRect.X} Y={leRect.Y}");
    Console.WriteLine($"{tabs}   Page {layoutEnumerator.PageIndex}");
}
```

### Ver también

* espacio de nombres [Aspose.Words.Layout](../../aspose.words.layout/)
* asamblea [Aspose.Words](../../)
