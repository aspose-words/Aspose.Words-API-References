---
title: Field Class
linktitle: Field
articleTitle: Field
second_title: .NET için Aspose.Words
description: Microsoft Word belgelerinizi gelişmiş işlevsellik ve verimlilik için dinamik alanlarla geliştirmenin anahtarı olan Aspose.Words.Fields.Field sınıfını keşfedin.
type: docs
weight: 1920
url: /tr/net/aspose.words.fields/field/
---
## Field class

Microsoft Word belge alanını temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class Field
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir tane alır[`FieldFormat`](../fieldformat/)alanın biçimlendirmesine yazılmış erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcısı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcısını temsil eden düğümü alır.`hükümsüz` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode)() | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode_1)(*bool*) | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alanın hemen ardından bir düğüm döndürür. Alanın sonu, üst düğümünün son alt 'siyse, üst paragrafını döndürür. Alan zaten kaldırılmışsa, şunu döndürür`hükümsüz` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Alan bağlantısını kaldırma işlemini gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/#update)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |
| [Update](../../aspose.words.fields/field/update/#update_1)(*bool*) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |

## Notlar

Word belgesindeki bir alan, alan başlangıcı, alan kodu, alan ayırıcısı, alan sonucu ve alan sonu gibi birden fazla düğümden oluşan karmaşık bir yapıdır. Alanlar iç içe geçebilir, zengin içerik barındırabilir ve bir belgede birden fazla paragraf veya bölüm içerebilir.`Field` sınıf, bir alanla tek bir nesne olarak çalışmaya izin veren özellikleri ve yöntemleri sağlayan bir "cephe" nesnesidir.

The[`Start`](./start/) ,[`Separator`](./separator/) Ve[`End`](./end/) özellikler sırasıyla alanın the alan başlangıç, ayırıcı ve bitiş düğümlerine işaret eder.

Alan başlangıcı ve ayırıcı arasındaki içerik alan kodudur. alan ayırıcısı ve alan sonu arasındaki içerik alan sonucudur. Alan kodu genellikle bir veya daha fazla [`Run`](../../aspose.words/run/) talimatları belirten nesneler. İşleme uygulamasının, alan sonucunu hesaplamak için alan kodunu execute yapması beklenir.

Alan sonuçlarını hesaplama işlemine alan güncellemesi denir. Aspose.Words, Microsoft Word'ün yaptığı gibi, çoğu alan türünün field sonuçlarını güncelleyebilir. En önemlisi, Aspose.Words en karmaşık formül alanlarının bile sonuçlarını hesaplayabilir. Tek bir alanın field sonucunu hesaplamak için şunu kullanın:[`Update`](./update/) yöntem. Tüm belgedeki alanları güncellemek için kullanın[`UpdateFields`](../../aspose.words/document/updatefields/).

Alan kodunun düz metin versiyonunu kullanarak alabilirsiniz.[`GetFieldCode`](./getfieldcode/)method. Alan sonucunun düz metin sürümünü kullanarak alabilir ve ayarlayabilirsiniz.[`Result`](./result/) property. Hem alan kodu hem de alan sonucu, iç içe geçmiş alanlar, paragraflar, şekiller, tablolar gibi karmaşık içerikler içerebilir ve bu durumda daha fazla kontrole ihtiyacınız varsa doğrudan alan düğümleriyle çalışmak isteyebilirsiniz.

Örnekleri oluşturmazsınız`Field` sınıf doğrudan. Yeni bir alan oluşturmak için şunu kullanın[`InsertField`](../../aspose.words/documentbuilder/insertfield/) yöntem.

## Örnekler

Alan kodu kullanılarak bir belgeye alanın nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// InsertField yönteminin bu aşırı yüklemesi eklenen alanları otomatik olarak günceller.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
