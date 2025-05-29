---
title: DocumentBuilderOptions Class
linktitle: DocumentBuilderOptions
articleTitle: DocumentBuilderOptions
second_title: Aspose.Words pour .NET
description: Découvrez Aspose.Words.DocumentBuilderOptions pour améliorer la création de vos documents avec des fonctionnalités personnalisables pour une expérience de création transparente.
type: docs
weight: 670
url: /fr/net/aspose.words/documentbuilderoptions/
---
## DocumentBuilderOptions class

Permet de spécifier des options supplémentaires pour le processus de création de documents.

```csharp
public class DocumentBuilderOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [DocumentBuilderOptions](documentbuilderoptions/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [ContextTableFormatting](../../aspose.words/documentbuilderoptions/contexttableformatting/) { get; set; } | Vrai si la mise en forme appliquée au contenu du tableau n'affecte pas la mise en forme du contenu qui le suit. La valeur par défaut est`vrai` . |
| [DesignMode](../../aspose.words/documentbuilderoptions/designmode/) { get; set; } | Correspond au mode Conception dans Microsoft Word. |

## Exemples

Montre comment ignorer la mise en forme du tableau pour le contenu après.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// Ajoute du contenu avant le tableau.
// La taille de police par défaut est 12.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// Modifie la taille de la police à l'intérieur du tableau.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// Si ContextTableFormatting est vrai, la mise en forme du tableau n'est pas appliquée au contenu après.
// Si ContextTableFormatting est faux, la mise en forme du tableau est appliquée au contenu après.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
