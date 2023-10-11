---
title: Range.Text
second_title: Référence de l'API Aspose.Words pour .NET
description: Range propriété. Récupère le texte de la plage.
type: docs
weight: 60
url: /fr/net/aspose.words/range/text/
---
## Range.Text property

Récupère le texte de la plage.

```csharp
public string Text { get; }
```

### Remarques

La chaîne renvoyée inclut tous les caractères de contrôle et spéciaux comme décrit dans[`ControlChar`](../../controlchar/).

### Exemples

Montre comment obtenir le contenu textuel de tous les nœuds couverts par une plage.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### Voir également

* class [Range](../)
* espace de noms [Aspose.Words](../../range/)
* Assemblée [Aspose.Words](../../../)


