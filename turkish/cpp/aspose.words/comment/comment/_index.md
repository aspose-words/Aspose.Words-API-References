---
title: "Aspose::Words::Comment::Comment yapıcı"
linktitle: "Yorum"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Comment::Comment yapıcı. C++'ta Comment sınıfının yeni bir örneğini başlatır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/comment/comment/
---
## Comment::Comment(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) constructor


Yeni bir [Comment](../) sınıfı örneği oluşturur.

```cpp
Aspose::Words::Comment::Comment(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| doküman | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Sahip belge. |
## Açıklamalar


Bir [Comment](../) oluşturulduğunda, belirtilen belgeye aittir, ancak henüz belgenin bir parçası değildir ve [ParentNode](../../node/get_parentnode/) **null**'dır.

Belgeye [Comment](../) eklemek için, yorumun eklenmesini istediğiniz paragrafta [InsertAfter1()</see> veya <see cref="Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertBefore1()](../) kullanın.

Bir yorum oluşturduktan sonra, [Author](../get_author/), [Initial](../get_initial/) ve [DateTime](../get_datetime/) özelliklerini ayarlamayı unutmayın.

## Ayrıca Bakınız

* Class [DocumentBase](../../documentbase/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Comment::Comment(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&, const System::String\&, System::DateTime) constructor


Yeni bir [Comment](../) sınıfı örneği oluşturur.

```cpp
Aspose::Words::Comment::Comment(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, const System::String &author, const System::String &initial, System::DateTime dateTime)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| doküman | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Sahip belge. |
| yazar | const System::String\& | Yorumun yazar adı. **null** olamaz. |
| ilk | const System::String\& | Yorumun yazar baş harfleri. **null** olamaz. |
| dateTime | System::DateTime | Yorumun tarih ve saati. |

## Örnekler



Bir paragrafa yorum eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);
builder->MoveTo(comment->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// Microsoft Word'te, belge gövdesindeki bu yoruma sağ tıklayarak düzenleyebilir veya yanıtlayabiliriz.
doc->Save(get_ArtifactsDir() + u"InlineStory.AddComment.docx");
```

## Ayrıca Bakınız

* Class [DocumentBase](../../documentbase/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
