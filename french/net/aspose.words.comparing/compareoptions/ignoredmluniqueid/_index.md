---
title: CompareOptions.IgnoreDmlUniqueId
linktitle: IgnoreDmlUniqueId
articleTitle: IgnoreDmlUniqueId
second_title: Aspose.Words pour .NET
description: CompareOptions IgnoreDmlUniqueId propriété. Spécifie sil faut ignorer la différence dans lID unique de DrawingML. La valeur par défaut estFAUX  en C#.
type: docs
weight: 60
url: /fr/net/aspose.words.comparing/compareoptions/ignoredmluniqueid/
---
## CompareOptions.IgnoreDmlUniqueId property

Spécifie s'il faut ignorer la différence dans l'ID unique de DrawingML. La valeur par défaut est`FAUX` .

```csharp
public bool IgnoreDmlUniqueId { get; set; }
```

## Exemples

Montre comment comparer des documents en ignorant l'ID unique DML.

```csharp
Document docA = new Document(MyDir + "DML unique ID original.docx");
Document docB = new Document(MyDir + "DML unique ID compare.docx");

// Par défaut, Aspose.Words n'ignore pas l'ID unique de DML et le nombre de révisions était de 2.
// Si nous ignorons l'ID unique de DML et que le nombre de révisions était de 0.
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.IgnoreDmlUniqueId = isIgnoreDmlUniqueId;

docA.Compare(docB, "Aspose.Words", DateTime.Now, compareOptions);

Assert.AreEqual(isIgnoreDmlUniqueId ? 0 : 2, docA.Revisions.Count);
```

### Voir également

* class [CompareOptions](../)
* espace de noms [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* Assemblée [Aspose.Words](../../../)
