---
title: Document.UpdatePageLayout
linktitle: UpdatePageLayout
articleTitle: UpdatePageLayout
second_title: Aspose.Words pour .NET
description: Réorganisez la structure de votre document avec la méthode UpdatePageLayout, garantissant une mise en page soignée et organisée pour une lisibilité et une présentation améliorées.
type: docs
weight: 830
url: /fr/net/aspose.words/document/updatepagelayout/
---
## Document.UpdatePageLayout method

Reconstruit la mise en page du document.

```csharp
public void UpdatePageLayout()
```

## Remarques

Cette méthode formate un document en pages et met à jour les champs liés aux numéros de page, tels que PAGE, PAGES, PAGEREF et REF. Des informations de mise en page à jour sont nécessaires pour un rendu correct du document aux formats de page fixes.

Cette méthode est automatiquement invoquée lors de la première conversion d'un document au format PDF, XPS, image ou lors de son impression. Cependant, si vous modifiez le document après le rendu, puis tentez de le restituer, Aspose.Words ne mettra pas à jour automatiquement la mise en page. Dans ce cas, appelez-le.`UpdatePageLayout` avant rendu à nouveau.

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

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
