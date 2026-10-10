---
title: "Aspose::Words::DocumentBuilder::StartBookmark yöntemi"
linktitle: "StartBookmark"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::StartBookmark yöntemi. Belgede mevcut konumu bir yer imi başlangıcı olarak işaretler C++'ta."
type: docs
weight: 68000
url: /tr/cpp/aspose.words/documentbuilder/startbookmark/
---
## DocumentBuilder::StartBookmark method


Belgedeki mevcut konumu bir yer imi başlangıcı olarak işaretler.

```cpp
System::SharedPtr<Aspose::Words::BookmarkStart> Aspose::Words::DocumentBuilder::StartBookmark(const System::String &bookmarkName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| bookmarkName | const System::String\& | Yer iminin adı. |

### ReturnValue

Yeni oluşturulan yer imi başlangıç düğümü.
## Açıklamalar


Bir belgede yer imleri çakışabilir ve herhangi bir aralığı kapsayabilir. Geçerli bir yer imi oluşturmak için aynı *bookmarkName* parametresiyle hem [StartBookmark()](../) hem de [EndBookmark()](../) metodunu çağırmanız gerekir.

Kötü biçimlendirilmiş yer imleri veya aynı ada sahip yer imleri belge kaydedildiğinde yok sayılacaktır.

## Örnekler



Bir yer iminin nasıl oluşturulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Geçerli bir yer imi, belge gövde metninin şu şekilde çevrelenmesini gerektirir
// Eşleşen bir yer imi adıyla oluşturulan BookmarkStart ve BookmarkEnd düğümleri.
builder->StartBookmark(u"MyBookmark");
builder->Writeln(u"Hello world!");
builder->EndBookmark(u"MyBookmark");

ASSERT_EQ(1, doc->get_Range()->get_Bookmarks()->get_Count());
ASSERT_EQ(u"MyBookmark", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Name());
ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Text().Trim());
```


Yerel bir yer imi referans veren bir köprünün nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartBookmark(u"Bookmark1");
builder->Write(u"Bookmarked text. ");
builder->EndBookmark(u"Bookmark1");
builder->Writeln(u"Text outside of the bookmark.");

// Yer imiyle bağlantı kuran bir HYPERLINK alanı ekleyin. Alan anahtarlarını
// "InsertHyperlink" metoduna, referans verilen yer iminin adını içeren argümanın bir parçası olarak geçirebiliriz.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
auto hyperlink = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertHyperlink(u"Link to Bookmark1", u"Bookmark1", true));
hyperlink->set_ScreenTip(u"Hyperlink Tip");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

## Ayrıca Bakınız

* Class [BookmarkStart](../../bookmarkstart/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
