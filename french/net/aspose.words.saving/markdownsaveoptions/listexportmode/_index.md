---
title: MarkdownSaveOptions.ListExportMode
linktitle: ListExportMode
articleTitle: ListExportMode
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ListExportMode de MarkdownSaveOptions, qui contrôle l'affichage des éléments de liste. Optimisez vos fichiers grâce à la syntaxe Markdown flexible !
type: docs
weight: 110
url: /fr/net/aspose.words.saving/markdownsaveoptions/listexportmode/
---
## MarkdownSaveOptions.ListExportMode property

Spécifie comment les éléments de la liste seront écrits dans le fichier de sortie. La valeur par défaut estMarkdownSyntax .

```csharp
public MarkdownListExportMode ListExportMode { get; set; }
```

## Remarques

Lorsque cette propriété est définie surPlainText toutes les étiquettes de liste sont mises à jour à l'aide de[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) et exportées avec leurs valeurs réelles. Ces listes peuvent être incompatibles avec le format Markdown et seront alors reconnues comme du texte brut lors de l'importation.

Lorsque cette propriété est définie surMarkdownSyntax, l'écrivain essaie d'exporter éléments de liste d'une manière qui permet de numéroter les éléments de liste en mode automatique par Markdown.

## Exemples

Montre comment les éléments de la liste seront écrits dans le document Markdown.

```csharp
Document doc = new Document(MyDir + "List item.docx");

// Utilisez MarkdownListExportMode.PlainText ou MarkdownListExportMode.MarkdownSyntax pour exporter la liste.
MarkdownSaveOptions options = new MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ListExportMode.md", options);
```

### Voir également

* enum [MarkdownListExportMode](../../markdownlistexportmode/)
* class [MarkdownSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
