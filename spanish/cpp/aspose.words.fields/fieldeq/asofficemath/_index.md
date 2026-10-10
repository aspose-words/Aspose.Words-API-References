---
title: "Aspose::Words::Fields::FieldEQ::AsOfficeMath método"
linktitle: "AsOfficeMath"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldEQ::AsOfficeMath método. Devuelve el objeto Office Math correspondiente al campo EQ en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/fieldeq/asofficemath/
---
## FieldEQ::AsOfficeMath method


Devuelve el objeto Office [Math](../../../aspose.words.math/) correspondiente al campo EQ.

```cpp
System::SharedPtr<Aspose::Words::Math::OfficeMath> Aspose::Words::Fields::FieldEQ::AsOfficeMath()
```


### ReturnValue

Devuelve **null** si el código del campo está vacío o es inválido, de lo contrario una instancia de [OfficeMath](../../../aspose.words.math/officemath/).

## Ejemplos



Muestra cómo reemplazar el campo EQ con Office [Math](../../../aspose.words.math/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - EQ.docx");
System::SharedPtr<Aspose::Words::Fields::FieldEQ> fieldEQ = doc->get_Range()->get_Fields()->LINQ_OfType<System::SharedPtr<Aspose::Words::Fields::FieldEQ> >()->LINQ_First();

System::SharedPtr<Aspose::Words::Math::OfficeMath> officeMath = fieldEQ->AsOfficeMath();

fieldEQ->get_Start()->get_ParentNode()->InsertBefore<System::SharedPtr<Aspose::Words::Math::OfficeMath>>(officeMath, fieldEQ->get_Start());
fieldEQ->Remove();

doc->Save(get_ArtifactsDir() + u"Field.EQAsOfficeMath.docx");
```

## Ver también

* Class [OfficeMath](../../../aspose.words.math/officemath/)
* Class [FieldEQ](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
