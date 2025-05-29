---
title: FieldGreetingLine Class
linktitle: FieldGreetingLine
articleTitle: FieldGreetingLine
second_title: .NET için Aspose.Words
description: Gelişmiş belge kişiselleştirmesi için GREETINGLINE alanlarını zahmetsizce uygulamak üzere tasarlanmış Aspose.Words.Fields.FieldGreetingLine sınıfını keşfedin.
type: docs
weight: 2390
url: /tr/net/aspose.words.fields/fieldgreetingline/
---
## FieldGreetingLine class

GREETINGLINE alanını uygular.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class FieldGreetingLine : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldGreetingLine](fieldgreetingline/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AlternateText](../../aspose.words.fields/fieldgreetingline/alternatetext/) { get; set; } | Ad boşsa alana eklenecek metni alır veya ayarlar. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir tane alır[`FieldFormat`](../fieldformat/)alanın biçimlendirmesine yazılmış erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LanguageId](../../aspose.words.fields/fieldgreetingline/languageid/) { get; set; } | Adı biçimlendirmek için kullanılan dil kimliğini alır veya ayarlar. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [NameFormat](../../aspose.words.fields/fieldgreetingline/nameformat/) { get; set; } | Alana dahil edilen adın biçimini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcısı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcısını temsil eden düğümü alır.`hükümsüz` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [GetFieldNames](../../aspose.words.fields/fieldgreetingline/getfieldnames/)() | Alan tarafından kullanılan bir posta birleştirme alanı adları koleksiyonunu döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alanın hemen ardından bir düğüm döndürür. Alanın sonu, üst düğümünün son alt 'siyse, üst paragrafını döndürür. Alan zaten kaldırılmışsa, şunu döndürür`hükümsüz` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Alan bağlantısını kaldırma işlemini gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |

## Notlar

Bir posta birleştirme selamlama satırı ekler.

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

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
