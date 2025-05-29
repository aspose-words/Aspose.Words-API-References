---
title: FieldPrintDate.UseLunarCalendar
linktitle: UseLunarCalendar
articleTitle: UseLunarCalendar
second_title: .NET için Aspose.Words
description: FieldPrintDate UseLunarCalendar özelliğiyle tarihleri zahmetsizce yönetin. Sorunsuz entegrasyon için Hicri ve İbrani Ay takvimleri arasında kolayca geçiş yapın.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldprintdate/uselunarcalendar/
---
## FieldPrintDate.UseLunarCalendar property

Hicri Ay takviminin mi yoksa İbrani Ay takviminin mi kullanılacağını alır veya ayarlar.

```csharp
public bool UseLunarCalendar { get; set; }
```

## Örnekler

Okunan PRINTDATE alanlarını gösterir.

```csharp
Document doc = new Document(MyDir + "Field sample - PRINTDATE.docx");

// Bir belge bir yazıcı tarafından yazdırıldığında veya PDF olarak yazdırıldığında (ancak PDF'ye aktarılmadığında),
// PRINTDATE alanları yazdırma işleminin tarih/saatini gösterecektir.
// Eğer herhangi bir yazdırma işlemi yapılmamışsa bu alanlarda "0/0/0000" gösterilecektir.
FieldPrintDate field = (FieldPrintDate)doc.Range.Fields[0];

Assert.AreEqual("3/25/2020 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE ", field.GetFieldCode());

// Aşağıda PRINTDATE alanının kullanıldığı üç farklı takvim türü bulunmaktadır
// Son yazdırma işleminin tarih ve saatini görüntüleyebilir.
// 1 - Hicri Takvim:
field = (FieldPrintDate)doc.Range.Fields[1];

Assert.True(field.UseLunarCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\h", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[2];

// 2 - Ümmü'l-Kurâ takvimi:
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
