---
title: "Aspose::Words::DocumentBuilder::EndColumnBookmark method"
linktitle: "EndColumnBookmark"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::EndColumnBookmark yöntemi. Belgedeki mevcut konumu bir sütun yer imi sonu olarak işaretler. Konum C++'ta bir tablo hücresinde olmalıdır."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/documentbuilder/endcolumnbookmark/
---
## DocumentBuilder::EndColumnBookmark method


Belgedeki mevcut konumu bir sütun yer imi sonu olarak işaretler. Konum bir tablo hücresinde olmalıdır.

```cpp
System::SharedPtr<Aspose::Words::BookmarkEnd> Aspose::Words::DocumentBuilder::EndColumnBookmark(const System::String &bookmarkName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| bookmarkName | const System::String\& | Yer iminin adı. |

### ReturnValue

Az önce oluşturulan yer imi son düğümü.
## Açıklamalar


Bir sütun yer imi, bir dizi satır içinde bir veya daha fazla sütunu kapsar. Geçerli bir yer imi oluşturmak için aynı *bookmarkName* parametresiyle hem [StartColumnBookmark()](../) hem de [EndColumnBookmark()](../) yöntemlerini çağırmanız gerekir.

Kötü biçimlendirilmiş yer imleri veya aynı ada sahip yer imleri belge kaydedildiğinde yok sayılacaktır.

Eklenen [BookmarkEnd](../../bookmarkend/) düğümünün gerçek konumu, mevcut belge oluşturucu konumundan farklı olabilir.

## Örnekler



Sütun yer işaretinin nasıl oluşturulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

builder->InsertCell();
// 1,2,4,5 hücreleri yer işaretlenecek.
builder->StartColumnBookmark(u"MyBookmark_1");
// Kötü biçimlendirilmiş yer imleri veya aynı ada sahip yer imleri belge kaydedildiğinde yok sayılacaktır.
builder->StartColumnBookmark(u"MyBookmark_1");
builder->StartColumnBookmark(u"BadStartBookmark");
builder->Write(u"Cell 1");

builder->InsertCell();
builder->Write(u"Cell 2");

builder->InsertCell();
builder->Write(u"Cell 3");

builder->EndRow();

builder->InsertCell();
builder->Write(u"Cell 4");

builder->InsertCell();
builder->Write(u"Cell 5");
builder->EndColumnBookmark(u"MyBookmark_1");
builder->EndColumnBookmark(u"MyBookmark_1");

ASSERT_THROW(static_cast<std::function<void()>>([&builder]() -> void
{
    builder->EndColumnBookmark(u"BadEndBookmark");

builder->InsertCell();
builder->Write(u"Cell 6");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"Bookmarks.CreateColumnBookmark.docx");
```

## Ayrıca Bakınız

* Class [BookmarkEnd](../../bookmarkend/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
