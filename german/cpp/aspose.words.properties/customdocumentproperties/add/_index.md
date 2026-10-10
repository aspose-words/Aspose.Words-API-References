---
title: "Aspose::Words::Properties::CustomDocumentProperties::Add Methode"
linktitle: "Add"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::CustomDocumentProperties::Add Methode. Erstellt eine neue benutzerdefinierte Dokumenteigenschaft des Datentyps Boolean in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.properties/customdocumentproperties/add/
---
## CustomDocumentProperties::Add(const System::String\&, bool) method


Erstellt eine neue benutzerdefinierte Dokumenteigenschaft des [Boolean](../../propertytype/) Datentyps.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::Add(const System::String &name, bool value)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | const System::String\& | Der Name der Eigenschaft. |
| Wert | bool | Der Wert der Eigenschaft. |

### ReturnValue

Das neu erstellte Eigenschaftsobjekt.

## Beispiele



Zeigt, wie man mit den benutzerdefinierten Eigenschaften eines Dokuments arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

ASSERT_EQ(0, properties->get_Count());

// Benutzerdefinierte Dokumenteigenschaften sind Schlüssel‑Wert‑Paare, die wir dem Dokument hinzufügen können.
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", System::DateTime::get_Today());
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

// Die Sammlung sortiert die benutzerdefinierten Eigenschaften alphabetisch.
ASSERT_EQ(1, properties->IndexOf(u"Authorized Amount"));
ASSERT_EQ(5, properties->get_Count());

// Gibt jede benutzerdefinierte Eigenschaft im Dokument aus.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Type(), enumerator->get_Current()->get_Value()) << std::endl;
    }
}

// Zeigt den Wert einer benutzerdefinierten Eigenschaft mithilfe eines DOCPROPERTY‑Feldes an.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY \"Authorized By\""));
field->Update();

ASSERT_EQ(u"John Doe", field->get_Result());

// Wir können diese benutzerdefinierten Eigenschaften in Microsoft Word über \"Datei\" -> \"Eigenschaften\" > \"Erweiterte Eigenschaften\" > \"Benutzerdefiniert\" finden.
doc->Save(get_ArtifactsDir() + u"DocumentProperties.DocumentPropertyCollection.docx");

// Im Folgenden sind drei Möglichkeiten zum Entfernen benutzerdefinierter Eigenschaften aus einem Dokument aufgeführt.
// 1 -  Entfernen nach Index:
properties->RemoveAt(1);

ASSERT_FALSE(properties->Contains(u"Authorized Amount"));
ASSERT_EQ(4, properties->get_Count());

// 2 -  Entfernen nach Name:
properties->Remove(u"Authorized Revision");

ASSERT_FALSE(properties->Contains(u"Authorized Revision"));
ASSERT_EQ(3, properties->get_Count());

// 3 -  Die gesamte Sammlung auf einmal leeren:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Siehe auch

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
## CustomDocumentProperties::Add(const System::String\&, const System::String\&) method


Erstellt eine neue benutzerdefinierte Dokumenteigenschaft des [String](../../propertytype/) Datentyps.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::Add(const System::String &name, const System::String &value)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | const System::String\& | Der Name der Eigenschaft. |
| Wert | const System::String\& | Der Wert der Eigenschaft. |

### ReturnValue

Das neu erstellte Eigenschaftsobjekt.

## Beispiele



Zeigt, wie man mit den benutzerdefinierten Eigenschaften eines Dokuments arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

ASSERT_EQ(0, properties->get_Count());

// Benutzerdefinierte Dokumenteigenschaften sind Schlüssel‑Wert‑Paare, die wir dem Dokument hinzufügen können.
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", System::DateTime::get_Today());
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

// Die Sammlung sortiert die benutzerdefinierten Eigenschaften alphabetisch.
ASSERT_EQ(1, properties->IndexOf(u"Authorized Amount"));
ASSERT_EQ(5, properties->get_Count());

// Gibt jede benutzerdefinierte Eigenschaft im Dokument aus.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Type(), enumerator->get_Current()->get_Value()) << std::endl;
    }
}

// Zeigt den Wert einer benutzerdefinierten Eigenschaft mithilfe eines DOCPROPERTY‑Feldes an.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY \"Authorized By\""));
field->Update();

ASSERT_EQ(u"John Doe", field->get_Result());

