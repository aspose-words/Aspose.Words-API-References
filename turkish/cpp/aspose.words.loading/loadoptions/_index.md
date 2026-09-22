---
title: "Aspose::Words::Loading::LoadOptions sınıfı"
linktitle: "LoadOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::LoadOptions sınıfı. Bir belgeyi Document nesnesine yüklerken ek seçenekler (örneğin parola veya temel URI) belirtmenizi sağlar. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.loading/loadoptions/
---
## LoadOptions class


Bir belgeyi bir [Document](../../aspose.words/document/) nesnesine yüklerken ek seçenekler (örneğin parola veya temel URI) belirtmenizi sağlar. Daha fazla bilgi için [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/) belge makalesini ziyaret edin.

```cpp
class LoadOptions : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Belirtilen nesnenin mevcut nesneyle değer olarak eşit olup olmadığını belirler. |
| [get_BaseUri](./get_baseuri/)() const | Belgede bulunan göreceli URI'leri gerektiğinde mutlak URI'lere dönüştürmek için kullanılacak dizeyi alır veya ayarlar. **null** veya boş dize olabilir. Varsayılan **null**'dır. |
| [get_ConvertMetafilesToPng](./get_convertmetafilestopng/)() const | Metafile ([Wmf](../) veya [Emf](../)) görüntülerinin [Png](../) görüntü formatına dönüştürülüp dönüştürülmeyeceğini alır veya ayarlar. |
| [get_ConvertShapeToOfficeMath](./get_convertshapetoofficemath/)() const | EquationXML içeren şekillerin Office [Math](../../aspose.words.math/) nesnelerine dönüştürülüp dönüştürülmeyeceğini alır veya ayarlar. |
| [get_Encoding](./get_encoding/)() const | Belge içinde kodlama belirtilmemişse bir HTML, TXT veya CHM belgesini yüklemek için kullanılacak kodlamayı alır veya ayarlar. **null** olabilir. Varsayılan **null**'dır. |
| [get_FontSettings](./get_fontsettings/)() const | Belge yazı tipi ayarlarını belirtmeye izin verir. |
| [get_IgnoreOleData](./get_ignoreoledata/)() const | OLE verisinin ihmal edilip edilmeyeceğini belirtir. |
| [get_LanguagePreferences](./get_languagepreferences/)() const | Belge yüklendiğinde kullanılacak dil tercihlerini alır. |
| [get_LoadFormat](./get_loadformat/)() const | Yüklenecek belgenin biçimini belirtir. Varsayılan değer [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](./get_mswversion/)() const | Belge yükleme işleminin belirli bir MS Word sürümüyle eşleşmesini belirtmeye izin verir. Varsayılan değer [Word2019](../../aspose.words.settings/mswordversion/). |
| [get_Password](./get_password/)() const | Şifreli bir belgeyi açmak için parolayı alır veya ayarlar. **null** veya boş dize olabilir. Varsayılan **null**. |
| [get_PreserveIncludePictureField](./get_preserveincludepicturefield/)() const | Microsoft Word formatlarını okurken INCLUDEPICTURE alanının korunup korunmayacağını alır veya ayarlar. Varsayılan değer **false**. |
| [get_ProgressCallback](./get_progresscallback/)() const | Bir belge yüklenirken çağrılır ve yükleme ilerlemesi hakkında veri alır. |
| [get_RecoveryMode](./get_recoverymode/)() const | Yükleme sırasında hatalar oluşursa belgenin nasıl işleneceğini tanımlar. Sistem belgenin kurtarılmaya çalışıp çalışmayacağını veya başka bir tanımlı davranışı izleyip izlemeyeceğini belirtmek için bu özelliği kullanın. Varsayılan değer [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](./get_resourceloadingcallback/)() const | Bir belge HTML veya MHTML'den içe aktarıldığında dış kaynakların (görseller, stil sayfaları) nasıl yükleneceğini kontrol etmeye izin verir. |
| [get_TempFolder](./get_tempfolder/)() const | Belge okunurken geçici dosyaların kullanılmasına izin verir. Varsayılan olarak bu özellik **null**'dır ve geçici dosya kullanılmaz. |
| [get_UpdateDirtyFields](./get_updatedirtyfields/)() const | **dirty** özniteliğine sahip alanların güncellenip güncellenmeyeceğini belirtir. |
| [get_UseSystemLcid](./get_usesystemlcid/)() const | Sayfa ayarı varsayılan kenar boşluklarını belirlemek için Windows kayıt defterinden alınan LCID değerinin kullanılıp kullanılmayacağını alır veya ayarlar. |
| [get_WarningCallback](./get_warningcallback/)() const | Bir yükleme işlemi sırasında, veri veya biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde çağrılır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](./loadoptions/)() | Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır. |
| [LoadOptions](./loadoptions/)(const System::String\&) | Şifreli bir belgeyi yüklemek için belirtilen parolayı kullanarak bu sınıfın yeni bir örneğini başlatmak için bir kısayol. |
| [LoadOptions](./loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | Özelliklerin belirtilen değerlere ayarlandığı bu sınıfın yeni bir örneğini başlatmak için bir kısayol. |
| [set_BaseUri](./set_baseuri/)(const System::String\&) | [Aspose::Words::Loading::LoadOptions::get_BaseUri](./get_baseuri/) için ayarlayıcı. |
| [set_ConvertMetafilesToPng](./set_convertmetafilestopng/)(bool) | [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](./get_convertmetafilestopng/) için ayarlayıcı. |
| [set_ConvertShapeToOfficeMath](./set_convertshapetoofficemath/)(bool) | [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](./get_convertshapetoofficemath/) için ayarlayıcı. |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | [Aspose::Words::Loading::LoadOptions::get_Encoding](./get_encoding/) için ayarlayıcı. |
| [set_FontSettings](./set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | [Aspose::Words::Loading::LoadOptions::get_FontSettings](./get_fontsettings/) için ayarlayıcı. |
| [set_IgnoreOleData](./set_ignoreoledata/)(bool) | [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](./get_ignoreoledata/) için ayarlayıcı. |
| [set_LoadFormat](./set_loadformat/)(Aspose::Words::LoadFormat) | [Aspose::Words::Loading::LoadOptions::get_LoadFormat](./get_loadformat/) için ayarlayıcı. |
| [set_MswVersion](./set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | [Aspose::Words::Loading::LoadOptions::get_MswVersion](./get_mswversion/) için ayarlayıcı. |
| [set_Password](./set_password/)(const System::String\&) | [Aspose::Words::Loading::LoadOptions::get_Password](./get_password/) için ayarlayıcı. |
| [set_PreserveIncludePictureField](./set_preserveincludepicturefield/)(bool) | [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](./get_preserveincludepicturefield/) için ayarlayıcı. |
| [set_ProgressCallback](./set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | Bir belge yüklenirken çağrılır ve yükleme ilerlemesi hakkında veri alır. |
| [set_RecoveryMode](./set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](./get_recoverymode/) için ayarlayıcı. |
| [set_ResourceLoadingCallback](./set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Bir belge HTML veya MHTML'den içe aktarıldığında dış kaynakların (görseller, stil sayfaları) nasıl yükleneceğini kontrol etmeye izin verir. |
| [set_TempFolder](./set_tempfolder/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_TempFolder](./get_tempfolder/). |
| [set_UpdateDirtyFields](./set_updatedirtyfields/)(bool) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](./get_updatedirtyfields/). |
| [set_UseSystemLcid](./set_usesystemlcid/)(bool) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](./get_usesystemlcid/). |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Bir yükleme işlemi sırasında, veri veya biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde çağrılır. |
| static [Type](./type/)() |  |

## Örnekler



Şifrelenmiş bir Microsoft Word belgesinin nasıl yükleneceğini gösterir.
```cpp
System::SharedPtr<Aspose::Words::Document> doc;

// Şifreli bir belgeyi parolasız açmaya çalışırsak Aspose.Words bir istisna fırlatır.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx");
})(), Aspose::Words::IncorrectPasswordException);

// Böyle bir belgeyi yüklerken, parola LoadOptions nesnesi kullanılarak belgenin yapıcı metoduna geçirilir.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword");

// Şifreli bir belgeyi LoadOptions nesnesiyle yüklemenin iki yolu vardır.
// 1 -  Belgeyi yerel dosya sisteminden dosya adıyla yükleyin:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", options);

// 2 -  Belgeyi bir akıştan yükleyin:
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Encrypted.docx");
    doc = System::MakeObject<Aspose::Words::Document>(stream, options);
}
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
