---
title: "Aspose::Words::DocumentBuilder::InsertCheckBox metodu"
linktitle: "InsertCheckBox"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::InsertCheckBox metodu. C++'ta geçerli konuma bir onay kutusu form alanı ekler."
type: docs
weight: 31000
url: /tr/cpp/aspose.words/documentbuilder/insertcheckbox/
---
## DocumentBuilder::InsertCheckBox(const System::String\&, bool, int32_t) method


Geçerli konuma bir onay kutusu form alanı ekler.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertCheckBox(const System::String &name, bool checkedValue, int32_t size)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | const System::String\& | Form alanının adı. Boş bir dize olabilir. 20 karakterden uzun değer kırpılacaktır. |
| checkedValue | bool | Onay kutusu form alanının işaretli durumu. |
| size | int32_t | Onay kutusunun boyutunu nokta cinsinden belirtir. MS Word'ün boyutu otomatik olarak hesaplaması için 0 belirtin. |

### ReturnValue

Az önce eklenen form alanı düğümü.
## Açıklamalar


Form alanı için bir ad belirtirseniz, aynı adla otomatik olarak bir yer imi oluşturulur.

## Örnekler



Belgeye onay kutuları eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Farklı boyutlarda ve varsayılan işaretli durumlarda onay kutuları ekleyin.
builder->Write(u"Unchecked check box of a default size: ");
builder->InsertCheckBox(System::String::Empty, false, false, 0);
builder->InsertParagraph();

builder->Write(u"Large checked check box: ");
builder->InsertCheckBox(u"CheckBox_Default", true, true, 50);
builder->InsertParagraph();

// Form alanlarının isim uzunluğu 20 karakterle sınırlıdır.
builder->Write(u"Very large checked check box: ");
builder->InsertCheckBox(u"CheckBox_OnlyCheckedValue", true, 100);

ASSERT_EQ(u"CheckBox_OnlyChecked", doc->get_Range()->get_FormFields()->idx_get(2)->get_Name());

// Bu onay kutularıyla Microsoft Word'de çift tıklayarak etkileşimde bulunabiliriz.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCheckBox.docx");
```

## Ayrıca Bakınız

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertCheckBox(const System::String\&, bool, bool, int32_t) method


Geçerli konuma bir onay kutusu form alanı ekler.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertCheckBox(const System::String &name, bool defaultValue, bool checkedValue, int32_t size)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | const System::String\& | Form alanının adı. Boş bir dize olabilir. 20 karakterden uzun değer kırpılacaktır. |
| defaultValue | bool | Onay kutusu form alanının varsayılan değeri. |
| checkedValue | bool | Onay kutusu form alanının mevcut işaretli durumu. |
| size | int32_t | Onay kutusunun boyutunu nokta cinsinden belirtir. MS Word'ün boyutu otomatik olarak hesaplaması için 0 belirtin. |

### ReturnValue

Az önce eklenen form alanı düğümü.
## Açıklamalar


Form alanı için bir ad belirtirseniz, aynı adla otomatik olarak bir yer imi oluşturulur.

## Örnekler



Belgeye onay kutuları eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Farklı boyutlarda ve varsayılan işaretli durumlarda onay kutuları ekleyin.
builder->Write(u"Unchecked check box of a default size: ");
builder->InsertCheckBox(System::String::Empty, false, false, 0);
builder->InsertParagraph();

builder->Write(u"Large checked check box: ");
builder->InsertCheckBox(u"CheckBox_Default", true, true, 50);
builder->InsertParagraph();

// Form alanlarının isim uzunluğu 20 karakterle sınırlıdır.
builder->Write(u"Very large checked check box: ");
builder->InsertCheckBox(u"CheckBox_OnlyCheckedValue", true, 100);

ASSERT_EQ(u"CheckBox_OnlyChecked", doc->get_Range()->get_FormFields()->idx_get(2)->get_Name());

// Bu onay kutularıyla Microsoft Word'de çift tıklayarak etkileşimde bulunabiliriz.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCheckBox.docx");
```

## Ayrıca Bakınız

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
