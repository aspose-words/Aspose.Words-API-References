---
title: "Aspose::Words::Loading::HtmlLoadOptions class"
linktitle: "HtmlLoadOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::HtmlLoadOptions sınıfı. HTML belgesini bir Document nesnesine yüklerken ek seçenekler belirtmeye olanak tanır. Daha fazla bilgi için C++'taki belge makalesini ziyaret edin."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class


HTML belgesini bir [Document](../../aspose.words/document/) nesnesine yüklerken ek seçenekler belirtmeye olanak tanır. Daha fazla bilgi için [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/) belge makalesini ziyaret edin.

```cpp
class HtmlLoadOptions : public Aspose::Words::Loading::LoadOptions
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Equals](../loadoptions/equals/)(System::SharedPtr\<System::Object\>) override | Belirtilen nesnenin mevcut nesneyle değer olarak eşit olup olmadığını belirler. |
| [get_BaseUri](../loadoptions/get_baseuri/)() const | Belgede bulunan göreceli URI'leri gerektiğinde mutlak URI'lere dönüştürmek için kullanılacak dizeyi alır veya ayarlar. **null** veya boş dize olabilir. Varsayılan **null**'dır. |
| [get_BlockImportMode](./get_blockimportmode/)() const | Blok düzeyindeki öğelerin özelliklerinin nasıl içe aktarılacağını belirten bir değeri alır veya ayarlar. Varsayılan değer [Merge](../blockimportmode/)'dir. |
| [get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/)() const | Metafile ([Wmf](../) veya [Emf](../)) görüntülerinin [Png](../) görüntü formatına dönüştürülüp dönüştürülmeyeceğini alır veya ayarlar. |
| [get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/)() const | EquationXML içeren şekillerin Office [Math](../../aspose.words.math/) nesnelerine dönüştürülüp dönüştürülmeyeceğini alır veya ayarlar. |
| [get_ConvertSvgToEmf](./get_convertsvgtoemf/)() const | Yüklenen SVG görüntülerinin EMF formatına dönüştürülüp dönüştürülmeyeceğini gösteren bir değeri alır veya ayarlar. Varsayılan değer **false**'dur ve mümkün olduğunda, yüklenen SVG görüntüleri dönüşüm olmadan olduğu gibi depolanır. |
| [get_Encoding](../loadoptions/get_encoding/)() const | Belge içinde kodlama belirtilmemişse bir HTML, TXT veya CHM belgesini yüklemek için kullanılacak kodlamayı alır veya ayarlar. **null** olabilir. Varsayılan **null**'dır. |
| [get_FontSettings](../loadoptions/get_fontsettings/)() const | Belge yazı tipi ayarlarını belirtmeye izin verir. |
| [get_IgnoreNoscriptElements](./get_ignorenoscriptelements/)() const | İhmal edilip edilmeyeceğini belirten bir değeri alır veya ayarlar <noscript> HTML öğeleri. Varsayılan değer **false**. |
| [get_IgnoreOleData](../loadoptions/get_ignoreoledata/)() const | OLE verisinin ihmal edilip edilmeyeceğini belirtir. |
| [get_LanguagePreferences](../loadoptions/get_languagepreferences/)() const | Belge yüklendiğinde kullanılacak dil tercihlerini alır. |
| [get_LoadFormat](../loadoptions/get_loadformat/)() const | Yüklenecek belgenin biçimini belirtir. Varsayılan değer [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](../loadoptions/get_mswversion/)() const | Belge yükleme işleminin belirli bir MS Word sürümüyle eşleşmesini belirtmeye izin verir. Varsayılan değer [Word2019](../../aspose.words.settings/mswordversion/). |
| [get_Password](../loadoptions/get_password/)() const | Şifreli bir belgeyi açmak için parolayı alır veya ayarlar. **null** veya boş dize olabilir. Varsayılan **null**. |
| [get_PreferredControlType](./get_preferredcontroltype/)() const | İçe aktarılan <input> ve <select> öğelerini temsil edecek tercih edilen belge düğümü tipini alır veya ayarlar. Varsayılan değer [FormField](../htmlcontroltype/). |
| [get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/)() const | Microsoft Word formatlarını okurken INCLUDEPICTURE alanının korunup korunmayacağını alır veya ayarlar. Varsayılan değer **false**. |
| [get_ProgressCallback](../loadoptions/get_progresscallback/)() const | Bir belge yüklenirken çağrılır ve yükleme ilerlemesi hakkında veri alır. |
| [get_RecoveryMode](../loadoptions/get_recoverymode/)() const | Yükleme sırasında hatalar oluşursa belgenin nasıl işleneceğini tanımlar. Sistem belgenin kurtarılmaya çalışıp çalışmayacağını veya başka bir tanımlı davranışı izleyip izlemeyeceğini belirtmek için bu özelliği kullanın. Varsayılan değer [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](../loadoptions/get_resourceloadingcallback/)() const | Bir belge HTML veya MHTML'den içe aktarıldığında dış kaynakların (görseller, stil sayfaları) nasıl yükleneceğini kontrol etmeye izin verir. |
| [get_SupportFontFaceRules](./get_supportfontfacerules/)() const | @font-face kurallarını destekleyip desteklemeyeceğini ve bildirilen yazı tiplerinin yüklenip yüklenmeyeceğini belirten bir değeri alır veya ayarlar. Varsayılan değer **false**. |
| [get_SupportVml](./get_supportvml/)() const | VML görsellerini destekleyip desteklemeyeceğini belirten bir değeri alır veya ayarlar. |
| [get_TempFolder](../loadoptions/get_tempfolder/)() const | Belge okunurken geçici dosyaların kullanılmasına izin verir. Varsayılan olarak bu özellik **null**'dır ve geçici dosya kullanılmaz. |
| [get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/)() const | **dirty** özniteliğine sahip alanların güncellenip güncellenmeyeceğini belirtir. |
| [get_UseSystemLcid](../loadoptions/get_usesystemlcid/)() const | Sayfa ayarı varsayılan kenar boşluklarını belirlemek için Windows kayıt defterinden alınan LCID değerinin kullanılıp kullanılmayacağını alır veya ayarlar. |
| [get_WarningCallback](../loadoptions/get_warningcallback/)() const | Bir yükleme işlemi sırasında, veri veya biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde çağrılır. |
| [get_WebRequestTimeout](./get_webrequesttimeout/)() const | Web isteğinin zaman aşımına uğramadan önce beklenecek milisaniye sayısı. Varsayılan değer 100000 milisaniye (100 saniye). |
| [GetType](./gettype/)() const override |  |
| [HtmlLoadOptions](./htmlloadoptions/)() | Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır. |
| [HtmlLoadOptions](./htmlloadoptions/)(const System::String\&) | Şifreli bir belgeyi yüklemek için belirtilen parolayı kullanarak bu sınıfın yeni bir örneğini başlatmak için bir kısayol. |
| [HtmlLoadOptions](./htmlloadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | Özelliklerin belirtilen değerlere ayarlandığı bu sınıfın yeni bir örneğini başlatmak için bir kısayol. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](../loadoptions/loadoptions/)() | Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır. |
| [LoadOptions](../loadoptions/loadoptions/)(const System::String\&) | Şifreli bir belgeyi yüklemek için belirtilen parolayı kullanarak bu sınıfın yeni bir örneğini başlatmak için bir kısayol. |
| [LoadOptions](../loadoptions/loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | Özelliklerin belirtilen değerlere ayarlandığı bu sınıfın yeni bir örneğini başlatmak için bir kısayol. |
| [set_BaseUri](../loadoptions/set_baseuri/)(const System::String\&) | [Aspose::Words::Loading::LoadOptions::get_BaseUri](../loadoptions/get_baseuri/) için ayarlayıcı. |
| [set_BlockImportMode](./set_blockimportmode/)(Aspose::Words::Loading::BlockImportMode) | [Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode](./get_blockimportmode/) için ayarlayıcı. |
| [set_ConvertMetafilesToPng](../loadoptions/set_convertmetafilestopng/)(bool) | [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/) için ayarlayıcı. |
| [set_ConvertShapeToOfficeMath](../loadoptions/set_convertshapetoofficemath/)(bool) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/). |
| [set_ConvertSvgToEmf](./set_convertsvgtoemf/)(bool) | Ayarlayıcı [Aspose::Words::Loading::HtmlLoadOptions::get_ConvertSvgToEmf](./get_convertsvgtoemf/). |
| [set_Encoding](../loadoptions/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_Encoding](../loadoptions/get_encoding/). |
| [set_FontSettings](../loadoptions/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_FontSettings](../loadoptions/get_fontsettings/). |
| [set_IgnoreNoscriptElements](./set_ignorenoscriptelements/)(bool) | Ayarlayıcı [Aspose::Words::Loading::HtmlLoadOptions::get_IgnoreNoscriptElements](./get_ignorenoscriptelements/). |
| [set_IgnoreOleData](../loadoptions/set_ignoreoledata/)(bool) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](../loadoptions/get_ignoreoledata/). |
| [set_LoadFormat](../loadoptions/set_loadformat/)(Aspose::Words::LoadFormat) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_LoadFormat](../loadoptions/get_loadformat/). |
| [set_MswVersion](../loadoptions/set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_MswVersion](../loadoptions/get_mswversion/). |
| [set_Password](../loadoptions/set_password/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_Password](../loadoptions/get_password/). |
| [set_PreferredControlType](./set_preferredcontroltype/)(Aspose::Words::Loading::HtmlControlType) | Ayarlayıcı [Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType](./get_preferredcontroltype/). |
| [set_PreserveIncludePictureField](../loadoptions/set_preserveincludepicturefield/)(bool) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/). |
| [set_ProgressCallback](../loadoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | Bir belge yüklenirken çağrılır ve yükleme ilerlemesi hakkında veri alır. |
| [set_RecoveryMode](../loadoptions/set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](../loadoptions/get_recoverymode/). |
| [set_ResourceLoadingCallback](../loadoptions/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Bir belge HTML veya MHTML'den içe aktarıldığında dış kaynakların (görseller, stil sayfaları) nasıl yükleneceğini kontrol etmeye izin verir. |
| [set_SupportFontFaceRules](./set_supportfontfacerules/)(bool) | Ayarlayıcı [Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules](./get_supportfontfacerules/). |
| [set_SupportVml](./set_supportvml/)(bool) | Ayarlayıcı [Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml](./get_supportvml/). |
| [set_TempFolder](../loadoptions/set_tempfolder/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_TempFolder](../loadoptions/get_tempfolder/). |
| [set_UpdateDirtyFields](../loadoptions/set_updatedirtyfields/)(bool) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/). |
| [set_UseSystemLcid](../loadoptions/set_usesystemlcid/)(bool) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](../loadoptions/get_usesystemlcid/). |
| [set_WarningCallback](../loadoptions/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Bir yükleme işlemi sırasında, veri veya biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde çağrılır. |
| [set_WebRequestTimeout](./set_webrequesttimeout/)(int32_t) | Web isteğinin zaman aşımına uğramadan önce beklenecek milisaniye sayısı. Varsayılan değer 100000 milisaniye (100 saniye). |
| static [Type](./type/)() |  |

## Örnekler



HTML belgesi yüklenirken koşullu yorumları nasıl destekleyeceğinizi gösterir.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();

// Değer doğru ise, yüklü belgeyi ayrıştırırken VML kodunu dikkate alırız.
loadOptions->set_SupportVml(supportVml);

// Bu belge, "<!--[if gte vml 1]>" etiketleri içinde bir JPEG görüntüsü içerir,
// ve "<![if !vml]>" etiketleri içinde farklı bir PNG görüntüsü içerir.
// Eğer "SupportVml" bayrağını "true" olarak ayarlarsak, Aspose.Words JPEG'i yükleyecektir.
// Bu bayrağı "false" olarak ayarlarsak, Aspose.Words sadece PNG'yi yükleyecektir.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VML conditional.htm", loadOptions);

if (supportVml)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
```

## Ayrıca Bakınız

* Class [LoadOptions](../loadoptions/)
* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
