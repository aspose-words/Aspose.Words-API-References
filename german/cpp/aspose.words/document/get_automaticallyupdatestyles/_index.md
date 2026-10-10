---
title: "Aspose::Words::Document::get_AutomaticallyUpdateStyles Methode"
linktitle: "get_AutomaticallyUpdateStyles"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_AutomaticallyUpdateStyles-Methode. Gibt ein Flag zurück oder legt es fest, das angibt, ob die Formatvorlagen im Dokument bei jedem Öffnen des Dokuments in MS Word an die Formatvorlagen der angehängten Vorlage angepasst werden, in C++."
type: docs
weight: 14000
url: /de/cpp/aspose.words/document/get_automaticallyupdatestyles/
---
## Document::get_AutomaticallyUpdateStyles method


Liest oder legt ein Flag fest, das angibt, ob die Formatvorlagen im Dokument jedes Mal, wenn das Dokument in MS Word geöffnet wird, an die Formatvorlagen der angehängten Vorlage angepasst werden.

```cpp
bool Aspose::Words::Document::get_AutomaticallyUpdateStyles()
```


## Beispiele



Zeigt, wie man eine Vorlage an ein Dokument anhängt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Microsoft‑Word‑Dokumente enthalten standardmäßig eine angehängte Vorlage mit dem Namen "Normal.dotm".
// Für leere Aspose.Words‑Dokumente gibt es keine Standardvorlage.
ASSERT_EQ(System::String::Empty, doc->get_AttachedTemplate());

// Fügen Sie eine Vorlage hinzu und setzen Sie anschließend das Flag, um Formatänderungen anzuwenden.
// innerhalb der Vorlage auf die Formatvorlagen in unserem Dokument.
doc->set_AttachedTemplate(get_MyDir() + u"Business brochure.dotx");
doc->set_AutomaticallyUpdateStyles(true);

doc->Save(get_ArtifactsDir() + u"Document.AutomaticallyUpdateStyles.docx");
```


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
