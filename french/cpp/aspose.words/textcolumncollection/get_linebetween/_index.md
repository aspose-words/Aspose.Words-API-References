---
title: "Aspose::Words::TextColumnCollection::get_LineBetween méthode"
linktitle: "get_LineBetween"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::TextColumnCollection::get_LineBetween méthode. Lorsque true, ajoute une ligne verticale entre les colonnes en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/textcolumncollection/get_linebetween/
---
## TextColumnCollection::get_LineBetween method


Lorsque **true**, ajoute une ligne verticale entre les colonnes.

```cpp
bool Aspose::Words::TextColumnCollection::get_LineBetween()
```


## Exemples



Montre comment séparer les colonnes avec une ligne verticale.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Configurez l’objet PageSetup de la section actuelle pour diviser le texte en plusieurs colonnes.
// Définissez la propriété \"LineBetween\" sur \"true\" pour placer une ligne de séparation entre les colonnes.
// Définissez la propriété \"LineBetween\" sur \"false\" pour laisser l’espace entre les colonnes vide.
System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_LineBetween(lineBetween);
columns->SetCount(3);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 3.");

doc->Save(get_ArtifactsDir() + u"PageSetup.VerticalLineBetweenColumns.docx");
```

## Voir aussi

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
