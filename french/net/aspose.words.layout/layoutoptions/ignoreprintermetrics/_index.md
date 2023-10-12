---
title: LayoutOptions.IgnorePrinterMetrics
second_title: Référence de l'API Aspose.Words pour .NET
description: LayoutOptions propriété. Obtient ou définit une indication indiquant si loption de compatibilité  Utiliser les métriques de limprimante pour mettre en page le document  est ignorée. La valeur par défaut estvrai .
type: docs
weight: 50
url: /fr/net/aspose.words.layout/layoutoptions/ignoreprintermetrics/
---
## LayoutOptions.IgnorePrinterMetrics property

Obtient ou définit une indication indiquant si l'option de compatibilité « Utiliser les métriques de l'imprimante pour mettre en page le document » est ignorée. La valeur par défaut est`vrai` .

```csharp
public bool IgnorePrinterMetrics { get; set; }
```

### Exemples

Montre comment ignorer l'option « Utiliser les métriques de l'imprimante pour mettre en page le document ».

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

doc.LayoutOptions.IgnorePrinterMetrics = false;

doc.Save(ArtifactsDir + "Document.IgnorePrinterMetrics.docx");
```

### Voir également

* class [LayoutOptions](../)
* espace de noms [Aspose.Words.Layout](../../layoutoptions/)
* Assemblée [Aspose.Words](../../../)


