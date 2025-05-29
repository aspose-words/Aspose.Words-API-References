---
title: FieldAddressBlock.GetFieldNames
linktitle: GetFieldNames
articleTitle: GetFieldNames
second_title: .NET için Aspose.Words
description: FieldAddressBlock'taki GetFieldNames yöntemini keşfedin. Belge otomasyon sürecinizi geliştirmek için posta birleştirme alan adlarını zahmetsizce alın.
type: docs
weight: 70
url: /tr/net/aspose.words.fields/fieldaddressblock/getfieldnames/
---
## FieldAddressBlock.GetFieldNames method

Alan tarafından kullanılan bir posta birleştirme alanı adları koleksiyonunu döndürür.

```csharp
public string[] GetFieldNames()
```

## Örnekler

Bir alan tarafından kullanılan birleştirme alan adlarının nasıl alınacağını gösterir.

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

### Ayrıca bakınız

* class [FieldAddressBlock](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
