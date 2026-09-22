---
title: "Aspose::Words::Rendering::NodeRendererBase::Save method"
linktitle: "Save"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Rendering::NodeRendererBase::Save method. Şekli bir görüntüye render eder ve C++'ta bir akışa kaydeder."
type: docs
weight: 13000
url: /tr/cpp/aspose.words.rendering/noderendererbase/save/
---
## NodeRendererBase::Save(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) method


Şekli bir görüntüye render eder ve bir akışa kaydeder.

```cpp
void Aspose::Words::Rendering::NodeRendererBase::Save(const System::SharedPtr<System::IO::Stream> &stream, System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> saveOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| akış | const System::SharedPtr\<System::IO::Stream\>\& | Şeklin görüntüsünün kaydedileceği akış. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\> | Şeklin nasıl render edileceğini ve kaydedileceğini kontrol eden seçenekleri belirtir. **null** olabilir. Eğer **null** ise, görüntü PNG formatında kaydedilir. |

## Örnekler



Yerel dosya sisteminde şekilleri dosyalara dışa aktarmak için bir şekil renderleyicisinin nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(7, shapes->get_Length());

// Belgede 7 şekil var, bunlar arasında 2 alt şekle sahip bir grup şekil de bulunuyor.
// Her şekli yerel dosya sisteminde bir görüntü dosyasına renderleyeceğiz.
// grup şekillerini görünümleri olmadığı için yok sayarken.
// Bu, 6 görüntü dosyası üretecek.
for (auto&& shape : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    System::SharedPtr<Aspose::Words::Rendering::ShapeRenderer> renderer = shape->GetShapeRenderer();
    auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
    renderer->Save(get_ArtifactsDir() + System::String::Format(u"Shape.RenderAllShapes.{0}.png", shape->get_Name()), options);
}
```

## Ayrıca Bakınız

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) method


Şekli bir SVG görüntüsüne render eder ve bir akışa kaydeder.

```cpp
void Aspose::Words::Rendering::NodeRendererBase::Save(const System::SharedPtr<System::IO::Stream> &stream, System::SharedPtr<Aspose::Words::Saving::SvgSaveOptions> saveOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| akış | const System::SharedPtr\<System::IO::Stream\>\& | Şeklin SVG görüntüsünün kaydedileceği akış. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\> | Şeklin nasıl render edildiğini ve kaydedildiğini kontrol eden seçenekleri belirtir. **null** olabilir. Bu **null** ise, görüntü varsayılan seçeneklerle kaydedilir. |

## Örnekler



Office matematiği render ederken kaydetme seçeneklerinin nasıl geçirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

auto options = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
options->set_TextOutputMode(Aspose::Words::Saving::SvgTextOutputMode::UsePlacedGlyphs);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"SvgSaveOptions.Output.svg", options);

{
    auto stream = System::MakeObject<System::IO::MemoryStream>();
    math->GetMathRenderer()->Save(stream, options);
}
```

## Ayrıca Bakınız

* Class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) method


Şekli bir görüntüye render eder ve bir dosyaya kaydeder.

```cpp
void Aspose::Words::Rendering::NodeRendererBase::Save(const System::String &fileName, System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> saveOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | const System::String\& | Görüntü dosyasının adı. Belirtilen adla bir dosya zaten mevcutsa, mevcut dosya üzerine yazılır. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\> | Şeklin nasıl render edildiğini ve kaydedildiğini kontrol eden seçenekleri belirtir. **null** olabilir. |

## Örnekler



Yerel dosya sisteminde bir Office [Math](../../../aspose.words.math/) nesnesini görüntü dosyasına nasıl renderleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// \"ImageSaveOptions\" nesnesi oluşturun ve düğüm renderleyicisinin \"Save\" yöntemine geçerek değiştirmek için
// OfficeMath düğümünün bir görüntüye nasıl renderlendiğini.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// \"Scale\" özelliğini 5 olarak ayarlayın, nesneyi orijinal boyutunun beş katına renderlemek için.
saveOptions->set_Scale(5.0f);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"Shape.RenderOfficeMath.png", saveOptions);
```

## Ayrıca Bakınız

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) method


Şekli bir SVG görüntüsüne render eder ve bir dosyaya kaydeder.

```cpp
void Aspose::Words::Rendering::NodeRendererBase::Save(const System::String &fileName, System::SharedPtr<Aspose::Words::Saving::SvgSaveOptions> saveOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | const System::String\& | Görüntü dosyasının adı. Belirtilen adla bir dosya zaten mevcutsa, mevcut dosya üzerine yazılır. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\> | Şeklin nasıl render edildiğini ve kaydedildiğini kontrol eden seçenekleri belirtir. **null** olabilir. |

## Örnekler



Office matematiği render ederken kaydetme seçeneklerinin nasıl geçirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

auto options = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
options->set_TextOutputMode(Aspose::Words::Saving::SvgTextOutputMode::UsePlacedGlyphs);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"SvgSaveOptions.Output.svg", options);

{
    auto stream = System::MakeObject<System::IO::MemoryStream>();
    math->GetMathRenderer()->Save(stream, options);
}
```

## Ayrıca Bakınız

* Class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Rendering::NodeRendererBase::Save(std::basic_ostream<CharType, Traits> &stream, System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> saveOptions)
```

## Ayrıca Bakınız

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Rendering::NodeRendererBase::Save(std::basic_ostream<CharType, Traits> &stream, System::SharedPtr<Aspose::Words::Saving::SvgSaveOptions> saveOptions)
```

## Ayrıca Bakınız

* Class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
