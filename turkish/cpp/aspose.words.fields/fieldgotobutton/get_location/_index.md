---
title: "Aspose::Words::Fields::FieldGoToButton::get_Location metodu"
linktitle: "get_Location"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldGoToButton::get_Location metodu. C++'ta bir yer iminin, sayfa numarasının veya atlanacak başka bir öğenin adını alır veya ayarlar."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.fields/fieldgotobutton/get_location/
---
## FieldGoToButton::get_Location method


Atlanacak bir yer imi, sayfa numarası veya başka bir öğenin adını alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldGoToButton::get_Location()
```


## Örnekler



GOTOBUTTON alanının nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir GOTOBUTTON alanı ekleyin. Microsoft Word'de bu alana çift tıkladığımızda,
// İmleç, Location özelliğinin başvurduğu yer iminin adına götürülür.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldGoToButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldGoToButton, true));
field->set_DisplayText(u"My Button");
field->set_Location(u"MyBookmark");

ASSERT_EQ(u" GOTOBUTTON  MyBookmark My Button", field->GetFieldCode());

// Alan tarafından başvurulacak geçerli bir yer imi ekleyin.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(field->get_Location());
builder->Writeln(u"Bookmark text contents.");
builder->EndBookmark(field->get_Location());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.GOTOBUTTON.docx");
```

## Ayrıca Bakınız

* Class [FieldGoToButton](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
