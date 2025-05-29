---
title: GroupShape.AcceptEnd
linktitle: AcceptEnd
articleTitle: AcceptEnd
second_title: Aspose.Words per .NET
description: Scopri il metodo AcceptEnd di GroupShape, gestisci senza problemi le interazioni dei visitatori e migliora l'esperienza utente della tua applicazione con questa potente funzionalità.
type: docs
weight: 40
url: /it/net/aspose.words.drawing/groupshape/acceptend/
---
## GroupShape.AcceptEnd method

Accetta un visitatore per aver visitato la fine del GroupShape.

```csharp
public override VisitorAction AcceptEnd(DocumentVisitor visitor)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| visitor | DocumentVisitor | Il visitatore del documento. |

### Valore di ritorno

L'azione che il visitatore deve intraprendere.

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

* enum [VisitorAction](../../../aspose.words/visitoraction/)
* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [GroupShape](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
