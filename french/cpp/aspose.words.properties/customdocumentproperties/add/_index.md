---
title: "Aspose::Words::Properties::CustomDocumentProperties::Add méthode"
linktitle: "Add"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Properties::CustomDocumentProperties::Add méthode. Crée une nouvelle propriété de document personnalisée de type de données Boolean en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.properties/customdocumentproperties/add/
---
## CustomDocumentProperties::Add(const System::String\&, bool) method


Crée une nouvelle propriété de document personnalisée du type de données [Boolean](../../propertytype/).

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::Add(const System::String &name, bool value)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| name | const System::String\& | Le nom de la propriété. |
| value | bool | La valeur de la propriété. |

### ReturnValue

L'objet de propriété nouvellement créé.

## Exemples



Montre comment travailler avec les propriétés personnalisées d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

ASSERT_EQ(0, properties->get_Count());

// Les propriétés personnalisées du document sont des paires clé-valeur que nous pouvons ajouter au document.
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", System::DateTime::get_Today());
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

// La collection trie les propriétés personnalisées par ordre alphabétique.
ASSERT_EQ(1, properties->IndexOf(u"Authorized Amount"));
ASSERT_EQ(5, properties->get_Count());

// Imprime chaque propriété personnalisée du document.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Type(), enumerator->get_Current()->get_Value()) << std::endl;
    }
}

// Affiche la valeur d'une propriété personnalisée à l'aide d'un champ DOCPROPERTY.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY \"Authorized By\""));
field->Update();

ASSERT_EQ(u"John Doe", field->get_Result());

// Nous pouvons trouver ces propriétés personnalisées dans Microsoft Word via "Fichier" -> "Propriétés" > "Propriétés avancées" > "Personnalisées".
doc->Save(get_ArtifactsDir() + u"DocumentProperties.DocumentPropertyCollection.docx");

// Voici trois façons de supprimer les propriétés personnalisées d'un document.
// 1 -  Supprimer par indice :
properties->RemoveAt(1);

ASSERT_FALSE(properties->Contains(u"Authorized Amount"));
ASSERT_EQ(4, properties->get_Count());

// 2 -  Supprimer par nom:
properties->Remove(u"Authorized Revision");

ASSERT_FALSE(properties->Contains(u"Authorized Revision"));
ASSERT_EQ(3, properties->get_Count());

// 3 -  Vider la collection entière d'un coup:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Voir aussi

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
## CustomDocumentProperties::Add(const System::String\&, const System::String\&) method


Crée une nouvelle propriété de document personnalisée du type de données [String](../../propertytype/).

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::Add(const System::String &name, const System::String &value)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| name | const System::String\& | Le nom de la propriété. |
| value | const System::String\& | La valeur de la propriété. |

### ReturnValue

L'objet de propriété nouvellement créé.

## Exemples



Montre comment travailler avec les propriétés personnalisées d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

ASSERT_EQ(0, properties->get_Count());

// Les propriétés personnalisées du document sont des paires clé-valeur que nous pouvons ajouter au document.
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", System::DateTime::get_Today());
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

// La collection trie les propriétés personnalisées par ordre alphabétique.
ASSERT_EQ(1, properties->IndexOf(u"Authorized Amount"));
ASSERT_EQ(5, properties->get_Count());

// Imprime chaque propriété personnalisée du document.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Type(), enumerator->get_Current()->get_Value()) << std::endl;
    }
}

// Affiche la valeur d'une propriété personnalisée à l'aide d'un champ DOCPROPERTY.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY \"Authorized By\""));
field->Update();

ASSERT_EQ(u"John Doe", field->get_Result());

// Nous pouvons trouver ces propriétés personnalisées dans Microsoft Word via "Fichier" -> "Propriétés" > "Propriétés avancées" > "Personnalisées".
doc->Save(get_ArtifactsDir() + u"DocumentProperties.DocumentPropertyCollection.docx");

// Voici trois façons de supprimer les propriétés personnalisées d'un document.
// 1 -  Supprimer par indice :
properties->RemoveAt(1);

ASSERT_FALSE(properties->Contains(u"Authorized Amount"));
ASSERT_EQ(4, properties->get_Count());

// 2 -  Supprimer par nom:
properties->Remove(u"Authorized Revision");

ASSERT_FALSE(properties->Contains(u"Authorized Revision"));
ASSERT_EQ(3, properties->get_Count());

// 3 -  Vider la collection entière d'un coup:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Voir aussi

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
## CustomDocumentProperties::Add(const System::String\&, double) method


Crée une nouvelle propriété de document personnalisée du type de données [Double](../../propertytype/).

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::Add(const System::String &name, double value)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| name | const System::String\& | Le nom de la propriété. |
| value | double | La valeur de la propriété. |

### ReturnValue

L'objet de propriété nouvellement créé.

## Exemples



Montre comment travailler avec les propriétés personnalisées d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

ASSERT_EQ(0, properties->get_Count());

// Les propriétés personnalisées du document sont des paires clé-valeur que nous pouvons ajouter au document.
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", System::DateTime::get_Today());
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

// La collection trie les propriétés personnalisées par ordre alphabétique.
ASSERT_EQ(1, properties->IndexOf(u"Authorized Amount"));
ASSERT_EQ(5, properties->get_Count());

// Imprime chaque propriété personnalisée du document.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Type(), enumerator->get_Current()->get_Value()) << std::endl;
    }
}

// Affiche la valeur d'une propriété personnalisée à l'aide d'un champ DOCPROPERTY.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY \"Authorized By\""));
field->Update();

