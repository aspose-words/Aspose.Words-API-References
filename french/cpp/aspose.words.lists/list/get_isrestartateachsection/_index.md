---
title: "Aspose::Words::Lists::List::get_IsRestartAtEachSection méthode"
linktitle: "get_IsRestartAtEachSection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Lists::List::get_IsRestartAtEachSection méthode. Spécifie si la liste doit être redémarrée à chaque section. La valeur par défaut est false en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.lists/list/get_isrestartateachsection/
---
## List::get_IsRestartAtEachSection method


Spécifie si la liste doit être redémarrée à chaque section. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Lists::List::get_IsRestartAtEachSection()
```

## Remarques


Cette option est prise en charge uniquement dans les formats de document RTF, DOC et DOCX.

Cette option sera écrite dans le DOCX uniquement si [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/) est supérieur à [Ecma376_2006](../../../aspose.words.saving/ooxmlcompliance/).

## Exemples



Montre comment configurer une liste pour redémarrer la numérotation à chaque section.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->idx_get(0);
list->set_IsRestartAtEachSection(restartListAtEachSection);

// La propriété "IsRestartAtEachSection" ne sera applicable que lorsque
// le niveau de conformité OOXML du document correspond à une norme plus récente que "OoxmlComplianceCore.Ecma376".
auto options = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
options->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

builder->get_ListFormat()->set_List(list);

builder->Writeln(u"List item 1");
builder->Writeln(u"List item 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"List item 3");
builder->Writeln(u"List item 4");

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.RestartingDocumentList.docx");

ASPOSE_ASSERT_EQ(restartListAtEachSection, doc->get_Lists()->idx_get(0)->get_IsRestartAtEachSection());
```

## Voir aussi

* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
