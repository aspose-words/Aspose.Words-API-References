---
title: Class LoadOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Loading.LoadOptions sınıf. Bir belgeyi bir belgeye yüklerken ek seçeneklerin şifre veya temel URI gibi belirtilmesine izin verirDocument nesne.
type: docs
weight: 3660
url: /tr/net/aspose.words.loading/loadoptions/
---
## LoadOptions class

Bir belgeyi bir belgeye yüklerken ek seçeneklerin (şifre veya temel URI gibi) belirtilmesine izin verir[`Document`](../../aspose.words/document/) nesne.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Yükleme Seçeneklerini Belirtin](https://docs.aspose.com/words/net/specify-load-options/) dokümantasyon makalesi.

```csharp
public class LoadOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [LoadOptions](loadoptions/#constructor)() | Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır. |
| [LoadOptions](loadoptions/#constructor_2)(string) | Şifrelenmiş bir belgeyi yüklemek için bu sınıfın yeni bir örneğini belirtilen parolayla başlatmak için kullanılan bir kısayol. |
| [LoadOptions](loadoptions/#constructor_1)(LoadFormat, string, string) | Özellikleri belirtilen değerlere ayarlanmış olarak bu sınıfın yeni bir örneğini başlatmak için kullanılan bir kısayol. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Gerektiğinde belgede bulunan göreli URI'leri mutlak URI'lere çözümlemek için kullanılacak dizeyi alır veya ayarlar. Olabilir`hükümsüz` veya boş dize. Varsayılan:`hükümsüz` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Meta dosyasının dönüştürülüp dönüştürülmeyeceğini alır veya ayarlar (Wmf veyaEmf ) görüntüleriPng resim formatı. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | EquationXML ile şekillerin Office Math nesnelerine dönüştürülüp dönüştürülmeyeceğini alır veya ayarlar. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Belgede kodlama belirtilmemişse bir HTML, TXT veya CHM belgesini yüklemek için kullanılacak kodlamayı alır veya ayarlar. Olabilir`hükümsüz` . Varsayılan:`hükümsüz` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Belge yazı tipi ayarlarını belirlemeye izin verir. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | OLE verilerinin yoksayılıp yok sayılmayacağını belirtir. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Belge yüklenirken kullanılacak dil tercihlerini alır. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Yüklenecek belgenin biçimini belirtir. Varsayılan:Auto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Belge yükleme işleminin belirli bir MS Word sürümüyle eşleşmesi gerektiğini belirtmeye olanak tanır. Varsayılan değer:Word2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Şifrelenmiş bir belgeyi açmak için parolayı alır veya ayarlar. Olabilir`hükümsüz` veya boş dize. Varsayılan:`hükümsüz` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Microsoft Word formatlarını okurken INCLUDEPICTURE alanının korunup korunmayacağını alır veya ayarlar. Varsayılan değer:`YANLIŞ` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Bir belge yüklenirken çağrılır ve yükleme ilerlemesiyle ilgili verileri kabul eder. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | HTML, MHTML'den bir belge içe aktarıldığında harici kaynakların (resimler, stil sayfaları) nasıl yükleneceğini kontrol etmeye olanak tanır. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Belgeyi okurken geçici dosyaların kullanılmasına izin verir. Varsayılan olarak bu özellik`hükümsüz` ve hiçbir geçici dosya kullanılmaz. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Alanların güncellenip güncellenmeyeceğini belirtir.`kirli` özellik. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Yükleme işlemi sırasında, veri veya biçimlendirme kalitesinin kaybına neden olabilecek bir sorun algılandığında çağrılır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(object) |  |

### Örnekler

Şifrelenmiş bir Microsoft Word belgesinin nasıl yükleneceğini gösterir.

```csharp
Document doc;

// Aspose.Words, şifrelenmiş bir belgeyi şifresi olmadan açmaya çalışırsak bir istisna atar.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Böyle bir belge yüklenirken parola, LoadOptions nesnesi kullanılarak belgenin yapıcısına iletilir.
LoadOptions options = new LoadOptions("docPassword");

// Şifrelenmiş bir belgeyi LoadOptions nesnesiyle yüklemenin iki yolu vardır.
// 1 - Belgeyi yerel dosya sisteminden dosya adına göre yükleyin:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Belgeyi bir akıştan yükleyin:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Loading](../../aspose.words.loading/)
* toplantı [Aspose.Words](../../)


