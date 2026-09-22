---
title: "Aspose::Words::Fields::FormField::RemoveField metodu"
linktitle: "RemoveField"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FormField::RemoveField metodu. C++'de sadece form alanı özel karakteri değil, tüm form alanını kaldırır."
type: docs
weight: 27000
url: /tr/cpp/aspose.words.fields/formfield/removefield/
---
## FormField::RemoveField method


Form alanının özel karakteri değil, tamamını kaldırır.

```cpp
void Aspose::Words::Fields::FormField::RemoveField()
```


## Örnekler



Bir form alanının nasıl silineceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Form fields.docx");

System::SharedPtr<Aspose::Words::Fields::FormField> formField = doc->get_Range()->get_FormFields()->idx_get(3);
formField->RemoveField();
```

## Ayrıca Bakınız

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
