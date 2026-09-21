---
title: "Aspose::Words::Layout::CommentDisplayMode enum"
linktitle: "CommentDisplayMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Layout::CommentDisplayMode enum. Anger renderingsläget för dokumentkommentarer i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.layout/commentdisplaymode/
---
## CommentDisplayMode enum


Anger renderingsläget för dokumentkommentarer.

```cpp
enum class CommentDisplayMode
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Dölj | 0 | Inga dokumentkommentarer renderas. |
| ShowInBalloons | 1 | Renderar dokumentkommentarer i ballonger i marginalen. Detta är standardvärdet. |
| ShowInAnnotations | 2 | Renderar dokumentkommentarer i annotationer. Detta är endast tillgängligt för Pdf-format. |


## Exempel



Visar hur man visar kommentarer när man sparar ett dokument till ett renderat format.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// ShowInAnnotations är endast tillgängligt i Pdf1.7- och Pdf1.5-format.
// I andra format kommer det att fungera på liknande sätt som Dölj.
doc->get_LayoutOptions()->set_CommentDisplayMode(Aspose::Words::Layout::CommentDisplayMode::ShowInAnnotations);

doc->Save(get_ArtifactsDir() + u"Document.ShowCommentsInAnnotations.pdf");

// Observera att det krävs att bygga om dokumentets sidlayout (via Document.UpdatePageLayout() metod)
// efter att ha ändrat värdena för Document.LayoutOptions.
doc->get_LayoutOptions()->set_CommentDisplayMode(Aspose::Words::Layout::CommentDisplayMode::ShowInBalloons);
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.ShowCommentsInBalloons.pdf");
```

## Se även

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
