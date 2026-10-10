---
title: "Aspose::Words::Fields::FieldRef::get_BookmarkName yöntemi"
linktitle: "get_BookmarkName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldRef::get_BookmarkName yöntemi. C++'de başvurulan yer işaretinin adını alır veya ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fieldref/get_bookmarkname/
---
## FieldRef::get_BookmarkName method


Referans alınan yer işaretinin adını alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldRef::get_BookmarkName()
```


## Örnekler



SET alanı ile yer işaretli metin oluşturmayı ve ardından REF alanı kullanarak belge içinde görüntülemeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Yer işaretli metni bir SET alanı ile adlandırın.
// Bu alan, metin içinde görünen bir yer işareti yapısı değil, adlandırılmış bir değişken olan "bookmark"a referans verir.
auto fieldSet = System::ExplicitCast<Aspose::Words::Fields::FieldSet>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSet, false));
fieldSet->set_BookmarkName(u"MyBookmark");
fieldSet->set_BookmarkText(u"Hello world!");
fieldSet->Update();

ASSERT_EQ(u" SET  MyBookmark \"Hello world!\"", fieldSet->GetFieldCode());

// REF alanında yer işaretine adını kullanarak referans verin ve içeriğini gösterin.
auto fieldRef = System::ExplicitCast<Aspose::Words::Fields::FieldRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRef, true));
fieldRef->set_BookmarkName(u"MyBookmark");
fieldRef->Update();

ASSERT_EQ(u" REF  MyBookmark", fieldRef->GetFieldCode());
ASSERT_EQ(u"Hello world!", fieldRef->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.SET.REF.docx");
```

## Ayrıca Bakınız

* Class [FieldRef](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
