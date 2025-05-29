---
title: HtmlLoadOptions Class
linktitle: HtmlLoadOptions
articleTitle: HtmlLoadOptions
second_title: .NET için Aspose.Words
description: En iyi performans için özelleştirilebilir seçeneklerle HTML belge yüklemesini bir Belge nesnesine geliştirmek üzere Aspose.Words.Loading.HtmlLoadOptions'ı keşfedin.
type: docs
weight: 4070
url: /tr/net/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class

HTML belgesini bir HTML dosyasına yüklerken ek seçeneklerin belirtilmesine olanak tanır.[`Document`](../../aspose.words/document/) nesne.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yükleme Seçeneklerini Belirleyin](https://docs.aspose.com/words/net/specify-load-options/) belgeleme makalesi.

```csharp
public class HtmlLoadOptions : LoadOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [HtmlLoadOptions](htmlloadoptions/#constructor)() | Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_2)(*string*) | Şifrelenmiş bir belgeyi yüklemek için belirtilen parolayla bu sınıfın yeni bir örneğini başlatmak için bir kısayol. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_1)(*[LoadFormat](../../aspose.words/loadformat/), string, string*) | Bu sınıfın özelliklerini belirtilen değerlere ayarlayarak yeni bir örneğini başlatmak için bir kısayol. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Gerektiğinde belgede bulunan bağıl URI'leri mutlak URI'lere dönüştürmek için kullanılacak dizeyi alır veya ayarlar. `hükümsüz` veya boş dize. Varsayılan`hükümsüz` . |
| [BlockImportMode](../../aspose.words.loading/htmlloadoptions/blockimportmode/) { get; set; } | Blok düzeyindeki öğelerin özelliklerinin nasıl içe aktarılacağını belirten bir değeri alır veya ayarlar. Varsayılan değerMerge . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Meta dosyasının dönüştürülüp dönüştürülmeyeceğini alır veya ayarlarWmf veyaEmf ) görüntüleriPnggörüntü biçimi. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Şekillerin EquationXML ile Office Math nesnelerine dönüştürülüp dönüştürülmeyeceğini alır veya ayarlar. |
| [ConvertSvgToEmf](../../aspose.words.loading/htmlloadoptions/convertsvgtoemf/) { get; set; } | Yüklenen SVG resimlerinin EMF biçimine dönüştürülüp dönüştürülmeyeceğini belirten bir değer alır veya ayarlar. Varsayılan değer`YANLIŞ` ve mümkünse, yüklenen SVG görüntüleri dönüştürülmeden olduğu gibi saklanır. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Kodlama belirtilmemişse HTML, TXT veya CHM belgesini yüklemek için kullanılacak kodlamayı alır veya ayarlar belgenin içinde. Şu şekilde olabilir:`hükümsüz` Varsayılan değer:`hükümsüz` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Belge yazı tipi ayarlarının belirlenmesine olanak tanır. |
| [IgnoreNoscriptElements](../../aspose.words.loading/htmlloadoptions/ignorenoscriptelements/) { get; set; } | &lt;noscript&gt; HTML öğelerinin yoksayılıp yoksayılmayacağını belirten bir değer alır veya ayarlar. Varsayılan değer`YANLIŞ` . |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | OLE verilerinin yoksayılıp yoksayılmayacağını belirtir. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Belge yüklenirken kullanılacak dil tercihlerini alır. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Yüklenecek belgenin biçimini belirtir. VarsayılanAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Belge yükleme işleminin belirli bir MS Word sürümüyle eşleşmesi gerektiğini belirtmenize olanak tanır. Varsayılan değerWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Şifrelenmiş bir belgeyi açmak için parolayı alır veya ayarlar. Şu şekilde olabilir:`hükümsüz` veya boş dize. Varsayılan`hükümsüz` . |
| [PreferredControlType](../../aspose.words.loading/htmlloadoptions/preferredcontroltype/) { get; set; } | İçeri aktarılan &lt;input&gt; ve &lt;select&gt; öğelerini temsil edecek tercih edilen belge düğümü türünü alır veya ayarlar. Varsayılan değerFormField . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Microsoft Word biçimlerini okurken INCLUDEPICTURE alanının korunup korunmayacağını alır veya ayarlar. Varsayılan değer`YANLIŞ` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Bir belge yüklenirken çağrılır ve yükleme ilerlemesiyle ilgili verileri kabul eder. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Bir belge HTML veya MHTML'den içe aktarıldığında harici kaynakların (resimler, stil sayfaları) nasıl yükleneceğini kontrol etmenizi sağlar. |
| [SupportFontFaceRules](../../aspose.words.loading/htmlloadoptions/supportfontfacerules/) { get; set; } | @font-face kurallarının desteklenip desteklenmeyeceğini ve beyan edilen fontların yüklenip yüklenmeyeceğini belirten bir değer alır veya ayarlar. Varsayılan değer`YANLIŞ` . |
| [SupportVml](../../aspose.words.loading/htmlloadoptions/supportvml/) { get; set; } | VML görüntülerinin desteklenip desteklenmeyeceğini belirten bir değer alır veya ayarlar. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Belgeyi okurken geçici dosyaların kullanılmasına izin verir. Varsayılan olarak bu özellik`hükümsüz` ve geçici dosyalar kullanılmaz. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Alanların güncellenip güncellenmeyeceğini belirtir`kirli` öznitelik. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | Sayfa düzeni varsayılan kenar boşluklarını belirlemek için Windows kayıt defterinden alınan LCID değerinin kullanılıp kullanılmayacağını alır veya ayarlar. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Veri veya biçimlendirme sadakat kaybına yol açabilecek bir sorun algılandığında, yükleme işlemi sırasında çağrılır. |
| [WebRequestTimeout](../../aspose.words.loading/htmlloadoptions/webrequesttimeout/) { get; set; } | Web isteği zaman aşımına uğramadan önce beklenecek milisaniye sayısı. Varsayılan değer 100000 milisaniyedir (100 saniye). |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | Belirtilen nesnenin geçerli nesneye eşit değerde olup olmadığını belirler. |

## Örnekler

Bir HTML belgesi yüklenirken koşullu yorumların nasıl destekleneceğini gösterir.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// Değer doğruysa, yüklenen belgeyi ayrıştırırken VML kodunu dikkate alırız.
loadOptions.SupportVml = supportVml;

// Bu belge "<!--[if gte vml 1]>" etiketleri arasında bir JPEG görüntüsü içeriyor,
// ve "<![if !vml]>" etiketleri arasında farklı bir PNG resmi.
// "SupportVml" bayrağını "true" olarak ayarlarsak, Aspose.Words JPEG'i yükleyecektir.
// Bu bayrağı "false" olarak ayarlarsak, Aspose.Words yalnızca PNG'yi yükleyecektir.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### Ayrıca bakınız

* class [LoadOptions](../loadoptions/)
* ad alanı [Aspose.Words.Loading](../../aspose.words.loading/)
* toplantı [Aspose.Words](../../)
