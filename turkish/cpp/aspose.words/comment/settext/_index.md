---
title: "Aspose::Words::Comment::SetText metodu"
linktitle: "SetText"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Comment::SetText yöntemi. Bu, C++'ta yorumun metnini kolayca ayarlamayı sağlayan bir kolaylık yöntemidir."
type: docs
weight: 22000
url: /tr/cpp/aspose.words/comment/settext/
---
## Comment::SetText method


Bu, yorum metnini kolayca ayarlamayı sağlayan bir kolaylık yöntemidir.

```cpp
void Aspose::Words::Comment::SetText(const System::String &text)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| metin | const System::String\& | Yorumun yeni metni. |
## Açıklamalar


Bu yöntem, bir dizeden yorumun metnini hızlıca ayarlamayı sağlar. Dize paragraf sonları içerebilir, bu da yorum içinde metin paragrafları oluşturur. Yorum içine yer işaretleri veya tablolar gibi daha karmaşık öğeler eklemek veya zengin biçimlendirme uygulamak istiyorsanız, yorum metnini oluşturmak için uygun düğüm sınıflarını kullanmanız gerekir.

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
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
