---
title: FieldAddressBlock.GetFieldNames
linktitle: GetFieldNames
articleTitle: GetFieldNames
second_title: Aspose.Words per .NET
description: Scopri il metodo GetFieldNames in FieldAddressBlock. Recupera facilmente i nomi dei campi di stampa unione per migliorare il processo di automazione dei documenti.
type: docs
weight: 70
url: /it/net/aspose.words.fields/fieldaddressblock/getfieldnames/
---
## FieldAddressBlock.GetFieldNames method

Restituisce una raccolta di nomi di campi di unione di posta utilizzati dal campo.

```csharp
public string[] GetFieldNames()
```

## Esempi

Mostra come ottenere i nomi dei campi di stampa unione utilizzati da un campo.

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

### Guarda anche

* class [FieldAddressBlock](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
