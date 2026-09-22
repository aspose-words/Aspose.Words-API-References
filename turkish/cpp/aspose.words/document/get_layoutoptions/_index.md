---
title: "Aspose::Words::Document::get_LayoutOptions metodu"
linktitle: "get_LayoutOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_LayoutOptions metodu. Bu belgenin yerleşim sürecini kontrol etmek için seçenekleri temsil eden bir LayoutOptions nesnesini C++'ta alır."
type: docs
weight: 36000
url: /tr/cpp/aspose.words/document/get_layoutoptions/
---
## Document::get_LayoutOptions method


Bu belgenin yerleşim sürecini kontrol etmek için seçenekleri temsil eden bir [LayoutOptions](../../../aspose.words.layout/layoutoptions/) nesnesi alır.

```cpp
System::SharedPtr<Aspose::Words::Layout::LayoutOptions> Aspose::Words::Document::get_LayoutOptions() const
```


## Örnekler



Bir oluşturulmuş çıktı belgesinde metnin nasıl gizleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Gizli metni ekleyin, ardından bunu oluşturulmuş bir belgeden çıkarıp çıkarmak istemediğinizi belirtin.
builder->Writeln(u"This text is not hidden.");
builder->get_Font()->set_Hidden(true);
builder->Writeln(u"This text is hidden.");

doc->get_LayoutOptions()->set_ShowHiddenText(showHiddenText);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsHiddenText.pdf");
```


Bir oluşturulmuş çıktı belgesinde paragraf işaretlerinin nasıl gösterileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bazı paragraflar ekleyin, ardından paragraf işaretlerini etkinleştirerek paragrafların sonlarını gösterin
// belgeyi oluşturduğumuzda pilcrow (¶) sembolüyle.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

doc->get_LayoutOptions()->set_ShowParagraphMarks(showParagraphMarks);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsParagraphMarks.pdf");
```


Bir oluşturulmuş çıktı belgesinde revizyonların görünümünün nasıl değiştirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir revizyon ekleyin, ardından tüm revizyonların rengini yeşile değiştirin.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Her revize edilmiş satırın solunda görünen çubuğu kaldırın.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## Ayrıca Bakınız

* Class [LayoutOptions](../../../aspose.words.layout/layoutoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
