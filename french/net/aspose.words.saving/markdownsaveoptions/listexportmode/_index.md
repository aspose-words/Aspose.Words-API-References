---
title: MarkdownSaveOptions.ListExportMode
linktitle: ListExportMode
articleTitle: ListExportMode
second_title: Aspose.Words pour .NET
description: MarkdownSaveOptions ListExportMode propriété. Spécifie comment les éléments de la liste seront écrits dans le fichier de sortie. La valeur par défaut estMarkdownSyntax  en C#.
type: docs
weight: 60
url: /fr/net/aspose.words.saving/markdownsaveoptions/listexportmode/
---
## MarkdownSaveOptions.ListExportMode property

Spécifie comment les éléments de la liste seront écrits dans le fichier de sortie. La valeur par défaut estMarkdownSyntax .

```csharp
public MarkdownListExportMode ListExportMode { get; set; }
```

## Remarques

Lorsque cette propriété est définie surPlainText toutes les étiquettes de liste sont mises à jour à l'aide[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/)et exportés avec leurs valeurs réelles. De telles lists peuvent être non compatibles avec le format Markdown et seront reconnues comme texte brut lors de l'importation dans ce cas.

Lorsque cette propriété est définie surMarkdownSyntax, l'écrivain essaie d'export les éléments de la liste d'une manière qui permet de numéroter les éléments de la liste en mode automatique par Markdown.

## Exemples

Montre comment répertorier les éléments qui seront écrits dans le document de démarque.

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
