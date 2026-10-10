---
title: "Aspose::Words::Layout::CommentDisplayMode enum"
linktitle: "CommentDisplayMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Layout::CommentDisplayMode enum. Spécifie le mode de rendu des commentaires de document en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.layout/commentdisplaymode/
---
## CommentDisplayMode enum


Spécifie le mode de rendu pour les commentaires du document.

```cpp
enum class CommentDisplayMode
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Hide | 0 | Aucun commentaire de document n'est rendu. |
| ShowInBalloons | 1 | Rend les commentaires de document dans des bulles dans la marge. C'est la valeur par défaut. |
| ShowInAnnotations | 2 | Rend les commentaires de document sous forme d'annotations. Ceci n'est disponible que pour le format Pdf. |


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

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
