---
title: FieldArgumentBuilder.AddNode
linktitle: AddNode
articleTitle: AddNode
second_title: Aspose.Words pour .NET
description: Améliorez votre code avec la méthode AddNode de FieldArgumentBuilder. Ajoutez facilement des nœuds aux arguments pour des fonctionnalités et des performances améliorées.
type: docs
weight: 30
url: /fr/net/aspose.words.fields/fieldargumentbuilder/addnode/
---
## FieldArgumentBuilder.AddNode method

Ajoute un nœud à l'argument.

```csharp
public FieldArgumentBuilder AddNode(Inline node)
```

## Remarques

Seuls les nœuds de niveau texte sont pris en charge pour le moment.

## Exemples

Montre comment construire des champs à l'aide d'un générateur de champs, puis les insérer dans le document.

```csharp
Document doc = new Document();

// Vous trouverez ci-dessous trois exemples de construction de champs réalisée à l'aide d'un générateur de champs.
// 1 - Champ unique :
// Utilisez un générateur de champs pour ajouter un champ SYMBOL qui affiche le symbole ƒ (Florin).
FieldBuilder builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(402);
builder.AddSwitch("\\f", "Arial");
builder.AddSwitch("\\s", 25);
builder.AddSwitch("\\u");
Field field = builder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph);

Assert.AreEqual(" SYMBOL 402 \\f Arial \\s 25 \\u ", field.GetFieldCode());

// 2 - Champ imbriqué :
// Utilisez un générateur de champs pour créer un champ de formule utilisé comme champ interne par un autre générateur de champs.
FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FieldFormula);
innerFormulaBuilder.AddArgument(100);
innerFormulaBuilder.AddArgument("+");
innerFormulaBuilder.AddArgument(74);

// Créez un autre générateur pour un autre champ SYMBOLE et insérez le champ de formule
 // que nous avons créé ci-dessus dans le champ SYMBOL comme argument.
builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(innerFormulaBuilder);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

// Le champ SYMBOLE externe utilisera le résultat du champ de formule, 174, comme argument,
// qui fera que le champ affichera le symbole ® (signe enregistré) puisque son numéro de caractère est 174.
Assert.AreEqual(" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field.GetFieldCode());

// 3 - Plusieurs champs et arguments imbriqués :
// Maintenant, nous allons utiliser un générateur pour créer un champ IF, qui affiche l'une des deux valeurs de chaîne personnalisées,
// selon la valeur vrai/faux de son expression. Pour obtenir une valeur vrai/faux
// qui détermine quelle chaîne le champ IF affiche, le champ IF testera deux expressions numériques pour l'égalité.
// Nous fournirons les deux expressions sous forme de champs de formule, que nous imbriquerons à l'intérieur du champ IF.
FieldBuilder leftExpression = new FieldBuilder(FieldType.FieldFormula);
leftExpression.AddArgument(2);
leftExpression.AddArgument("+");
leftExpression.AddArgument(3);

FieldBuilder rightExpression = new FieldBuilder(FieldType.FieldFormula);
rightExpression.AddArgument(2.5);
rightExpression.AddArgument("*");
rightExpression.AddArgument(5.2);

// Ensuite, nous allons créer deux arguments de champ, qui serviront de chaînes de sortie vrai/faux pour le champ IF.
// Ces arguments réutiliseront les valeurs de sortie de nos expressions numériques.
FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
trueOutput.AddText("True, both expressions amount to ");
trueOutput.AddField(leftExpression);

FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
falseOutput.AddNode(new Run(doc, "False, "));
falseOutput.AddField(leftExpression);
falseOutput.AddNode(new Run(doc, " does not equal "));
falseOutput.AddField(rightExpression);

 // Enfin, nous allons créer un autre générateur de champ pour le champ IF et combiner toutes les expressions.
builder = new FieldBuilder(FieldType.FieldIf);
builder.AddArgument(leftExpression);
builder.AddArgument("=");
builder.AddArgument(rightExpression);
builder.AddArgument(trueOutput);
builder.AddArgument(falseOutput);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

Assert.AreEqual(" IF \u0013 = 2 + 3 \u0014\u0015 = \u0013 = 2.5 * 5.2 \u0014\u0015 " +
                "\"True, both expressions amount to \u0013 = 2 + 3 \u0014\u0015\" " +
                "\"False, \u0013 = 2 + 3 \u0014\u0015 does not equal \u0013 = 2.5 * 5.2 \u0014\u0015\" ", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SYMBOL.docx");
```

### Voir également

* class [Inline](../../../aspose.words/inline/)
* class [FieldArgumentBuilder](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
