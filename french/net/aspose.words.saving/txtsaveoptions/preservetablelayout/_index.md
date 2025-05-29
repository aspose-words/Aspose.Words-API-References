---
title: TxtSaveOptions.PreserveTableLayout
linktitle: PreserveTableLayout
articleTitle: PreserveTableLayout
second_title: Aspose.Words pour .NET
description: Découvrez la fonctionnalité PreserveTableLayout de TxtSaveOptions, qui préserve la mise en page de vos tableaux lors de leur enregistrement au format texte brut. Améliorez la lisibilité de vos documents !
type: docs
weight: 50
url: /fr/net/aspose.words.saving/txtsaveoptions/preservetablelayout/
---
## TxtSaveOptions.PreserveTableLayout property

Spécifie si le programme doit tenter de conserver la mise en page des tableaux lors de l'enregistrement au format texte brut. La valeur par défaut est`FAUX` .

```csharp
public bool PreserveTableLayout { get; set; }
```

## Exemples

Montre comment conserver la mise en page des tableaux lors de la conversion en texte brut.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1");
builder.InsertCell();
builder.Write("Row 1, cell 2");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, cell 1");
builder.InsertCell();
builder.Write("Row 2, cell 2");
builder.EndTable();

// Créez un objet « TxtSaveOptions », que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la façon dont nous enregistrons le document en texte brut.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Définissez la propriété « PreserveTableLayout » sur « true » pour appliquer un remplissage d'espaces blancs au contenu
// du document de sortie en texte brut pour préserver autant que possible la mise en page du tableau.
// Définissez la propriété « PreserveTableLayout » sur « false » pour enregistrer le contenu de toutes les tables
// comme un corps de texte continu, avec juste une nouvelle ligne pour chaque ligne.
txtSaveOptions.PreserveTableLayout = preserveTableLayout;

doc.Save(ArtifactsDir + "TxtSaveOptions.PreserveTableLayout.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.PreserveTableLayout.txt");

if (preserveTableLayout)
    Assert.AreEqual("Row 1, cell 1                                            Row 1, cell 2\r\n" +
                    "Row 2, cell 1                                            Row 2, cell 2\r\n\r\n", docText);
else
    Assert.AreEqual("Row 1, cell 1\r" +
                    "Row 1, cell 2\r" +
                    "Row 2, cell 1\r" +
                    "Row 2, cell 2\r\r\n", docText);
```

### Voir également

* class [TxtSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
