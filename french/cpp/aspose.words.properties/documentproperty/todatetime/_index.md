---
title: "Aspose::Words::Properties::DocumentProperty::ToDateTime méthode"
linktitle: "ToDateTime"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Properties::DocumentProperty::ToDateTime méthode. Retourne la valeur de la propriété en tant que DateTime en UTC en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words.properties/documentproperty/todatetime/
---
## DocumentProperty::ToDateTime method


Renvoie la valeur de la propriété en tant que **DateTime** en UTC.

```cpp
System::DateTime Aspose::Words::Properties::DocumentProperty::ToDateTime()
```

## Remarques


Lance une exception si le type de propriété n'est pas [DateTime](../../propertytype/).

Microsoft Word ne stocke que la partie date (pas d'heure) pour les propriétés de date personnalisées.

## Exemples



Montre comment créer une propriété de document personnalisée qui contient une date et une heure.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_CustomDocumentProperties()->Add(u"AuthorizationDate", System::DateTime::get_Now());
System::DateTime authorizationDate = doc->get_CustomDocumentProperties()->idx_get(u"AuthorizationDate")->ToDateTime();
std::cout << System::String::Format(u"Document authorized on {0}", authorizationDate) << std::endl;
```


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
