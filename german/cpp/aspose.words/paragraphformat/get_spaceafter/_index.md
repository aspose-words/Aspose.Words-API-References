---
title: "Aspose::Words::ParagraphFormat::get_SpaceAfter Methode"
linktitle: "get_SpaceAfter"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ParagraphFormat::get_SpaceAfter Methode. Gibt die Menge des Abstands (in Punkten) nach dem Absatz in C++ zurück oder setzt sie."
type: docs
weight: 31000
url: /de/cpp/aspose.words/paragraphformat/get_spaceafter/
---
## ParagraphFormat::get_SpaceAfter method


Liest oder setzt den Abstand (in Punkten) nach dem Absatz.

```cpp
double Aspose::Words::ParagraphFormat::get_SpaceAfter()
```

## Hinweise


Hat keine Wirkung, wenn [SpaceAfterAuto](../get_spaceafterauto/) **true** ist.

Gültige Werte liegen im Bereich von 0 bis 1584, einschließlich.

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


Zeigt, wie man keinen Abstand zwischen Absätzen mit demselben Stil anwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Wendet einen großen Abstand vor und nach den Absätzen an, die dieser Builder erstellt.
builder->get_ParagraphFormat()->set_SpaceBefore(24);
builder->get_ParagraphFormat()->set_SpaceAfter(24);

// Setzen Sie das Flag "NoSpaceBetweenParagraphsOfSameStyle" auf "true", um anzuwenden
// Kein Abstand zwischen Absätzen mit demselben Stil, wodurch ähnliche Absätze gruppiert werden.
// Lassen Sie das Flag "NoSpaceBetweenParagraphsOfSameStyle" auf "false".
// um den Abstand gleichmäßig auf jeden Absatz anzuwenden.
builder->get_ParagraphFormat()->set_NoSpaceBetweenParagraphsOfSameStyle(noSpaceBetweenParagraphsOfSameStyle);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Quote"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphSpacingSameStyle.docx");
```

## Siehe auch

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