// Wir können diese benutzerdefinierten Eigenschaften in Microsoft Word über \"Datei\" -> \"Eigenschaften\" > \"Erweiterte Eigenschaften\" > \"Benutzerdefiniert\" finden.
doc->Save(get_ArtifactsDir() + u"DocumentProperties.DocumentPropertyCollection.docx");

// Im Folgenden sind drei Möglichkeiten zum Entfernen benutzerdefinierter Eigenschaften aus einem Dokument aufgeführt.
// 1 -  Entfernen nach Index:
properties->RemoveAt(1);

ASSERT_FALSE(properties->Contains(u"Authorized Amount"));
ASSERT_EQ(4, properties->get_Count());

// 2 -  Entfernen nach Name:
properties->Remove(u"Authorized Revision");

ASSERT_FALSE(properties->Contains(u"Authorized Revision"));
ASSERT_EQ(3, properties->get_Count());

// 3 -  Die gesamte Sammlung auf einmal leeren:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Siehe auch

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
## CustomDocumentProperties::Add(const System::String\&, double) method


Erstellt eine neue benutzerdefinierte Dokumenteigenschaft des [Double](../../propertytype/) Datentyps.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::Add(const System::String &name, double value)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | const System::String\& | Der Name der Eigenschaft. |
| Wert | double | Der Wert der Eigenschaft. |

### ReturnValue

Das neu erstellte Eigenschaftsobjekt.

## Beispiele



Zeigt, wie man mit den benutzerdefinierten Eigenschaften eines Dokuments arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

ASSERT_EQ(0, properties->get_Count());

// Benutzerdefinierte Dokumenteigenschaften sind Schlüssel‑Wert‑Paare, die wir dem Dokument hinzufügen können.
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", System::DateTime::get_Today());
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

// Die Sammlung sortiert die benutzerdefinierten Eigenschaften alphabetisch.
ASSERT_EQ(1, properties->IndexOf(u"Authorized Amount"));
ASSERT_EQ(5, properties->get_Count());

// Gibt jede benutzerdefinierte Eigenschaft im Dokument aus.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Type(), enumerator->get_Current()->get_Value()) << std::endl;
    }
}

// Zeigt den Wert einer benutzerdefinierten Eigenschaft mithilfe eines DOCPROPERTY‑Feldes an.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY \"Authorized By\""));
field->Update();

ASSERT_EQ(u"John Doe", field->get_Result());

// Wir können diese benutzerdefinierten Eigenschaften in Microsoft Word über \"Datei\" -> \"Eigenschaften\" > \"Erweiterte Eigenschaften\" > \"Benutzerdefiniert\" finden.
doc->Save(get_ArtifactsDir() + u"DocumentProperties.DocumentPropertyCollection.docx");

// Im Folgenden sind drei Möglichkeiten zum Entfernen benutzerdefinierter Eigenschaften aus einem Dokument aufgeführt.
// 1 -  Entfernen nach Index:
properties->RemoveAt(1);

ASSERT_FALSE(properties->Contains(u"Authorized Amount"));
ASSERT_EQ(4, properties->get_Count());

// 2 -  Entfernen nach Name:
properties->Remove(u"Authorized Revision");

ASSERT_FALSE(properties->Contains(u"Authorized Revision"));
ASSERT_EQ(3, properties->get_Count());

// 3 -  Die gesamte Sammlung auf einmal leeren:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Siehe auch

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
## CustomDocumentProperties::Add(const System::String\&, int32_t) method


Erstellt eine neue benutzerdefinierte Dokumenteigenschaft des [Number](../../propertytype/) Datentyps.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::Add(const System::String &name, int32_t value)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | const System::String\& | Der Name der Eigenschaft. |
| Wert | int32_t | Der Wert der Eigenschaft. |

### ReturnValue

Das neu erstellte Eigenschaftsobjekt.

## Beispiele



Zeigt, wie man mit den benutzerdefinierten Eigenschaften eines Dokuments arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

ASSERT_EQ(0, properties->get_Count());

// Benutzerdefinierte Dokumenteigenschaften sind Schlüssel‑Wert‑Paare, die wir dem Dokument hinzufügen können.
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", System::DateTime::get_Today());
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

// Die Sammlung sortiert die benutzerdefinierten Eigenschaften alphabetisch.
ASSERT_EQ(1, properties->IndexOf(u"Authorized Amount"));
ASSERT_EQ(5, properties->get_Count());

