---
title: "Aspose::Words::Font::get_EmphasisMark méthode"
linktitle: "get_EmphasisMark"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Font::get_EmphasisMark méthode. Obtient ou définit le signe d'emphase appliqué à ce formatage en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words/font/get_emphasismark/
---
## Font::get_EmphasisMark method


Obtient ou définit le signe d'emphase appliqué à ce formatage.

```cpp
Aspose::Words::EmphasisMark Aspose::Words::Font::get_EmphasisMark()
```


## Exemples



Montre comment ajouter un caractère supplémentaire rendu au-dessus/en dessous du glyphe.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// Types possibles de marque d'emphase :
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder->get_Font()->set_EmphasisMark(emphasisMark);

builder->Write(u"Emphasis text");
builder->Writeln();
builder->get_Font()->ClearFormatting();
builder->Write(u"Simple text");

builder->get_Document()->Save(get_ArtifactsDir() + u"Fonts.SetEmphasisMark.docx");
```

## Voir aussi

* Enum [EmphasisMark](../../emphasismark/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
