---
title: "Aspose::Words::Fields::FormFieldCollection::idx_get yöntemi"
linktitle: "idx_get"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FormFieldCollection::idx_get yöntemi. C++'ta yer işareti adıyla bir form alanı döndürür."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.fields/formfieldcollection/idx_get/
---
## FormFieldCollection::idx_get(const System::String\&) method


Yer imi adıyla bir form alanını döndürür.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::Fields::FormFieldCollection::idx_get(const System::String &bookmarkName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| bookmarkName | const System::String\& | Büyük/küçük harfe duyarsız yer işareti adı. |

## Ayrıca Bakınız

* Class [FormField](../../formfield/)
* Class [FormFieldCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## FormFieldCollection::idx_get(int32_t) method


Belirtilen indeksteki bir form alanını döndürür.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::Fields::FormFieldCollection::idx_get(int32_t index)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int32_t | Koleksiyona bir indeks. |
## Açıklamalar


İndeks sıfır tabanlıdır.

Negatif indekslere izin verilir ve koleksiyonun sonundan erişimi gösterir. Örneğin -1 son öğeyi, -2 sondan bir önceki öğeyi vb. ifade eder.

İndeks listedeki öğe sayısına eşit veya daha büyükse, bu null referans döndürür.

İndeks negatif ve mutlak değeri listedeki öğe sayısından büyükse, bu null referans döndürür.

## Ayrıca Bakınız

* Class [FormField](../../formfield/)
* Class [FormFieldCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
