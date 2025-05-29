---
title: List.HasSameTemplate
linktitle: HasSameTemplate
articleTitle: HasSameTemplate
second_title: Aspose.Words pour .NET
description: Découvrez la méthode HasSameTemplate, vérifiez facilement si deux listes partagent le même modèle, garantissant cohérence et efficacité dans votre gestion des données.
type: docs
weight: 120
url: /fr/net/aspose.words.lists/list/hassametemplate/
---
## List.HasSameTemplate method

Renvoie vrai si la liste actuelle et la liste donnée sont créées à partir du même modèle.

```csharp
public bool HasSameTemplate(List other)
```

## Exemples

Montre comment définir des listes avec le même ListDefId.

```csharp
Document doc = new Document(MyDir + "Different lists.docx");

Assert.True(doc.Lists[0].HasSameTemplate(doc.Lists[1]));
Assert.False(doc.Lists[1].HasSameTemplate(doc.Lists[2]));
```

### Voir également

* class [List](../)
* espace de noms [Aspose.Words.Lists](../../../aspose.words.lists/)
* Assemblée [Aspose.Words](../../../)
