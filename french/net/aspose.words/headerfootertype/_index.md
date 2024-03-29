---
title: HeaderFooterType Enum
linktitle: HeaderFooterType
articleTitle: HeaderFooterType
second_title: Aspose.Words pour .NET
description: Aspose.Words.HeaderFooterType énumération. Identifie le type dentête ou de pied de page trouvé dans un fichier Word en C#.
type: docs
weight: 3120
url: /fr/net/aspose.words/headerfootertype/
---
## HeaderFooterType enumeration

Identifie le type d'en-tête ou de pied de page trouvé dans un fichier Word.

```csharp
public enum HeaderFooterType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| HeaderEven | `0` | En-tête pour les pages paires. |
| HeaderPrimary | `1` | En-tête principal, également utilisé pour les pages impaires. |
| FooterEven | `2` | Pied de page pour les pages paires. |
| FooterPrimary | `3` | Pied de page principal, également utilisé pour les pages impaires. |
| HeaderFirst | `4` | En-tête de la première page de la section. |
| FooterFirst | `5` | Pied de page de la première page de la section. |

## Exemples

Montre comment créer des en-têtes et des pieds de page dans un document à l'aide de DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Spécifie que nous voulons des en-têtes et pieds de page différents pour les premières pages, paires et impaires.
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

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