ASSERT_EQ(u"John Doe", field->get_Result());

// Nous pouvons trouver ces propriétés personnalisées dans Microsoft Word via "Fichier" -> "Propriétés" > "Propriétés avancées" > "Personnalisées".
doc->Save(get_ArtifactsDir() + u"DocumentProperties.DocumentPropertyCollection.docx");

// Voici trois façons de supprimer les propriétés personnalisées d'un document.
// 1 -  Supprimer par indice :
properties->RemoveAt(1);

ASSERT_FALSE(properties->Contains(u"Authorized Amount"));
ASSERT_EQ(4, properties->get_Count());

// 2 -  Supprimer par nom:
properties->Remove(u"Authorized Revision");

ASSERT_FALSE(properties->Contains(u"Authorized Revision"));
ASSERT_EQ(3, properties->get_Count());

// 3 -  Vider la collection entière d'un coup:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Voir aussi

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
## CustomDocumentProperties::Add(const System::String\&, int32_t) method


Crée une nouvelle propriété de document personnalisée du type de données [Number](../../propertytype/).

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::Add(const System::String &name, int32_t value)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| name | const System::String\& | Le nom de la propriété. |
| value | int32_t | La valeur de la propriété. |

### ReturnValue

L'objet de propriété nouvellement créé.

## Exemples



Montre comment travailler avec les propriétés personnalisées d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

ASSERT_EQ(0, properties->get_Count());

// Les propriétés personnalisées du document sont des paires clé-valeur que nous pouvons ajouter au document.
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", System::DateTime::get_Today());
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

// La collection trie les propriétés personnalisées par ordre alphabétique.
ASSERT_EQ(1, properties->IndexOf(u"Authorized Amount"));
ASSERT_EQ(5, properties->get_Count());

// Imprime chaque propriété personnalisée du document.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Type(), enumerator->get_Current()->get_Value()) << std::endl;
    }
}

// Affiche la valeur d'une propriété personnalisée à l'aide d'un champ DOCPROPERTY.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY \"Authorized By\""));
field->Update();

ASSERT_EQ(u"John Doe", field->get_Result());

// Nous pouvons trouver ces propriétés personnalisées dans Microsoft Word via "Fichier" -> "Propriétés" > "Propriétés avancées" > "Personnalisées".
doc->Save(get_ArtifactsDir() + u"DocumentProperties.DocumentPropertyCollection.docx");

// Voici trois façons de supprimer les propriétés personnalisées d'un document.
// 1 -  Supprimer par indice :
properties->RemoveAt(1);

ASSERT_FALSE(properties->Contains(u"Authorized Amount"));
ASSERT_EQ(4, properties->get_Count());

// 2 -  Supprimer par nom:
properties->Remove(u"Authorized Revision");

ASSERT_FALSE(properties->Contains(u"Authorized Revision"));
ASSERT_EQ(3, properties->get_Count());

// 3 -  Vider la collection entière d'un coup:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Voir aussi

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
## CustomDocumentProperties::Add(const System::String\&, System::DateTime) method


Crée une nouvelle propriété de document personnalisée du type de données [DateTime](../../propertytype/).

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::Add(const System::String &name, System::DateTime value)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| name | const System::String\& | Le nom de la propriété. |
| value | System::DateTime | La valeur de la propriété. |

### ReturnValue

L'objet de propriété nouvellement créé.

## Exemples



Montre comment créer une propriété de document personnalisée qui contient une date et une heure.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_CustomDocumentProperties()->Add(u"AuthorizationDate", System::DateTime::get_Now());
System::DateTime authorizationDate = doc->get_CustomDocumentProperties()->idx_get(u"AuthorizationDate")->ToDateTime();
std::cout << System::String::Format(u"Document authorized on {0}", authorizationDate) << std::endl;
```


Montre comment travailler avec les propriétés personnalisées d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

ASSERT_EQ(0, properties->get_Count());

// Les propriétés personnalisées du document sont des paires clé-valeur que nous pouvons ajouter au document.
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", System::DateTime::get_Today());
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

// La collection trie les propriétés personnalisées par ordre alphabétique.
ASSERT_EQ(1, properties->IndexOf(u"Authorized Amount"));
ASSERT_EQ(5, properties->get_Count());

// Imprime chaque propriété personnalisée du document.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Type(), enumerator->get_Current()->get_Value()) << std::endl;
    }
}

// Affiche la valeur d'une propriété personnalisée à l'aide d'un champ DOCPROPERTY.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY \"Authorized By\""));
field->Update();

ASSERT_EQ(u"John Doe", field->get_Result());

// Nous pouvons trouver ces propriétés personnalisées dans Microsoft Word via "Fichier" -> "Propriétés" > "Propriétés avancées" > "Personnalisées".
doc->Save(get_ArtifactsDir() + u"DocumentProperties.DocumentPropertyCollection.docx");

// Voici trois façons de supprimer les propriétés personnalisées d'un document.
// 1 -  Supprimer par indice :
properties->RemoveAt(1);

ASSERT_FALSE(properties->Contains(u"Authorized Amount"));
ASSERT_EQ(4, properties->get_Count());

// 2 -  Supprimer par nom:
properties->Remove(u"Authorized Revision");

ASSERT_FALSE(properties->Contains(u"Authorized Revision"));
ASSERT_EQ(3, properties->get_Count());

// 3 -  Vider la collection entière d'un coup:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Voir aussi

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
