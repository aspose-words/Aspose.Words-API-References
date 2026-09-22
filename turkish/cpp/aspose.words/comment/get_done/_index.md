---
title: "Aspose::Words::Comment::get_Done metodu"
linktitle: "get_Done"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Comment::get_Done metodu. Yorumun C++'da tamamlandı olarak işaretlenip işaretlenmediğini gösteren bayrağı alır veya ayarlar."
type: docs
weight: 8000
url: /tr/cpp/aspose.words/comment/get_done/
---
## Comment::get_Done method


Yorumun tamamlandı olarak işaretlenip işaretlenmediğini gösteren bayrağı alır veya ayarlar.

```cpp
bool Aspose::Words::Comment::get_Done() const
```


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

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
