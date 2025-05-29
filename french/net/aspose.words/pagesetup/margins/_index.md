---
title: PageSetup.Margins
linktitle: Margins
articleTitle: Margins
second_title: Aspose.Words pour .NET
description: Ajustez facilement les marges de votre page grâce à la propriété PageSetup. Personnalisez les paramètres pour une mise en page et une présentation optimales. Améliorez l'apparence de votre document !
type: docs
weight: 260
url: /fr/net/aspose.words/pagesetup/margins/
---
## PageSetup.Margins property

Renvoie ou définit le préréglage[`Margins`](../../margins/) de la page.

```csharp
public Margins Margins { get; set; }
```

## Exemples

Indique quand recalculer la mise en page du document.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// L'enregistrement d'un document au format PDF, dans une image ou l'impression pour la première fois sera automatiquement
// mettre en cache la mise en page du document dans ses pages.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Modifier le document d'une manière ou d'une autre.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// Dans la version actuelle d'Aspose.Words, la modification du document ne le reconstruit pas automatiquement
// la mise en page en cache. Si nous souhaitons la mise en page en cache
// pour rester à jour, nous devrons le mettre à jour manuellement.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Voir également

* enum [Margins](../../margins/)
* class [PageSetup](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
