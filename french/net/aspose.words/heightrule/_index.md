---
title: HeightRule Enum
linktitle: HeightRule
articleTitle: HeightRule
second_title: Aspose.Words pour .NET
description: Aspose.Words.HeightRule énumération. Spécifie la règle permettant de déterminer la hauteur dun objet en C#.
type: docs
weight: 3130
url: /fr/net/aspose.words/heightrule/
---
## HeightRule enumeration

Spécifie la règle permettant de déterminer la hauteur d'un objet.

```csharp
public enum HeightRule
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| AtLeast | `0` | La hauteur sera au moins la hauteur spécifiée en points. Il s'agrandira, si nécessaire, pour accueillir tout le texte à l'intérieur d'un objet. |
| Exactly | `1` | La hauteur est spécifiée exactement en points. Veuillez noter que si le texte ne peut pas rentrer à l'intérieur de l'objet de cette hauteur, il apparaîtra tronqué. |
| Auto | `2` | La hauteur augmentera automatiquement pour accueillir tout le texte à l'intérieur d'un objet. |

## Exemples

Montre comment formater les lignes avec un générateur de documents.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Démarre une deuxième ligne, puis configure sa hauteur. Le constructeur appliquera ces paramètres à
// sa ligne actuelle, ainsi que toutes les nouvelles lignes créées par la suite.
builder.EndRow();

RowFormat rowFormat = builder.RowFormat;
rowFormat.Height = 100;
rowFormat.HeightRule = HeightRule.Exactly;

builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.EndTable();

// La première ligne n'a pas été affectée par la reconfiguration du remplissage et contient toujours les valeurs par défaut.
Assert.AreEqual(0.0d, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);

Assert.AreEqual(100.0d, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
