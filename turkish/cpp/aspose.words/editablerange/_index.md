---
title: "Aspose::Words::EditableRange class"
linktitle: "EditableRange"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::EditableRange sınıfı. Tek bir düzenlenebilir aralığı temsil eder. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 24000
url: /tr/cpp/aspose.words/editablerange/
---
## EditableRange class


Tek bir düzenlenebilir aralığı temsil eder. Daha fazla bilgi edinmek için [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) dokümantasyon makalesini ziyaret edin.

```cpp
class EditableRange : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_EditableRangeEnd](./get_editablerangeend/)() | Düzenlenebilir aralığın sonunu temsil eden düğümü alır. |
| [get_EditableRangeStart](./get_editablerangestart/)() const | Düzenlenebilir aralığın başlangıcını temsil eden düğümü alır. |
| [get_EditorGroup](./get_editorgroup/)() | Bu düzenlenebilir aralığı düzenlemesine izin verilip verilmeyeceğini belirlemek için kullanılacak bir takma ad (veya düzenleme grubu) döndürür veya ayarlar. |
| [get_Id](./get_id/)() | Düzenlenebilir aralık tanımlayıcısını alır. |
| [get_SingleUser](./get_singleuser/)() | Düzenlenebilir aralık için tek kullanıcıyı döndürür veya ayarlar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Düzenlenebilir aralığı belgeden kaldırır. Düzenlenebilir aralık içindeki içeriği kaldırmaz. |
| [set_EditorGroup](./set_editorgroup/)(Aspose::Words::EditorType) | Ayarlayıcı: [Aspose::Words::EditableRange::get_EditorGroup](./get_editorgroup/). |
| [set_SingleUser](./set_singleuser/)(const System::String\&) | Ayarlayıcı: [Aspose::Words::EditableRange::get_SingleUser](./get_singleuser/). |
| static [Type](./type/)() |  |
## Açıklamalar


[EditableRange](./) is a "facade" object that encapsulates two nodes [EditableRangeStart](./get_editablerangestart/) and [EditableRangeEnd](./get_editablerangeend/) in a document tree and allows to work with an editable range as a single object.

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
