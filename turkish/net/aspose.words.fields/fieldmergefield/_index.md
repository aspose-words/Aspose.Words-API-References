---
title: FieldMergeField
second_title: Aspose.Words for .NET API Referansı
description: MERGEFIELD alanını uygular.
type: docs
weight: 2000
url: /tr/net/aspose.words.fields/fieldmergefield/
---
## FieldMergeField class

MERGEFIELD alanını uygular.

```csharp
public class FieldMergeField : Field
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [FieldName](../../aspose.words.fields/fieldmergefield/fieldname/) { get; set; } | Bir veri alanının adını alır veya ayarlar. |
| [FieldNameNoPrefix](../../aspose.words.fields/fieldmergefield/fieldnamenoprefix/) { get; } | Yalnızca veri alanının adını döndürür. Herhangi bir önek, önek özelliğine çıkarılır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | [`FieldFormat`](../fieldformat/) alanın biçimlendirmesine yazılı erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [IsMapped](../../aspose.words.fields/fieldmergefield/ismapped/) { get; set; } | Bu alanın eşlenmiş bir alan olup olmadığını alır veya ayarlar. |
| [IsVerticalFormatting](../../aspose.words.fields/fieldmergefield/isverticalformatting/) { get; set; } | Dikey biçimlendirme için karakter dönüştürmenin etkinleştirilip etkinleştirilmeyeceğini alır veya ayarlar. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. null. olabilir |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| [TextAfter](../../aspose.words.fields/fieldmergefield/textafter/) { get; set; } | Alan boş değilse, alandan sonra eklenecek metni alır veya ayarlar. |
| [TextBefore](../../aspose.words.fields/fieldmergefield/textbefore/) { get; set; } | Alan boş değilse, alanın önüne eklenecek metni alır veya ayarlar. |
| override [Type](../../aspose.words.fields/fieldmergefield/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Alt alanların hem alan kodu hem de alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alandan hemen sonra bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğu ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa, döner **hükümsüz** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Bağlantıyı kaldır alanını gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar. |

### Notlar

Adres mektup birleştirme ana belgesindeki birleştirme karakterleri içindeki bir veri alanının adını alır. Ana belge seçilen veri kaynağıyla birleştirildiğinde, birleştirme alanının yerine belirtilen veri alanındaki bilgiler eklenir.

### Örnekler

Adres mektup birleştirme gerçekleştirmek için MERGEFIELD alanlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Adres mektup birleştirme veri kaynağı olarak kullanılacak bir veri tablosu oluşturun.
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

// Birleştirme gerçekleştiğinde bu alanın kabul ettiği değerden önce ve sonra metin uygulayabiliriz.
fieldMergeField.TextBefore = "Dear ";
fieldMergeField.TextAfter = " ";

Assert.AreEqual(" MERGEFIELD  \"Courtesy Title\" \\m \\b \"Dear \" \\f \" \"", fieldMergeField.GetFieldCode());

// Veri kaynağında farklı bir sütun için başka bir MERGEFIELD ekleyin.
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Last Name";
fieldMergeField.TextAfter = ":";

doc.UpdateFields();
doc.MailMerge.Execute(table);

Assert.AreEqual("Dear Mr. Doe:\u000cDear Mrs. Cardholder:", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
