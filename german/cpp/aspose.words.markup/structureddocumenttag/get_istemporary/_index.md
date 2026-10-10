---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary Methode"
linktitle: "get_IsTemporary"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary Methode. Gibt an, ob dieses SDT aus dem WordProcessingML-Dokument entfernt werden soll, wenn sein Inhalt in C++ geändert wird."
type: docs
weight: 19000
url: /de/cpp/aspose.words.markup/structureddocumenttag/get_istemporary/
---
## StructuredDocumentTag::get_IsTemporary method


Gibt an, ob dieses **SDT** aus dem WordProcessingML‑Dokument entfernt werden soll, wenn sein Inhalt geändert wird.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary() const
```


## Beispiele



Zeigt, wie man Einmal-Steuerelemente erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Fügen Sie ein strukturiertes Dokument-Tag für Klartext ein,
// das als ein Klartext-Formular dient, in das der Benutzer Text eingeben kann.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Setzen Sie die Eigenschaft "IsTemporary" auf "true", um das strukturierte Dokument-Tag verschwinden zu lassen und
// und seine Inhalte nach einer einzigen Bearbeitung durch den Benutzer in Microsoft Word in das Dokument zu übernehmen.
// Setzen Sie die Eigenschaft "IsTemporary" auf "false", um dem Benutzer das Bearbeiten des Inhalts zu ermöglichen.
// des strukturierten Dokumenttags beliebig oft.
tag->set_IsTemporary(isTemporary);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Please enter text: ");
builder->InsertNode(tag);

// Fügen Sie einen weiteren strukturierten Dokumenttag in Form einer Checkbox ein und setzen Sie dessen Standardzustand auf "checked".
tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Checkbox, Aspose::Words::Markup::MarkupLevel::Inline);
tag->set_Checked(true);

// Setzen Sie die Eigenschaft "IsTemporary" auf "true", um die Checkbox zu einem Symbol zu machen
// sobald der Benutzer darauf in Microsoft Word klickt.
// Setzen Sie die Eigenschaft "IsTemporary" auf "false", um dem Benutzer zu erlauben, die Checkbox beliebig oft anzuklicken.
tag->set_IsTemporary(isTemporary);

builder->Write(u"\nPlease click the check box: ");
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.IsTemporary.docx");
```

## Siehe auch

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
