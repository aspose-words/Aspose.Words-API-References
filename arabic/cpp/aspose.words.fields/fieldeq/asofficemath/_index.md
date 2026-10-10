---
title: "Aspose::Words::Fields::FieldEQ::AsOfficeMath طريقة"
linktitle: "AsOfficeMath"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldEQ::AsOfficeMath. تُرجع كائن Office Math المقابل لحقل EQ في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fieldeq/asofficemath/
---
## FieldEQ::AsOfficeMath method


تُرجع كائن Office [Math](../../../aspose.words.math/) المقابل لحقل EQ.

```cpp
System::SharedPtr<Aspose::Words::Math::OfficeMath> Aspose::Words::Fields::FieldEQ::AsOfficeMath()
```


### ReturnValue

تُرجع **null** إذا كان رمز الحقل فارغًا أو غير صالح، وإلا تُرجع مثيلًا من [OfficeMath](../../../aspose.words.math/officemath/).

## أمثلة



يوضح كيفية استبدال حقل EQ بـ Office [Math](../../../aspose.words.math/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - EQ.docx");
System::SharedPtr<Aspose::Words::Fields::FieldEQ> fieldEQ = doc->get_Range()->get_Fields()->LINQ_OfType<System::SharedPtr<Aspose::Words::Fields::FieldEQ> >()->LINQ_First();

System::SharedPtr<Aspose::Words::Math::OfficeMath> officeMath = fieldEQ->AsOfficeMath();

fieldEQ->get_Start()->get_ParentNode()->InsertBefore<System::SharedPtr<Aspose::Words::Math::OfficeMath>>(officeMath, fieldEQ->get_Start());
fieldEQ->Remove();

doc->Save(get_ArtifactsDir() + u"Field.EQAsOfficeMath.docx");
```

## انظر أيضًا

* Class [OfficeMath](../../../aspose.words.math/officemath/)
* Class [FieldEQ](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
