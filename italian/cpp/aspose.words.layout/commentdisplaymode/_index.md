---
title: "Aspose::Words::Layout::CommentDisplayMode enum"
linktitle: "CommentDisplayMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Layout::CommentDisplayMode enum. Specifica la modalità di rendering per i commenti del documento in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.layout/commentdisplaymode/
---
## CommentDisplayMode enum


Specifica la modalità di rendering per i commenti del documento.

```cpp
enum class CommentDisplayMode
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Hide | 0 | Nessun commento del documento viene renderizzato. |
| ShowInBalloons | 1 | Renderizza i commenti del documento in balloon nel margine. Questo è il valore predefinito. |
| ShowInAnnotations | 2 | Renderizza i commenti del documento in annotazioni. Questo è disponibile solo per il formato Pdf. |


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

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
