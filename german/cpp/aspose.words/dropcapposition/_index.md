---
title: "Aspose::Words::DropCapPosition enum"
linktitle: "DropCapPosition"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DropCapPosition enum. Gibt die Position für einen Drop-Cap-Text in C++ an."
type: docs
weight: 87000
url: /de/cpp/aspose.words/dropcapposition/
---
## DropCapPosition enum


Gibt die Position für einen Drop-Cap-Text an.

```cpp
enum class DropCapPosition
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | 0 | Der Absatz hat keinen Drop-Cap. |
| Normal | 1 | Der Drop-Cap ist innerhalb des Textrandes im Ankerabsatz positioniert. |
| Rand | 2 | Der Drop-Cap ist außerhalb des Textrandes im Ankerabsatz positioniert. |


## Beispiele



Zeigt, wie man einen Drop-Cap erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie einen Absatz mit einem großen Buchstaben ein, mit dem der Text im zweiten und dritten Absatz beginnt.
builder->get_Font()->set_Size(54);
builder->Writeln(u"L");

builder->get_Font()->set_Size(18);
builder->Writeln(System::String(u"orem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder->Writeln(System::String(u"Ut enim ad minim veniam, quis nostrud exercitation ") + u"ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Derzeit erscheinen der zweite und dritte Absatz unter dem ersten.
// Wir können den ersten Absatz über sein "ParagraphFormat"-Objekt in einen Drop-Cap für die anderen Absätze umwandeln.
// Setzen Sie die Eigenschaft "DropCapPosition" auf "DropCapPosition.Margin", um den Drop-Cap zu platzieren
// außerhalb des linken Seitenrandes, wenn unser Text von links nach rechts verläuft.
// Setzen Sie die Eigenschaft "DropCapPosition" auf "DropCapPosition.Normal", um den Drop-Cap innerhalb der Seitenränder zu platzieren
// und den restlichen Text darum fließen zu lassen.
// "DropCapPosition.None" ist der Standardzustand für alle Absätze.
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();
format->set_DropCapPosition(dropCapPosition);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.DropCap.docx");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
