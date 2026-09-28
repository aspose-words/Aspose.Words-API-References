---
title: "Aspose::Words::Fields::FieldEQ::AsOfficeMath метод"
linktitle: "AsOfficeMath"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldEQ::AsOfficeMath метод. Возвращает объект Office Math, соответствующий полю EQ в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fieldeq/asofficemath/
---
## FieldEQ::AsOfficeMath method


Возвращает объект Office [Math](../../../aspose.words.math/) , соответствующий полю EQ.

```cpp
System::SharedPtr<Aspose::Words::Math::OfficeMath> Aspose::Words::Fields::FieldEQ::AsOfficeMath()
```


### ReturnValue

Возвращает **null**, если код поля пустой или недействительный, в противном случае — экземпляр [OfficeMath](../../../aspose.words.math/officemath/).

## Примеры



Показывает, как заменить поле EQ объектом Office [Math](../../../aspose.words.math/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - EQ.docx");
System::SharedPtr<Aspose::Words::Fields::FieldEQ> fieldEQ = doc->get_Range()->get_Fields()->LINQ_OfType<System::SharedPtr<Aspose::Words::Fields::FieldEQ> >()->LINQ_First();

System::SharedPtr<Aspose::Words::Math::OfficeMath> officeMath = fieldEQ->AsOfficeMath();

fieldEQ->get_Start()->get_ParentNode()->InsertBefore<System::SharedPtr<Aspose::Words::Math::OfficeMath>>(officeMath, fieldEQ->get_Start());
fieldEQ->Remove();

doc->Save(get_ArtifactsDir() + u"Field.EQAsOfficeMath.docx");
```

## См. также

* Class [OfficeMath](../../../aspose.words.math/officemath/)
* Class [FieldEQ](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
