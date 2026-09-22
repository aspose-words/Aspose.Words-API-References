---
title: "Aspose::Words::EditableRange::get_EditorGroup yöntemi"
linktitle: "get_EditorGroup"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::EditableRange::get_EditorGroup yöntemi. Mevcut kullanıcının bu düzenlenebilir aralığı düzenleyip düzenleyemeyeceğini belirlemek için kullanılacak bir takma ad (veya düzenleme grubu) döndürür veya ayarlar. C++'ta."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/editablerange/get_editorgroup/
---
## EditableRange::get_EditorGroup method


Bu düzenlenebilir aralığı düzenlemesine izin verilip verilmeyeceğini belirlemek için kullanılacak bir takma ad (veya düzenleme grubu) döndürür veya ayarlar.

```cpp
Aspose::Words::EditorType Aspose::Words::EditableRange::get_EditorGroup()
```

## Açıklamalar


Belirli bir düzenlenebilir aralık için tek kullanıcı ve düzenleyici grubu aynı anda ayarlanamaz; biri ayarlanırsa diğeri temizlenir.

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

* Enum [EditorType](../../editortype/)
* Class [EditableRange](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
