---
title: TxtLoadOptions Class
linktitle: TxtLoadOptions
articleTitle: TxtLoadOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.Loading.TxtLoadOptions sınıf. Yükleme sırasında ek seçeneklerin belirtilmesine izin verirText bir belgeyeDocument nesne C#'da.
type: docs
weight: 3730
url: /tr/net/aspose.words.loading/txtloadoptions/
---
## TxtLoadOptions class

Yükleme sırasında ek seçeneklerin belirtilmesine izin verirText bir belgeye[`Document`](../../aspose.words/document/) nesne.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Yükleme Seçeneklerini Belirtin](https://docs.aspose.com/words/net/specify-load-options/) dokümantasyon makalesi.

```csharp
public class TxtLoadOptions : LoadOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [TxtLoadOptions](txtloadoptions/)() | Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AutoNumberingDetection](../../aspose.words.loading/txtloadoptions/autonumberingdetection/) { get; set; } | Bir belge yüklenirken otomatik numaralandırma algılamasının gerçekleştirileceğini belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`doğru` . |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Gerektiğinde belgede bulunan göreli URI'leri mutlak URI'lere çözümlemek için kullanılacak dizeyi alır veya ayarlar. Olabilir`hükümsüz` veya boş dize. Varsayılan:`hükümsüz` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Meta dosyasının dönüştürülüp dönüştürülmeyeceğini alır veya ayarlar (Wmf veyaEmf ) görüntüleriPng resim formatı. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | EquationXML ile şekillerin Office Math nesnelerine dönüştürülüp dönüştürülmeyeceğini alır veya ayarlar. |
| [DetectNumberingWithWhitespaces](../../aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/) { get; set; } | Belge düz metin biçiminden içe aktarıldığında numaralı liste öğelerinin nasıl tanınacağını belirlemeye olanak tanır. Varsayılan değer:`doğru`. |
| [DocumentDirection](../../aspose.words.loading/txtloadoptions/documentdirection/) { get; set; } | Belge yönünü alır veya ayarlar. Varsayılan değer:LeftToRight . |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Belgede kodlama belirtilmemişse bir HTML, TXT veya CHM belgesini yüklemek için kullanılacak kodlamayı alır veya ayarlar. Olabilir`hükümsüz` . Varsayılan:`hükümsüz` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Belge yazı tipi ayarlarını belirlemeye izin verir. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | OLE verilerinin yoksayılıp yok sayılmayacağını belirtir. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Belge yüklenirken kullanılacak dil tercihlerini alır. |
| [LeadingSpacesOptions](../../aspose.words.loading/txtloadoptions/leadingspacesoptions/) { get; set; } | Önde gelen alan işlemenin tercih edilen seçeneğini alır veya ayarlar. Varsayılan değer:ConvertToIndent . |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Yüklenecek belgenin biçimini belirtir. Varsayılan:Auto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Belge yükleme işleminin belirli bir MS Word sürümüyle eşleşmesi gerektiğini belirtmeye olanak tanır. Varsayılan değer:Word2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Şifrelenmiş bir belgeyi açmak için parolayı alır veya ayarlar. Olabilir`hükümsüz` veya boş dize. Varsayılan:`hükümsüz` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Microsoft Word formatlarını okurken INCLUDEPICTURE alanının korunup korunmayacağını alır veya ayarlar. Varsayılan değer:`YANLIŞ` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Bir belge yüklenirken çağrılır ve yükleme ilerlemesiyle ilgili verileri kabul eder. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | HTML, MHTML'den bir belge içe aktarıldığında harici kaynakların (resimler, stil sayfaları) nasıl yükleneceğini kontrol etmeye olanak tanır. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Belgeyi okurken geçici dosyaların kullanılmasına izin verir. Varsayılan olarak bu özellik`hükümsüz` ve hiçbir geçici dosya kullanılmaz. |
| [TrailingSpacesOptions](../../aspose.words.loading/txtloadoptions/trailingspacesoptions/) { get; set; } | Sondaki boşluk işlemenin tercih edilen seçeneğini alır veya ayarlar. Varsayılan değer:Trim . |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Alanların güncellenip güncellenmeyeceğini belirtir.`kirli` özellik. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Yükleme işlemi sırasında, veri veya biçimlendirme kalitesinin kaybına neden olabilecek bir sorun algılandığında çağrılır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) |  |

### Ayrıca bakınız

* class [LoadOptions](../loadoptions/)
* ad alanı [Aspose.Words.Loading](../../aspose.words.loading/)
* toplantı [Aspose.Words](../../)
