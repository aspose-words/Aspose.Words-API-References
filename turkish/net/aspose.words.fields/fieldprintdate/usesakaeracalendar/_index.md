---
title: FieldPrintDate.UseSakaEraCalendar
linktitle: UseSakaEraCalendar
articleTitle: UseSakaEraCalendar
second_title: Aspose.Words for .NET
description: FieldPrintDate UseSakaEraCalendar mülk. Saka Dönemi takviminin kullanılıp kullanılmayacağını alır veya ayarlar C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldprintdate/usesakaeracalendar/
---
## FieldPrintDate.UseSakaEraCalendar property

Saka Dönemi takviminin kullanılıp kullanılmayacağını alır veya ayarlar.

```csharp
public bool UseSakaEraCalendar { get; set; }
```

## Örnekler

Okunan PRINTDATE alanlarını gösterir.

```csharp
Document doc = new Document(MyDir + "Field sample - PRINTDATE.docx");

// Bir belge yazıcı tarafından yazdırıldığında veya PDF olarak yazdırıldığında (ancak PDF'ye aktarılmadığında),
// PRINTDATE alanları yazdırma işleminin tarih/saatini gösterecektir.
// Yazdırma yapılmadıysa bu alanlarda "0/0/0000" görüntülenecektir.
FieldPrintDate field = (FieldPrintDate)doc.Range.Fields[0];

Assert.AreEqual("3/25/2020 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE ", field.GetFieldCode());

// Aşağıda PRINTDATE alanının bağlı olduğu üç farklı takvim türü bulunmaktadır.
// son yazdırma işleminin tarih ve saatini görüntüleyebiliriz.
// 1 - İslami Ay Takvimi:
field = (FieldPrintDate)doc.Range.Fields[1];

Assert.True(field.UseLunarCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\h", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[2];

// 2 - Ümmü'l-Kura takvimi:
Assert.True(field.UseUmAlQuraCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\u", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[3];

// 3 - Hindistan Ulusal Takvimi:
Assert.True(field.UseSakaEraCalendar);
Assert.AreEqual("1/5/1942 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\s", field.GetFieldCode());
```

### Ayrıca bakınız

* class [FieldPrintDate](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
