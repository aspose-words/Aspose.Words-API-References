---
title: "Aspose::Words::Font::get_Italic Methode"
linktitle: "get_Italic"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_Italic Methode. Wahr, wenn die Schriftart in C++ kursiv formatiert ist."
type: docs
weight: 18000
url: /de/cpp/aspose.words/font/get_italic/
---
## Font::get_Italic method


True, wenn die Schrift als kursiv formatiert ist.

```cpp
bool Aspose::Words::Font::get_Italic()
```


## Beispiele



Zeigt, wie man kursiven Text mit einem Document Builder schreibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_Italic(true);
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"Font.Italic.docx");
```

## Siehe auch

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
