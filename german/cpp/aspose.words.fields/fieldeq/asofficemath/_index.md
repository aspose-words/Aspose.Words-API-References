---
title: "Aspose::Words::Fields::FieldEQ::AsOfficeMath Methode"
linktitle: "AsOfficeMath"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldEQ::AsOfficeMath Methode. Gibt das Office‑Math‑Objekt zurück, das dem EQ‑Feld in C++ entspricht."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fieldeq/asofficemath/
---
## FieldEQ::AsOfficeMath method


Gibt das Office [Math](../../../aspose.words.math/) Objekt zurück, das dem EQ‑Feld entspricht.

```cpp
System::SharedPtr<Aspose::Words::Math::OfficeMath> Aspose::Words::Fields::FieldEQ::AsOfficeMath()
```


### ReturnValue

Gibt **null** zurück, wenn der Feldcode leer oder ungültig ist, andernfalls eine [OfficeMath](../../../aspose.words.math/officemath/) Instanz.

## Beispiele



Zeigt, wie das EQ‑Feld durch Office [Math](../../../aspose.words.math/) ersetzt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - EQ.docx");
System::SharedPtr<Aspose::Words::Fields::FieldEQ> fieldEQ = doc->get_Range()->get_Fields()->LINQ_OfType<System::SharedPtr<Aspose::Words::Fields::FieldEQ> >()->LINQ_First();

System::SharedPtr<Aspose::Words::Math::OfficeMath> officeMath = fieldEQ->AsOfficeMath();

fieldEQ->get_Start()->get_ParentNode()->InsertBefore<System::SharedPtr<Aspose::Words::Math::OfficeMath>>(officeMath, fieldEQ->get_Start());
fieldEQ->Remove();

doc->Save(get_ArtifactsDir() + u"Field.EQAsOfficeMath.docx");
```

## Siehe auch

* Class [OfficeMath](../../../aspose.words.math/officemath/)
* Class [FieldEQ](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
