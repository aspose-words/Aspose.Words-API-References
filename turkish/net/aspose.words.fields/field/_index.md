---
title: Class Field
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fields.Field sınıf. Bir Microsoft Word belge alanını temsil eder.
type: docs
weight: 1360
url: /tr/net/aspose.words.fields/field/
---
## Field class

Bir Microsoft Word belge alanını temsil eder.

```csharp
public class Field
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | [`FieldFormat`](../fieldformat/) alanın biçimlendirmesine yazılı erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. null. olabilir |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Alt alanların hem alan kodu hem de alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode_1)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alandan hemen sonra bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğu ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa, döner **hükümsüz** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Bağlantıyı kaldır alanını gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/#update)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [Update](../../aspose.words.fields/field/update/#update_1)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar. |

### Notlar

Word belgesindeki bir alan, alan başlangıcı, alan kodu, alan ayırıcı, alan sonucu ve alan sonunu içeren birden çok düğümden oluşan karmaşık bir yapıdır. Alanlar iç içe yerleştirilebilir, zengin içerik ve bir belgede span birden çok paragraf veya bölüm içerebilir. bu`Field`class, bir alanla tek bir nesne olarak çalışmaya izin veren özelliklerini ve yöntemlerini sağlayan bir "cephe" nesnesidir.

bu[`Start`](./start/) ,[`Separator`](./separator/) ve[`End`](./end/) özellikler sırasıyla alanın the alanı başlangıç, ayırıcı ve bitiş düğümlerine işaret eder.

Alan başlangıcı ile ayırıcı arasındaki içerik alan kodudur. the alan ayırıcısı ile alan sonu arasındaki içerik, alan sonucudur. Alan kodu tipik olarak bir veya daha fazla 'den oluşur[`Run`](../../aspose.words/run/) yönergeleri belirten nesneler. İşleme uygulamasının, alan sonucunu hesaplamak için alan kodunu yürütmesi beklenir.

Alan sonuçlarını hesaplama işlemine alan güncelleme adı verilir. Aspose.Words, alan türlerinin çoğunun field sonuçlarını Microsoft Word'ün yaptığı gibi tam olarak güncelleyebilir. En önemlisi, Aspose.Words en karmaşık formül alanlarının bile sonuçlarını hesaplayabilir. Tek bir alanın field sonucunu hesaplamak için[`Update`](./update/) yöntem. Tüm belgedeki alanları güncellemek için kullanın[`UpdateFields`](../../aspose.words/document/updatefields/).

Alan kodunun düz metin sürümünü aşağıdakileri kullanarak alabilirsiniz:[`GetFieldCode`](./getfieldcode/) method. Alan sonucunun düz metin versiyonunu aşağıdaki komutu kullanarak alabilir ve ayarlayabilirsiniz.[`Result`](./result/) property. Hem alan kodu hem de alan sonucu, iç içe alanlar, paragraflar, şekiller, tablolar gibi karmaşık içerik içerebilir ve bu durumda, daha fazla kontrole ihtiyacınız varsa, doğrudan alan düğümleriyle çalışmak isteyebilirsiniz.

Örneklerini oluşturmazsınız`Field` doğrudan sınıf. Yeni bir alan oluşturmak için[`InsertField`](../../aspose.words/documentbuilder/insertfield/) yöntem.

### Örnekler

Alan kodu kullanarak bir belgeye nasıl alan ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// InsertField yönteminin bu aşırı yüklemesi, eklenen alanları otomatik olarak günceller.
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)


