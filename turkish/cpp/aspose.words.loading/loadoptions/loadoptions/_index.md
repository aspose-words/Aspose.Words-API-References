---
title: "Aspose::Words::Loading::LoadOptions::LoadOptions yapıcı"
linktitle: "LoadOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::LoadOptions::LoadOptions yapıcı. Bu sınıfın yeni bir örneğini varsayılan değerlerle C++'ta başlatır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions::LoadOptions() constructor


Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions()
```


## Örnekler



Bir akıştan temel URI kullanarak görüntülü bir HTML belgesinin nasıl açılacağını gösterir.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.html");
    // Yüklerken temel klasörün URI'sını geçirin
    // böylece HTML belgesindeki göreli URI'li tüm görüntüler bulunabilir.
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_BaseUri(get_ImageDir());

    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Belgenin ilk şeklinin geçerli bir görüntü içerdiğini doğrulayın.
    auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

    ASSERT_TRUE(shape->get_IsImage());
    ASSERT_FALSE(System::TestTools::IsNull(shape->get_ImageData()->get_ImageBytes()));
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Width()), 0.01);
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Height()), 0.01);
}
```

## Ayrıca Bakınız

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## LoadOptions::LoadOptions(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) constructor


Özelliklerin belirtilen değerlere ayarlandığı bu sınıfın yeni bir örneğini başlatmak için bir kısayol.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions(Aspose::Words::LoadFormat loadFormat, const System::String &password, const System::String &baseUri)
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
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## LoadOptions::LoadOptions(const System::String\&) constructor


Şifreli bir belgeyi yüklemek için belirtilen parolayı kullanarak bu sınıfın yeni bir örneğini başlatmak için bir kısayol.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions(const System::String &password)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| password | const System::String\& | Şifreli bir belgeyi açmak için şifre. **null** veya boş dize olabilir. |

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

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
