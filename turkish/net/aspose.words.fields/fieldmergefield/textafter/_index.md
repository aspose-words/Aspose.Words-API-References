---
title: FieldMergeField.TextAfter
linktitle: TextAfter
articleTitle: TextAfter
second_title: Aspose.Words for .NET
description: FieldMergeField TextAfter mülk. Alan boş değilse alandan sonra eklenecek metni alır veya ayarlar C#'da.
type: docs
weight: 50
url: /tr/net/aspose.words.fields/fieldmergefield/textafter/
---
## FieldMergeField.TextAfter property

Alan boş değilse alandan sonra eklenecek metni alır veya ayarlar.

```csharp
public string TextAfter { get; set; }
```

## Örnekler

Adres-mektup birleştirme gerçekleştirmek için MERGEFIELD alanlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Adres-mektup birleştirme veri kaynağı olarak kullanılacak bir veri tablosu oluşturun.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Veri kaynağındaki bir sütunun adına ayarlanmış FieldName özelliğine sahip bir MERGEFIELD ekleyin.
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Courtesy Title";
fieldMergeField.IsMapped = true;
fieldMergeField.IsVerticalFormatting = false;

// Birleştirme gerçekleştiğinde bu alanın kabul ettiği değerin önüne ve arkasına metin uygulayabiliriz.
fieldMergeField.TextBefore = "Dear ";
fieldMergeField.TextAfter = " ";

Assert.AreEqual(" MERGEFIELD  \"Courtesy Title\" \\m \\b \"Dear \" \\f \" \"", fieldMergeField.GetFieldCode());

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
