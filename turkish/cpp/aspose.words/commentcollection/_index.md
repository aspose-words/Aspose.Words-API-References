---
title: "Aspose::Words::CommentCollection class"
linktitle: "CommentCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::CommentCollection class. Yorum düğümlerinin bir koleksiyonuna tiplenmiş erişim sağlar. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 12000
url: /tr/cpp/aspose.words/commentcollection/
---
## CommentCollection class


Yorum düğümlerinin bir koleksiyonuna tiplenmiş erişim sağlar. Daha fazla bilgi için [Working with Comments](https://docs.aspose.com/words/cpp/working-with-comments/) dokümantasyon makalesini ziyaret edin.

```cpp
class CommentCollection : public Aspose::Words::NodeCollection
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Bir düğümü koleksiyonun sonuna ekler. |
| [Clear](../nodecollection/clear/)() | Bu koleksiyondaki ve belgedeki tüm düğümleri kaldırır. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Bir düğümün koleksiyonda olup olmadığını belirler. |
| [get_Count](../nodecollection/get_count/)() | Koleksiyondaki düğüm sayısını alır. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | Düğümlerin koleksiyonu üzerinde basit bir "foreach" tarzı yineleme sağlar. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Verilen indeksteki bir [Comment](../comment/) alır. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Belirtilen düğümün sıfır tabanlı indeksini döndürür. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Belirtilen indeksde bir düğümü koleksiyona ekler. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Düğümü koleksiyondan ve belgeden kaldırır. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Belirtilen indeksteki düğümü koleksiyondan ve belgeden kaldırır. |
| [ToArray](../nodecollection/toarray/)() | Koleksiyondaki tüm düğümleri yeni bir düğüm dizisine kopyalar. |
| static [Type](./type/)() |  |

## Örnekler



Bir yorumu "done" olarak işaretlemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Helo world!");

// Bir hatayı göstermek için bir yorum ekleyin.
auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Fix the spelling error!");
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Yorumların "Done" bayrağı vardır ve varsayılan olarak "false" olarak ayarlanır.
// Bir yorum, belgede bir değişiklik yapmamızı öneriyorsa,
// değişikliği uygulayabilir ve ardından düzeltmeyi göstermek için "Done" bayrağını da ayarlayabiliriz.
ASSERT_FALSE(comment->get_Done());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Hello world!");
comment->set_Done(true);

// "done" olan yorumlar kendilerini farklılaştıracaktır.
// "done" olmayanlardan soluk bir metin rengiyle.
comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Add text to this paragraph.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

doc->Save(get_ArtifactsDir() + u"Comment.Done.docx");
```

## Ayrıca Bakınız

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
