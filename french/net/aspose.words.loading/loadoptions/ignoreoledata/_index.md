---
title: LoadOptions.IgnoreOleData
second_title: Référence de l'API Aspose.Words pour .NET
description: LoadOptions propriété. Spécifie sil faut ignorer les données OLE.
type: docs
weight: 70
url: /fr/net/aspose.words.loading/loadoptions/ignoreoledata/
---
## LoadOptions.IgnoreOleData property

Spécifie s'il faut ignorer les données OLE.

```csharp
public bool IgnoreOleData { get; set; }
```

### Remarques

Ignorer les données OLE peut réduire la consommation de mémoire et augmenter les performances sans perte de données dans le cas où le format de destination ne prend pas en charge les objets OLE.

La valeur par défaut est`FAUX`.

### Exemples

Montre comment intégrer des données OLE lors du chargement.

```csharp
// Ignorer les données OLE peut réduire la consommation de mémoire et augmenter les performances
// sans perte de données dans le cas où le format de destination ne prend pas en charge les objets OLE.
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Document doc = new Document(MyDir + "OLE objects.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.IgnoreOleData.docx");
```

### Voir également

* class [LoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../loadoptions/)
* Assemblée [Aspose.Words](../../../)


