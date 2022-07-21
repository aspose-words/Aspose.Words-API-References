---
title: FieldHyperlink
second_title: Aspose.Words for .NET API Referansı
description: HYPERLINK alanını uygular
type: docs
weight: 1840
url: /tr/net/aspose.words.fields/fieldhyperlink/
---
## FieldHyperlink class

HYPERLINK alanını uygular

```csharp
public class FieldHyperlink : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldHyperlink](fieldhyperlink)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Address](../../aspose.words.fields/fieldhyperlink/address) { get; set; } | Bu köprünün atladığı bir konumu alır veya ayarlar. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format) { get; } | [`FieldFormat`](../fieldformat) alanın biçimlendirmesine yazılı erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsImageMap](../../aspose.words.fields/fieldhyperlink/isimagemap) { get; set; } | Sunucu tarafı görüntü haritası için köprüye koordinatların eklenip eklenmeyeceğini alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [OpenInNewWindow](../../aspose.words.fields/fieldhyperlink/openinnewwindow) { get; set; } | Hedef sitenin yeni bir web tarayıcı penceresinde açılıp açılmayacağını belirler. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [ScreenTip](../../aspose.words.fields/fieldhyperlink/screentip) { get; set; } | Köprü için Ekran İpucu metnini alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Alan ayırıcıyı temsil eden düğümü alır. null. olabilir |
| [Start](../../aspose.words.fields/field/start) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| [SubAddress](../../aspose.words.fields/fieldhyperlink/subaddress) { get; set; } | Dosyada, bu köprünün atladığı yer işareti gibi bir konumu alır veya ayarlar. |
| [Target](../../aspose.words.fields/fieldhyperlink/target) { get; set; } | Bağlantının yönlendirileceği hedefi alır veya ayarlar. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Alt alanların hem alan kodu hem de alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove)() | Alanı belgeden kaldırır. Alandan hemen sonra bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğu ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa, döner **hükümsüz** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Bağlantıyı kaldır alanını gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [Update](../../aspose.words.fields/field/update)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar. |

### Notlar

Seçildiğinde, kontrolün yer işareti veya URL gibi bir konuma atlamasına neden olur.

### Örnekler

Yerel dosya sistemindeki belgelere bağlanmak için KÖPRÜ alanlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldHyperlink field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);

// Microsoft Word'de bu KÖPRÜ alanına tıkladığımızda,
// bağlantılı belgeyi açacak ve ardından imleci belirtilen yer işaretine yerleştirecek.
field.Address = MyDir + "Bookmarks.docx";
field.SubAddress = "MyBookmark3";
field.ScreenTip = "Open " + field.Address + " on bookmark " + field.SubAddress + " in a new window";

builder.Writeln();

// Microsoft Word'de bu KÖPRÜ alanına tıkladığımızda,
// bağlantılı belgeyi açacak ve otomatik olarak belirtilen iframe'e inecek.
field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);
field.Address = MyDir + "Iframes.html";
field.ScreenTip = "Open " + field.Address;
field.Target = "iframe_3";
field.OpenInNewWindow = true;
field.IsImageMap = false;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.HYPERLINK.docx");
```

### Ayrıca bakınız

* class [Field](../field)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
