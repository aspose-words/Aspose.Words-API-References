---
title: GroupShape
linktitle: GroupShape
articleTitle: GroupShape
second_title: Aspose.Words para .NET
description: Diseña fácilmente formas de grupo impactantes con el constructor GroupShape. Mejora tus proyectos con herramientas personalizables e intuitivas para crear creaciones únicas.
type: docs
weight: 10
url: /es/net/aspose.words.drawing/groupshape/groupshape/
---
## GroupShape constructor

Crea una nueva forma de grupo.

```csharp
public GroupShape(DocumentBase doc)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| doc | DocumentBase | El documento del propietario. |

## Observaciones

De forma predeterminada, la forma es flotante y tiene una ubicación y un tamaño predeterminados.

Debes especificar las propiedades de forma deseadas después de crear una forma.

## Ejemplos

Muestra cómo crear un grupo de formas e imprimir su contenido mediante un visitante de documentos.

```csharp
public void GroupOfShapes()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Si necesita crear formas "No primitivas", como SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
    // EsquinasSuperioresUnaRedondeadaUnaRecortada, EsquinaÚnicaRedondeada, EsquinasSuperioresRedondeadas, EsquinasDiagonalesRedondeadas
    // utilice los métodos DocumentBuilder.InsertShape.
    Shape balloon = new Shape(doc, ShapeType.Balloon)
    {
        Width = 200,
        Height = 200,
        Stroke = { Color = Color.Red }
    };

    Shape cube = new Shape(doc, ShapeType.Cube)
    {
        Width = 100,
        Height = 100,
        Stroke = { Color = Color.Blue }
    };

    GroupShape group = new GroupShape(doc);
    group.AppendChild(balloon);
    group.AppendChild(cube);

    Assert.True(group.IsGroup);

    builder.InsertNode(group);

    ShapeGroupPrinter printer = new ShapeGroupPrinter();
    group.Accept(printer);

    Console.WriteLine(printer.GetText());
}

/// <summary>
/// Imprime el contenido de un grupo de formas visitado en la consola.
/// </summary>
public class ShapeGroupPrinter : DocumentVisitor
{
    public ShapeGroupPrinter()
    {
        mBuilder = new StringBuilder();
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        mBuilder.AppendLine("Shape group started:");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitGroupShapeEnd(GroupShape groupShape)
    {
        mBuilder.AppendLine("End of shape group");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitShapeStart(Shape shape)
    {
        mBuilder.AppendLine("\tShape - " + shape.ShapeType + ":");
        mBuilder.AppendLine("\t\tWidth: " + shape.Width);
        mBuilder.AppendLine("\t\tHeight: " + shape.Height);
        mBuilder.AppendLine("\t\tStroke color: " + shape.Stroke.Color);
        mBuilder.AppendLine("\t\tFill color: " + shape.Fill.ForeColor);
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitShapeEnd(Shape shape)
    {
        mBuilder.AppendLine("\tEnd of shape");
        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

### Ver también

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [GroupShape](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
