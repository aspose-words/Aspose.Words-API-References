---
title: Enum TableStyleOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Tables.TableStyleOptions énumération. Spécifie comment le style de tableau est appliqué à un tableau.
type: docs
weight: 6370
url: /fr/net/aspose.words.tables/tablestyleoptions/
---
## TableStyleOptions enumeration

Spécifie comment le style de tableau est appliqué à un tableau.

```csharp
[Flags]
public enum TableStyleOptions
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Aucun formatage de style de tableau n'est appliqué. |
| FirstRow | `20` | Appliquer la mise en forme conditionnelle de la première ligne. |
| LastRow | `40` | Appliquer la mise en forme conditionnelle de la dernière ligne. |
| FirstColumn | `80` | Appliquer la mise en forme conditionnelle d'une première colonne. |
| LastColumn | `100` | Appliquer la mise en forme conditionnelle de la dernière colonne. |
| RowBands | `200` | Appliquer la mise en forme conditionnelle des bandes de lignes. |
| ColumnBands | `400` | Appliquer la mise en forme conditionnelle des bandes de colonnes. |
| Default2003 | `600` | Les bandes de lignes et de colonnes sont appliquées. Il s'agit de la valeur par défaut de Microsoft Word pour les anciens formats tels que DOC, WML et RTF. |
| Default | `2A0` | Il s'agit des valeurs par défaut de Microsoft Word. |

### Exemples

Montre comment créer un nouveau tableau tout en appliquant un style.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Nous devons insérer au moins une ligne avant de définir un formatage de tableau.
builder.InsertCell();

// Définit le style de tableau utilisé en fonction de l'identifiant de style.
// Notez que tous les styles de tableau ne sont pas disponibles lors de l'enregistrement au format .doc.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Applique partiellement le style aux fonctionnalités de la table en fonction des prédicats, puis construit la table.
table.StyleOptions =
    TableStyleOptions.FirstColumn | TableStyleOptions.RowBands | TableStyleOptions.FirstRow;
table.AutoFit(AutoFitBehavior.AutoFitToContents);

builder.Writeln("Item");
builder.CellFormat.RightPadding = 40;
builder.InsertCell();
builder.Writeln("Quantity (kg)");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Apples");
builder.InsertCell();
builder.Writeln("20");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Bananas");
builder.InsertCell();
builder.Writeln("40");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Carrots");
builder.InsertCell();
builder.Writeln("50");
builder.EndRow();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithStyle.docx");
```

### Voir également

* property [StyleOptions](../table/styleoptions/)
* espace de noms [Aspose.Words.Tables](../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../)


