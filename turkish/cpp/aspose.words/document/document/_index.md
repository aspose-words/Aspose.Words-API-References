---
title: "Aspose::Words::Document::Document yapıcı"
linktitle: "Belge"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::Document yapıcı. C++'ta boş bir Word belgesi oluşturur."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/document/document/
---
## Document::Document() constructor


Boş bir Word belgesi oluşturur.

```cpp
Aspose::Words::Document::Document()
```

## Açıklamalar


Boş bir belge kaynaklardan alınır ve varsayılan olarak, ortaya çıkan belge [Word2007](../../../aspose.words.settings/mswordversion/) tarafından oluşturulmuş gibi görünür. Bu boş belge varsayılan bir yazı tipi tablosu, minimal varsayılan stiller ve gizli stiller içerir.

[OptimizeFor()](../../../aspose.words.settings/compatibilityoptions/optimizefor/) method can be used to optimize the document contents as well as default Aspose.Words behavior to a particular version of MS Word.

Belgenin kağıt boyutu varsayılan olarak Letter'dır. Sayfa düzenini değiştirmek isterseniz, [PageSetup](../../section/get_pagesetup/) kullanın.

Oluşturulduktan sonra, belge içeriğini kolayca eklemek için [DocumentBuilder](../../documentbuilder/) kullanabilirsiniz.

## Örnekler



Basit bir belge nasıl oluşturulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Yeni Document nesneleri varsayılan olarak minimum düğüm setiyle gelir
// metin ve şekiller gibi içerik eklemeye başlamak için gereken: bir Section, bir Body ve bir Paragraph.
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```


Belgeleri oluşturma ve yükleme yöntemlerini gösterir.
```cpp
// Aspose.Words kullanarak bir Document nesnesi oluşturmanın iki yolu vardır.
// 1 -  Boş bir belge oluşturun:
auto doc = System::MakeObject<Aspose::Words::Document>();

// Yeni Document nesneleri varsayılan olarak minimum düğüm setiyle gelir
// metin ve şekiller gibi içerik eklemeye başlamak için gereken: bir Section, bir Body ve bir Paragraph.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// 2 -  Yerel dosya sisteminde bulunan bir belgeyi yükleyin:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Yüklenen belgelerin erişip düzenleyebileceğimiz içerikleri olacaktır.
ASSERT_EQ(u"Hello World!", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());

// Yükleme sırasında gerçekleşmesi gereken bazı işlemler, örneğin bir belgeyi şifre çözmek için parola kullanmak,
// belgeyi yüklerken bir LoadOptions nesnesi geçirerek yapılabilir.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword"));

ASSERT_EQ(u"Test encrypted document.", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```


Bir metin run'ını font özelliğini kullanarak nasıl biçimlendireceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::SharedPtr\<System::IO::Stream\>\&) constructor


Varolan bir belgeyi akıştan açar. Dosya formatını otomatik olarak algılar.

```cpp
Aspose::Words::Document::Document(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| akış | const System::SharedPtr\<System::IO::Stream\>\& | Belgenin yükleneceği akış. |
## Açıklamalar


Belge akışın başında depolanmalıdır. Akış rastgele konumlandırmayı desteklemelidir.

## Örnekler



Bir akış kullanarak belge nasıl yüklenir gösterir.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.docx");
    auto doc = System::MakeObject<Aspose::Words::Document>(stream);

    ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", doc->GetText().Trim());
}
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Varolan bir belgeyi akıştan açar. Şifreleme parolası gibi ek seçenekleri belirtmeye olanak tanır.

```cpp
Aspose::Words::Document::Document(const System::SharedPtr<System::IO::Stream> &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| akış | const System::SharedPtr\<System::IO::Stream\>\& | Belgenin yükleneceği akış. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Bir belgeyi yüklerken kullanılacak ek seçenekler. **null** olabilir. |
## Açıklamalar


Belge akışın başında depolanmalıdır. Akış rastgele konumlandırmayı desteklemelidir.

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

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::String\&) constructor


Varolan bir belgeyi dosyadan açar. Dosya formatını otomatik olarak algılar.

```cpp
Aspose::Words::Document::Document(const System::String &fileName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | const System::String\& | Açılacak belgenin dosya adı. |

## Örnekler



Bir belgeyi açma ve .PDF'ye dönüştürme yöntemini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToPdf.pdf");
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Varolan bir belgeyi dosyadan açar. Şifreleme parolası gibi ek seçenekleri belirtmeye olanak tanır.

```cpp
Aspose::Words::Document::Document(const System::String &fileName, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | const System::String\& | Açılacak belgenin dosya adı. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Bir belgeyi yüklerken kullanılacak ek seçenekler. **null** olabilir. |

## Örnekler



Belgeleri oluşturma ve yükleme yöntemlerini gösterir.
```cpp
// Aspose.Words kullanarak bir Document nesnesi oluşturmanın iki yolu vardır.
// 1 -  Boş bir belge oluşturun:
auto doc = System::MakeObject<Aspose::Words::Document>();

// Yeni Document nesneleri varsayılan olarak minimum düğüm setiyle gelir
// metin ve şekiller gibi içerik eklemeye başlamak için gereken: bir Section, bir Body ve bir Paragraph.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// 2 -  Yerel dosya sisteminde bulunan bir belgeyi yükleyin:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Yüklenen belgelerin erişip düzenleyebileceğimiz içerikleri olacaktır.
ASSERT_EQ(u"Hello World!", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());

// Yükleme sırasında gerçekleşmesi gereken bazı işlemler, örneğin bir belgeyi şifre çözmek için parola kullanmak,
// belgeyi yüklerken bir LoadOptions nesnesi geçirerek yapılabilir.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword"));

ASSERT_EQ(u"Test encrypted document.", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```


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

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(std::istream\&) constructor




```cpp
Aspose::Words::Document::Document(std::istream &stream)
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor




```cpp
Aspose::Words::Document::Document(std::istream &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```

## Ayrıca Bakınız

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
