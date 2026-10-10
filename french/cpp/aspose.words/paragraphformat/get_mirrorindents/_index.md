---
title: "Aspose::Words::ParagraphFormat::get_MirrorIndents méthode"
linktitle: "get_MirrorIndents"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::ParagraphFormat::get_MirrorIndents. Obtient ou définit un indicateur indiquant si les retraits gauche et droit ont la même largeur en C++."
type: docs
weight: 24500
url: /fr/cpp/aspose.words/paragraphformat/get_mirrorindents/
---
## ParagraphFormat::get_MirrorIndents method


Obtient ou définit un indicateur indiquant si les retraits gauche et droit ont la même largeur.

```cpp
bool Aspose::Words::ParagraphFormat::get_MirrorIndents()
```


## Exemples



Montrez comment rendre les retraits gauche et droit identiques.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat();

format->set_MirrorIndents(true);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.MirrorIndents.docx");
```

## Voir aussi

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
