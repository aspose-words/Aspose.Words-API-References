---
title: "Aspose::Words::Font::get_Shadow Methode"
linktitle: "get_Shadow"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_Shadow Methode. Wahr, wenn die Schriftart in C++ als schattiert formatiert ist."
type: docs
weight: 35000
url: /de/cpp/aspose.words/font/get_shadow/
---
## Font::get_Shadow method


Wahr, wenn die Schriftart als schattiert formatiert ist.

```cpp
bool Aspose::Words::Font::get_Shadow()
```


## Beispiele



Zeigt, wie man einen Textlauf erstellt, der mit einem Schatten formatiert ist.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Setzen Sie das Shadow-Flag, um einen versetzten Schatteneffekt anzuwenden,
// so dass die Buchstaben aussehen, als würden sie über der Seite schweben.
builder->get_Font()->set_Shadow(true);
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text has a shadow.");

doc->Save(get_ArtifactsDir() + u"Font.Shadow.docx");
```

## Siehe auch

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
