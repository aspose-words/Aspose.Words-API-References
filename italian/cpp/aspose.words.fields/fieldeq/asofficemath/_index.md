---
title: "Aspose::Words::Fields::FieldEQ::AsOfficeMath metodo"
linktitle: "AsOfficeMath"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldEQ::AsOfficeMath method. Restituisce l'oggetto Office Math corrispondente al campo EQ in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldeq/asofficemath/
---
## FieldEQ::AsOfficeMath method


Restituisce l'oggetto Office [Math](../../../aspose.words.math/) corrispondente al campo EQ.

```cpp
System::SharedPtr<Aspose::Words::Math::OfficeMath> Aspose::Words::Fields::FieldEQ::AsOfficeMath()
```


### ReturnValue

Restituisce **null** se il codice del campo è vuoto o non valido, altrimenti un'istanza di [OfficeMath](../../../aspose.words.math/officemath/).

## Esempi



Mostra come sostituire il campo EQ con Office [Math](../../../aspose.words.math/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - EQ.docx");
System::SharedPtr<Aspose::Words::Fields::FieldEQ> fieldEQ = doc->get_Range()->get_Fields()->LINQ_OfType<System::SharedPtr<Aspose::Words::Fields::FieldEQ> >()->LINQ_First();

System::SharedPtr<Aspose::Words::Math::OfficeMath> officeMath = fieldEQ->AsOfficeMath();

fieldEQ->get_Start()->get_ParentNode()->InsertBefore<System::SharedPtr<Aspose::Words::Math::OfficeMath>>(officeMath, fieldEQ->get_Start());
fieldEQ->Remove();

doc->Save(get_ArtifactsDir() + u"Field.EQAsOfficeMath.docx");
```

## Vedi anche

* Class [OfficeMath](../../../aspose.words.math/officemath/)
* Class [FieldEQ](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
