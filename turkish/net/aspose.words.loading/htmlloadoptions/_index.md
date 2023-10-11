---
title: Class HtmlLoadOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Loading.HtmlLoadOptions sınıf. HTML belgesini bir dosyaya yüklerken ek seçenekleri belirtmenize olanak tanır.Document nesne.
type: docs
weight: 3620
url: /tr/net/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class

HTML belgesini bir dosyaya yüklerken ek seçenekleri belirtmenize olanak tanır.[`Document`](../../aspose.words/document/) nesne.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Yükleme Seçeneklerini Belirtin](https://docs.aspose.com/words/net/specify-load-options/) dokümantasyon makalesi.

```csharp
public class HtmlLoadOptions : LoadOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [HtmlLoadOptions](htmlloadoptions/#constructor)() | Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_2)(string) | Şifrelenmiş bir belgeyi yüklemek için bu sınıfın yeni bir örneğini belirtilen parolayla başlatmak için kullanılan bir kısayol. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_1)(LoadFormat, string, string) | Özellikleri belirtilen değerlere ayarlanmış olarak bu sınıfın yeni bir örneğini başlatmak için kullanılan bir kısayol. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Gerektiğinde belgede bulunan göreli URI'leri mutlak URI'lere çözümlemek için kullanılacak dizeyi alır veya ayarlar. Olabilir`hükümsüz` veya boş dize. Varsayılan:`hükümsüz` . |
| [BlockImportMode](../../aspose.words.loading/htmlloadoptions/blockimportmode/) { get; set; } | Blok düzeyindeki öğelerin özelliklerinin nasıl içe aktarıldığını belirten bir değer alır veya ayarlar. Varsayılan değer:Merge . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Meta dosyasının dönüştürülüp dönüştürülmeyeceğini alır veya ayarlar (Wmf veyaEmf ) görüntüleriPng resim formatı. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | EquationXML ile şekillerin Office Math nesnelerine dönüştürülüp dönüştürülmeyeceğini alır veya ayarlar. |
| [ConvertSvgToEmf](../../aspose.words.loading/htmlloadoptions/convertsvgtoemf/) { get; set; } | Yüklenen SVG görüntülerinin EMF formatına dönüştürülüp dönüştürülmeyeceğini belirten bir değer alır veya ayarlar. Varsayılan değer:`YANLIŞ` ve mümkünse yüklenen SVG görüntüleri dönüştürme yapılmadan olduğu gibi depolanır. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Belgede kodlama belirtilmemişse bir HTML, TXT veya CHM belgesini yüklemek için kullanılacak kodlamayı alır veya ayarlar. Olabilir`hükümsüz` . Varsayılan:`hükümsüz` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Belge yazı tipi ayarlarını belirlemeye izin verir. |
| [IgnoreNoscriptElements](../../aspose.words.loading/htmlloadoptions/ignorenoscriptelements/) { get; set; } | &lt;noscript&gt; HTML öğelerinin göz ardı edilip edilmeyeceğini belirten bir değer alır veya ayarlar. Varsayılan değer:`YANLIŞ` . |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | OLE verilerinin yoksayılıp yok sayılmayacağını belirtir. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Belge yüklenirken kullanılacak dil tercihlerini alır. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Yüklenecek belgenin biçimini belirtir. Varsayılan:Auto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Belge yükleme işleminin belirli bir MS Word sürümüyle eşleşmesi gerektiğini belirtmeye olanak tanır. Varsayılan değer:Word2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Şifrelenmiş bir belgeyi açmak için parolayı alır veya ayarlar. Olabilir`hükümsüz` veya boş dize. Varsayılan:`hükümsüz` . |
| [PreferredControlType](../../aspose.words.loading/htmlloadoptions/preferredcontroltype/) { get; set; } | İçe aktarılan &lt;giriş&gt; ve &lt;seçim&gt; öğelerini temsil edecek tercih edilen belge düğümü türünü alır veya ayarlar. Varsayılan değer:FormField . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Microsoft Word formatlarını okurken INCLUDEPICTURE alanının korunup korunmayacağını alır veya ayarlar. Varsayılan değer:`YANLIŞ` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Bir belge yüklenirken çağrılır ve yükleme ilerlemesiyle ilgili verileri kabul eder. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | HTML, MHTML'den bir belge içe aktarıldığında harici kaynakların (resimler, stil sayfaları) nasıl yükleneceğini kontrol etmeye olanak tanır. |
| [SupportVml](../../aspose.words.loading/htmlloadoptions/supportvml/) { get; set; } | VML görüntülerinin desteklenip desteklenmeyeceğini belirten bir değer alır veya ayarlar. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Belgeyi okurken geçici dosyaların kullanılmasına izin verir. Varsayılan olarak bu özellik`hükümsüz` ve hiçbir geçici dosya kullanılmaz. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Alanların güncellenip güncellenmeyeceğini belirtir.`kirli` özellik. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Yükleme işlemi sırasında, veri veya biçimlendirme kalitesinin kaybına neden olabilecek bir sorun algılandığında çağrılır. |
| [WebRequestTimeout](../../aspose.words.loading/htmlloadoptions/webrequesttimeout/) { get; set; } | Web isteği zaman aşımına uğramadan önce beklenecek milisaniye sayısı. Varsayılan değer 100000 milliseconds (100 saniye). 'dir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(object) |  |

### Ayrıca bakınız

* class [LoadOptions](../loadoptions/)
* ad alanı [Aspose.Words.Loading](../../aspose.words.loading/)
* toplantı [Aspose.Words](../../)


