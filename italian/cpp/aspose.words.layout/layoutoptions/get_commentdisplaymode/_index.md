---
title: "Metodo Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode"
linktitle: "get_CommentDisplayMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode. Ottiene o imposta il modo in cui i commenti vengono visualizzati. Il valore predefinito è ShowInBalloons in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.layout/layoutoptions/get_commentdisplaymode/
---
## LayoutOptions::get_CommentDisplayMode method


Ottiene o imposta il modo in cui i commenti vengono visualizzati. Il valore predefinito è [ShowInBalloons](../../commentdisplaymode/).

```cpp
Aspose::Words::Layout::CommentDisplayMode Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode() const
```


## Esempi



Mostra come visualizzare i commenti durante il salvataggio di un documento in un formato renderizzato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// ShowInAnnotations è disponibile solo nei formati Pdf1.7 e Pdf1.5.
// In altri formati, funzionerà in modo simile a Hide.
doc->get_LayoutOptions()->set_CommentDisplayMode(Aspose::Words::Layout::CommentDisplayMode::ShowInAnnotations);

doc->Save(get_ArtifactsDir() + u"Document.ShowCommentsInAnnotations.pdf");

// Nota che è necessario ricostruire il layout della pagina del documento (tramite il metodo Document.UpdatePageLayout())
// dopo aver modificato i valori di Document.LayoutOptions.
doc->get_LayoutOptions()->set_CommentDisplayMode(Aspose::Words::Layout::CommentDisplayMode::ShowInBalloons);
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.ShowCommentsInBalloons.pdf");
```

## Vedi anche

* Enum [CommentDisplayMode](../../commentdisplaymode/)
* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
