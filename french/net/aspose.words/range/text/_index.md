---
title: Range.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Plage de texte pour récupérer et manipuler facilement du texte dans une plage spécifiée pour une gestion de contenu améliorée.
type: docs
weight: 60
url: /fr/net/aspose.words/range/text/
---
## Range.Text property

Obtient le texte de la plage.

```csharp
public string Text { get; }
```

## Remarques

La chaîne renvoyée inclut tous les caractères de contrôle et spéciaux comme décrit dans[`ControlChar`](../../controlchar/).

## Exemples

Montre comment obtenir le contenu textuel de tous les nœuds couverts par une plage.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### Voir également

* class [Range](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
