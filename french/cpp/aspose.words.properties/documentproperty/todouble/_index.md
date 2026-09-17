---
title: "Aspose::Words::Properties::DocumentProperty::ToDouble méthode"
linktitle: "ToDouble"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Properties::DocumentProperty::ToDouble méthode. Retourne la valeur de la propriété en tant que double en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words.properties/documentproperty/todouble/
---
## DocumentProperty::ToDouble method


Renvoie la valeur de la propriété en tant que double.

```cpp
double Aspose::Words::Properties::DocumentProperty::ToDouble()
```


## Exemples



Présente diverses méthodes de conversion de type des propriétés de document personnalisées.
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

## Voir aussi

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
