---
title: "Aspose::Words::Saving::PageRange sınıfı"
linktitle: "PageRange"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PageRange sınıfı. Sürekli bir sayfa aralığını temsil eder. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 18000
url: /tr/cpp/aspose.words.saving/pagerange/
---
## PageRange class


Sürekli bir sayfa aralığını temsil eder. Daha fazla bilgi için, [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) dokümantasyon makalesini ziyaret edin.

```cpp
class PageRange : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageRange](./pagerange/)(int32_t, int32_t) | Yeni bir sayfa aralığı nesnesi oluşturur. |
| static [Type](./type/)() |  |

## Örnekler



Tam sayfa aralıklarına dayalı olarak sayfaları nasıl çıkaracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
auto pageSet = System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<System::SharedPtr<Aspose::Words::Saving::PageRange>>({System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 4), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1)}));

imageOptions->set_PageSet(pageSet);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
