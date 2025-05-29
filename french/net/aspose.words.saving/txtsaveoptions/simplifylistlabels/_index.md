---
title: TxtSaveOptions.SimplifyListLabels
linktitle: SimplifyListLabels
articleTitle: SimplifyListLabels
second_title: Aspose.Words pour .NET
description: Découvrez comment la fonctionnalité SimplifyListLabels de TxtSaveOptions améliore la clarté en rationalisant les étiquettes de liste complexes pour une meilleure représentation du texte.
type: docs
weight: 70
url: /fr/net/aspose.words.saving/txtsaveoptions/simplifylistlabels/
---
## TxtSaveOptions.SimplifyListLabels property

Spécifie si le programme doit simplifier les étiquettes de liste dans le cas où le formatage d'étiquette complexe n'est pas correctement représenté par du texte brut.

Si défini sur`vrai` Les libellés des listes numérotées sont écrits au format numérique simple (x000d) et les libellés des listes détaillées en caractères ASCII simples. La valeur par défaut est`FAUX`.

```csharp
public bool SimplifyListLabels { get; set; }
```

## Exemples

Montre comment modifier l'apparence des listes lors de l'enregistrement d'un document en texte brut.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Créez une liste à puces avec cinq niveaux d'indentation.
builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Item 1");
builder.ListFormat.ListIndent();
builder.Writeln("Item 2");
builder.ListFormat.ListIndent();
builder.Writeln("Item 3");
builder.ListFormat.ListIndent();
builder.Writeln("Item 4");
builder.ListFormat.ListIndent();
builder.Write("Item 5");

// Créez un objet « TxtSaveOptions », que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la façon dont nous enregistrons le document en texte brut.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Définissez la propriété « SimplifyListLabels » sur « true » pour convertir une liste
// symboles en caractères ASCII plus simples, tels que '*', 'o', '+', '>', etc.
// Définissez la propriété « SimplifyListLabels » sur « false » pour conserver autant de symboles de liste d'origine que possible.
txtSaveOptions.SimplifyListLabels = simplifyListLabels;

doc.Save(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt");

string newLine = Environment.NewLine;

if (simplifyListLabels)
    Assert.AreEqual($"* Item 1{newLine}" +
                    $"  > Item 2{newLine}" +
                    $"    + Item 3{newLine}" +
                    $"      - Item 4{newLine}" +
                    $"        o Item 5{newLine}", docText);
else
    Assert.AreEqual($"· Item 1{newLine}" +
                    $"o Item 2{newLine}" +
                    $"§ Item 3{newLine}" +
                    $"· Item 4{newLine}" +
                    $"o Item 5{newLine}", docText);
```

### Voir également

* class [TxtSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
