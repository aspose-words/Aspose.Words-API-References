---
title: FieldAddressBlock.GetFieldNames
linktitle: GetFieldNames
articleTitle: GetFieldNames
second_title: Aspose.Words pour .NET
description: FieldAddressBlock GetFieldNames méthode. Renvoie une collection de noms de champs de publipostage utilisés par le champ en C#.
type: docs
weight: 70
url: /fr/net/aspose.words.fields/fieldaddressblock/getfieldnames/
---
## FieldAddressBlock.GetFieldNames method

Renvoie une collection de noms de champs de publipostage utilisés par le champ.

```csharp
public string[] GetFieldNames()
```

## Exemples

Montre comment obtenir les noms de champs de publipostage utilisés par un champ.

```csharp
Document doc = new Document(MyDir + "Field sample - ADDRESSBLOCK.docx");

string[] addressFieldsExpect =
{
    "Company", "First Name", "Middle Name", "Last Name", "Suffix", "Address 1", "City", "State",
    "Country or Region", "Postal Code"
};

FieldAddressBlock addressBlockField = (FieldAddressBlock) doc.Range.Fields[0];
string[] addressBlockFieldNames = addressBlockField.GetFieldNames();
```

### Voir également

* class [FieldAddressBlock](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
