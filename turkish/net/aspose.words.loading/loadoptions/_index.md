---
title: LoadOptions
second_title: Aspose.Words for .NET API Referansı
description: Bir belgeyi bir belgeye yüklerken ek seçeneklerin parola veya temel URI gibi belirtilmesine izin verir.Document../aspose.words/document nesne.
type: docs
weight: 3460
url: /tr/net/aspose.words.loading/loadoptions/
---
## LoadOptions class

Bir belgeyi bir belgeye yüklerken ek seçeneklerin (parola veya temel URI gibi) belirtilmesine izin verir.[`Document`](../../aspose.words/document) nesne.

```csharp
public class LoadOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [LoadOptions](loadoptions#constructor)() | Varsayılan değerlerle bu sınıfın yeni bir örneğini başlatır. |
| [LoadOptions](loadoptions#constructor_2)(string) | Şifrelenmiş bir belgeyi yüklemek için belirtilen parolayla bu sınıfın yeni bir örneğini başlatmak için bir kısayol. |
| [LoadOptions](loadoptions#constructor_1)(LoadFormat, string, string) | Belirtilen değerlere ayarlanmış özelliklerle bu sınıfın yeni bir örneğini başlatmak için bir kısayol. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri) { get; set; } | Belgede bulunan göreli URI'leri gerektiğinde mutlak URI'lere çözümlemek için kullanılacak dizeyi alır veya ayarlar. Boş veya boş dize olabilir. Varsayılan null. |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng) { get; set; } | Meta dosyasının (Wmf veyaEmf ) resimler içinPng resim formatı. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath) { get; set; } | EquationXML ile şekillerin Office Math nesnelerine dönüştürülüp dönüştürülmeyeceğini belirler. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding) { get; set; } | Belge içinde kodlama belirtilmemişse bir HTML, TXT veya CHM belgesini yüklemek için kullanılacak kodlamayı alır veya ayarlar. Boş olabilir. Varsayılan null. |
| [FlatOpcXmlMappingOnly](../../aspose.words.loading/loadoptions/flatopcxmlmappingonly) { get; set; } | Hangi belge biçimlerinin eşlenmesine izin verildiğini belirleyen değeri alır veya ayarlar.[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping) . Yalnızca varsayılan olarakFlatOpc belge biçiminin eşlenmesine izin verilir. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings) { get; set; } | Belge yazı tipi ayarlarını belirlemeye izin verir. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences) { get; } | Belge yüklenirken kullanılacak dil tercihlerini alır. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat) { get; set; } | Yüklenecek belgenin biçimini belirtir. VarsayılanAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion) { get; set; } | Belge yükleme işleminin belirli bir MS Word sürümüyle eşleşmesi gerektiğini belirtmeye izin verir. Varsayılan değerWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password) { get; set; } | Şifrelenmiş bir belgeyi açmak için parolayı alır veya ayarlar. Boş veya boş dize olabilir. Varsayılan null. |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield) { get; set; } | Microsoft Word biçimlerini okurken INCLUDEPICTURE alanının korunup korunmayacağını alır veya ayarlar. Varsayılan değer false'dir. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback) { get; set; } | Bir belge yüklenirken çağrılır ve yükleme ilerlemesiyle ilgili verileri kabul eder. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback) { get; set; } | Bir belge HTML, MHTML'den içe aktarıldığında harici kaynakların (resimler, stil sayfaları) nasıl yükleneceğini kontrol etmeyi sağlar. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder) { get; set; } | Belge okunurken geçici dosyaların kullanılmasına izin verir. Varsayılan olarak bu özellik`hükümsüz` ve hiçbir geçici dosya kullanılmaz. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields) { get; set; } | Alanların aşağıdakilerle güncellenip güncellenmeyeceğini belirtir.`kirli` nitelik. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback) { get; set; } | Veri veya biçimlendirme aslına uygunluğu kaybına neden olabilecek bir sorun algılandığında, yükleme işlemi sırasında çağrılır. |

### Örnekler

Şifrelenmiş bir Microsoft Word belgesinin nasıl yükleneceğini gösterir.

```csharp
Document doc;

// Aspose.Words şifreli bir belgeyi şifresi olmadan açmaya çalışırsak bir istisna atar.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Böyle bir belge yüklenirken parola, bir LoadOptions nesnesi kullanılarak belgenin oluşturucusuna iletilir.
LoadOptions options = new LoadOptions("docPassword");

// Şifreli bir belgeyi LoadOptions nesnesiyle yüklemenin iki yolu vardır.
// 1 - Belgeyi yerel dosya sisteminden dosya adına göre yükleyin:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Belgeyi bir akıştan yükleyin:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Loading](../../aspose.words.loading)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
