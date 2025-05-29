---
title: RtfLoadOptions Class
linktitle: RtfLoadOptions
articleTitle: RtfLoadOptions
second_title: .NET için Aspose.Words
description: Projelerinize kusursuz entegrasyon için özelleştirilebilir ayarlarla RTF belge yüklemesini geliştirmek üzere Aspose.Words.RtfLoadOptions'ı keşfedin.
type: docs
weight: 4170
url: /tr/net/aspose.words.loading/rtfloadoptions/
---
## RtfLoadOptions class

Yükleme sırasında ek seçeneklerin belirlenmesine olanak tanırRtf belgeye dönüştürmek[`Document`](../../aspose.words/document/) nesne.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yükleme Seçeneklerini Belirleyin](https://docs.aspose.com/words/net/specify-load-options/) belgeleme makalesi.

```csharp
public class RtfLoadOptions : LoadOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [RtfLoadOptions](rtfloadoptions/)() | Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Gerektiğinde belgede bulunan bağıl URI'leri mutlak URI'lere dönüştürmek için kullanılacak dizeyi alır veya ayarlar. `hükümsüz` veya boş dize. Varsayılan`hükümsüz` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Meta dosyasının dönüştürülüp dönüştürülmeyeceğini alır veya ayarlarWmf veyaEmf ) görüntüleriPnggörüntü biçimi. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Şekillerin EquationXML ile Office Math nesnelerine dönüştürülüp dönüştürülmeyeceğini alır veya ayarlar. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Kodlama belirtilmemişse HTML, TXT veya CHM belgesini yüklemek için kullanılacak kodlamayı alır veya ayarlar belgenin içinde. Şu şekilde olabilir:`hükümsüz` Varsayılan değer:`hükümsüz` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Belge yazı tipi ayarlarının belirlenmesine olanak tanır. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | OLE verilerinin yoksayılıp yoksayılmayacağını belirtir. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Belge yüklenirken kullanılacak dil tercihlerini alır. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Yüklenecek belgenin biçimini belirtir. VarsayılanAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Belge yükleme işleminin belirli bir MS Word sürümüyle eşleşmesi gerektiğini belirtmenize olanak tanır. Varsayılan değerWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Şifrelenmiş bir belgeyi açmak için parolayı alır veya ayarlar. Şu şekilde olabilir:`hükümsüz` veya boş dize. Varsayılan`hükümsüz` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Microsoft Word biçimlerini okurken INCLUDEPICTURE alanının korunup korunmayacağını alır veya ayarlar. Varsayılan değer`YANLIŞ` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Bir belge yüklenirken çağrılır ve yükleme ilerlemesiyle ilgili verileri kabul eder. |
| [RecognizeUtf8Text](../../aspose.words.loading/rtfloadoptions/recognizeutf8text/) { get; set; } | Ayarlandığında`doğru` , UTF8 karakterlerini algılamaya çalışacak, bunlar içe aktarma sırasında korunacaktır. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Bir belge HTML veya MHTML'den içe aktarıldığında harici kaynakların (resimler, stil sayfaları) nasıl yükleneceğini kontrol etmenizi sağlar. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Belgeyi okurken geçici dosyaların kullanılmasına izin verir. Varsayılan olarak bu özellik`hükümsüz` ve geçici dosyalar kullanılmaz. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Alanların güncellenip güncellenmeyeceğini belirtir`kirli` öznitelik. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | Sayfa düzeni varsayılan kenar boşluklarını belirlemek için Windows kayıt defterinden alınan LCID değerinin kullanılıp kullanılmayacağını alır veya ayarlar. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Veri veya biçimlendirme sadakat kaybına yol açabilecek bir sorun algılandığında, yükleme işlemi sırasında çağrılır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | Belirtilen nesnenin geçerli nesneye eşit değerde olup olmadığını belirler. |

## Örnekler

Bir RTF belgesi yüklenirken UTF-8 karakterlerinin nasıl algılanacağını gösterir.

```csharp
// Bir RTF belgesini nasıl yükleyeceğimizi değiştirmek için bir "RtfLoadOptions" nesnesi oluşturun.
RtfLoadOptions loadOptions = new RtfLoadOptions();

// Belgenin ISO 8859-1 karakter setini kullandığını varsaymak için "RecognizeUtf8Text" özelliğini "false" olarak ayarlayın
// ve belgedeki her karakteri yükler.
// Metinde bulunabilecek değişken uzunluktaki karakterleri ayrıştırmak için "RecognizeUtf8Text" özelliğini "true" olarak ayarlayın.
loadOptions.RecognizeUtf8Text = recognizeUtf8Text;

Document doc = new Document(MyDir + "UTF-8 characters.rtf", loadOptions);

Assert.AreEqual(
    recognizeUtf8Text
        ? "“John Doe´s list of currency symbols”™\r" +
          "€, ¢, £, ¥, ¤"
        : "â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r" +
          "â‚¬, Â¢, Â£, Â¥, Â¤",
    doc.FirstSection.Body.GetText().Trim());
```

### Ayrıca bakınız

* class [LoadOptions](../loadoptions/)
* ad alanı [Aspose.Words.Loading](../../aspose.words.loading/)
* toplantı [Aspose.Words](../../)
