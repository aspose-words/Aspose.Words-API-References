---
title: FieldStart.FieldData
linktitle: FieldData
articleTitle: FieldData
second_title: Aspose.Words pour .NET
description: Déverrouillez les données de champ personnalisées avec la propriété FieldData de FieldStart, améliorant ainsi votre gestion des données et augmentant votre productivité sans effort.
type: docs
weight: 10
url: /fr/net/aspose.words.fields/fieldstart/fielddata/
---
## FieldStart.FieldData property

Obtient les données de champ personnalisées associées au champ.

```csharp
public byte[] FieldData { get; }
```

## Exemples

Montre comment obtenir les données associées au champ.

```csharp
Document doc = new Document(MyDir + "Field sample - Field with data.docx");

Field field = doc.Range.Fields[2];
Console.WriteLine(Encoding.UTF8.GetString(field.Start.FieldData));
```

### Voir également

* class [FieldStart](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
