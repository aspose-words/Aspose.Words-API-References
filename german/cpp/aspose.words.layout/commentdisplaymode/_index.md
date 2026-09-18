---
title: "Aspose::Words::Layout::CommentDisplayMode Enum"
linktitle: "CommentDisplayMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Layout::CommentDisplayMode Enum. Gibt den Rendermodus für Dokumentkommentare in C++ an."
type: docs
weight: 7000
url: /de/cpp/aspose.words.layout/commentdisplaymode/
---
## CommentDisplayMode enum


Gibt den Rendermodus für Dokumentkommentare an.

```cpp
enum class CommentDisplayMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Ausblenden | 0 | Es werden keine Dokumentkommentare gerendert. |
| ShowInBalloons | 1 | Rendert Dokumentkommentare in Ballons im Rand. Dies ist der Standardwert. |
| ShowInAnnotations | 2 | Rendert Dokumentkommentare in Anmerkungen. Dies ist nur für das PDF-Format verfügbar. |


## Beispiele



Zeigt, wie Kommentare beim Speichern eines Dokuments in ein gerendertes Format angezeigt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// ShowInAnnotations ist nur in den Formaten Pdf1.7 und Pdf1.5 verfügbar.
// In anderen Formaten funktioniert es ähnlich wie Hide.
doc->get_LayoutOptions()->set_CommentDisplayMode(Aspose::Words::Layout::CommentDisplayMode::ShowInAnnotations);

doc->Save(get_ArtifactsDir() + u"Document.ShowCommentsInAnnotations.pdf");

// Beachten Sie, dass es erforderlich ist, das Seitenlayout des Dokuments neu zu erstellen (über die Methode Document.UpdatePageLayout()).
// nach dem Ändern der Werte von Document.LayoutOptions.
doc->get_LayoutOptions()->set_CommentDisplayMode(Aspose::Words::Layout::CommentDisplayMode::ShowInBalloons);
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.ShowCommentsInBalloons.pdf");
```

## Siehe auch

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
