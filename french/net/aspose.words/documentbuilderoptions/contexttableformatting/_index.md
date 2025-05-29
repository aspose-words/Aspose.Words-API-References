---
title: DocumentBuilderOptions.ContextTableFormatting
linktitle: ContextTableFormatting
articleTitle: ContextTableFormatting
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ContextTableFormatting dans DocumentBuilderOptions. Assurez-vous que la mise en forme des tableaux reste indépendante, améliorant ainsi la clarté et le style de votre document.
type: docs
weight: 20
url: /fr/net/aspose.words/documentbuilderoptions/contexttableformatting/
---
## DocumentBuilderOptions.ContextTableFormatting property

Vrai si la mise en forme appliquée au contenu du tableau n'affecte pas la mise en forme du contenu qui le suit. La valeur par défaut est`vrai` .

```csharp
public bool ContextTableFormatting { get; set; }
```

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

* class [DocumentBuilderOptions](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
