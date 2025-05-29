---
title: DocumentVisitor.VisitShapeEnd
linktitle: VisitShapeEnd
articleTitle: VisitShapeEnd
second_title: Aspose.Words per .NET
description: Esplora il metodo VisitShapeEnd di DocumentVisitor, essenziale per gestire l'enumerazione delle forme nelle tue applicazioni. Migliora l'efficienza della tua programmazione oggi stesso!
type: docs
weight: 390
url: /it/net/aspose.words/documentvisitor/visitshapeend/
---
## DocumentVisitor.VisitShapeEnd method

Chiamato quando l'enumerazione di una forma è terminata.

```csharp
public virtual VisitorAction VisitShapeEnd(Shape shape)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| shape | Shape | L'oggetto che viene visitato. |

### Valore di ritorno

UN[`VisitorAction`](../../visitoraction/) valore che specifica come continuare l'enumerazione.

## Esempi

Mostra come creare un gruppo di forme e stamparne il contenuto utilizzando un documento visitatore.

```csharp
public void GroupOfShapes()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Se è necessario creare forme "NonPrimitive", come SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
    // AngoliSuperioriUnoArrotondatoUnoTagliato, AngoloSingoloArrotondato, AngoliSuperioriArrotondati, AngoliDiagonaliArrotondati
    // si prega di utilizzare i metodi DocumentBuilder.InsertShape.
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
/// Stampa sulla console il contenuto di un gruppo di forme visitato.
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

### Guarda anche

* enum [VisitorAction](../../visitoraction/)
* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentVisitor](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
