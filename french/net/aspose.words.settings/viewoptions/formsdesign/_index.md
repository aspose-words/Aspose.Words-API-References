---
title: ViewOptions.FormsDesign
linktitle: FormsDesign
articleTitle: FormsDesign
second_title: Aspose.Words pour .NET
description: Découvrez comment ViewOptions FormsDesign améliore votre expérience documentaire en basculant le mode de conception de formulaires pour une édition et une personnalisation transparentes.
type: docs
weight: 30
url: /fr/net/aspose.words.settings/viewoptions/formsdesign/
---
## ViewOptions.FormsDesign property

Spécifie si le document est en mode de conception de formulaires.

```csharp
public bool FormsDesign { get; set; }
```

## Remarques

Fonctionne actuellement uniquement pour les documents au format WordML.

## Exemples

Montre comment activer/désactiver le mode de conception de formulaires.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Définissez la propriété « FormsDesign » sur « false » pour conserver le mode de conception de formulaires désactivé.
// Définissez la propriété « FormsDesign » sur « true » pour activer le mode de conception de formulaires.
doc.ViewOptions.FormsDesign = useFormsDesign;

doc.Save(ArtifactsDir + "ViewOptions.FormsDesign.xml");

Assert.AreEqual(useFormsDesign,
    File.ReadAllText(ArtifactsDir + "ViewOptions.FormsDesign.xml").Contains("<w:formsDesign />"));
```

### Voir également

* class [ViewOptions](../)
* espace de noms [Aspose.Words.Settings](../../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../../)
