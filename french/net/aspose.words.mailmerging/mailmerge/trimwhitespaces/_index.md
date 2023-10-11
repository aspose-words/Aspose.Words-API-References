---
title: MailMerge.TrimWhitespaces
second_title: Référence de l'API Aspose.Words pour .NET
description: MailMerge propriété. Obtient ou définit une valeur indiquant si les espaces de fin et de début sont supprimés des valeurs de publipostage.
type: docs
weight: 130
url: /fr/net/aspose.words.mailmerging/mailmerge/trimwhitespaces/
---
## MailMerge.TrimWhitespaces property

Obtient ou définit une valeur indiquant si les espaces de fin et de début sont supprimés des valeurs de publipostage.

```csharp
public bool TrimWhitespaces { get; set; }
```

### Remarques

La valeur par défaut est`vrai` .

### Exemples

Montre comment supprimer les espaces des valeurs d’une source de données lors de l’exécution d’un publipostage.

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
* espace de noms [Aspose.Words.MailMerging](../../mailmerge/)
* Assemblée [Aspose.Words](../../../)


