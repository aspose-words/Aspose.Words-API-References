---
title: FieldMergeField.IsMapped
linktitle: IsMapped
articleTitle: IsMapped
second_title: .NET için Aspose.Words
description: Eşlenen alanları kolayca yönetmek, veri bütünleştirmenizi ve iş akışı verimliliğinizi artırmak için FieldMergeField IsMapped özelliğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldmergefield/ismapped/
---
## FieldMergeField.IsMapped property

Bu alanın eşlenmiş bir alan olup olmadığını alır veya ayarlar.

```csharp
public bool IsMapped { get; set; }
```

## Örnekler

MERGEFIELD alanlarının bir posta birleştirme işlemini gerçekleştirmek için nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Posta birleştirme veri kaynağı olarak kullanılacak bir veri tablosu oluşturun.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Veri kaynağındaki bir sütunun adına ayarlanmış bir FieldName özelliğine sahip bir MERGEFIELD ekleyin.
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Courtesy Title";
fieldMergeField.IsMapped = true;
fieldMergeField.IsVerticalFormatting = false;

// Birleştirme gerçekleştiğinde bu alanın kabul edeceği değerin önüne ve arkasına metin uygulayabiliriz.
fieldMergeField.TextBefore = "Dear ";
fieldMergeField.TextAfter = " ";

Assert.AreEqual(" MERGEFIELD  \"Courtesy Title\" \\m \\b \"Dear \" \\f \" \"", fieldMergeField.GetFieldCode());
Assert.AreEqual(FieldType.FieldMergeField, fieldMergeField.Type);

// Veri kaynağındaki farklı bir sütun için başka bir MERGEFIELD ekleyin.
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Last Name";
fieldMergeField.TextAfter = ":";

doc.UpdateFields();
doc.MailMerge.Execute(table);

Assert.AreEqual("Dear Mr. Doe:\u000cDear Mrs. Cardholder:", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [FieldMergeField](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
