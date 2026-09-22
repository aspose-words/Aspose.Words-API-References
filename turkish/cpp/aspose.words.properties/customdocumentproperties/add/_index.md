---
title: "Aspose::Words::Properties::CustomDocumentProperties::Add yöntemi"
linktitle: "Add"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::CustomDocumentProperties::Add yöntemi. C++'ta Boolean veri tipinde yeni bir özel belge özelliği oluşturur."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.properties/customdocumentproperties/add/
---
## CustomDocumentProperties::Add(const System::String\&, bool) method


[Boolean](../../propertytype/) veri tipinde yeni bir özel belge özelliği oluşturur.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::Add(const System::String &name, bool value)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | const System::String\& | Özelliğin adı. |
| value | bool | Özelliğin değeri. |

### ReturnValue

Yeni oluşturulan özelliğin nesnesi.

## Örnekler



Bir belgenin özel özellikleriyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

ASSERT_EQ(0, properties->get_Count());

// Özel belge özellikleri, belgeye ekleyebileceğimiz anahtar-değer çiftleridir.
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", System::DateTime::get_Today());
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

// Koleksiyon, özel özellikleri alfabetik sıraya göre sıralar.
ASSERT_EQ(1, properties->IndexOf(u"Authorized Amount"));
ASSERT_EQ(5, properties->get_Count());

// Belgedeki tüm özel özellikleri yazdır.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Type(), enumerator->get_Current()->get_Value()) << std::endl;
    }
}

// DOCPROPERTY alanı kullanarak bir özel özelliğin değerini göster.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY \"Authorized By\""));
field->Update();

ASSERT_EQ(u"John Doe", field->get_Result());

// Bu özel özellikleri Microsoft Word'de \"File\" -> \"Properties\" > \"Advanced Properties\" > \"Custom\" yoluyla bulabiliriz.
doc->Save(get_ArtifactsDir() + u"DocumentProperties.DocumentPropertyCollection.docx");

// Aşağıda bir belgeden özel özellikleri kaldırmanın üç yolu verilmiştir.
// 1 -  İndekse göre kaldır:
properties->RemoveAt(1);

ASSERT_FALSE(properties->Contains(u"Authorized Amount"));
ASSERT_EQ(4, properties->get_Count());

// 2 -  İsme göre kaldır:
properties->Remove(u"Authorized Revision");

ASSERT_FALSE(properties->Contains(u"Authorized Revision"));
ASSERT_EQ(3, properties->get_Count());

// 3 -  Tüm koleksiyonu bir kerede boşalt:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Ayrıca Bakınız

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
## CustomDocumentProperties::Add(const System::String\&, const System::String\&) method


Yeni bir özel belge özelliği oluşturur; veri türü [String](../../propertytype/).

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::Add(const System::String &name, const System::String &value)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | const System::String\& | Özelliğin adı. |
| value | const System::String\& | Özelliğin değeri. |

### ReturnValue

Yeni oluşturulan özelliğin nesnesi.

## Örnekler



Bir belgenin özel özellikleriyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

ASSERT_EQ(0, properties->get_Count());

// Özel belge özellikleri, belgeye ekleyebileceğimiz anahtar-değer çiftleridir.
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", System::DateTime::get_Today());
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

// Koleksiyon, özel özellikleri alfabetik sıraya göre sıralar.
ASSERT_EQ(1, properties->IndexOf(u"Authorized Amount"));
ASSERT_EQ(5, properties->get_Count());

// Belgedeki tüm özel özellikleri yazdır.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Type(), enumerator->get_Current()->get_Value()) << std::endl;
    }
}

// DOCPROPERTY alanı kullanarak bir özel özelliğin değerini göster.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY \"Authorized By\""));
field->Update();

ASSERT_EQ(u"John Doe", field->get_Result());

// Bu özel özellikleri Microsoft Word'de \"File\" -> \"Properties\" > \"Advanced Properties\" > \"Custom\" yoluyla bulabiliriz.
doc->Save(get_ArtifactsDir() + u"DocumentProperties.DocumentPropertyCollection.docx");

// Aşağıda bir belgeden özel özellikleri kaldırmanın üç yolu verilmiştir.
// 1 -  İndekse göre kaldır:
properties->RemoveAt(1);

ASSERT_FALSE(properties->Contains(u"Authorized Amount"));
ASSERT_EQ(4, properties->get_Count());

// 2 -  İsme göre kaldır:
properties->Remove(u"Authorized Revision");

ASSERT_FALSE(properties->Contains(u"Authorized Revision"));
ASSERT_EQ(3, properties->get_Count());

// 3 -  Tüm koleksiyonu bir kerede boşalt:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Ayrıca Bakınız

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
## CustomDocumentProperties::Add(const System::String\&, double) method


Yeni bir özel belge özelliği oluşturur; veri türü [Double](../../propertytype/).

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::Add(const System::String &name, double value)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | const System::String\& | Özelliğin adı. |
| value | double | Özelliğin değeri. |

### ReturnValue

Yeni oluşturulan özelliğin nesnesi.

## Örnekler



Bir belgenin özel özellikleriyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

ASSERT_EQ(0, properties->get_Count());

// Özel belge özellikleri, belgeye ekleyebileceğimiz anahtar-değer çiftleridir.
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", System::DateTime::get_Today());
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

// Koleksiyon, özel özellikleri alfabetik sıraya göre sıralar.
ASSERT_EQ(1, properties->IndexOf(u"Authorized Amount"));
ASSERT_EQ(5, properties->get_Count());

// Belgedeki tüm özel özellikleri yazdır.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Type(), enumerator->get_Current()->get_Value()) << std::endl;
    }
}

