---
title: "Aspose::Words::Fields::FieldEQ::AsOfficeMath metodu"
linktitle: "AsOfficeMath"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldEQ::AsOfficeMath yöntemi. C++'ta EQ alanına karşılık gelen Office Math nesnesini döndürür."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fieldeq/asofficemath/
---
## FieldEQ::AsOfficeMath method


EQ alanına karşılık gelen Office [Math](../../../aspose.words.math/) nesnesini döndürür.

```cpp
System::SharedPtr<Aspose::Words::Math::OfficeMath> Aspose::Words::Fields::FieldEQ::AsOfficeMath()
```


### ReturnValue

Alan kodu boş veya geçersiz ise **null** döndürür, aksi takdirde bir [OfficeMath](../../../aspose.words.math/officemath/) örneği.

## Örnekler



EQ alanını Office [Math](../../../aspose.words.math/) ile nasıl değiştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - EQ.docx");
System::SharedPtr<Aspose::Words::Fields::FieldEQ> fieldEQ = doc->get_Range()->get_Fields()->LINQ_OfType<System::SharedPtr<Aspose::Words::Fields::FieldEQ> >()->LINQ_First();

System::SharedPtr<Aspose::Words::Math::OfficeMath> officeMath = fieldEQ->AsOfficeMath();

fieldEQ->get_Start()->get_ParentNode()->InsertBefore<System::SharedPtr<Aspose::Words::Math::OfficeMath>>(officeMath, fieldEQ->get_Start());
fieldEQ->Remove();

doc->Save(get_ArtifactsDir() + u"Field.EQAsOfficeMath.docx");
```

## Ayrıca Bakınız

* Class [OfficeMath](../../../aspose.words.math/officemath/)
* Class [FieldEQ](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
