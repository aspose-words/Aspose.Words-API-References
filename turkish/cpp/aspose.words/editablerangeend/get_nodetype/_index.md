---
title: "Aspose::Words::EditableRangeEnd::get_NodeType metodu"
linktitle: "get_NodeType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::EditableRangeEnd::get_NodeType metodu. C++'ta EditableRangeEnd'i döndürür."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/editablerangeend/get_nodetype/
---
## EditableRangeEnd::get_NodeType method


Döndürür [EditableRangeEnd](../../nodetype/).

```cpp
Aspose::Words::NodeType Aspose::Words::EditableRangeEnd::get_NodeType() const override
```


## Örnekler



Düzenlenebilir bir aralıkla nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"MyPassword");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(System::String(u"Hello world! Since we have set the document's protection level to read-only,") + u" we cannot edit this paragraph without the password.");

// Düzenlenebilir aralıklar, korumalı belgelerin bölümlerini düzenlemeye açık bırakmamıza olanak tanır.
System::SharedPtr<Aspose::Words::EditableRangeStart> editableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph is inside an editable range, and can be edited.");
System::SharedPtr<Aspose::Words::EditableRangeEnd> editableRangeEnd = builder->EndEditableRange();

// İyi biçimlendirilmiş bir düzenlenebilir aralık bir başlangıç düğümüne ve bir bitiş düğümüne sahiptir.
// Bu düğümlerin eşleşen kimlikleri vardır ve düzenlenebilir düğümleri kapsar.
System::SharedPtr<Aspose::Words::EditableRange> editableRange = editableRangeStart->get_EditableRange();

ASSERT_EQ(editableRangeStart->get_Id(), editableRange->get_Id());
ASSERT_EQ(editableRangeEnd->get_Id(), editableRange->get_Id());

// Düzenlenebilir aralığın farklı bölümleri birbirine bağlanır.
ASSERT_EQ(editableRangeStart->get_Id(), editableRange->get_EditableRangeStart()->get_Id());
ASSERT_EQ(editableRangeStart->get_Id(), editableRangeEnd->get_EditableRangeStart()->get_Id());
ASSERT_EQ(editableRange->get_Id(), editableRangeStart->get_EditableRange()->get_Id());
ASSERT_EQ(editableRangeEnd->get_Id(), editableRange->get_EditableRangeEnd()->get_Id());

// Her bir bölümün düğüm tiplerine şu şekilde erişebiliriz. Düzenlenebilir aralık kendisi bir düğüm değildir,
// ancak bir başlangıç, bir bitiş ve bunların kapsadığı içeriklerden oluşan bir varlıktır.
ASSERT_EQ(Aspose::Words::NodeType::EditableRangeStart, editableRangeStart->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::EditableRangeEnd, editableRangeEnd->get_NodeType());

builder->Writeln(u"This paragraph is outside the editable range, and cannot be edited.");

doc->Save(get_ArtifactsDir() + u"EditableRange.CreateAndRemove.docx");

// Bir düzenlenebilir aralığı kaldırın. Aralık içindeki tüm düğümler bozulmadan kalacaktır.
editableRange->Remove();
```

## Ayrıca Bakınız

* Enum [NodeType](../../nodetype/)
* Class [EditableRangeEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
