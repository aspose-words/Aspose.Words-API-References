---
title: "Aspose::Words::Font::get_Spacing Methode"
linktitle: "get_Spacing"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_Spacing Methode. Gibt den Abstand (in Punkten) zwischen Zeichen zurück oder setzt ihn in C++."
type: docs
weight: 40000
url: /de/cpp/aspose.words/font/get_spacing/
---
## Font::get_Spacing method


Gibt den Abstand (in Punkten) zwischen Zeichen zurück oder legt ihn fest.

```cpp
double Aspose::Words::Font::get_Spacing()
```


## Beispiele



Zeigt, wie die horizontale Skalierung und der Abstand für Zeichen eingestellt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie einen Textlauf hinzu und erhöhen Sie die Zeichenbreite auf 150 %.
builder->get_Font()->set_Scaling(150);
builder->Writeln(u"Wide characters");

// Fügen Sie einen Textlauf hinzu und fügen Sie zwischen jedem Zeichen einen zusätzlichen horizontalen Abstand von 1 pt hinzu.
builder->get_Font()->set_Spacing(1);
builder->Writeln(u"Expanded by 1pt");

// Fügen Sie einen Textlauf hinzu und bringen Sie die Zeichen um 1 pt näher zusammen.
builder->get_Font()->set_Spacing(-1);
builder->Writeln(u"Condensed by 1pt");

doc->Save(get_ArtifactsDir() + u"Font.ScalingSpacing.docx");
```

## Siehe auch

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
