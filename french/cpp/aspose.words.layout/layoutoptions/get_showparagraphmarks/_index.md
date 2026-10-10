---
title: "Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks méthode"
linktitle: "get_ShowParagraphMarks"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks méthode. Obtient ou définit l'indication de savoir si les marques de paragraphe sont rendues. La valeur par défaut est false en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.layout/layoutoptions/get_showparagraphmarks/
---
## LayoutOptions::get_ShowParagraphMarks method


Obtient ou définit l'indication de savoir si les marques de paragraphe sont rendues. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks() const
```


## Exemples



Montre comment afficher les marques de paragraphe dans un document de sortie rendu.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ajoutez quelques paragraphes, puis activez les marques de paragraphe pour afficher la fin des paragraphes
// avec le symbole pilcrow (¶) lorsque nous rendons le document.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

doc->get_LayoutOptions()->set_ShowParagraphMarks(showParagraphMarks);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsParagraphMarks.pdf");
```

## Voir aussi

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
