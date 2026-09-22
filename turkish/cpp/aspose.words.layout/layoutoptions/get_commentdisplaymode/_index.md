---
title: "Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode metodu"
linktitle: "get_CommentDisplayMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode metodu. Yorumların nasıl görüntüleneceğini alır veya ayarlar. Varsayılan değer C++'ta ShowInBalloons'dir."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.layout/layoutoptions/get_commentdisplaymode/
---
## LayoutOptions::get_CommentDisplayMode method


Yorumların nasıl görüntüleneceğini alır veya ayarlar. Varsayılan değer [ShowInBalloons](../../commentdisplaymode/)'dır.

```cpp
Aspose::Words::Layout::CommentDisplayMode Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode() const
```


## Örnekler



Bir belgeyi işlenmiş bir formata kaydederken yorumların nasıl gösterileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// ShowInAnnotations yalnızca Pdf1.7 ve Pdf1.5 formatlarında mevcuttur.
// Diğer formatlarda, Hide gibi çalışacaktır.
doc->get_LayoutOptions()->set_CommentDisplayMode(Aspose::Words::Layout::CommentDisplayMode::ShowInAnnotations);

doc->Save(get_ArtifactsDir() + u"Document.ShowCommentsInAnnotations.pdf");

// Belge sayfa düzeninin (Document.UpdatePageLayout() yöntemiyle) yeniden oluşturulmasının gerektiğini unutmayın.
// Document.LayoutOptions değerleri değiştirildikten sonra.
doc->get_LayoutOptions()->set_CommentDisplayMode(Aspose::Words::Layout::CommentDisplayMode::ShowInBalloons);
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.ShowCommentsInBalloons.pdf");
```

## Ayrıca Bakınız

* Enum [CommentDisplayMode](../../commentdisplaymode/)
* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
