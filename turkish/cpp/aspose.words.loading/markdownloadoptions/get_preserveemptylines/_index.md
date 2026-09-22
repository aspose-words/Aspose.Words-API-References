---
title: "Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines metodu"
linktitle: "get_PreserveEmptyLines"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines metodu. Bir Markdown belgesi yüklenirken boş satırların korunup korunmayacağını belirten bir boolean değer alır veya ayarlar. Varsayılan değer false'tur. Normalde, Markdown'da blok düzeyindeki öğeler arasındaki boş satırlar yok sayılır. Belgenin başındaki ve sonundaki boş satırlar da yok sayılır. Bu seçenek, C++'ta bu tür boş satırların içe aktarılmasını sağlar."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.loading/markdownloadoptions/get_preserveemptylines/
---
## MarkdownLoadOptions::get_PreserveEmptyLines method


Bir [Markdown](../../../aspose.words/loadformat/) belgesi yüklenirken boş satırların korunup korunmayacağını belirten bir boolean değer alır veya ayarlar. Varsayılan değer **false**'tür. Normalde, Markdown'da blok düzeyindeki öğeler arasındaki boş satırlar yok sayılır. Belgenin başındaki ve sonundaki boş satırlar da yok sayılır. Bu seçenek, bu tür boş satırların içe aktarılmasını sağlar.

```cpp
bool Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines() const
```


## Örnekler



Bir belge yüklenirken boş satırın nasıl korunacağını gösterir.
```cpp
System::String mdText = System::String::Format(u"{0}Line1{1}{2}Line2{3}{4}", System::Environment::get_NewLine(), System::Environment::get_NewLine(), System::Environment::get_NewLine(), System::Environment::get_NewLine(), System::Environment::get_NewLine());
{
    auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(mdText));
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_PreserveEmptyLines(true);
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    ASSERT_EQ(u"\rLine1\r\rLine2\r\f", doc->GetText());
}
```

## Ayrıca Bakınız

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
