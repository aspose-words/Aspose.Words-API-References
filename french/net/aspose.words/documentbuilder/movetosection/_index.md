---
title: DocumentBuilder.MoveToSection
linktitle: MoveToSection
articleTitle: MoveToSection
second_title: Aspose.Words pour .NET
description: Découvrez la méthode MoveToSection de DocumentBuilder pour naviguer facilement jusqu'au début du corps de n'importe quelle section, améliorant ainsi l'efficacité de l'édition de votre document.
type: docs
weight: 610
url: /fr/net/aspose.words/documentbuilder/movetosection/
---
## DocumentBuilder.MoveToSection method

Déplace le curseur au début du corps dans une section spécifiée.

```csharp
public void MoveToSection(int sectionIndex)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| sectionIndex | Int32 | L'index de la section vers laquelle se déplacer. |

## Remarques

Quand*sectionIndex*est supérieur ou égal à 0, il spécifie un index à partir de le début du document, 0 étant la première section. Lorsque*sectionIndex* est inférieur à 0, il a spécifié un index à partir de la fin du document avec -1 étant la dernière section.

Le curseur est déplacé vers le premier paragraphe du[`Body`](../../body/) de la section spécifiée.

## Exemples

Montre comment créer des en-têtes et des pieds de page dans un document à l'aide de DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Spécifiez que nous voulons des en-têtes et des pieds de page différents pour les premières pages, les pages paires et les pages impaires.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Créez les en-têtes, puis ajoutez trois pages au document pour afficher chaque type d'en-tête.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

### Voir également

* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
