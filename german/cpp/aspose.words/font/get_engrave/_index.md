---
title: "Aspose::Words::Font::get_Engrave Methode"
linktitle: "get_Engrave"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_Engrave-Methode. True, wenn die Schriftart in C++ als graviert formatiert ist."
type: docs
weight: 14000
url: /de/cpp/aspose.words/font/get_engrave/
---
## Font::get_Engrave method


True, wenn die Schrift als graviert formatiert ist.

```cpp
bool Aspose::Words::Font::get_Engrave()
```


## Beispiele



Zeigt, wie man Gravur-/Erhebungs-Effekte auf Text anwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_Color(System::Drawing::Color::get_LightBlue());

// Unten sind zwei Methoden aufgeführt, um Schatten zu verwenden, um einen 3D-ähnlichen Effekt auf den Text anzuwenden.
// 1 -  Text gravieren, damit er aussieht, als wären die Buchstaben in die Seite eingesunken:
builder->get_Font()->set_Engrave(true);

builder->Writeln(u"This text is engraved.");

// 2 -  Text erheben, damit er aussieht, als würden die Buchstaben aus der Seite hervortreten:
builder->get_Font()->set_Engrave(false);
builder->get_Font()->set_Emboss(true);

builder->Writeln(u"This text is embossed.");

doc->Save(get_ArtifactsDir() + u"Font.EngraveEmboss.docx");
```

## Siehe auch

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
