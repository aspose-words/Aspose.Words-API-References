---
title: "Aspose::Words::DocumentBuilder::InsertTextInput method"
linktitle: "InsertTextInput"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::InsertTextInput yöntemi. C++'da geçerli konuma bir metin form alanı ekler."
type: docs
weight: 49000
url: /tr/cpp/aspose.words/documentbuilder/inserttextinput/
---
## DocumentBuilder::InsertTextInput method


Geçerli konuma bir metin form alanı ekler.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertTextInput(const System::String &name, Aspose::Words::Fields::TextFormFieldType type, const System::String &format, const System::String &fieldValue, int32_t maxLength)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | const System::String\& | Form alanının adı. Boş bir dize olabilir. |
| tür | Aspose::Words::Fields::TextFormFieldType | Metin form alanının tipini belirtir. |
| biçim | const System::String\& | Form alanının değerini biçimlendirmek için kullanılan format dizesi. |
| fieldValue | const System::String\& | Alanda gösterilecek metin. |
| maxLength | int32_t | Kullanıcının form alanına girebileceği maksimum uzunluk. Sınırsız uzunluk için sıfır olarak ayarlayın. |

### ReturnValue

Az önce eklenen form alanı düğümü.
## Açıklamalar


Form alanı için bir ad belirtirseniz, aynı adla otomatik olarak bir yer imi oluşturulur.

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


Bir belgeye metin girişi form alanı eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Kullanıcıdan metin girmesini isteyen bir form ekleyin.
builder->InsertTextInput(u"TextInput", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Enter your text here", 0);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTextInput.docx");
```


Metin girişi form alanı eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please enter text here: ");

// Kullanıcının tıklayıp metin girebilmesini sağlayan bir metin girişi alanı ekleyin.
// Kullanıcının üzerine yazabileceği ve geçebileceği bir yer tutucu metin atayın
// form alanının içeriği için sınırsız uygulamak amacıyla maksimum metin uzunluğu 0.
builder->InsertTextInput(u"TextInput1", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Placeholder text", 0);

// Form alanı, "input" HTML etiketi şeklinde ve "text" türüyle görünecektir.
doc->Save(get_ArtifactsDir() + u"FormFields.TextInput.html");
```

## Ayrıca Bakınız

* Class [FormField](../../../aspose.words.fields/formfield/)
* Enum [TextFormFieldType](../../../aspose.words.fields/textformfieldtype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
