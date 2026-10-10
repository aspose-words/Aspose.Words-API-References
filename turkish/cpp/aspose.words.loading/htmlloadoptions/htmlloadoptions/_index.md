---
title: "Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions yapıcı"
linktitle: "HtmlLoadOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions yapıcı. C++'ta bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.loading/htmlloadoptions/htmlloadoptions/
---
## HtmlLoadOptions::HtmlLoadOptions() constructor


Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions()
```


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

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## HtmlLoadOptions::HtmlLoadOptions(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) constructor


Özelliklerin belirtilen değerlere ayarlandığı bu sınıfın yeni bir örneğini başlatmak için bir kısayol.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions(Aspose::Words::LoadFormat loadFormat, const System::String &password, const System::String &baseUri)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| loadFormat | Aspose::Words::LoadFormat | Yüklenecek belgenin formatı. |
| password | const System::String\& | Şifreli bir belgeyi açmak için şifre. **null** veya boş dize olabilir. |
| baseUri | const System::String\& | Göreli URI'leri mutlak hale getirmek için kullanılacak dize. **null** veya boş dize olabilir. |

## Örnekler



Bir html belgesi açılırken temel URI'nin nasıl belirtileceğini gösterir.
```cpp
// .html belgesi içinde göreli bir URI ile bağlanmış bir resmi yüklemek istediğimizi varsayalım
// Resim farklı bir konumda iken. Bu durumda, göreli URI'yi mutlak bir URI'ye dönüştürmemiz gerekir.
// Bir HtmlLoadOptions nesnesi kullanarak temel URI sağlayabiliriz.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// Giriş .html dosyasındaki resim bozuk olsa da, özel temel URI'muz bağlantıyı onarmamıza yardımcı oldu.
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// Bu çıktı belgesi eksik olan resmi gösterecek.
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## Ayrıca Bakınız

* Enum [LoadFormat](../../../aspose.words/loadformat/)
* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## HtmlLoadOptions::HtmlLoadOptions(const System::String\&) constructor


Şifreli bir belgeyi yüklemek için belirtilen parolayı kullanarak bu sınıfın yeni bir örneğini başlatmak için bir kısayol.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions(const System::String &password)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| password | const System::String\& | Şifreli bir belgeyi açmak için şifre. **null** veya boş dize olabilir. |

## Örnekler



Bir Html belgesini nasıl şifreleyeceğinizi ve ardından şifre kullanarak nasıl açacağınızı gösterir.
```cpp
// Şifreli bir .docx dosyasından şifreli bir HTML belgesi oluşturun ve imzalayın.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

System::String inputFileName = get_MyDir() + u"Encrypted.docx";
System::String outputFileName = get_ArtifactsDir() + u"HtmlLoadOptions.EncryptedHtml.html";
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);

// Bu belgeyi yüklemek ve okumak için, şifre çözme
// şifresini bir HtmlLoadOptions nesnesi kullanarak geçmemiz gerekir.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(u"docPassword");

ASSERT_EQ(signOptions->get_DecryptionPassword(), loadOptions->get_Password());

auto doc = System::MakeObject<Aspose::Words::Document>(outputFileName, loadOptions);

ASSERT_EQ(u"Test encrypted document.", doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
