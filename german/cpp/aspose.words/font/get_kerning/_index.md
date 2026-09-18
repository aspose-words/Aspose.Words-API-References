---
title: "Aspose::Words::Font::get_Kerning Methode"
linktitle: "get_Kerning"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_Kerning Methode. Gibt die Schriftgröße zurück oder legt sie fest, bei der das Kerning beginnt, in C++."
type: docs
weight: 20000
url: /de/cpp/aspose.words/font/get_kerning/
---
## Font::get_Kerning method


Liest oder setzt die Schriftgröße, bei der das Kerning beginnt.

```cpp
double Aspose::Words::Font::get_Kerning()
```


## Beispiele



Zeigt, wie die Schriftgröße angegeben wird, bei der das Kerning wirksam wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Arial Black");

// Setzen Sie die Schriftgröße des Builders und die Mindestgröße, bei der das Kerning wirksam wird.
// Die Schriftgröße fällt unter die Kerning‑Schwelle, sodass der untenstehende Lauf kein Kerning hat.
builder->get_Font()->set_Size(18);
builder->get_Font()->set_Kerning(24);

builder->Writeln(u"TALLY. (Kerning not applied)");

// Setzen Sie den Kerning‑Schwellenwert, sodass die aktuelle Schriftgröße des Builders darüber liegt.
// Jeder Text, den wir ab diesem Punkt hinzufügen, wird mit Kerning versehen. Die Abstände zwischen Zeichen
// werden angepasst, was normalerweise zu einem leicht ästhetisch ansprechenderen Textlauf führt.
builder->get_Font()->set_Kerning(12);

builder->Writeln(u"TALLY. (Kerning applied)");

doc->Save(get_ArtifactsDir() + u"Font.Kerning.docx");
```

## Siehe auch

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
