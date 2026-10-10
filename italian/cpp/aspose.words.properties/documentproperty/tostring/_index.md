---
title: "Aspose::Words::Properties::DocumentProperty::ToString metodo"
linktitle: "ToString"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Properties::DocumentProperty::ToString metodo. Restituisce il valore della proprietà come stringa formattata secondo le impostazioni locali correnti in C++."
type: docs
weight: 15000
url: /it/cpp/aspose.words.properties/documentproperty/tostring/
---
## DocumentProperty::ToString method


Restituisce il valore della proprietà come stringa formattata secondo le impostazioni locali correnti.

```cpp
System::String Aspose::Words::Properties::DocumentProperty::ToString() const override
```

## Note


Converte una proprietà booleana in "Y" o "N". Converte una proprietà data in una stringa di data breve. Per tutti gli altri tipi converte una proprietà usando Object.ToString().

## Esempi



Mostra come lavorare con le proprietà personalizzate del documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// Ogni documento contiene una raccolta di proprietà personalizzate, che, come le proprietà integrate, sono coppie chiave-valore.
// Il documento ha un elenco fisso di proprietà integrate. L'utente crea tutte le proprietà personalizzate.
ASSERT_EQ(u"Value of custom document property", System::ObjectExt::ToString(doc->get_CustomDocumentProperties()->idx_get(u"CustomProperty")));

doc->get_CustomDocumentProperties()->Add(u"CustomProperty2", System::String(u"Value of custom document property #2"));

std::cout << "Custom Properties:" << std::endl;
for (auto&& customDocumentProperty : System::IterateOver(doc->get_CustomDocumentProperties()))
{
    std::cout << customDocumentProperty->get_Name() << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", customDocumentProperty->get_Type()) << std::endl;
    std::cout << System::String::Format(u"\tValue:\t\"{0}\"", customDocumentProperty->get_Value()) << std::endl;
}
```


Mostra vari metodi di conversione di tipo delle proprietà di documento personalizzate.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

System::DateTime authDate = System::DateTime::get_Today();
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", authDate);
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

ASPOSE_ASSERT_EQ(true, properties->idx_get(u"Authorized")->ToBool());
ASSERT_EQ(u"John Doe", System::ObjectExt::ToString(properties->idx_get(u"Authorized By")));
ASSERT_EQ(authDate, properties->idx_get(u"Authorized Date")->ToDateTime());
ASSERT_EQ(1, properties->idx_get(u"Authorized Revision")->ToInt());
ASPOSE_ASSERT_EQ(123.45, properties->idx_get(u"Authorized Amount")->ToDouble());
```

## Vedi anche

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
