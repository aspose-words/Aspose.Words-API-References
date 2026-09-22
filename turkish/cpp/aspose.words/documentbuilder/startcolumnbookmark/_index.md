---
title: "Aspose::Words::DocumentBuilder::StartColumnBookmark method"
linktitle: "StartColumnBookmark"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::StartColumnBookmark yöntemi. Belgedeki mevcut konumu bir sütun yer imi başlangıcı olarak işaretler. Konum C++'ta bir tablo hücresi içinde olmalıdır."
type: docs
weight: 69000
url: /tr/cpp/aspose.words/documentbuilder/startcolumnbookmark/
---
## DocumentBuilder::StartColumnBookmark method


Belgedeki mevcut konumu bir sütun yer imi başlangıcı olarak işaretler. Konum bir tablo hücresinde olmalıdır.

```cpp
System::SharedPtr<Aspose::Words::BookmarkStart> Aspose::Words::DocumentBuilder::StartColumnBookmark(const System::String &bookmarkName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| bookmarkName | const System::String\& | Yer iminin adı. |

### ReturnValue

Yeni oluşturulan yer imi başlangıç düğümü.
## Açıklamalar


Bir sütun yer imi, bir dizi satır içinde bir veya daha fazla sütunu kapsar. Geçerli bir yer imi oluşturmak için aynı *bookmarkName* parametresiyle hem [StartColumnBookmark()](../) hem de [EndColumnBookmark()](../) yöntemlerini çağırmanız gerekir.

Kötü biçimlendirilmiş yer imleri veya aynı ada sahip yer imleri belge kaydedildiğinde yok sayılacaktır.

Eklenen [BookmarkStart](../../bookmarkstart/) düğümünün gerçek konumu, mevcut belge oluşturucu konumundan farklı olabilir.

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

* Class [BookmarkStart](../../bookmarkstart/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
