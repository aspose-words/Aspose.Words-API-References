---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement Methode"
linktitle: "get_SmartParagraphBreakReplacement"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement Methode. Gibt einen booleschen Wert zurück oder legt ihn fest, der angibt, ob es erlaubt ist, einen Absatzumbruch zu ersetzen, wenn kein nachfolgender Geschwisterabsatz vorhanden ist. Der Standardwert ist false in C++."
type: docs
weight: 16000
url: /de/cpp/aspose.words.replacing/findreplaceoptions/get_smartparagraphbreakreplacement/
---
## FindReplaceOptions::get_SmartParagraphBreakReplacement method


Liest oder setzt einen booleschen Wert, der angibt, ob ein Absatzumbruch ersetzt werden darf, wenn kein nachfolgender Geschwisterabsatz vorhanden ist. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement() const
```


## Beispiele



Zeigt, wie man einen Absatz aus einer Tabellenzelle mit einer verschachtelten Tabelle entfernt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstelle eine Tabelle mit Absatz und innerer Tabelle in der ersten Zelle.
builder->StartTable();
builder->InsertCell();
builder->Write(u"TEXT1");
builder->StartTable();
builder->InsertCell();
builder->EndTable();
builder->EndTable();
builder->Writeln();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
// Wenn die folgende Option auf 'true' gesetzt ist, entfernt Aspose.Words den Text des Absatzes
// vollständig zusammen mit seinem Absatzzeichen. Andernfalls wird Aspose.Words Word nachahmen und entfernen
// nur den Text des Absatzes und lässt das Absatzzeichen unverändert (wenn einer Tabelle dem Text folgt).
options->set_SmartParagraphBreakReplacement(isSmartParagraphBreakReplacement);
doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"TEXT1&p"), u"", options);

doc->Save(get_ArtifactsDir() + u"Table.RemoveParagraphTextAndMark.docx");
```

## Siehe auch

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
