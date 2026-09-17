---
title: "Aspose::Words::Font::get_ComplexScript méthode"
linktitle: "get_ComplexScript"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Font::get_ComplexScript méthode. Spécifie si le contenu de ce run doit être traité comme du texte à script complexe, quels que soient leurs valeurs de caractères Unicode, lors de la détermination du formatage de ce run en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words/font/get_complexscript/
---
## Font::get_ComplexScript method


Spécifie si le contenu de cet enchaînement doit être traité comme du texte à script complexe, indépendamment de leurs valeurs de caractères Unicode, lors de la détermination du formatage de cet enchaînement.

```cpp
bool Aspose::Words::Font::get_ComplexScript()
```


## Exemples



Montre comment ajouter du texte qui est toujours traité comme un script complexe.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_ComplexScript(true);

builder->Writeln(u"Text treated as complex script.");

doc->Save(get_ArtifactsDir() + u"Font.ComplexScript.docx");
```

## Voir aussi

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
