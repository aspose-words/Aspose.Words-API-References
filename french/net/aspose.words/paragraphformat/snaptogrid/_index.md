---
title: ParagraphFormat.SnapToGrid
linktitle: SnapToGrid
articleTitle: SnapToGrid
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété ParagraphFormat SnapToGrid améliore la précision de la mise en page en alignant vos paragraphes avec les lignes de la grille du document pour un aspect soigné.
type: docs
weight: 300
url: /fr/net/aspose.words/paragraphformat/snaptogrid/
---
## ParagraphFormat.SnapToGrid property

Spécifie si le paragraphe actuel doit utiliser les paramètres de lignes de grille du document par page lors de la mise en page du contenu du paragraphe.

```csharp
public bool SnapToGrid { get; set; }
```

## Exemples

Montre comment spécifier une limite pour le nombre de lignes que chaque page peut contenir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Activez le pitching, puis utilisez-le pour définir le nombre de lignes par page dans cette section.
// Une taille de police suffisamment grande repoussera certaines lignes vers la page suivante pour éviter le chevauchement des caractères.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### Voir également

* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
