---
title: "Aspose::Words::Comment::get_Done méthode"
linktitle: "get_Done"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Comment::get_Done méthode. Obtient ou définit le drapeau indiquant que le commentaire a été marqué comme terminé en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words/comment/get_done/
---
## Comment::get_Done method


Obtient ou définit le drapeau indiquant que le commentaire a été marqué comme terminé.

```cpp
bool Aspose::Words::Comment::get_Done() const
```


## Exemples



Montre comment marquer un commentaire comme "done".
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Helo world!");

// Insérez un commentaire pour signaler une erreur.
auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Fix the spelling error!");
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Les commentaires possèdent un indicateur "Done", qui est défini sur "false" par défaut.
// Si un commentaire suggère que nous apportions une modification dans le document,
// nous pouvons appliquer la modification, puis également définir l’indicateur "Done" par la suite pour indiquer la correction.
ASSERT_FALSE(comment->get_Done());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Hello world!");
comment->set_Done(true);

// Les commentaires qui sont "done" se différencieront
// des éléments qui ne sont pas "terminés" avec une couleur de texte atténuée.
comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Add text to this paragraph.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

doc->Save(get_ArtifactsDir() + u"Comment.Done.docx");
```

## Voir aussi

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
