---
title: "Aspose::Words::Lists::List::get_IsRestartAtEachSection método"
linktitle: "get_IsRestartAtEachSection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Lists::List::get_IsRestartAtEachSection método. Especifica si la lista debe reiniciarse en cada sección. El valor predeterminado es false en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.lists/list/get_isrestartateachsection/
---
## List::get_IsRestartAtEachSection method


Especifica si la lista debe reiniciarse en cada sección. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Lists::List::get_IsRestartAtEachSection()
```

## Observaciones


Esta opción solo es compatible con los formatos de documento RTF, DOC y DOCX.

Esta opción se escribirá en DOCX solo si [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/) es superior a [Ecma376_2006](../../../aspose.words.saving/ooxmlcompliance/).

## Ejemplos



Muestra cómo configurar una lista para reiniciar la numeración en cada sección.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->idx_get(0);
list->set_IsRestartAtEachSection(restartListAtEachSection);

// La propiedad "IsRestartAtEachSection" solo será aplicable cuando
// el nivel de cumplimiento OOXML del documento sea un estándar más reciente que "OoxmlComplianceCore.Ecma376".
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

## Ver también

* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
