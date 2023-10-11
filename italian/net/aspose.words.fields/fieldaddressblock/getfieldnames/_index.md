---
title: FieldAddressBlock.GetFieldNames
second_title: Aspose.Words per .NET API Reference
description: FieldAddressBlock metodo. Restituisce una raccolta di nomi di campi di stampa unione utilizzati dal campo.
type: docs
weight: 70
url: /it/net/aspose.words.fields/fieldaddressblock/getfieldnames/
---
## FieldAddressBlock.GetFieldNames method

Restituisce una raccolta di nomi di campi di stampa unione utilizzati dal campo.

```csharp
public string[] GetFieldNames()
```

### Esempi

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
* spazio dei nomi [Aspose.Words.Fields](../../fieldaddressblock/)
* assemblea [Aspose.Words](../../../)


