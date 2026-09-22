---
title: "Aspose::Words::Fields::FieldIndex::get_PageRangeSeparator yöntemi"
linktitle: "get_PageRangeSeparator"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldIndex::get_PageRangeSeparator yöntemi. C++'ta bir sayfa aralığının başlangıç ve bitişini ayırmak için kullanılan karakter dizisini alır veya ayarlar."
type: docs
weight: 13000
url: /tr/cpp/aspose.words.fields/fieldindex/get_pagerangeseparator/
---
## FieldIndex::get_PageRangeSeparator method


Sayfa aralığının başlangıç ve sonunu ayırmak için kullanılan karakter dizisini alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_PageRangeSeparator()
```


## Örnekler



Bir INDEX alanı girişi için yer iminin kapsadığı sayfaları sayfa aralığı olarak nasıl belirteceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Belgedeki her XE alanı için bir giriş gösteren bir INDEX alanı oluşturun.
// Her giriş, XE alanının Text özelliği değerini sol tarafta gösterir,
// ve XE alanını içeren sayfanın numarasını sağ tarafta.
// INDEX girişi, "Text" özelliğinde eşleşen değerlere sahip tüm XE alanlarını toplayacaktır
// her XE alanı için ayrı bir giriş oluşturmak yerine tek bir girişte birleştirir.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Sayfa aralıklarını gösteren INDEX girişleri için bir ayırıcı dize belirtebiliriz
// bu, ilk sayfanın numarası ile son sayfanın numarası arasında görünecektir.
index->set_PageNumberSeparator(u", on page(s) ");
index->set_PageRangeSeparator(u" to ");

ASSERT_EQ(u" INDEX  \\e \", on page(s) \" \\g \" to \"", index->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"My entry");

// Bir XE alanı, PageRangeBookmarkName özelliğini kullanarak bir yer imi adlandırırsa,
// INDEX girişi, yer iminin kapsadığı sayfa aralığını gösterecektir
// XE alanını içeren sayfanın numarası yerine.
indexEntry->set_PageRangeBookmarkName(u"MyBookmark");

ASSERT_EQ(u" XE  \"My entry\" \\r MyBookmark", indexEntry->GetFieldCode());
ASSERT_EQ(u"MyBookmark", indexEntry->get_PageRangeBookmarkName());

// Sayfa 3'te başlayan ve sayfa 5'te sona eren bir yer imi ekleyin.
// Bu yer imine referans veren XE alanı için INDEX girişi bu sayfa aralığını gösterecektir.
// Tablomuzda, INDEX girişi "My entry, on page(s) 3 to 5" görüntülenecektir.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Start of MyBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"End of MyBookmark");
builder->EndBookmark(u"MyBookmark");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.PageRangeBookmark.docx");
```

## Ayrıca Bakınız

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
