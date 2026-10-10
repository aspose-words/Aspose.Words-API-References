---
title: "Aspose::Words::ParagraphFormat::get_SpaceBeforeAuto Methode"
linktitle: "get_SpaceBeforeAuto"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ParagraphFormat::get_SpaceBeforeAuto Methode. True, wenn der Abstand vor dem Absatz in C++ automatisch festgelegt wird."
type: docs
weight: 34000
url: /de/cpp/aspose.words/paragraphformat/get_spacebeforeauto/
---
## ParagraphFormat::get_SpaceBeforeAuto method


True, wenn der Abstand vor dem Absatz automatisch festgelegt wird.

```cpp
bool Aspose::Words::ParagraphFormat::get_SpaceBeforeAuto()
```

## Hinweise


Wenn auf **true** gesetzt, überschreibt es die Wirkung von [SpaceBefore](../get_spacebefore/).

Wenn Sie den Absatz Space Before und Space After auf Auto setzen, fügt **Microsoft** Word automatisch 14 Punkte Abstand zwischen Absätzen gemäß den folgenden Regeln hinzu:

* Normally, spacing is added after all paragraphs.
* In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
* In a nested bulleted or numbered list spacing is not added.
* Spacing is normally added after a table.
* Spacing is not added after a table if it is the last block in a table cell.
* Spacing is not added after the last paragraph in a table cell.



## Beispiele



Zeigt, wie man automatischen Absatzabstand einstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Wendet einen großen Abstand vor und nach den Absätzen an, die dieser Builder erstellt.
builder->get_ParagraphFormat()->set_SpaceBefore(24);
builder->get_ParagraphFormat()->set_SpaceAfter(24);

// Setzen Sie diese Flags auf "true", um automatischen Abstand anzuwenden,
// ignoriert dabei effektiv den Abstand in den oben gesetzten Eigenschaften.
// Wenn Sie sie auf "false" belassen, wird unser benutzerdefinierter Absatzabstand angewendet.
builder->get_ParagraphFormat()->set_SpaceAfterAuto(autoSpacing);
builder->get_ParagraphFormat()->set_SpaceBeforeAuto(autoSpacing);

// Fügen Sie zwei Absätze ein, die oben und unten Abstand haben, und speichern Sie das Dokument.
builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphSpacingAuto.docx");
```

## Siehe auch

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
