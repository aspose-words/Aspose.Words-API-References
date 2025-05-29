---
title: OdtSaveOptions.IsStrictSchema11
linktitle: IsStrictSchema11
articleTitle: IsStrictSchema11
second_title: Aspose.Words pour .NET
description: Optimisez vos exportations ODT avec la propriété IsStrictSchema11. Assurez une conformité stricte avec ODT 1.1 ou activez la compatibilité 1.2 pour de meilleurs résultats.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/odtsaveoptions/isstrictschema11/
---
## OdtSaveOptions.IsStrictSchema11 property

Spécifie si l'exportation doit correspondre strictement à la spécification ODT 1.1. OOo 3.0 affiche correctement les fichiers lorsqu'ils contiennent des éléments et des attributs d'ODT 1.2. Utilisez « false » à cette fin, ou « true » pour une conformité stricte à la spécification 1.1. La valeur par défaut est`FAUX` .

```csharp
public bool IsStrictSchema11 { get; set; }
```

## Exemples

Montre comment rendre un document enregistré conforme à un ancien schéma ODT.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Voir également

* class [OdtSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
