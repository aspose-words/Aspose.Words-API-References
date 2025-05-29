---
title: MailMerge.TrimWhitespaces
linktitle: TrimWhitespaces
articleTitle: TrimWhitespaces
second_title: Aspose.Words pour .NET
description: Optimisez votre processus de publipostage avec la propriété TrimWhitespaces, garantissant des données propres en supprimant les espaces de début et de fin pour des résultats précis.
type: docs
weight: 130
url: /fr/net/aspose.words.mailmerging/mailmerge/trimwhitespaces/
---
## MailMerge.TrimWhitespaces property

Obtient ou définit une valeur indiquant si les espaces de fin et de début sont supprimés des valeurs de publipostage.

```csharp
public bool TrimWhitespaces { get; set; }
```

## Remarques

La valeur par défaut est`vrai` .

## Exemples

Montre comment supprimer les espaces blancs des valeurs d'une source de données lors de l'exécution d'un publipostage.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField("MERGEFIELD myMergeField", null);

doc.MailMerge.TrimWhitespaces = trimWhitespaces;
doc.MailMerge.Execute(new[] { "myMergeField" }, new object[] { "\t hello world! " });

Assert.AreEqual(trimWhitespaces ? "hello world!\f" : "\t hello world! \f", doc.GetText());
```

### Voir également

* class [MailMerge](../)
* espace de noms [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../../)
