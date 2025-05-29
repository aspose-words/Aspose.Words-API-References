---
title: FieldAddressBlock.GetFieldNames
linktitle: GetFieldNames
articleTitle: GetFieldNames
second_title: Aspose.Words för .NET
description: Upptäck GetFieldNames-metoden i FieldAddressBlock. Hämta enkelt fältnamn för kopplingar för att förbättra din dokumentautomatiseringsprocess.
type: docs
weight: 70
url: /sv/net/aspose.words.fields/fieldaddressblock/getfieldnames/
---
## FieldAddressBlock.GetFieldNames method

Returnerar en samling namn på fält för kopplingsmeddelanden som används av fältet.

```csharp
public string[] GetFieldNames()
```

## Exempel

Visar hur man hämtar fältnamn för dokumentkoppling som används av ett fält.

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

### Se även

* class [FieldAddressBlock](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
