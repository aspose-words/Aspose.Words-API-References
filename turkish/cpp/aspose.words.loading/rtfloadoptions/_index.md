---
title: "Aspose::Words::Loading::RtfLoadOptions sınıfı"
linktitle: "RtfLoadOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::RtfLoadOptions sınıfı. Rtf belgesini bir Document nesnesine yüklerken ek seçenekler belirtmeye olanak tanır. Daha fazla bilgi için C++'ta belge makalesini ziyaret edin."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.loading/rtfloadoptions/
---
## RtfLoadOptions class


[Rtf](../../aspose.words/loadformat/) belgesini bir [Document](../../aspose.words/document/) nesnesine yüklerken ek seçenekler belirtmeye olanak tanır. Daha fazla bilgi için [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/) belge makalesini ziyaret edin.

```cpp
class RtfLoadOptions : public Aspose::Words::Loading::LoadOptions
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Equals](../loadoptions/equals/)(System::SharedPtr\<System::Object\>) override | Belirtilen nesnenin mevcut nesneyle değer olarak eşit olup olmadığını belirler. |
| [get_BaseUri](../loadoptions/get_baseuri/)() const | Belgede bulunan göreceli URI'leri gerektiğinde mutlak URI'lere dönüştürmek için kullanılacak dizeyi alır veya ayarlar. **null** veya boş dize olabilir. Varsayılan **null**'dır. |
| [get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/)() const | Metafile ([Wmf](../) veya [Emf](../)) görüntülerinin [Png](../) görüntü formatına dönüştürülüp dönüştürülmeyeceğini alır veya ayarlar. |
| [get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/)() const | EquationXML içeren şekillerin Office [Math](../../aspose.words.math/) nesnelerine dönüştürülüp dönüştürülmeyeceğini alır veya ayarlar. |
| [get_Encoding](../loadoptions/get_encoding/)() const | Belge içinde kodlama belirtilmemişse bir HTML, TXT veya CHM belgesini yüklemek için kullanılacak kodlamayı alır veya ayarlar. **null** olabilir. Varsayılan **null**'dır. |
| [get_FontSettings](../loadoptions/get_fontsettings/)() const | Belge yazı tipi ayarlarını belirtmeye izin verir. |
| [get_IgnoreOleData](../loadoptions/get_ignoreoledata/)() const | OLE verisinin ihmal edilip edilmeyeceğini belirtir. |
| [get_LanguagePreferences](../loadoptions/get_languagepreferences/)() const | Belge yüklendiğinde kullanılacak dil tercihlerini alır. |
| [get_LoadFormat](../loadoptions/get_loadformat/)() const | Yüklenecek belgenin biçimini belirtir. Varsayılan değer [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](../loadoptions/get_mswversion/)() const | Belge yükleme işleminin belirli bir MS Word sürümüyle eşleşmesini belirtmeye izin verir. Varsayılan değer [Word2019](../../aspose.words.settings/mswordversion/). |
| [get_Password](../loadoptions/get_password/)() const | Şifreli bir belgeyi açmak için parolayı alır veya ayarlar. **null** veya boş dize olabilir. Varsayılan **null**. |
| [get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/)() const | Microsoft Word formatlarını okurken INCLUDEPICTURE alanının korunup korunmayacağını alır veya ayarlar. Varsayılan değer **false**. |
| [get_ProgressCallback](../loadoptions/get_progresscallback/)() const | Bir belge yüklenirken çağrılır ve yükleme ilerlemesi hakkında veri alır. |
| [get_RecognizeUtf8Text](./get_recognizeutf8text/)() const | **true** olarak ayarlandığında, UTF8 karakterlerini tespit etmeye çalışır ve içe aktarma sırasında korunur. |
| [get_RecoveryMode](../loadoptions/get_recoverymode/)() const | Yükleme sırasında hatalar oluşursa belgenin nasıl işleneceğini tanımlar. Sistem belgenin kurtarılmaya çalışıp çalışmayacağını veya başka bir tanımlı davranışı izleyip izlemeyeceğini belirtmek için bu özelliği kullanın. Varsayılan değer [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](../loadoptions/get_resourceloadingcallback/)() const | Bir belge HTML veya MHTML'den içe aktarıldığında dış kaynakların (görseller, stil sayfaları) nasıl yükleneceğini kontrol etmeye izin verir. |
| [get_TempFolder](../loadoptions/get_tempfolder/)() const | Belge okunurken geçici dosyaların kullanılmasına izin verir. Varsayılan olarak bu özellik **null**'dır ve geçici dosya kullanılmaz. |
| [get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/)() const | **dirty** özniteliğine sahip alanların güncellenip güncellenmeyeceğini belirtir. |
| [get_UseSystemLcid](../loadoptions/get_usesystemlcid/)() const | Sayfa ayarı varsayılan kenar boşluklarını belirlemek için Windows kayıt defterinden alınan LCID değerinin kullanılıp kullanılmayacağını alır veya ayarlar. |
| [get_WarningCallback](../loadoptions/get_warningcallback/)() const | Bir yükleme işlemi sırasında, veri veya biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde çağrılır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](../loadoptions/loadoptions/)() | Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır. |
| [LoadOptions](../loadoptions/loadoptions/)(const System::String\&) | Şifreli bir belgeyi yüklemek için belirtilen parolayı kullanarak bu sınıfın yeni bir örneğini başlatmak için bir kısayol. |
| [LoadOptions](../loadoptions/loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | Özelliklerin belirtilen değerlere ayarlandığı bu sınıfın yeni bir örneğini başlatmak için bir kısayol. |
| [RtfLoadOptions](./rtfloadoptions/)() | Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır. |
| [set_BaseUri](../loadoptions/set_baseuri/)(const System::String\&) | [Aspose::Words::Loading::LoadOptions::get_BaseUri](../loadoptions/get_baseuri/) için ayarlayıcı. |
| [set_ConvertMetafilesToPng](../loadoptions/set_convertmetafilestopng/)(bool) | [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/) için ayarlayıcı. |
| [set_ConvertShapeToOfficeMath](../loadoptions/set_convertshapetoofficemath/)(bool) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/). |
| [set_Encoding](../loadoptions/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_Encoding](../loadoptions/get_encoding/). |
| [set_FontSettings](../loadoptions/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_FontSettings](../loadoptions/get_fontsettings/). |
| [set_IgnoreOleData](../loadoptions/set_ignoreoledata/)(bool) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](../loadoptions/get_ignoreoledata/). |
| [set_LoadFormat](../loadoptions/set_loadformat/)(Aspose::Words::LoadFormat) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_LoadFormat](../loadoptions/get_loadformat/). |
| [set_MswVersion](../loadoptions/set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_MswVersion](../loadoptions/get_mswversion/). |
| [set_Password](../loadoptions/set_password/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_Password](../loadoptions/get_password/). |
| [set_PreserveIncludePictureField](../loadoptions/set_preserveincludepicturefield/)(bool) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/). |
| [set_ProgressCallback](../loadoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | Bir belge yüklenirken çağrılır ve yükleme ilerlemesi hakkında veri alır. |
| [set_RecognizeUtf8Text](./set_recognizeutf8text/)(bool) | Ayarlayıcı: [Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text](./get_recognizeutf8text/). |
| [set_RecoveryMode](../loadoptions/set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](../loadoptions/get_recoverymode/). |
| [set_ResourceLoadingCallback](../loadoptions/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Bir belge HTML veya MHTML'den içe aktarıldığında dış kaynakların (görseller, stil sayfaları) nasıl yükleneceğini kontrol etmeye izin verir. |
| [set_TempFolder](../loadoptions/set_tempfolder/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_TempFolder](../loadoptions/get_tempfolder/). |
| [set_UpdateDirtyFields](../loadoptions/set_updatedirtyfields/)(bool) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/). |
| [set_UseSystemLcid](../loadoptions/set_usesystemlcid/)(bool) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](../loadoptions/get_usesystemlcid/). |
| [set_WarningCallback](../loadoptions/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Bir yükleme işlemi sırasında, veri veya biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde çağrılır. |
| static [Type](./type/)() |  |

## Örnekler



Bir RTF belgesi yüklenirken UTF-8 karakterlerinin nasıl tespit edileceğini gösterir.
```cpp
// "RtfLoadOptions" nesnesi oluşturun, RTF belgesini nasıl yüklediğimizi değiştirmek için.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::RtfLoadOptions>();

// "RecognizeUtf8Text" özelliğini "false" olarak ayarlayın, belgenin ISO 8859-1 karakter kümesini kullandığını varsaymak için
// ve belgedeki her karakteri yükler.
// "RecognizeUtf8Text" özelliğini "true" olarak ayarlayın, metinde ortaya çıkabilecek değişken uzunlukta karakterleri ayrıştırmak için.
loadOptions->set_RecognizeUtf8Text(recognizeUtf8Text);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"UTF-8 characters.rtf", loadOptions);

ASSERT_EQ(recognizeUtf8Text ? System::String(u"“John Doe´s list of currency symbols”™\r") + u"€, ¢, £, ¥, ¤" : System::String(u"â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r") + u"â‚¬, Â¢, Â£, Â¥, Â¤", doc->get_FirstSection()->get_Body()->GetText().Trim());
```

## Ayrıca Bakınız

* Class [LoadOptions](../loadoptions/)
* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
