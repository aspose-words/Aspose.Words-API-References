---
title: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks méthode"
linktitle: "get_ForcePageBreaks"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks méthode. Permet de spécifier si les sauts de page doivent être conservés lors de l'exportation. La valeur par défaut est false en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.saving/txtsaveoptionsbase/get_forcepagebreaks/
---
## TxtSaveOptionsBase::get_ForcePageBreaks method


Permet de spécifier si les sauts de page doivent être conservés lors de l'exportation. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks() const
```


## Exemples



Montre comment spécifier s'il faut conserver les sauts de page lors de l'exportation d'un document en texte brut.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3");

// Créez un objet "TxtSaveOptions", que nous pouvons transmettre à la méthode "Save" du document
// méthode pour modifier la façon dont nous enregistrons le document en texte brut.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Les objets "Document" d'Aspose.Words possèdent des sauts de page, tout comme les documents Microsoft Word.
// Les formats d'enregistrement tels que ".txt" constituent un corps de texte continu sans sauts de page.
// Définissez la propriété "ForcePageBreaks" sur "true" pour conserver tous les sauts de page sous forme de caractères '\f'.
// Définissez la propriété "ForcePageBreaks" sur "false" pour supprimer tous les sauts de page.
saveOptions->set_ForcePageBreaks(forcePageBreaks);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.PageBreaks.txt", saveOptions);

// Si nous chargeons un document texte brut avec des sauts de page,
// l'objet "Document" les utilisera pour diviser le corps en pages.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"TxtSaveOptions.PageBreaks.txt");

ASSERT_EQ(forcePageBreaks ? 3 : 1, doc->get_PageCount());
```

## Voir aussi

* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
