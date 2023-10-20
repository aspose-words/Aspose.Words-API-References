---
title: Document.UpdatePageLayout
linktitle: UpdatePageLayout
articleTitle: UpdatePageLayout
second_title: Aspose.Words pour .NET
description: Document UpdatePageLayout méthode. Reconstruit la mise en page du document en C#.
type: docs
weight: 770
url: /fr/net/aspose.words/document/updatepagelayout/
---
## Document.UpdatePageLayout method

Reconstruit la mise en page du document.

```csharp
public void UpdatePageLayout()
```

## Remarques

Cette méthode formate un document en pages et met à jour les champs liés au numéro de page dans le document tels que comme PAGE, PAGES, PAGEREF et REF. Les informations de mise en page à jour sont requises pour un rendu correct du document aux formats de page fixes.

Cette méthode est automatiquement invoquée lorsque vous convertissez pour la première fois un document en PDF, XPS, image ou que vous l'imprimez. Cependant, si vous modifiez le document après le rendu, puis tentez de le restituer à nouveau, Aspose.Words ne mettra pas automatiquement à jour la mise en page . Dans ce cas, vous devriez appeler`UpdatePageLayout` before rendu à nouveau.

## Exemples

Indique quand recalculer la mise en page du document.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// L'enregistrement d'un document au format PDF, dans une image ou l'impression pour la première fois sera automatiquement
// cache la mise en page du document dans ses pages.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Modifier le document d'une manière ou d'une autre.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

 // Dans la version actuelle d'Aspose.Words, la modification du document ne reconstruit pas automatiquement
// la mise en page mise en cache. Si nous souhaitons la mise en cache
// pour rester à jour, nous devrons le mettre à jour manuellement.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
