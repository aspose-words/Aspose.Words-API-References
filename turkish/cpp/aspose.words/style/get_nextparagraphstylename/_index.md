---
title: "Aspose::Words::Style::get_NextParagraphStyleName metodu"
linktitle: "get_NextParagraphStyleName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Style::get_NextParagraphStyleName metodu. Belirtilen stil ile biçimlendirilmiş bir paragraftan sonra eklenen yeni paragrafa otomatik olarak uygulanacak stilin adını alır/ayar. C++ içinde."
type: docs
weight: 15000
url: /tr/cpp/aspose.words/style/get_nextparagraphstylename/
---
## Style::get_NextParagraphStyleName method


Belirtilen stil ile biçimlendirilmiş bir paragraftan sonra eklenen yeni paragrafa otomatik olarak uygulanacak stilin adını alır/ayar.

```cpp
System::String Aspose::Words::Style::get_NextParagraphStyleName()
```


## Örnekler



Bir belgenin stil koleksiyonuna nasıl erişileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(4, doc->get_Styles()->get_Count());

// Aspose.Words kullanılarak oluşturulan bir belgenin varsayılan olarak içerdiği tüm stilleri numaralandırın ve listeleyin.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Style>>> stylesEnum = doc->get_Styles()->GetEnumerator();
    while (stylesEnum->MoveNext())
    {
        System::SharedPtr<Aspose::Words::Style> curStyle = stylesEnum->get_Current();
        std::cout << System::String::Format(u"Style name:\t\"{0}\", of type \"{1}\"", curStyle->get_Name(), curStyle->get_Type()) << std::endl;
        std::cout << System::String::Format(u"\tSubsequent style:\t{0}", curStyle->get_NextParagraphStyleName()) << std::endl;
        std::cout << System::String::Format(u"\tIs heading:\t\t\t{0}", curStyle->get_IsHeading()) << std::endl;
        std::cout << System::String::Format(u"\tIs QuickStyle:\t\t{0}", curStyle->get_IsQuickStyle()) << std::endl;

        ASPOSE_ASSERT_EQ(doc, curStyle->get_Document());
    }
}
```

## Ayrıca Bakınız

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
