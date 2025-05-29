---
title: SaveOptions.Dml3DEffectsRenderingMode
linktitle: Dml3DEffectsRenderingMode
articleTitle: Dml3DEffectsRenderingMode
second_title: Aspose.Words pour .NET
description: Découvrez la propriété SaveOptions Dml3DEffectsRenderingMode pour contrôler facilement le rendu des effets 3D pour une qualité visuelle améliorée dans vos applications.
type: docs
weight: 50
url: /fr/net/aspose.words.saving/saveoptions/dml3deffectsrenderingmode/
---
## SaveOptions.Dml3DEffectsRenderingMode property

Obtient ou définit une valeur déterminant la manière dont les effets 3D sont rendus.

```csharp
public Dml3DEffectsRenderingMode Dml3DEffectsRenderingMode { get; set; }
```

## Remarques

La valeur par défaut estBasic .

## Exemples

Montre comment les effets 3D sont rendus.

```csharp
Document doc = new Document(MyDir + "DrawingML shape 3D effects.docx");

RenderCallback warningCallback = new RenderCallback();
doc.WarningCallback = warningCallback;

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.Dml3DEffectsRenderingMode = Dml3DEffectsRenderingMode.Advanced;

doc.Save(ArtifactsDir + "PdfSaveOptions.Dml3DEffectsRenderingModeTest.pdf", saveOptions);
```

### Voir également

* enum [Dml3DEffectsRenderingMode](../../dml3deffectsrenderingmode/)
* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
