---
title: OdtSaveOptions.IsStrictSchema11
second_title: Référence de l'API Aspose.Words pour .NET
description: OdtSaveOptions propriété. Spécifie si lexportation doit correspondre strictement à la spécification ODT 1.1. OOo 3.0 affiche correctement les fichiers lorsquils contiennent des éléments et attributs dODT 1.2. Utilisez false à cet effet ou true pour une stricte conformité à la spécification 1.1. La valeur par défaut estFAUX .
type: docs
weight: 20
url: /fr/net/aspose.words.saving/odtsaveoptions/isstrictschema11/
---
## OdtSaveOptions.IsStrictSchema11 property

Spécifie si l'exportation doit correspondre strictement à la spécification ODT 1.1. OOo 3.0 affiche correctement les fichiers lorsqu'ils contiennent des éléments et attributs d'ODT 1.2. Utilisez "false" à cet effet, ou "true" pour une stricte conformité à la spécification 1.1. La valeur par défaut est`FAUX` .

```csharp
public bool IsStrictSchema11 { get; set; }
```

### Exemples

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
* espace de noms [Aspose.Words.Saving](../../odtsaveoptions/)
* Assemblée [Aspose.Words](../../../)


