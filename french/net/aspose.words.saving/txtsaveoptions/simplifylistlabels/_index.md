---
title: TxtSaveOptions.SimplifyListLabels
linktitle: SimplifyListLabels
articleTitle: SimplifyListLabels
second_title: Aspose.Words pour .NET
description: TxtSaveOptions SimplifyListLabels propriété. Spécifie si le programme doit simplifier les étiquettes de liste dans le cas où le formatage des étiquettes complexes nest pas correctement représenté par du texte brut en C#.
type: docs
weight: 70
url: /fr/net/aspose.words.saving/txtsaveoptions/simplifylistlabels/
---
## TxtSaveOptions.SimplifyListLabels property

Spécifie si le programme doit simplifier les étiquettes de liste dans le cas où le formatage des étiquettes complexes n'est pas correctement représenté par du texte brut.

Si réglé sur`vrai` , les étiquettes de liste numérotée sont écrites au format numérique simple et les étiquettes de liste détaillée sous forme de simples caractères ASCII. La valeur par défaut est`FAUX`.

```csharp
public bool SimplifyListLabels { get; set; }
```

## Exemples

Montre comment modifier l’apparence des listes lors de l’enregistrement d’un document en texte brut.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crée une liste à puces avec cinq niveaux d'indentation.
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

// Crée un objet "TxtSaveOptions", que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont nous enregistrons le document en texte brut.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Définit la propriété "SimplifyListLabels" sur "true" pour convertir une liste
// les symboles en caractères ASCII plus simples, tels que '*', 'o', '+', '>', etc.
// Définissez la propriété "SimplifyListLabels" sur "false" pour conserver autant de symboles de liste d'origine que possible.
txtSaveOptions.SimplifyListLabels = simplifyListLabels;

doc.Save(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt");

if (simplifyListLabels)
    Assert.AreEqual("* Item 1\r\n" +
                    "  > Item 2\r\n" +
                    "    + Item 3\r\n" +
                    "      - Item 4\r\n" +
                    "        o Item 5\r\n", docText);
else
    Assert.AreEqual("· Item 1\r\n" +
                    "o Item 2\r\n" +
                    "§ Item 3\r\n" +
                    "· Item 4\r\n" +
                    "o Item 5\r\n", docText);
```

### Voir également

* class [TxtSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
