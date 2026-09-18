---
title: "Aspose::Words::Document::get_AttachedTemplate Methode"
linktitle: "get_AttachedTemplate"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_AttachedTemplate Methode. Liest oder setzt den vollständigen Pfad der an das Dokument angehängten Vorlage in C++."
type: docs
weight: 13000
url: /de/cpp/aspose.words/document/get_attachedtemplate/
---
## Document::get_AttachedTemplate method


Liest oder legt den vollständigen Pfad der dem Dokument angehängten Vorlage fest.

```cpp
System::String Aspose::Words::Document::get_AttachedTemplate()
```

## Hinweise


Ein leerer String bedeutet, dass das Dokument an die Normalvorlage angehängt ist.

## Beispiele



Zeigt, wie man eine Standardvorlage für Dokumente festlegt, die keine angehängten Vorlagen haben.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Aktivieren Sie die automatische Stilaktualisierung, aber hängen Sie kein Vorlagendokument an.
doc->set_AutomaticallyUpdateStyles(true);

ASSERT_EQ(System::String::Empty, doc->get_AttachedTemplate());

// Da kein Vorlagendokument vorhanden ist, hatte das Dokument keinen Ort, um Stiländerungen nachzuverfolgen.
// Verwenden Sie ein SaveOptions-Objekt, um automatisch eine Vorlage festzulegen
// wenn ein Dokument, das wir speichern, keine hat.
System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = Aspose::Words::Saving::SaveOptions::CreateSaveOptions(u"Document.DefaultTemplate.docx");
options->set_DefaultTemplate(get_MyDir() + u"Business brochure.dotx");

doc->Save(get_ArtifactsDir() + u"Document.DefaultTemplate.docx", options);
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
