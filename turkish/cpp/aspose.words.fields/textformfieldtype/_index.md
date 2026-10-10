---
title: "Aspose::Words::Fields::TextFormFieldType enum"
linktitle: "TextFormFieldType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::TextFormFieldType enum. C++'da bir metin form alanının türünü belirtir."
type: docs
weight: 134000
url: /tr/cpp/aspose.words.fields/textformfieldtype/
---
## TextFormFieldType enum


Metin form alanının türünü belirtir.

```cpp
enum class TextFormFieldType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Regular | 0 | Metin form alanı herhangi bir metin içerebilir. |
| Number | 1 | Metin form alanı yalnızca sayılar içerebilir. |
| Tarih | 2 | Metin form alanı yalnızca geçerli bir tarih değeri içerebilir. |
| CurrentDate | 3 | Metin form alanı değeri, alan güncellendiğinde geçerli tarih olur. |
| CurrentTime | 4 | Metin form alanı değeri, alan güncellendiğinde geçerli zaman olur. |
| Calculated | 5 | Metin form alanı değeri, [TextInputDefault](../formfield/get_textinputdefault/) özelliğinde belirtilen ifadeden hesaplanır. |


## Örnekler



Form alanlarının nasıl oluşturulacağını gösterir.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// Form alanları, kullanıcının değer girmesi istendiğinde etkileşime girebileceği belge içindeki nesnelerdir.
// Bunları bir belge oluşturucu kullanarak oluşturabiliriz ve aşağıda iki farklı yöntem gösterilmiştir.
// 1 -  Temel metin girişi:
builder->InsertTextInput(u"My text input", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Enter your name here", 30);

// 2 -  İpucu metni ve olası değer aralığı olan açılır kutu:
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"-- Select your favorite footwear --", u"Sneakers", u"Oxfords", u"Flip-flops", u"Other"});

builder->InsertParagraph();
builder->InsertComboBox(u"My combo box", items, 0);

builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateForm.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
