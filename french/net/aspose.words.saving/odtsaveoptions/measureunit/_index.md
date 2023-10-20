---
title: OdtSaveOptions.MeasureUnit
linktitle: MeasureUnit
articleTitle: MeasureUnit
second_title: Aspose.Words pour .NET
description: OdtSaveOptions MeasureUnit propriété. Permet de spécifier les unités de mesure à appliquer au contenu du document. La valeur par défaut estCentimeters en C#.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/odtsaveoptions/measureunit/
---
## OdtSaveOptions.MeasureUnit property

Permet de spécifier les unités de mesure à appliquer au contenu du document. La valeur par défaut estCentimeters

```csharp
public OdtSaveMeasureUnit MeasureUnit { get; set; }
```

## Remarques

Open Office utilise des centimètres pour spécifier les longueurs, les largeurs et autres formats mesurables et les propriétés de contenu dans les documents, tandis que MS Office utilise les pouces.

## Exemples

Montre comment utiliser différentes unités de mesure pour définir les paramètres de style d'un document ODT enregistré.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Lorsque nous exportons le document au format .odt, nous pouvons utiliser un objet OdtSaveOptions pour modifier la façon dont nous enregistrons le document.
// Nous pouvons définir la propriété "MeasureUnit" sur "OdtSaveMeasureUnit.Centimeters"
 // pour définir le contenu tel que les paramètres de style à l'aide du système métrique utilisé par Open Office.
// Nous pouvons définir la propriété "MeasureUnit" sur "OdtSaveMeasureUnit.Inches"
// pour définir le contenu tel que les paramètres de style en utilisant le système impérial, utilisé par Microsoft Word.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Voir également

* enum [OdtSaveMeasureUnit](../../odtsavemeasureunit/)
* class [OdtSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
