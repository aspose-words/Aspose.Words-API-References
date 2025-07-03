---
title: Aspose::Words::Fields::FieldEQ::AsOfficeMath method
linktitle: AsOfficeMath
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldEQ::AsOfficeMath method. Returns Office Math object corresponded to the EQ field in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fields/fieldeq/asofficemath/
---
## FieldEQ::AsOfficeMath method


Returns Office [Math](../../../aspose.words.math/) object corresponded to the EQ field.

```cpp
System::SharedPtr<Aspose::Words::Math::OfficeMath> Aspose::Words::Fields::FieldEQ::AsOfficeMath()
```


### ReturnValue

Returns **null** if field code is empty or invalid, otherwise an [OfficeMath](../../../aspose.words.math/officemath/) instance.

## Examples



Shows how to replace the EQ field with Office [Math](../../../aspose.words.math/). 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - EQ.docx");
System::SharedPtr<Aspose::Words::Fields::FieldEQ> fieldEQ = doc->get_Range()->get_Fields()->LINQ_OfType<System::SharedPtr<Aspose::Words::Fields::FieldEQ> >()->LINQ_First();

System::SharedPtr<Aspose::Words::Math::OfficeMath> officeMath = fieldEQ->AsOfficeMath();

fieldEQ->get_Start()->get_ParentNode()->InsertBefore<System::SharedPtr<Aspose::Words::Math::OfficeMath>>(officeMath, fieldEQ->get_Start());
fieldEQ->Remove();

doc->Save(get_ArtifactsDir() + u"Field.EQAsOfficeMath.docx");
```

## See Also

* Class [OfficeMath](../../../aspose.words.math/officemath/)
* Class [FieldEQ](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
