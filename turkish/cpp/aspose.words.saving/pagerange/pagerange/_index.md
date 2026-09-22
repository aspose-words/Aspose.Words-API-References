---
title: "Aspose::Words::Saving::PageRange::PageRange yapıcı"
linktitle: "PageRange"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PageRange::PageRange yapıcı. C++'ta yeni bir sayfa aralığı nesnesi oluşturur."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.saving/pagerange/pagerange/
---
## PageRange::PageRange constructor


Yeni bir sayfa aralığı nesnesi oluşturur.

```cpp
Aspose::Words::Saving::PageRange::PageRange(int32_t from, int32_t to)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| başlangıç | int32_t | Başlangıç sayfasının sıfır tabanlı indeksi. |
| bitiş | int32_t | Bitiş sayfasının sıfır tabanlı indeksi. Belge içindeki son sayfanın indeksini aşarsa, render sırasında belgeye sığacak şekilde kırpılır. |

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

* Class [PageRange](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
