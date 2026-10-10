---
title: "Aspose::Words::DocumentBuilder::EndEditableRange method"
linktitle: "EndEditableRange"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::EndEditableRange yöntemi. Belgedeki mevcut konumu C++'ta düzenlenebilir bir aralık sonu olarak işaretler."
type: docs
weight: 6000
url: /tr/cpp/aspose.words/documentbuilder/endeditablerange/
---
## DocumentBuilder::EndEditableRange() method


Belgedeki mevcut konumu düzenlenebilir bir aralık sonu olarak işaretler.

```cpp
System::SharedPtr<Aspose::Words::EditableRangeEnd> Aspose::Words::DocumentBuilder::EndEditableRange()
```


### ReturnValue

Yeni oluşturulan düzenlenebilir aralık son düğümü.
## Açıklamalar


Bir belgedeki düzenlenebilir aralık üst üste gelebilir ve herhangi bir aralığı kapsayabilir. Geçerli bir düzenlenebilir aralık oluşturmak için hem [StartEditableRange](../starteditablerange/) hem de [EndEditableRange](./) ya da [EndEditableRange()](../) yöntemlerini çağırmanız gerekir.

Kötü biçimlendirilmiş düzenlenebilir aralık, belge kaydedildiğinde yok sayılır.

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

* Class [EditableRangeEnd](../../editablerangeend/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::EndEditableRange(const System::SharedPtr\<Aspose::Words::EditableRangeStart\>\&) method


Belgedeki mevcut konumu düzenlenebilir bir aralık sonu olarak işaretler.

```cpp
System::SharedPtr<Aspose::Words::EditableRangeEnd> Aspose::Words::DocumentBuilder::EndEditableRange(const System::SharedPtr<Aspose::Words::EditableRangeStart> &start)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| başlat | const System::SharedPtr\<Aspose::Words::EditableRangeStart\>\& | Bu düzenlenebilir aralık başlangıcı. |

### ReturnValue

Yeni oluşturulan düzenlenebilir aralık son düğümü.
## Açıklamalar


İç içe düzenlenebilir aralıklar oluştururken bu aşırı yüklemeyi kullanın.

Bir belgedeki düzenlenebilir aralık üst üste gelebilir ve herhangi bir aralığı kapsayabilir. Geçerli bir düzenlenebilir aralık oluşturmak için hem [StartEditableRange](../starteditablerange/) hem de [EndEditableRange](./) ya da [EndEditableRange()](../) yöntemlerini çağırmanız gerekir.

Kötü biçimlendirilmiş düzenlenebilir aralık, belge kaydedildiğinde yok sayılır.

## Örnekler



İç içe düzenlenebilir aralıkların nasıl oluşturulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"MyPassword");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(System::String(u"Hello world! Since we have set the document's protection level to read-only, ") + u"we cannot edit this paragraph without the password.");

// İki iç içe düzenlenebilir aralık oluşturun.
System::SharedPtr<Aspose::Words::EditableRangeStart> outerEditableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph inside the outer editable range and can be edited.");

System::SharedPtr<Aspose::Words::EditableRangeStart> innerEditableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph inside both the outer and inner editable ranges and can be edited.");

// Şu anda, belge oluşturucunun düğüm ekleme imleci birden fazla devam eden düzenlenebilir aralık içinde.
// Bu durumda bir düzenlenebilir aralığı sonlandırmak istediğimizde,
// Hangi aralığı sonlandırmak istediğimizi, onun EditableRangeStart düğümünü geçirerek belirtmemiz gerekir.
builder->EndEditableRange(innerEditableRangeStart);

builder->Writeln(u"This paragraph inside the outer editable range and can be edited.");

builder->EndEditableRange(outerEditableRangeStart);

builder->Writeln(u"This paragraph is outside any editable ranges, and cannot be edited.");

// Bir metin bölgesi, belirtilen gruplara sahip iki üst üste gelen düzenlenebilir aralığa sahipse,
// Her iki grup tarafından dışlanan kullanıcıların birleşik grubu, metni düzenlemesinden engellenir.
outerEditableRangeStart->get_EditableRange()->set_EditorGroup(Aspose::Words::EditorType::Everyone);
innerEditableRangeStart->get_EditableRange()->set_EditorGroup(Aspose::Words::EditorType::Contributors);

doc->Save(get_ArtifactsDir() + u"EditableRange.Nested.docx");
```

## Ayrıca Bakınız

* Class [EditableRangeEnd](../../editablerangeend/)
* Class [EditableRangeStart](../../editablerangestart/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
