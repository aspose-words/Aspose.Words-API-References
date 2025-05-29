---
title: MarkdownLoadOptions Class
linktitle: MarkdownLoadOptions
articleTitle: MarkdownLoadOptions
second_title: .NET için Aspose.Words
description: Markdown belge yükleme deneyiminizi geliştirmek için Aspose.Words.MarkdownLoadOptions'ı keşfedin. Projelerinize sorunsuz entegrasyon için seçenekleri özelleştirin.
type: docs
weight: 4120
url: /tr/net/aspose.words.loading/markdownloadoptions/
---
## MarkdownLoadOptions class

Yükleme sırasında ek seçeneklerin belirlenmesine olanak tanırMarkdown belgeye dönüştürmek[`Document`](../../aspose.words/document/) nesne.

```csharp
public class MarkdownLoadOptions : LoadOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [MarkdownLoadOptions](markdownloadoptions/)() | Yeni bir örneğini başlatır`MarkdownLoadOptions` sınıf. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Gerektiğinde belgede bulunan bağıl URI'leri mutlak URI'lere dönüştürmek için kullanılacak dizeyi alır veya ayarlar. `hükümsüz` veya boş dize. Varsayılan`hükümsüz` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Meta dosyasının dönüştürülüp dönüştürülmeyeceğini alır veya ayarlarWmf veyaEmf ) görüntüleriPnggörüntü biçimi. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Şekillerin EquationXML ile Office Math nesnelerine dönüştürülüp dönüştürülmeyeceğini alır veya ayarlar. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Kodlama belirtilmemişse HTML, TXT veya CHM belgesini yüklemek için kullanılacak kodlamayı alır veya ayarlar belgenin içinde. Şu şekilde olabilir:`hükümsüz` Varsayılan değer:`hükümsüz` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Belge yazı tipi ayarlarının belirlenmesine olanak tanır. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | OLE verilerinin yoksayılıp yoksayılmayacağını belirtir. |
| [ImportUnderlineFormatting](../../aspose.words.loading/markdownloadoptions/importunderlineformatting/) { get; set; } | İki artı karakterden oluşan bir diziyi "++" alt çizgi metin biçimlendirmesi olarak tanımayı belirten bir Boole değeri alır veya ayarlar. Varsayılan değer`YANLIŞ` . |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Belge yüklenirken kullanılacak dil tercihlerini alır. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Yüklenecek belgenin biçimini belirtir. VarsayılanAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Belge yükleme işleminin belirli bir MS Word sürümüyle eşleşmesi gerektiğini belirtmenize olanak tanır. Varsayılan değerWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Şifrelenmiş bir belgeyi açmak için parolayı alır veya ayarlar. Şu şekilde olabilir:`hükümsüz` veya boş dize. Varsayılan`hükümsüz` . |
| [PreserveEmptyLines](../../aspose.words.loading/markdownloadoptions/preserveemptylines/) { get; set; } | Yükleme sırasında boş satırların korunup korunmayacağını belirten bir Boole değeri alır veya ayarlarMarkdown document. Varsayılan değer`YANLIŞ` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Microsoft Word biçimlerini okurken INCLUDEPICTURE alanının korunup korunmayacağını alır veya ayarlar. Varsayılan değer`YANLIŞ` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Bir belge yüklenirken çağrılır ve yükleme ilerlemesiyle ilgili verileri kabul eder. |
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

Belge yüklenirken boş satırın nasıl korunacağını gösterir.

```csharp
string mdText = $"{Environment.NewLine}Line1{Environment.NewLine}{Environment.NewLine}Line2{Environment.NewLine}{Environment.NewLine}";
using (MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(mdText)))
{
    MarkdownLoadOptions loadOptions = new MarkdownLoadOptions() { PreserveEmptyLines = true };
    Document doc = new Document(stream, loadOptions);

    Assert.AreEqual("\rLine1\r\rLine2\r\f", doc.GetText());
}
```

### Ayrıca bakınız

* class [LoadOptions](../loadoptions/)
* ad alanı [Aspose.Words.Loading](../../aspose.words.loading/)
* toplantı [Aspose.Words](../../)
