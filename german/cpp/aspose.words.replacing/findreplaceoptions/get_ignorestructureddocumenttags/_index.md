---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags‑Methode"
linktitle: "get_IgnoreStructuredDocumentTags"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags‑Methode. Gibt einen booleschen Wert zurück oder setzt ihn, der angibt, ob der Inhalt von StructuredDocumentTag ignoriert werden soll. Der Standardwert ist false in C++."
type: docs
weight: 12000
url: /de/cpp/aspose.words.replacing/findreplaceoptions/get_ignorestructureddocumenttags/
---
## FindReplaceOptions::get_IgnoreStructuredDocumentTags method


Gibt einen booleschen Wert zurück oder setzt ihn, der angibt, ob der Inhalt von [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) ignoriert werden soll. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags() const
```

## Hinweise


Wenn diese Option auf **true** gesetzt ist, wird der Inhalt von [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) als einfacher Text behandelt.

Andernfalls wird [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) als eigenständige [Story](../../../aspose.words/story/) verarbeitet und das Ersetzungsmuster wird für jedes [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) separat gesucht, sodass, wenn das Muster ein [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) überschreitet, die Ersetzung für ein solches Muster nicht durchgeführt wird.

## Beispiele



Zeigt, wie der Inhalt von Tags bei der Ersetzung ignoriert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// Dieser Absatz enthält SDT.
auto p = System::ExplicitCast<Aspose::Words::Paragraph>(doc->get_FirstSection()->get_Body()->GetChild(Aspose::Words::NodeType::Paragraph, 2, true));
System::String textToSearch = p->ToString(Aspose::Words::SaveFormat::Text).Trim();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreStructuredDocumentTags(true);
doc->get_Range()->Replace(textToSearch, u"replacement", options);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
```

## Siehe auch

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
