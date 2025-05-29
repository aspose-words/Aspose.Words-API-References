---
title: OdtSaveMeasureUnit Enum
linktitle: OdtSaveMeasureUnit
articleTitle: OdtSaveMeasureUnit
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.OdtSaveMeasureUnit pour un contrôle précis des mesures de vos documents. Améliorez facilement la mise en forme de vos documents !
type: docs
weight: 6100
url: /fr/net/aspose.words.saving/odtsavemeasureunit/
---
## OdtSaveMeasureUnit enumeration

Unités de mesure spécifiées à appliquer au contenu mesurable du document, tel que la forme, les largeurs et autres, lors de l'enregistrement.

```csharp
public enum OdtSaveMeasureUnit
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Centimeters | `0` | Spécifie que le contenu du document est enregistré en centimètres. |
| Inches | `1` | Spécifie que le contenu du document est enregistré en pouces. |

## Exemples

Montre comment utiliser différentes unités de mesure pour définir les paramètres de style d'un document ODT enregistré.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Lorsque nous exportons le document vers .odt, nous pouvons utiliser un objet OdtSaveOptions pour modifier la façon dont nous enregistrons le document.
// Nous pouvons définir la propriété « MeasureUnit » sur « OdtSaveMeasureUnit.Centimeters »
 // pour définir du contenu tel que des paramètres de style à l'aide du système métrique, utilisé par Open Office.
// Nous pouvons définir la propriété « MeasureUnit » sur « OdtSaveMeasureUnit.Inches »
// pour définir du contenu tel que des paramètres de style à l'aide du système impérial, utilisé par Microsoft Word.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