// DOCPROPERTY alanı kullanarak bir özel özelliğin değerini göster.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY \"Authorized By\""));
field->Update();

ASSERT_EQ(u"John Doe", field->get_Result());

// Bu özel özellikleri Microsoft Word'de \"File\" -> \"Properties\" > \"Advanced Properties\" > \"Custom\" yoluyla bulabiliriz.
doc->Save(get_ArtifactsDir() + u"DocumentProperties.DocumentPropertyCollection.docx");

// Aşağıda bir belgeden özel özellikleri kaldırmanın üç yolu verilmiştir.
// 1 -  İndekse göre kaldır:
properties->RemoveAt(1);

ASSERT_FALSE(properties->Contains(u"Authorized Amount"));
ASSERT_EQ(4, properties->get_Count());

// 2 -  İsme göre kaldır:
properties->Remove(u"Authorized Revision");

ASSERT_FALSE(properties->Contains(u"Authorized Revision"));
ASSERT_EQ(3, properties->get_Count());

// 3 -  Tüm koleksiyonu bir kerede boşalt:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Ayrıca Bakınız

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
## CustomDocumentProperties::Add(const System::String\&, int32_t) method


Yeni bir özel belge özelliği oluşturur; veri türü [Number](../../propertytype/).

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::Add(const System::String &name, int32_t value)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | const System::String\& | Özelliğin adı. |
| value | int32_t | Özelliğin değeri. |

### ReturnValue

Yeni oluşturulan özelliğin nesnesi.

## Örnekler



Bir belgenin özel özellikleriyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

ASSERT_EQ(0, properties->get_Count());

// Özel belge özellikleri, belgeye ekleyebileceğimiz anahtar-değer çiftleridir.
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", System::DateTime::get_Today());
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

// Koleksiyon, özel özellikleri alfabetik sıraya göre sıralar.
ASSERT_EQ(1, properties->IndexOf(u"Authorized Amount"));
ASSERT_EQ(5, properties->get_Count());

// Belgedeki tüm özel özellikleri yazdır.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Type(), enumerator->get_Current()->get_Value()) << std::endl;
    }
}

// DOCPROPERTY alanı kullanarak bir özel özelliğin değerini göster.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY \"Authorized By\""));
field->Update();

ASSERT_EQ(u"John Doe", field->get_Result());

// Bu özel özellikleri Microsoft Word'de \"File\" -> \"Properties\" > \"Advanced Properties\" > \"Custom\" yoluyla bulabiliriz.
doc->Save(get_ArtifactsDir() + u"DocumentProperties.DocumentPropertyCollection.docx");

// Aşağıda bir belgeden özel özellikleri kaldırmanın üç yolu verilmiştir.
// 1 -  İndekse göre kaldır:
properties->RemoveAt(1);

ASSERT_FALSE(properties->Contains(u"Authorized Amount"));
ASSERT_EQ(4, properties->get_Count());

// 2 -  İsme göre kaldır:
properties->Remove(u"Authorized Revision");

ASSERT_FALSE(properties->Contains(u"Authorized Revision"));
ASSERT_EQ(3, properties->get_Count());

// 3 -  Tüm koleksiyonu bir kerede boşalt:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Ayrıca Bakınız

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
## CustomDocumentProperties::Add(const System::String\&, System::DateTime) method


Yeni bir özel belge özelliği oluşturur; veri türü [DateTime](../../propertytype/).

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::Add(const System::String &name, System::DateTime value)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | const System::String\& | Özelliğin adı. |
| value | System::DateTime | Özelliğin değeri. |

### ReturnValue

Yeni oluşturulan özelliğin nesnesi.

## Örnekler



Tarih ve saat içeren bir özel belge özelliğinin nasıl oluşturulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_CustomDocumentProperties()->Add(u"AuthorizationDate", System::DateTime::get_Now());
System::DateTime authorizationDate = doc->get_CustomDocumentProperties()->idx_get(u"AuthorizationDate")->ToDateTime();
std::cout << System::String::Format(u"Document authorized on {0}", authorizationDate) << std::endl;
```


Bir belgenin özel özellikleriyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

ASSERT_EQ(0, properties->get_Count());

// Özel belge özellikleri, belgeye ekleyebileceğimiz anahtar-değer çiftleridir.
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", System::DateTime::get_Today());
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

// Koleksiyon, özel özellikleri alfabetik sıraya göre sıralar.
ASSERT_EQ(1, properties->IndexOf(u"Authorized Amount"));
ASSERT_EQ(5, properties->get_Count());

// Belgedeki tüm özel özellikleri yazdır.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Type(), enumerator->get_Current()->get_Value()) << std::endl;
    }
}

// DOCPROPERTY alanı kullanarak bir özel özelliğin değerini göster.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY \"Authorized By\""));
field->Update();

ASSERT_EQ(u"John Doe", field->get_Result());

// Bu özel özellikleri Microsoft Word'de \"File\" -> \"Properties\" > \"Advanced Properties\" > \"Custom\" yoluyla bulabiliriz.
doc->Save(get_ArtifactsDir() + u"DocumentProperties.DocumentPropertyCollection.docx");

// Aşağıda bir belgeden özel özellikleri kaldırmanın üç yolu verilmiştir.
// 1 -  İndekse göre kaldır:
properties->RemoveAt(1);

ASSERT_FALSE(properties->Contains(u"Authorized Amount"));
ASSERT_EQ(4, properties->get_Count());

// 2 -  İsme göre kaldır:
properties->Remove(u"Authorized Revision");

ASSERT_FALSE(properties->Contains(u"Authorized Revision"));
ASSERT_EQ(3, properties->get_Count());

// 3 -  Tüm koleksiyonu bir kerede boşalt:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Ayrıca Bakınız

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
