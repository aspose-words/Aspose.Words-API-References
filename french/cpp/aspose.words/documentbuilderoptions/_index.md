---
title: "Aspose::Words::DocumentBuilderOptions classe"
linktitle: "DocumentBuilderOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilderOptions classe. Permet de spécifier des options supplémentaires pour le processus de construction du document en C++."
type: docs
weight: 22500
url: /fr/cpp/aspose.words/documentbuilderoptions/
---
## DocumentBuilderOptions class


Permet de spécifier des options supplémentaires pour le processus de création du document.

```cpp
class DocumentBuilderOptions : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [DocumentBuilderOptions](./documentbuilderoptions/)() |  |
| [get_ContextTableFormatting](./get_contexttableformatting/)() const | Vrai si le formatage appliqué au contenu du tableau n'affecte pas le formatage du contenu qui le suit. La valeur par défaut est **true**. |
| [get_DesignMode](./get_designmode/)() const | Correspond au mode Création dans Microsoft Word. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ContextTableFormatting](./set_contexttableformatting/)(bool) | Mutateur pour [Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting](./get_contexttableformatting/). |
| [set_DesignMode](./set_designmode/)(bool) | Correspond au mode Création dans Microsoft Word. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
