---
title: "Aspose::Words::Document::Save metodu"
linktitle: "Save"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::Save metodu. Belirtilen formatı kullanarak belgeyi bir akışa C++'ta kaydeder."
type: docs
weight: 72000
url: /tr/cpp/aspose.words/document/save/
---
## Document::Save(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


Belgeyi belirtilen formatı kullanarak bir akışa kaydeder.

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::SharedPtr<System::IO::Stream> &stream, Aspose::Words::SaveFormat saveFormat)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| akış | const System::SharedPtr\<System::IO::Stream\>\& | Belgeyi kaydetmek için akış. |
| saveFormat | Aspose::Words::SaveFormat | Belgenin kaydedileceği format. |

### ReturnValue

İsteğe bağlı olarak kullanabileceğiniz ek bilgiler.

## Örnekler



Bir belgeyi akış aracılığıyla bir görüntüye nasıl kaydedeceğinizi ve ardından görüntüyü aynı akıştan nasıl okuyacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");
```


Bir belgeyi akışa nasıl kaydedeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

{
    auto dstStream = System::MakeObject<System::IO::MemoryStream>();
    doc->Save(dstStream, Aspose::Words::SaveFormat::Docx);

    // Akışın belgeyi içerdiğini doğrulayın.
    ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", System::MakeObject<Aspose::Words::Document>(dstStream)->GetText().Trim());
}
```

## Ayrıca Bakınız

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Enum [SaveFormat](../../saveformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Belgeyi belirtilen kaydetme seçeneklerini kullanarak bir akışa kaydeder.

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::SharedPtr<System::IO::Stream> &stream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| akış | const System::SharedPtr\<System::IO::Stream\>\& | Belgeyi kaydetmek için akış. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Belgenin nasıl kaydedileceğini kontrol eden seçenekleri belirtir. **null** olabilir. Bu **null** ise, belge ikili DOC formatında kaydedilir. |

### ReturnValue

İsteğe bağlı olarak kullanabileceğiniz ek bilgiler.

## Ayrıca Bakınız

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(const System::String\&) method


Belgeyi bir dosyaya kaydeder. Uzantıdan kaydetme formatını otomatik olarak belirler.

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::String &fileName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | const System::String\& | Belge için ad. Belirtilen dosya adıyla zaten bir belge varsa, mevcut belge üzerine yazılır. |

### ReturnValue

İsteğe bağlı olarak kullanabileceğiniz ek bilgiler.

## Örnekler



Bir belgeyi açma ve .PDF'ye dönüştürme yöntemini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToPdf.pdf");
```

## Ayrıca Bakınız

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(const System::String\&, Aspose::Words::SaveFormat) method


Belgeyi belirtilen formatta bir dosyaya kaydeder.

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::String &fileName, Aspose::Words::SaveFormat saveFormat)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | const System::String\& | Belge için ad. Belirtilen dosya adıyla zaten bir belge varsa, mevcut belge üzerine yazılır. |
| saveFormat | Aspose::Words::SaveFormat | Belgenin kaydedileceği format. |

### ReturnValue

İsteğe bağlı olarak kullanabileceğiniz ek bilgiler.

## Örnekler



DOCX'ten HTML formatına nasıl dönüştürüleceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToHtml.html", Aspose::Words::SaveFormat::Html);
```

## Ayrıca Bakınız

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Enum [SaveFormat](../../saveformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Belgeyi belirtilen kaydetme seçeneklerini kullanarak bir dosyaya kaydeder.

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::String &fileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | const System::String\& | Belge için ad. Belirtilen dosya adıyla zaten bir belge varsa, mevcut belge üzerine yazılır. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Belgenin nasıl kaydedileceğini kontrol eden seçenekleri belirtir. **null** olabilir. |

### ReturnValue

İsteğe bağlı olarak kullanabileceğiniz ek bilgiler.

## Örnekler



SaveOptions ile oluşturulan belgenin kalitesini nasıl artıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(60);
builder->Writeln(u"Some text.");

System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.Default.jpg", options);

options->set_UseAntiAliasing(true);
options->set_UseHighQualityRendering(true);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.HighQuality.jpg", options);
```


Bir belgeden bir sayfayı JPEG görüntüsüne nasıl render edeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Belgenin "Save" yöntemine geçirebileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// Bu yöntemin belgeyi bir görüntüye render etme şeklini değiştirmek için
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// İkinci sayfayı seçmek için "PageSet" değerini "1" olarak ayarlayın
// belgeyi render etmeye başlayacağınız sıfır tabanlı indeks
options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(1));

// Belgeyi JPEG formatında kaydettiğimizde, Aspose.Words yalnızca bir sayfayı render eder.
// Bu görüntü, ikinci sayfadan başlayan bir sayfa içerir,
// ki bu da orijinal belgenin sadece ikinci sayfasıdır.
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.OnePage.jpg", options);
```


Bir belgenin her sayfasını ayrı bir TIFF görüntüsüne nasıl render edeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Belgenin "Save" yöntemine geçirebileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// Bu yöntemin belgeyi bir görüntüye render etme şeklini değiştirmek için
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);

for (int32_t i = 0; i < doc->get_PageCount(); i++)
{
    // İlk sayfanın numarasını belirten "PageSet" özelliğini şu sayıdan ayarlayın
    // belirtilen sayfadan belgeyi oluşturmaya başlayın.
    options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(i));
    // Sayfayı 2325x5325 piksel ve 600 dpi olarak dışa aktar.
    options->set_Resolution(600.0f);
    options->set_ImageSize(System::Drawing::Size(2325, 5325));

    doc->Save(get_ArtifactsDir() + System::String::Format(u"ImageSaveOptions.PageByPage.{0}.tiff", i + 1), options);
}
```


Bir belgeyi JPEG olarak kaydederken sıkıştırmayı nasıl yapılandıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Belgenin "Save" yöntemine geçirebileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// Bu yöntemin belgeyi bir görüntüye render etme şeklini değiştirmek için
auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// \"JpegQuality\" özelliğini \"10\" olarak ayarlayarak belgeyi render ederken daha güçlü sıkıştırma kullanın.
// Bu, belgenin dosya boyutunu azaltacak, ancak görüntü daha belirgin sıkıştırma artefaktları gösterecektir.
imageOptions->set_JpegQuality(10);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// \"JpegQuality\" özelliğini \"100\" olarak ayarlayarak belgeyi render ederken daha zayıf sıkıştırma kullanın.
// Bu, dosya boyutunun artması pahasına görüntü kalitesini artıracaktır.
imageOptions->set_JpegQuality(100);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

## Ayrıca Bakınız

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(std::basic_ostream\<CharType, Traits\>\&, Aspose::Words::SaveFormat) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(std::basic_ostream<CharType, Traits> &stream, Aspose::Words::SaveFormat saveFormat)
```

## Ayrıca Bakınız

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Enum [SaveFormat](../../saveformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(std::basic_ostream<CharType, Traits> &stream, System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions)
```

## Ayrıca Bakınız

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
