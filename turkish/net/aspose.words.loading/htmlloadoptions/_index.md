---
title: Class HtmlLoadOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Loading.HtmlLoadOptions sınıf. HTML belgesini bir dosyaya yüklerken ek seçeneklerin belirtilmesine izin verir.Document nesne.
type: docs
weight: 3420
url: /tr/net/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class

HTML belgesini bir dosyaya yüklerken ek seçeneklerin belirtilmesine izin verir.[`Document`](../../aspose.words/document/) nesne.

```csharp
public class HtmlLoadOptions : LoadOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [HtmlLoadOptions](htmlloadoptions/#constructor)() | Varsayılan değerlerle bu sınıfın yeni bir örneğini başlatır. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_2)(string) | Şifrelenmiş bir belgeyi yüklemek için belirtilen parolayla bu sınıfın yeni bir örneğini başlatmak için bir kısayol. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_1)(LoadFormat, string, string) | Belirtilen değerlere ayarlanmış özelliklerle bu sınıfın yeni bir örneğini başlatmak için bir kısayol. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Belgede bulunan göreli URI'leri gerektiğinde mutlak URI'lere çözümlemek için kullanılacak dizeyi alır veya ayarlar. Boş veya boş dize olabilir. Varsayılan null. |
| [BlockImportMode](../../aspose.words.loading/htmlloadoptions/blockimportmode/) { get; set; } | Blok düzeyi öğelerin özelliklerinin nasıl içe aktarıldığını belirten bir değer alır veya ayarlar. Varsayılan değerMerge . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Meta dosyasının (Wmf veyaEmf ) resimler içinPng resim formatı. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | EquationXML ile şekillerin Office Math nesnelerine dönüştürülüp dönüştürülmeyeceğini belirler. |
| [ConvertSvgToEmf](../../aspose.words.loading/htmlloadoptions/convertsvgtoemf/) { get; set; } | Yüklenen SVG görüntülerinin EMF biçimine dönüştürülüp dönüştürülmeyeceğini belirten bir değer alır veya ayarlar. Varsayılan değer`yanlış` ve mümkünse, yüklenen SVG görüntüleri dönüştürülmeden olduğu gibi saklanır. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Belge içinde kodlama belirtilmemişse bir HTML, TXT veya CHM belgesini yüklemek için kullanılacak kodlamayı alır veya ayarlar. Boş olabilir. Varsayılan null. |
| [FlatOpcXmlMappingOnly](../../aspose.words.loading/loadoptions/flatopcxmlmappingonly/) { get; set; } | Hangi belge biçimlerinin eşlenmesine izin verildiğini belirleyen değeri alır veya ayarlar.[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Yalnızca varsayılan olarakFlatOpc belge biçiminin eşlenmesine izin verilir. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Belge yazı tipi ayarlarını belirlemeye izin verir. |
| [IgnoreNoscriptElements](../../aspose.words.loading/htmlloadoptions/ignorenoscriptelements/) { get; set; } | &lt;noscript&gt; HTML öğelerinin göz ardı edilip edilmeyeceğini belirten bir değer alır veya ayarlar. Varsayılan değer`yanlış` . |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Belge yüklenirken kullanılacak dil tercihlerini alır. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Yüklenecek belgenin biçimini belirtir. VarsayılanAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Belge yükleme işleminin belirli bir MS Word sürümüyle eşleşmesi gerektiğini belirtmeye izin verir. Varsayılan değerWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Şifrelenmiş bir belgeyi açmak için parolayı alır veya ayarlar. Boş veya boş dize olabilir. Varsayılan null. |
| [PreferredControlType](../../aspose.words.loading/htmlloadoptions/preferredcontroltype/) { get; set; } | İçe aktarılan &lt;input&gt; ve &lt;select&gt; öğelerini temsil edecek tercih edilen belge düğümü türünü alır veya ayarlar. Varsayılan değerFormField . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Microsoft Word biçimlerini okurken INCLUDEPICTURE alanının korunup korunmayacağını alır veya ayarlar. Varsayılan değer false'dir. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Bir belge yüklenirken çağrılır ve yükleme ilerlemesiyle ilgili verileri kabul eder. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Bir belge HTML, MHTML'den içe aktarıldığında harici kaynakların (resimler, stil sayfaları) nasıl yükleneceğini kontrol etmeyi sağlar. |
| [SupportVml](../../aspose.words.loading/htmlloadoptions/supportvml/) { get; set; } | VML görüntülerinin desteklenip desteklenmediğini belirten bir değer alır veya ayarlar. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Belge okunurken geçici dosyaların kullanılmasına izin verir. Varsayılan olarak bu özellik`hükümsüz` ve hiçbir geçici dosya kullanılmaz. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Alanların aşağıdakilerle güncellenip güncellenmeyeceğini belirtir.`kirli` nitelik. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Veri veya biçimlendirme aslına uygunluğu kaybına neden olabilecek bir sorun algılandığında, yükleme işlemi sırasında çağrılır. |
| [WebRequestTimeout](../../aspose.words.loading/htmlloadoptions/webrequesttimeout/) { get; set; } | Web isteğinin zaman aşımına uğramadan önce beklenecek milisaniye sayısı. Varsayılan değer 100.000 milisaniyedir (100 saniye). |

### Ayrıca bakınız

* class [LoadOptions](../loadoptions/)
* ad alanı [Aspose.Words.Loading](../../aspose.words.loading/)
* toplantı [Aspose.Words](../../)


