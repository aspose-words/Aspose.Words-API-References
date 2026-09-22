---
title: "Aspose::Words::Loading::TxtLoadOptions sınıfı"
linktitle: "TxtLoadOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::TxtLoadOptions sınıfı. Bir Metin belgesini Document nesnesine yüklerken ek seçenekler belirtmeye olanak tanır. Daha fazla bilgi için C++'taki belge makalesini ziyaret edin."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.loading/txtloadoptions/
---
## TxtLoadOptions class


[Text](../../aspose.words/loadformat/) belgesini bir [Document](../../aspose.words/document/) nesnesine yüklerken ek seçenekler belirtmeye olanak tanır. Daha fazla bilgi için [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/) belge makalesini ziyaret edin.

```cpp
class TxtLoadOptions : public Aspose::Words::Loading::LoadOptions
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Equals](../loadoptions/equals/)(System::SharedPtr\<System::Object\>) override | Belirtilen nesnenin mevcut nesneyle değer olarak eşit olup olmadığını belirler. |
| [get_AutoNumberingDetection](./get_autonumberingdetection/)() const | Bir belge yüklenirken otomatik numaralandırma algılamasının yapılacağını belirten bir boolean değer alır veya ayarlar. Varsayılan değer **true**. |
| [get_BaseUri](../loadoptions/get_baseuri/)() const | Belgede bulunan göreceli URI'leri gerektiğinde mutlak URI'lere dönüştürmek için kullanılacak dizeyi alır veya ayarlar. **null** veya boş dize olabilir. Varsayılan **null**'dır. |
| [get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/)() const | Metafile ([Wmf](../) veya [Emf](../)) görüntülerinin [Png](../) görüntü formatına dönüştürülüp dönüştürülmeyeceğini alır veya ayarlar. |
| [get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/)() const | EquationXML içeren şekillerin Office [Math](../../aspose.words.math/) nesnelerine dönüştürülüp dönüştürülmeyeceğini alır veya ayarlar. |
| [get_DetectHyperlinks](./get_detecthyperlinks/)() const | Metinde hiperlinkleri algılayıp algılamayacağını belirtir. Varsayılan değer **false**. |
| [get_DetectNumberingWithWhitespaces](./get_detectnumberingwithwhitespaces/)() const | Belge düz metin formatından içe aktarıldığında numaralı liste öğelerinin nasıl tanındığını belirtmeye olanak tanır. Varsayılan değer **true**. |
| [get_DocumentDirection](./get_documentdirection/)() const | Bir belge yönü alır veya ayarlar. Varsayılan değer [LeftToRight](../documentdirection/). |
| [get_Encoding](../loadoptions/get_encoding/)() const | Belge içinde kodlama belirtilmemişse bir HTML, TXT veya CHM belgesini yüklemek için kullanılacak kodlamayı alır veya ayarlar. **null** olabilir. Varsayılan **null**'dır. |
| [get_FontSettings](../loadoptions/get_fontsettings/)() const | Belge yazı tipi ayarlarını belirtmeye izin verir. |
| [get_IgnoreOleData](../loadoptions/get_ignoreoledata/)() const | OLE verisinin ihmal edilip edilmeyeceğini belirtir. |
| [get_LanguagePreferences](../loadoptions/get_languagepreferences/)() const | Belge yüklendiğinde kullanılacak dil tercihlerini alır. |
| [get_LeadingSpacesOptions](./get_leadingspacesoptions/)() const | Ön boşluk işleme için tercih edilen seçeneği alır veya ayarlar. Varsayılan değer [ConvertToIndent](../txtleadingspacesoptions/). |
| [get_LoadFormat](../loadoptions/get_loadformat/)() const | Yüklenecek belgenin biçimini belirtir. Varsayılan değer [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](../loadoptions/get_mswversion/)() const | Belge yükleme işleminin belirli bir MS Word sürümüyle eşleşmesini belirtmeye izin verir. Varsayılan değer [Word2019](../../aspose.words.settings/mswordversion/). |
| [get_Password](../loadoptions/get_password/)() const | Şifreli bir belgeyi açmak için parolayı alır veya ayarlar. **null** veya boş dize olabilir. Varsayılan **null**. |
| [get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/)() const | Microsoft Word formatlarını okurken INCLUDEPICTURE alanının korunup korunmayacağını alır veya ayarlar. Varsayılan değer **false**. |
| [get_ProgressCallback](../loadoptions/get_progresscallback/)() const | Bir belge yüklenirken çağrılır ve yükleme ilerlemesi hakkında veri alır. |
| [get_RecoveryMode](../loadoptions/get_recoverymode/)() const | Yükleme sırasında hatalar oluşursa belgenin nasıl işleneceğini tanımlar. Sistem belgenin kurtarılmaya çalışıp çalışmayacağını veya başka bir tanımlı davranışı izleyip izlemeyeceğini belirtmek için bu özelliği kullanın. Varsayılan değer [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](../loadoptions/get_resourceloadingcallback/)() const | Bir belge HTML veya MHTML'den içe aktarıldığında dış kaynakların (görseller, stil sayfaları) nasıl yükleneceğini kontrol etmeye izin verir. |
| [get_TempFolder](../loadoptions/get_tempfolder/)() const | Belge okunurken geçici dosyaların kullanılmasına izin verir. Varsayılan olarak bu özellik **null**'dır ve geçici dosya kullanılmaz. |
| [get_TrailingSpacesOptions](./get_trailingspacesoptions/)() const | Satır sonu boşluk işleme için tercih edilen seçeneği alır veya ayarlar. Varsayılan değer [Trim](../txttrailingspacesoptions/). |
| [get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/)() const | **dirty** özniteliğine sahip alanların güncellenip güncellenmeyeceğini belirtir. |
| [get_UseSystemLcid](../loadoptions/get_usesystemlcid/)() const | Sayfa ayarı varsayılan kenar boşluklarını belirlemek için Windows kayıt defterinden alınan LCID değerinin kullanılıp kullanılmayacağını alır veya ayarlar. |
| [get_WarningCallback](../loadoptions/get_warningcallback/)() const | Bir yükleme işlemi sırasında, veri veya biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde çağrılır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](../loadoptions/loadoptions/)() | Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır. |
| [LoadOptions](../loadoptions/loadoptions/)(const System::String\&) | Şifreli bir belgeyi yüklemek için belirtilen parolayı kullanarak bu sınıfın yeni bir örneğini başlatmak için bir kısayol. |
| [LoadOptions](../loadoptions/loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | Özelliklerin belirtilen değerlere ayarlandığı bu sınıfın yeni bir örneğini başlatmak için bir kısayol. |
| [set_AutoNumberingDetection](./set_autonumberingdetection/)(bool) | Ayarlayıcı: [Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection](./get_autonumberingdetection/). |
| [set_BaseUri](../loadoptions/set_baseuri/)(const System::String\&) | [Aspose::Words::Loading::LoadOptions::get_BaseUri](../loadoptions/get_baseuri/) için ayarlayıcı. |
| [set_ConvertMetafilesToPng](../loadoptions/set_convertmetafilestopng/)(bool) | [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/) için ayarlayıcı. |
| [set_ConvertShapeToOfficeMath](../loadoptions/set_convertshapetoofficemath/)(bool) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/). |
| [set_DetectHyperlinks](./set_detecthyperlinks/)(bool) | Ayarlayıcı: [Aspose::Words::Loading::TxtLoadOptions::get_DetectHyperlinks](./get_detecthyperlinks/). |
| [set_DetectNumberingWithWhitespaces](./set_detectnumberingwithwhitespaces/)(bool) | Ayarlayıcı: [Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces](./get_detectnumberingwithwhitespaces/). |
| [set_DocumentDirection](./set_documentdirection/)(Aspose::Words::Loading::DocumentDirection) | Ayarlayıcı: [Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection](./get_documentdirection/). |
| [set_Encoding](../loadoptions/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_Encoding](../loadoptions/get_encoding/). |
| [set_FontSettings](../loadoptions/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_FontSettings](../loadoptions/get_fontsettings/). |
| [set_IgnoreOleData](../loadoptions/set_ignoreoledata/)(bool) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](../loadoptions/get_ignoreoledata/). |
| [set_LeadingSpacesOptions](./set_leadingspacesoptions/)(Aspose::Words::Loading::TxtLeadingSpacesOptions) | Ayarlayıcı: [Aspose::Words::Loading::TxtLoadOptions::get_LeadingSpacesOptions](./get_leadingspacesoptions/). |
| [set_LoadFormat](../loadoptions/set_loadformat/)(Aspose::Words::LoadFormat) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_LoadFormat](../loadoptions/get_loadformat/). |
| [set_MswVersion](../loadoptions/set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_MswVersion](../loadoptions/get_mswversion/). |
| [set_Password](../loadoptions/set_password/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_Password](../loadoptions/get_password/). |
| [set_PreserveIncludePictureField](../loadoptions/set_preserveincludepicturefield/)(bool) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/). |
| [set_ProgressCallback](../loadoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | Bir belge yüklenirken çağrılır ve yükleme ilerlemesi hakkında veri alır. |
| [set_RecoveryMode](../loadoptions/set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](../loadoptions/get_recoverymode/). |
| [set_ResourceLoadingCallback](../loadoptions/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Bir belge HTML veya MHTML'den içe aktarıldığında dış kaynakların (görseller, stil sayfaları) nasıl yükleneceğini kontrol etmeye izin verir. |
| [set_TempFolder](../loadoptions/set_tempfolder/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_TempFolder](../loadoptions/get_tempfolder/). |
| [set_TrailingSpacesOptions](./set_trailingspacesoptions/)(Aspose::Words::Loading::TxtTrailingSpacesOptions) | Ayarlayıcı: [Aspose::Words::Loading::TxtLoadOptions::get_TrailingSpacesOptions](./get_trailingspacesoptions/). |
| [set_UpdateDirtyFields](../loadoptions/set_updatedirtyfields/)(bool) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/). |
| [set_UseSystemLcid](../loadoptions/set_usesystemlcid/)(bool) | Ayarlayıcı [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](../loadoptions/get_usesystemlcid/). |
| [set_WarningCallback](../loadoptions/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Bir yükleme işlemi sırasında, veri veya biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde çağrılır. |
| [TxtLoadOptions](./txtloadoptions/)() | Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır. |
| static [Type](./type/)() |  |

## Örnekler



Hipermetin bağlantılarını okuma ve gösterme yöntemini gösterir.
```cpp
const System::String inputText = System::String(u"Some links in TXT:\n") + u"https://www.aspose.com/\n" + u"https://docs.aspose.com/words/net/\n";

{
    System::SharedPtr<System::IO::Stream> stream = System::MakeObject<System::IO::MemoryStream>();
    System::ArrayPtr<uint8_t> buf = System::Text::Encoding::get_ASCII()->GetBytes(inputText);
    stream->Write(buf, 0, buf->get_Length());
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();
    loadOptions->set_DetectHyperlinks(true);

    // Hipermetin bağlantılı belgeyi yükle.
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Hipermetin bağlantı metnini yazdır.
    for (auto&& field : System::IterateOver(doc->get_Range()->get_Fields()))
    {
        std::cout << field->get_Result() << std::endl;
    }

    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_Result().Trim(), u"https://www.aspose.com/");
    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Result().Trim(), u"https://docs.aspose.com/words/net/");
}
```

## Ayrıca Bakınız

* Class [LoadOptions](../loadoptions/)
* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