// Gibt jede benutzerdefinierte Eigenschaft im Dokument aus.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Type(), enumerator->get_Current()->get_Value()) << std::endl;
    }
}

// Zeigt den Wert einer benutzerdefinierten Eigenschaft mithilfe eines DOCPROPERTY‑Feldes an.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY \"Authorized By\""));
field->Update();

ASSERT_EQ(u"John Doe", field->get_Result());

// Wir können diese benutzerdefinierten Eigenschaften in Microsoft Word über \"Datei\" -> \"Eigenschaften\" > \"Erweiterte Eigenschaften\" > \"Benutzerdefiniert\" finden.
doc->Save(get_ArtifactsDir() + u"DocumentProperties.DocumentPropertyCollection.docx");

// Im Folgenden sind drei Möglichkeiten zum Entfernen benutzerdefinierter Eigenschaften aus einem Dokument aufgeführt.
// 1 -  Entfernen nach Index:
properties->RemoveAt(1);

ASSERT_FALSE(properties->Contains(u"Authorized Amount"));
ASSERT_EQ(4, properties->get_Count());

// 2 -  Entfernen nach Name:
properties->Remove(u"Authorized Revision");

ASSERT_FALSE(properties->Contains(u"Authorized Revision"));
ASSERT_EQ(3, properties->get_Count());

// 3 -  Die gesamte Sammlung auf einmal leeren:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Siehe auch

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
## CustomDocumentProperties::Add(const System::String\&, System::DateTime) method


Erstellt eine neue benutzerdefinierte Dokumenteigenschaft des [DateTime](../../propertytype/) Datentyps.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::Add(const System::String &name, System::DateTime value)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | const System::String\& | Der Name der Eigenschaft. |
| Wert | System::DateTime | Der Wert der Eigenschaft. |

### ReturnValue

Das neu erstellte Eigenschaftsobjekt.

## Beispiele



Zeigt, wie man eine benutzerdefinierte Dokumenteigenschaft erstellt, die ein Datum und eine Uhrzeit enthält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_CustomDocumentProperties()->Add(u"AuthorizationDate", System::DateTime::get_Now());
System::DateTime authorizationDate = doc->get_CustomDocumentProperties()->idx_get(u"AuthorizationDate")->ToDateTime();
std::cout << System::String::Format(u"Document authorized on {0}", authorizationDate) << std::endl;
```


Zeigt, wie man mit den benutzerdefinierten Eigenschaften eines Dokuments arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

ASSERT_EQ(0, properties->get_Count());

// Benutzerdefinierte Dokumenteigenschaften sind Schlüssel‑Wert‑Paare, die wir dem Dokument hinzufügen können.
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", System::DateTime::get_Today());
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

// Die Sammlung sortiert die benutzerdefinierten Eigenschaften alphabetisch.
ASSERT_EQ(1, properties->IndexOf(u"Authorized Amount"));
ASSERT_EQ(5, properties->get_Count());

// Gibt jede benutzerdefinierte Eigenschaft im Dokument aus.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Type(), enumerator->get_Current()->get_Value()) << std::endl;
    }
}

// Zeigt den Wert einer benutzerdefinierten Eigenschaft mithilfe eines DOCPROPERTY‑Feldes an.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY \"Authorized By\""));
field->Update();

ASSERT_EQ(u"John Doe", field->get_Result());

// Wir können diese benutzerdefinierten Eigenschaften in Microsoft Word über \"Datei\" -> \"Eigenschaften\" > \"Erweiterte Eigenschaften\" > \"Benutzerdefiniert\" finden.
doc->Save(get_ArtifactsDir() + u"DocumentProperties.DocumentPropertyCollection.docx");

// Im Folgenden sind drei Möglichkeiten zum Entfernen benutzerdefinierter Eigenschaften aus einem Dokument aufgeführt.
// 1 -  Entfernen nach Index:
properties->RemoveAt(1);

ASSERT_FALSE(properties->Contains(u"Authorized Amount"));
ASSERT_EQ(4, properties->get_Count());

// 2 -  Entfernen nach Name:
properties->Remove(u"Authorized Revision");

ASSERT_FALSE(properties->Contains(u"Authorized Revision"));
ASSERT_EQ(3, properties->get_Count());

// 3 -  Die gesamte Sammlung auf einmal leeren:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Siehe auch

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
