---
title: "Méthode get_ContextTableFormatting de Aspose::Words::DocumentBuilderOptions"
linktitle: "get_ContextTableFormatting"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode get_ContextTableFormatting de Aspose::Words::DocumentBuilderOptions. Vrai si le formatage appliqué au contenu du tableau n'affecte pas le formatage du contenu qui le suit. La valeur par défaut est vraie en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words/documentbuilderoptions/get_contexttableformatting/
---
## DocumentBuilderOptions::get_ContextTableFormatting method


Vrai si le formatage appliqué au contenu du tableau n'affecte pas le formatage du contenu qui le suit. La valeur par défaut est **true**.

```cpp
bool Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting() const
```


## Exemples



Montre comment ignorer le formatage du tableau pour le contenu suivant.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builderOptions = System::MakeObject<Aspose::Words::DocumentBuilderOptions>();
builderOptions->set_ContextTableFormatting(true);
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc, builderOptions);

// Ajoute du contenu avant le tableau.
// La taille de police par défaut est 12.
builder->Writeln(u"Font size 12 here.");
builder->StartTable();
builder->InsertCell();
// Modifie la taille de police à l'intérieur du tableau.
builder->get_Font()->set_Size(5);
builder->Write(u"Font size 5 here");
builder->InsertCell();
builder->Write(u"Font size 5 here");
builder->EndRow();
builder->EndTable();

// Si ContextTableFormatting est vrai, alors le formatage du tableau n'est pas appliqué au contenu suivant.
// Si ContextTableFormatting est faux, alors le formatage du tableau est appliqué au contenu suivant.
builder->Writeln(u"Font size 12 here.");

doc->Save(get_ArtifactsDir() + u"Table.ContextTableFormatting.docx");
```

## Voir aussi

* Class [DocumentBuilderOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
