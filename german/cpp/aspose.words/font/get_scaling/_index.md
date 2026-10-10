---
title: "Aspose::Words::Font::get_Scaling Methode"
linktitle: "get_Scaling"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_Scaling Methode. Ermittelt oder legt die Zeichenbreiten‑Skalierung in Prozent in C++ fest."
type: docs
weight: 33000
url: /de/cpp/aspose.words/font/get_scaling/
---
## Font::get_Scaling method


Liest oder legt die Skalierung der Zeichenbreite in Prozent fest.

```cpp
int32_t Aspose::Words::Font::get_Scaling()
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
