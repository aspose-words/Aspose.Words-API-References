---
title: FieldGreetingLine.AlternateText
second_title: Aspose.Words for .NET API Referansı
description: FieldGreetingLine mülk. Adın boş olması durumunda alana eklenecek metni alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldgreetingline/alternatetext/
---
## FieldGreetingLine.AlternateText property

Adın boş olması durumunda alana eklenecek metni alır veya ayarlar.

```csharp
public string AlternateText { get; set; }
```

### Örnekler

GREETINGLINE alanının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// GREETINGLINE alanını ve ardından bir miktar metni kullanarak genel bir karşılama oluşturun.
FieldGreetingLine field = (FieldGreetingLine)builder.InsertField(FieldType.FieldGreetingLine, true);
builder.Writeln("\n\n\tThis is your custom greeting, created programmatically using Aspose Words!");

// GREETINGLINE alanı, adres-mektup birleştirme sırasında MERGEFIELD gibi bir veri kaynağından gelen değerleri kabul eder.
// Adres-mektup birleştirme tamamlandıktan sonra kaynağın verilerinin yerine nasıl yazılacağını da biçimlendirebilir.
// Alan adları koleksiyonu, veri kaynağındaki sütunlara karşılık gelir
// alanın değerleri alacağı yer.
Assert.AreEqual(0, field.GetFieldNames().Length);

// Bu diziyi doldurmak için selamlama satırımıza bir format belirtmemiz gerekiyor.
field.NameFormat = "<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> ";

// Artık alanımız veri kaynağındaki bu iki sütundan değerleri kabul edecek.
Assert.AreEqual("Courtesy Title", field.GetFieldNames()[0]);
Assert.AreEqual("Last Name", field.GetFieldNames()[1]);
Assert.AreEqual(2, field.GetFieldNames().Length);

// Bu dize, veri tablosu verilerinin geçersiz olduğu tüm durumları kapsayacaktır
// hatalı biçimlendirilmiş adı bir dizeyle değiştirerek.
field.AlternateText = "Sir or Madam";

// Sonucu biçimlendirmek için bir yerel ayar belirleyin.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(" GREETINGLINE  \\f \"<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> \" \\e \"Sir or Madam\" \\l 1033", 
    field.GetFieldCode());

// Adları öğelerle eşleşen sütunlarla bir veri tablosu oluşturun
// alanın alan adları koleksiyonundan alın ve ardından adres-mektup birleştirmeyi gerçekleştirin.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Bu satırın Nezaket Başlığı sütununda geçersiz bir değeri var, dolayısıyla selamlamamız varsayılan olarak alternatif metni kullanacak.
table.Rows.Add("", "No", "Name");

doc.MailMerge.Execute(table);

Assert.That(doc.Range.Fields, Is.Empty);
Assert.AreEqual("Dear Mr. Doe,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Mrs. Cardholder,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Sir or Madam,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!",
    doc.GetText().Trim());
```

### Ayrıca bakınız

* class [FieldGreetingLine](../)
* ad alanı [Aspose.Words.Fields](../../fieldgreetingline/)
* toplantı [Aspose.Words](../../../)


