---
title: FieldBuilder
second_title: Référence de l'API Aspose.Words pour .NET
description: Construit un champ à partir de jetons de code de champ arguments et commutateurs.
type: docs
weight: 1510
url: /fr/net/aspose.words.fields/fieldbuilder/
---
## FieldBuilder class

Construit un champ à partir de jetons de code de champ (arguments et commutateurs).

```csharp
public class FieldBuilder
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldBuilder](fieldbuilder/)(FieldType) | Initialise une instance du`FieldBuilder` classe. |

## Méthodes

| Nom | La description |
| --- | --- |
| [AddArgument](../../aspose.words.fields/fieldbuilder/addargument/#addargument_2)(double) | Ajoute l'argument d'un champ. |
| [AddArgument](../../aspose.words.fields/fieldbuilder/addargument/#addargument)(FieldArgumentBuilder) | Ajoute un argument de champ représenté par[`FieldArgumentBuilder`](../fieldargumentbuilder/) au code du champ. |
| [AddArgument](../../aspose.words.fields/fieldbuilder/addargument/#addargument_1)(FieldBuilder) | Ajoute un champ enfant représenté par un autre`FieldBuilder` au code du champ. |
| [AddArgument](../../aspose.words.fields/fieldbuilder/addargument/#addargument_3)(int) | Ajoute l'argument d'un champ. |
| [AddArgument](../../aspose.words.fields/fieldbuilder/addargument/#addargument_4)(string) | Ajoute l'argument d'un champ. |
| [AddSwitch](../../aspose.words.fields/fieldbuilder/addswitch/#addswitch)(string) | Ajoute un commutateur de champ. |
| [AddSwitch](../../aspose.words.fields/fieldbuilder/addswitch/#addswitch_1)(string, double) | Ajoute un commutateur de champ. |
| [AddSwitch](../../aspose.words.fields/fieldbuilder/addswitch/#addswitch_2)(string, int) | Ajoute un commutateur de champ. |
| [AddSwitch](../../aspose.words.fields/fieldbuilder/addswitch/#addswitch_3)(string, string) | Ajoute un commutateur de champ. |
| [BuildAndInsert](../../aspose.words.fields/fieldbuilder/buildandinsert/#buildandinsert)(Inline) | Construit et insère un champ dans le document avant le nœud en ligne spécifié. |
| [BuildAndInsert](../../aspose.words.fields/fieldbuilder/buildandinsert/#buildandinsert_1)(Paragraph) | Construit et insère un champ dans le document à la fin du paragraphe spécifié. |

### Exemples

Montre comment créer des champs à l'aide d'un générateur de champs, puis les insérer dans le document.

```csharp
Document doc = new Document();

// Vous trouverez ci-dessous trois exemples de construction de champs réalisés à l'aide d'un constructeur de champs.
// 1 - Champ unique :
// Utilisez un constructeur de champ pour ajouter un champ SYMBOLE qui affiche le symbole ƒ (Florin).
FieldBuilder builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(402);
builder.AddSwitch("\\f", "Arial");
builder.AddSwitch("\\s", 25);
builder.AddSwitch("\\u");
Field field = builder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph);

Assert.AreEqual(" SYMBOL 402 \\f Arial \\s 25 \\u ", field.GetFieldCode());

// 2 - Champ imbriqué :
// Utilisez un générateur de champ pour créer un champ de formule utilisé comme champ interne par un autre générateur de champ.
FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FieldFormula);
innerFormulaBuilder.AddArgument(100);
innerFormulaBuilder.AddArgument("+");
innerFormulaBuilder.AddArgument(74);

// Crée un autre builder pour un autre champ SYMBOL, et insère le champ de formule
 // que nous avons créé ci-dessus dans le champ SYMBOL comme argument.
builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(innerFormulaBuilder);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

// Le champ SYMBOL externe utilisera le résultat du champ de formule, 174, comme argument,
// ce qui fera que le champ affichera le symbole ® (Signe enregistré) puisque son numéro de caractère est 174.
Assert.AreEqual(" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field.GetFieldCode());

// 3 - Plusieurs champs et arguments imbriqués :
// Maintenant, nous allons utiliser un générateur pour créer un champ IF, qui affiche l'une des deux valeurs de chaîne personnalisées,
// en fonction de la valeur vrai/faux de son expression. Pour obtenir une valeur vrai/faux
// qui détermine quelle chaîne le champ IF affiche, le champ IF testera l'égalité de deux expressions numériques.
// Nous fournirons les deux expressions sous la forme de champs de formule, que nous imbriquerons dans le champ IF.
FieldBuilder leftExpression = new FieldBuilder(FieldType.FieldFormula);
leftExpression.AddArgument(2);
leftExpression.AddArgument("+");
leftExpression.AddArgument(3);

FieldBuilder rightExpression = new FieldBuilder(FieldType.FieldFormula);
rightExpression.AddArgument(2.5);
rightExpression.AddArgument("*");
rightExpression.AddArgument(5.2);

// Ensuite, nous allons construire deux arguments de champ, qui serviront de chaînes de sortie vrai/faux pour le champ IF.
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

* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
