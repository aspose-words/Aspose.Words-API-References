---
title: LoadOptions.IgnoreOleData
linktitle: IgnoreOleData
articleTitle: IgnoreOleData
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété LoadOptions IgnoreOleData optimise la gestion de vos données en vous permettant de contrôler le traitement des données OLE. Optimisez votre flux de travail dès aujourd'hui !
type: docs
weight: 70
url: /fr/net/aspose.words.loading/loadoptions/ignoreoledata/
---
## LoadOptions.IgnoreOleData property

Spécifie s'il faut ignorer les données OLE.

```csharp
public bool IgnoreOleData { get; set; }
```

## Remarques

Ignorer les données OLE peut réduire la consommation de mémoire et augmenter les performances sans perte de données dans le cas où le format de destination ne prend pas en charge les objets OLE.

La valeur par défaut est`FAUX`.

## Exemples

Montre comment ignorer les données OLE lors du chargement.

```csharp
// Ignorer les données OLE peut réduire la consommation de mémoire et augmenter les performances
// sans perte de données dans le cas où le format de destination ne prend pas en charge les objets OLE.
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Document doc = new Document(MyDir + "OLE objects.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.IgnoreOleData.docx");
```

### Voir également

* class [LoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
