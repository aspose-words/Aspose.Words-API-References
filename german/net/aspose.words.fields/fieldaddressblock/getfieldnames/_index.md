---
title: FieldAddressBlock.GetFieldNames
linktitle: GetFieldNames
articleTitle: GetFieldNames
second_title: Aspose.Words für .NET
description: FieldAddressBlock GetFieldNames methode. Gibt eine Sammlung von Serienbrieffeldnamen zurück die vom Feld verwendet werden in C#.
type: docs
weight: 70
url: /de/net/aspose.words.fields/fieldaddressblock/getfieldnames/
---
## FieldAddressBlock.GetFieldNames method

Gibt eine Sammlung von Serienbrieffeldnamen zurück, die vom Feld verwendet werden.

```csharp
public string[] GetFieldNames()
```

## Beispiele

Zeigt, wie von einem Feld verwendete Serienbrieffeldnamen abgerufen werden.

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

### Siehe auch

* class [FieldAddressBlock](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
