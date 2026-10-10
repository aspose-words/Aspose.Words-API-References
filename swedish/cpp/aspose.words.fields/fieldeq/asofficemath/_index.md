---
title: "Aspose::Words::Fields::FieldEQ::AsOfficeMath metod"
linktitle: "AsOfficeMath"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldEQ::AsOfficeMath metod. Returnerar Office Math-objekt som motsvarar EQ-fältet i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fieldeq/asofficemath/
---
## FieldEQ::AsOfficeMath method


Returnerar Office [Math](../../../aspose.words.math/) objekt som motsvarar EQ-fältet.

```cpp
System::SharedPtr<Aspose::Words::Math::OfficeMath> Aspose::Words::Fields::FieldEQ::AsOfficeMath()
```


### ReturnValue

Returnerar **null** om fältkoden är tom eller ogiltig, annars en [OfficeMath](../../../aspose.words.math/officemath/) instans.

## Exempel



Visar hur man ersätter EQ-fältet med Office [Math](../../../aspose.words.math/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - EQ.docx");
System::SharedPtr<Aspose::Words::Fields::FieldEQ> fieldEQ = doc->get_Range()->get_Fields()->LINQ_OfType<System::SharedPtr<Aspose::Words::Fields::FieldEQ> >()->LINQ_First();

System::SharedPtr<Aspose::Words::Math::OfficeMath> officeMath = fieldEQ->AsOfficeMath();

fieldEQ->get_Start()->get_ParentNode()->InsertBefore<System::SharedPtr<Aspose::Words::Math::OfficeMath>>(officeMath, fieldEQ->get_Start());
fieldEQ->Remove();

doc->Save(get_ArtifactsDir() + u"Field.EQAsOfficeMath.docx");
```

## Se även

* Class [OfficeMath](../../../aspose.words.math/officemath/)
* Class [FieldEQ](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
