---
title: Class PdfLoadOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Loading.PdfLoadOptions sınıf. Pdf belgesini bir dosyaya yüklerken ek seçeneklerin belirtilmesine izin verir.Document nesne.
type: docs
weight: 3470
url: /tr/net/aspose.words.loading/pdfloadoptions/
---
## PdfLoadOptions class

Pdf belgesini bir dosyaya yüklerken ek seçeneklerin belirtilmesine izin verir.[`Document`](../../aspose.words/document/) nesne.

```csharp
public class PdfLoadOptions : LoadOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [PdfLoadOptions](pdfloadoptions/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Belgede bulunan göreli URI'leri gerektiğinde mutlak URI'lere çözümlemek için kullanılacak dizeyi alır veya ayarlar. Boş veya boş dize olabilir. Varsayılan null. |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Meta dosyasının (Wmf veyaEmf ) resimler içinPng resim formatı. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | EquationXML ile şekillerin Office Math nesnelerine dönüştürülüp dönüştürülmeyeceğini belirler. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Belge içinde kodlama belirtilmemişse bir HTML, TXT veya CHM belgesini yüklemek için kullanılacak kodlamayı alır veya ayarlar. Boş olabilir. Varsayılan null. |
| [FlatOpcXmlMappingOnly](../../aspose.words.loading/loadoptions/flatopcxmlmappingonly/) { get; set; } | Hangi belge biçimlerinin eşlenmesine izin verildiğini belirleyen değeri alır veya ayarlar.[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Yalnızca varsayılan olarakFlatOpc belge biçiminin eşlenmesine izin verilir. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Belge yazı tipi ayarlarını belirlemeye izin verir. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Belge yüklenirken kullanılacak dil tercihlerini alır. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Yüklenecek belgenin biçimini belirtir. VarsayılanAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Belge yükleme işleminin belirli bir MS Word sürümüyle eşleşmesi gerektiğini belirtmeye izin verir. Varsayılan değerWord2019 |
| [PageCount](../../aspose.words.loading/pdfloadoptions/pagecount/) { get; set; } | Okunacak sayfa sayısını alır veya ayarlar. Varsayılan, belgenin tüm sayfalarının okunacağı anlamına gelen MaxValue'dir. |
| [PageIndex](../../aspose.words.loading/pdfloadoptions/pageindex/) { get; set; } | Okunacak ilk sayfanın 0 tabanlı dizinini alır veya ayarlar. Varsayılan 0. |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Şifrelenmiş bir belgeyi açmak için parolayı alır veya ayarlar. Boş veya boş dize olabilir. Varsayılan null. |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Microsoft Word biçimlerini okurken INCLUDEPICTURE alanının korunup korunmayacağını alır veya ayarlar. Varsayılan değer false'dir. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Bir belge yüklenirken çağrılır ve yükleme ilerlemesiyle ilgili verileri kabul eder. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Bir belge HTML, MHTML'den içe aktarıldığında harici kaynakların (resimler, stil sayfaları) nasıl yükleneceğini kontrol etmeyi sağlar. |
| [SkipPdfImages](../../aspose.words.loading/pdfloadoptions/skippdfimages/) { get; set; } | PDF belgesi yüklenirken görüntülerin atlanması gerekip gerekmediğini belirten bayrağı alır veya ayarlar. Varsayılan, Yanlış'tır. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Belge okunurken geçici dosyaların kullanılmasına izin verir. Varsayılan olarak bu özellik`hükümsüz` ve hiçbir geçici dosya kullanılmaz. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Alanların aşağıdakilerle güncellenip güncellenmeyeceğini belirtir.`kirli` nitelik. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Veri veya biçimlendirme aslına uygunluğu kaybına neden olabilecek bir sorun algılandığında, yükleme işlemi sırasında çağrılır. |

### Ayrıca bakınız

* class [LoadOptions](../loadoptions/)
* ad alanı [Aspose.Words.Loading](../../aspose.words.loading/)
* toplantı [Aspose.Words](../../)


