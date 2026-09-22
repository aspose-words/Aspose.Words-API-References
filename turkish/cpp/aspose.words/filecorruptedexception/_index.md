---
title: "Aspose::Words::FileCorruptedException typedef"
linktitle: "FileCorruptedException"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::FileCorruptedException typedef. Belge yüklenirken, belge bozuk göründüğünde ve yüklenemediğinde fırlatılır. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 133000
url: /tr/cpp/aspose.words/filecorruptedexception/
---
## FileCorruptedException typedef


Belge yüklenirken, belgenin bozuk göründüğü ve yüklenemediği durumlarda fırlatılır. Daha fazla bilgi için [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) dokümantasyon makalesini ziyaret edin.

```cpp
using Aspose::Words::FileCorruptedException = typedef System::ExceptionWrapper<Details_FileCorruptedException>
```


## Örnekler



Bir FileCorruptedException nasıl yakalanır gösterir.
```cpp
try
{
    // Microsoft Word kullanarak bir belge açmaya çalışırken "Unreadable content" hata mesajı alırsak,
    // muhtemelen o belgeyi Aspose.Words ile yüklemeye çalışırken bir istisna fırlatılacaktır.
    auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted document.docx");
}
catch (Aspose::Words::FileCorruptedException& e)
{
    std::cout << e->get_Message() << std::endl;
}
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
