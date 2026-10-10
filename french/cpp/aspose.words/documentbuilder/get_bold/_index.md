---
title: "Aspose::Words::DocumentBuilder::get_Bold méthode"
linktitle: "get_Bold"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::get_Bold méthode. Vrai si la police est formatée en gras en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words/documentbuilder/get_bold/
---
## DocumentBuilder::get_Bold method


Vrai si la police est formatée en gras.

```cpp
bool Aspose::Words::DocumentBuilder::get_Bold()
```


## Exemples



Montre comment remplir les MERGEFIELDs avec des données à l'aide d'un constructeur de document au lieu d'une fusion de courrier.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez quelques MERGEFIELDS, qui acceptent des données provenant de colonnes du même nom dans une source de données lors d'une fusion de courrier,
// et remplissez-les ensuite manuellement.
builder->InsertField(u" MERGEFIELD Chairman ");
builder->InsertField(u" MERGEFIELD ChiefFinancialOfficer ");
builder->InsertField(u" MERGEFIELD ChiefTechnologyOfficer ");

builder->MoveToMergeField(u"Chairman");
builder->set_Bold(true);
builder->Writeln(u"John Doe");

builder->MoveToMergeField(u"ChiefFinancialOfficer");
builder->set_Italic(true);
builder->Writeln(u"Jane Doe");

builder->MoveToMergeField(u"ChiefTechnologyOfficer");
builder->set_Italic(true);
builder->Writeln(u"John Bloggs");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.FillMergeFields.docx");
```

## Voir aussi

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
