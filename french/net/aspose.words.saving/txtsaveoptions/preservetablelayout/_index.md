---
title: TxtSaveOptions.PreserveTableLayout
second_title: Référence de l'API Aspose.Words pour .NET
description: TxtSaveOptions propriété. Spécifie si le programme doit tenter de conserver la disposition des tableaux lors de lenregistrement au format texte brut. La valeur par défaut estFAUX .
type: docs
weight: 50
url: /fr/net/aspose.words.saving/txtsaveoptions/preservetablelayout/
---
## TxtSaveOptions.PreserveTableLayout property

Spécifie si le programme doit tenter de conserver la disposition des tableaux lors de l'enregistrement au format texte brut. La valeur par défaut est`FAUX` .

```csharp
public bool PreserveTableLayout { get; set; }
```

### Exemples

Montre comment conserver la disposition des tableaux lors de la conversion en texte brut.

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

// Crée un objet "TxtSaveOptions", que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont nous enregistrons le document en texte brut.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Définissez la propriété "PreserveTableLayout" sur "true" pour appliquer un remplissage d'espaces au contenu
// du document en texte brut de sortie pour conserver autant que possible la disposition du tableau.
// Définissez la propriété "PreserveTableLayout" sur "false" pour enregistrer le contenu de toutes les tables
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
* espace de noms [Aspose.Words.Saving](../../txtsaveoptions/)
* Assemblée [Aspose.Words](../../../)


