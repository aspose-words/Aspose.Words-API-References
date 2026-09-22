---
title: "Aspose::Words::Layout::CommentDisplayMode enum"
linktitle: "CommentDisplayMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout::CommentDisplayMode enum. C++'ta belge yorumları için işleme modunu belirtir."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.layout/commentdisplaymode/
---
## CommentDisplayMode enum


Belge yorumları için render modunu belirtir.

```cpp
enum class CommentDisplayMode
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Hide | 0 | Belge yorumları işlenmez. |
| ShowInBalloons | 1 | Belge yorumlarını kenarda balon içinde işler. Bu varsayılan değerdir. |
| ShowInAnnotations | 2 | Belge yorumlarını ek açıklamalarda işler. Bu yalnızca Pdf formatı için mevcuttur. |


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

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
