---
title: Field Class
linktitle: Field
articleTitle: Field
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.Field sınıf. Bir Microsoft Word belge alanını temsil eder C#'da.
type: docs
weight: 1510
url: /tr/net/aspose.words.fields/field/
---
## Field class

Bir Microsoft Word belge alanını temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Alanlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fields/) dokümantasyon makalesi.

```csharp
public class Field
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir alır[`FieldFormat`](../fieldformat/) Alanın formatlamasına yazılı erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucu yeniden hesaplanmamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. Olabilir`hükümsüz` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Alt alanların hem alan kodu hem de alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode_1)(*bool*) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alanın hemen ardından bir düğüm döndürür. Alanın sonu, üst düğümünün son child 'si ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa şunu döndürür:`hükümsüz` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Alanın bağlantısını kaldırır. |
| [Update](../../aspose.words.fields/field/update/#update)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [Update](../../aspose.words.fields/field/update/#update_1)(*bool*) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar. |

## Notlar

Bir Word belgesindeki alan, alan başlangıcı, alan kodu, alan ayırıcı, alan sonucu ve alan sonu içeren birden çok düğümden oluşan karmaşık bir yapıdır. Alanlar iç içe yerleştirilebilir, zengin içerik içerebilir ve bir belgede span birden fazla paragraf veya bölüm içerebilir.`Field` sınıf, bir alanla tek bir nesne olarak çalışmaya olanak tanıyan özelliklerini ve yöntemlerini sağlayan bir "cephe" nesnesidir.

[`Start`](./start/) ,[`Separator`](./separator/) Ve[`End`](./end/) özellikler sırasıyla the alanının başlangıç, ayırıcı ve bitiş düğümlerine işaret eder.

Alan başlangıcı ile ayırıcı arasındaki içerik alan kodudur. the alan ayırıcısı ile alan sonu arasındaki içerik, alan sonucudur. Alan kodu genellikle bir veya daha fazla öğesinden oluşur[`Run`](../../aspose.words/run/) Talimatları belirten nesneler. İşleme uygulamasının, alan sonucunu hesaplamak için alan kodunu yürütmesi bekleniyor.

Saha sonuçlarının hesaplanması işlemine saha güncellemesi denir. Aspose.Words, çoğu alan türünün field sonuçlarını Microsoft Word'ün yaptığı gibi güncelleyebilir. En önemlisi, Aspose.Words en karmaşık formül alanlarının sonuçlarını bile hesaplayabilir. Tek bir alanın field sonucunu hesaplamak için şunu kullanın:[`Update`](./update/) yöntem. Tüm document kullanımındaki alanları güncellemek için[`UpdateFields`](../../aspose.words/document/updatefields/).

Alan kodunun düz metin versiyonunu aşağıdaki komutu kullanarak alabilirsiniz:[`GetFieldCode`](./getfieldcode/) method. Alan sonucunun düz metin versiyonunu aşağıdaki komutu kullanarak alabilir ve ayarlayabilirsiniz:[`Result`](./result/) property. Hem alan kodu hem de alan sonucu, iç içe geçmiş alanlar, paragraflar, şekiller, tablolar gibi karmaşık içerik içerebilir ve bu durumda daha fazla kontrole ihtiyacınız varsa doğrudan alan düğümleriyle çalışmak isteyebilirsiniz.

Örneklerini oluşturmazsınız`Field` doğrudan sınıf. Yeni bir alan oluşturmak için şunu kullanın:[`InsertField`](../../aspose.words/documentbuilder/insertfield/) yöntem.

## Örnekler

Alan kodu kullanarak belgeye nasıl alan ekleneceğini gösterir.

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
