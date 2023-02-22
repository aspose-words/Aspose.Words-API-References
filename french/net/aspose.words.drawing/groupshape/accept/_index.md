---
title: GroupShape.Accept
second_title: Référence de l'API Aspose.Words pour .NET
description: GroupShape méthode. Accepte un visiteur.
type: docs
weight: 30
url: /fr/net/aspose.words.drawing/groupshape/accept/
---
## GroupShape.Accept method

Accepte un visiteur.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| visitor | DocumentVisitor | Le visiteur qui visitera les nœuds. |

### Return_Value

Vrai si tous les nœuds ont été visités ; false si DocumentVisitor a arrêté l'opération avant de visiter tous les nœuds.

### Remarques

Énumère ce nœud et tous ses enfants. Chaque nœud appelle une méthode correspondante sur DocumentVisitor.

Pour plus d'informations, consultez le modèle de conception Visiteur.

Appels[`VisitGroupShapeStart`](../../../aspose.words/documentvisitor/visitgroupshapestart/) , puis appelle[`Accept`](../../../aspose.words/node/accept/) pour toutes les formes enfant de cette forme de groupe et appels[`VisitGroupShapeEnd`](../../../aspose.words/documentvisitor/visitgroupshapeend/) à la fin.

### Exemples

Montre comment créer un groupe de formes et imprimer son contenu à l'aide d'un visiteur de document.

```csharp
public void GroupOfShapes()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Si vous avez besoin de créer des formes "NonPrimitives", telles que SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
    // TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, DiagonalCornersRounded
    // veuillez utiliser les méthodes DocumentBuilder.InsertShape.
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
/// Imprime le contenu d'un groupe de formes visité sur la console.
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

### Voir également

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [GroupShape](../)
* espace de noms [Aspose.Words.Drawing](../../groupshape/)
* Assemblée [Aspose.Words](../../../)


