---
title: "Méthode Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode"
linktitle: "get_CommentDisplayMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode. Obtient ou définit la façon dont les commentaires sont rendus. La valeur par défaut est ShowInBalloons en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.layout/layoutoptions/get_commentdisplaymode/
---
## LayoutOptions::get_CommentDisplayMode method


Obtient ou définit la façon dont les commentaires sont rendus. La valeur par défaut est [ShowInBalloons](../../commentdisplaymode/).

```cpp
Aspose::Words::Layout::CommentDisplayMode Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode() const
```


## Exemples



Montre comment afficher les commentaires lors de l'enregistrement d'un document dans un format rendu.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// ShowInAnnotations n'est disponible que dans les formats Pdf1.7 et Pdf1.5.
// Dans les autres formats, cela fonctionnera de manière similaire à Hide.
doc->get_LayoutOptions()->set_CommentDisplayMode(Aspose::Words::Layout::CommentDisplayMode::ShowInAnnotations);

doc->Save(get_ArtifactsDir() + u"Document.ShowCommentsInAnnotations.pdf");

// Notez qu'il est nécessaire de reconstruire la mise en page du document (via la méthode Document.UpdatePageLayout()).
// après avoir modifié les valeurs de Document.LayoutOptions.
doc->get_LayoutOptions()->set_CommentDisplayMode(Aspose::Words::Layout::CommentDisplayMode::ShowInBalloons);
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.ShowCommentsInBalloons.pdf");
```

## Voir aussi

* Enum [CommentDisplayMode](../../commentdisplaymode/)
* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
