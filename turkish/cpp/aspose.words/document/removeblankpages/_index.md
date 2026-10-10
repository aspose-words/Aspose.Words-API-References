---
title: "Aspose::Words::Document::RemoveBlankPages yöntemi"
linktitle: "RemoveBlankPages"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::RemoveBlankPages yöntemi. C++'ta belgede boş sayfaları kaldırır."
type: docs
weight: 67500
url: /tr/cpp/aspose.words/document/removeblankpages/
---
## Document::RemoveBlankPages method


Belgedeki boş sayfaları kaldırır.

```cpp
System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::Document::RemoveBlankPages()
```


### ReturnValue

Sayfa numaraları listesi boş olarak kabul edildi ve kaldırıldı.

## Örnekler



Belgeden boş sayfaları nasıl kaldıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Blank pages.docx");
ASSERT_EQ(2, doc->get_PageCount());
doc->RemoveBlankPages();
doc->UpdatePageLayout();
ASSERT_EQ(1, doc->get_PageCount());
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
