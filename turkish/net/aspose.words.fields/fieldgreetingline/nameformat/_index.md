---
title: FieldGreetingLine.NameFormat
linktitle: NameFormat
articleTitle: NameFormat
second_title: .NET için Aspose.Words
description: Alanlarınızdaki ad biçimlerini kolayca özelleştirmek, kullanıcı deneyimini ve kişiselleştirmeyi geliştirmek için FieldGreetingLine NameFormat özelliğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.fields/fieldgreetingline/nameformat/
---
## FieldGreetingLine.NameFormat property

Alana dahil edilen adın biçimini alır veya ayarlar.

```csharp
public string NameFormat { get; set; }
```

## Örnekler

GEETINGLINE alanının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// GREETINGLINE alanını ve ardından biraz metin kullanarak genel bir selamlama oluşturun.
FieldGreetingLine field = (FieldGreetingLine)builder.InsertField(FieldType.FieldGreetingLine, true);
builder.Writeln("\n\n\tThis is your custom greeting, created programmatically using Aspose Words!");

// GREETINGLINE alanı, bir posta birleştirme sırasında MERGEFIELD gibi bir veri kaynağından gelen değerleri kabul eder.
// Ayrıca, birleştirme işlemi tamamlandıktan sonra kaynak verilerinin yerine nasıl yazılacağını biçimlendirebilir.
// Alan adları koleksiyonu, veri kaynağındaki sütunlara karşılık gelir
// alanın değerlerini alacağı yer.
Assert.AreEqual(0, field.GetFieldNames().Length);

// Bu diziyi doldurmak için selamlama satırımız için bir format belirtmemiz gerekiyor.
field.NameFormat = "<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> ";

// Artık alanımız veri kaynağındaki bu iki sütundan gelen değerleri kabul edecek.
Assert.AreEqual("Courtesy Title", field.GetFieldNames()[0]);
Assert.AreEqual("Last Name", field.GetFieldNames()[1]);
Assert.AreEqual(2, field.GetFieldNames().Length);

// Bu dize, veri tablosu verilerinin geçersiz olduğu tüm durumları kapsayacaktır
// hatalı ismi bir string ile değiştirerek.
field.AlternateText = "Sir or Madam";

// Sonucu biçimlendirmek için bir yerel ayar belirleyin.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(" GREETINGLINE  \\f \"<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> \" \\e \"Sir or Madam\" \\l 1033", 
    field.GetFieldCode());

// Adları öğelerle eşleşen sütunlardan oluşan bir veri tablosu oluşturun
// alanın alan adları koleksiyonundan alın ve ardından posta birleştirme işlemini gerçekleştirin.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Bu satırın Nezaket Başlığı sütununda geçersiz bir değer var, bu nedenle selamlamamız varsayılan olarak alternatif metne ayarlanacaktır.
table.Rows.Add("", "No", "Name");

doc.MailMerge.Execute(table);

Assert.AreEqual(0, doc.Range.Fields.Count);
Assert.AreEqual("Dear Mr. Doe,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Mrs. Cardholder,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Sir or Madam,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!",
    doc.GetText().Trim());
```

### Ayrıca bakınız

* class [FieldGreetingLine](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
