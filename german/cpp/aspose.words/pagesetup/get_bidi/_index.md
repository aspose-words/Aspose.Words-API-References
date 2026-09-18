---
title: "Aspose::Words::PageSetup::get_Bidi Methode"
linktitle: "get_Bidi"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageSetup::get_Bidi Methode. Gibt an, dass dieser Abschnitt bidirektionalen (komplexen Skripte) Text enthält in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words/pagesetup/get_bidi/
---
## PageSetup::get_Bidi method


Gibt an, dass dieser Abschnitt bidirektionalen (komplexen Skripte) Text enthält.

```cpp
bool Aspose::Words::PageSetup::get_Bidi()
```

## Hinweise


Wenn **true**, werden die Spalten in diesem Abschnitt von rechts nach links angeordnet.

## Beispiele



Zeigt, wie die Reihenfolge von Textspalten in einem Abschnitt festgelegt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->get_TextColumns()->SetCount(3);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Write(u"Column 2.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Write(u"Column 3.");

// Setzen Sie die Eigenschaft "Bidi" auf "true", um die Spalten ab der rechten Seite der Seite anzuordnen.
// Die Reihenfolge der Spalten entspricht der Richtung des Rechts-nach-Links-Textes.
// Setzen Sie die Eigenschaft "Bidi" auf "false", um die Spalten ab der linken Seite der Seite anzuordnen.
// Die Reihenfolge der Spalten entspricht der Richtung des Links-nach-Rechts-Textes.
pageSetup->set_Bidi(reverseColumns);

doc->Save(get_ArtifactsDir() + u"PageSetup.Bidi.docx");
```

## Siehe auch

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
