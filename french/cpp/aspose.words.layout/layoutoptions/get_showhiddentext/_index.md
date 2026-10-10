---
title: "Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText méthode"
linktitle: "get_ShowHiddenText"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText méthode. Obtient ou définit l'indication de savoir si le texte masqué dans le document est rendu. La valeur par défaut est false en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.layout/layoutoptions/get_showhiddentext/
---
## LayoutOptions::get_ShowHiddenText method


Obtient ou définit l'indication de savoir si le texte masqué dans le document est rendu. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText() const
```


## Exemples



Montre comment masquer du texte dans un document de sortie rendu.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez du texte masqué, puis spécifiez si nous souhaitons l'omettre d'un document rendu.
builder->Writeln(u"This text is not hidden.");
builder->get_Font()->set_Hidden(true);
builder->Writeln(u"This text is hidden.");

doc->get_LayoutOptions()->set_ShowHiddenText(showHiddenText);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsHiddenText.pdf");
```

## Voir aussi

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
