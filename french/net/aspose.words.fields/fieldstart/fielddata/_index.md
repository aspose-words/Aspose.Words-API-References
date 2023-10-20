---
title: FieldStart.FieldData
linktitle: FieldData
articleTitle: FieldData
second_title: Aspose.Words pour .NET
description: FieldStart FieldData propriété. Obtient les données de champ personnalisées associées au champ en C#.
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

Montre comment obtenir des données associées au champ.

```csharp
Document doc = new Document(MyDir + "Field sample - Field with data.docx");

Field field = doc.Range.Fields[2];
Console.WriteLine(Encoding.Default.GetString(field.Start.FieldData));
```

### Voir également

* class [FieldStart](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
