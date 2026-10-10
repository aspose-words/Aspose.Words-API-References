---
title: "Aspose::Words::Comment::AddReply yöntemi"
linktitle: "AddReply"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Comment::AddReply yöntemi. C++'de bu yoruma bir yanıt ekler."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/comment/addreply/
---
## Comment::AddReply method


Bu yoruma bir yanıt ekler.

```cpp
System::SharedPtr<Aspose::Words::Comment> Aspose::Words::Comment::AddReply(const System::String &author, const System::String &initial, System::DateTime dateTime, const System::String &text)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| yazar | const System::String\& | Yanıt için yazar adı. |
| ilk | const System::String\& | Yanıt için yazar baş harfleri. |
| dateTime | System::DateTime | Yanıt için tarih ve saat. |
| metin | const System::String\& | Yanıt metni. |

### ReturnValue

Yanıt için oluşturulan [Comment](../) düğümü.
## Açıklamalar


Mevcut MS Office sınırlamaları nedeniyle belgede yalnızca 1 düzey yanıt izin verilir.

## Örnekler



Bir belgeye yorum eklemeyi ve ardından ona yanıt vermeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

// Yorumu belgenin gövdesindeki bir düğüme yerleştirin.
// Bu yorum, paragrafının konumunda görünecek,
// sayfanın sağ kenar boşluğunun dışında ve paragrafına noktalı bir çizgiyle bağlanarak.
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Üst yorumun altında görünecek bir yanıt ekleyin.
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");

// Yorumlar ve yanıtlar her ikisi de Comment düğümüdür.
ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Comment, true)->get_Count());

// Diğer yorumlara yanıt vermeyen yorumlar "üst düzey"dir. Bunların üst yorumları yoktur.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_Ancestor()));

// Yanıtların bir üst düzey yorum üst öğesi vardır.
ASPOSE_ASSERT_EQ(comment, comment->get_Replies()->idx_get(0)->get_Ancestor());

doc->Save(get_ArtifactsDir() + u"Comment.AddCommentWithReply.docx");
```

## Ayrıca Bakınız

* Class [Comment](../)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
