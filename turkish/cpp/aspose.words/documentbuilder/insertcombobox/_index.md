---
title: "Aspose::Words::DocumentBuilder::InsertComboBox method"
linktitle: "InsertComboBox"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::InsertComboBox yöntemi. C++'ta geçerli konuma bir combobox form alanı ekler."
type: docs
weight: 32000
url: /tr/cpp/aspose.words/documentbuilder/insertcombobox/
---
## DocumentBuilder::InsertComboBox method


Geçerli konuma bir açılır kutu form alanı ekler.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertComboBox(const System::String &name, const System::ArrayPtr<System::String> &items, int32_t selectedIndex)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | const System::String\& | Form alanının adı. Boş bir dize olabilir. 20 karakterden uzun değer kırpılacaktır. |
| items | const System::ArrayPtr\<System::String\>\& | ComboBox öğeleri. Azami 25 öğe. |
| selectedIndex | int32_t | ComboBox'ta seçilen öğenin indeksi. |

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


Bir belgeye combo box form alanı eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Kullanıcıyı menüden bir öğe seçmeye yönlendiren bir form ekleyin.
builder->Write(u"Pick a fruit: ");
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"});
builder->InsertComboBox(u"DropDown", items, 0);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertComboBox.docx");
```

## Ayrıca Bakınız

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
