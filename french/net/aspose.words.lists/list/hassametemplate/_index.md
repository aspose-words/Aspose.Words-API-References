---
title: List.HasSameTemplate
second_title: Référence de l'API Aspose.Words pour .NET
description: List méthode. Renvoie vrai si la liste actuelle et la liste donnée sont créées à partir du même modèle.
type: docs
weight: 120
url: /fr/net/aspose.words.lists/list/hassametemplate/
---
## List.HasSameTemplate method

Renvoie vrai si la liste actuelle et la liste donnée sont créées à partir du même modèle.

```csharp
public bool HasSameTemplate(List other)
```

### Exemples

Montre comment définir des listes avec le même ListDefId.

```csharp
Document doc = new Document(MyDir + "Different lists.docx");

Assert.True(doc.Lists[0].HasSameTemplate(doc.Lists[1]));
Assert.False(doc.Lists[1].HasSameTemplate(doc.Lists[2]));
```

### Voir également

* class [List](../)
* espace de noms [Aspose.Words.Lists](../../list/)
* Assemblée [Aspose.Words](../../../)


