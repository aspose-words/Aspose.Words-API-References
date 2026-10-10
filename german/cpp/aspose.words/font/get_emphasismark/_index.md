---
title: "Aspose::Words::Font::get_EmphasisMark Methode"
linktitle: "get_EmphasisMark"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_EmphasisMark Methode. Gibt das Hervorhebungszeichen zurück oder legt es fest, das auf diese Formatierung in C++ angewendet wird."
type: docs
weight: 13000
url: /de/cpp/aspose.words/font/get_emphasismark/
---
## Font::get_EmphasisMark method


Liest oder setzt das Betonungszeichen, das auf diese Formatierung angewendet wird.

```cpp
Aspose::Words::EmphasisMark Aspose::Words::Font::get_EmphasisMark()
```


## Beispiele



Zeigt, wie ein zusätzliches Zeichen über/unter dem Glyphen‑Zeichen dargestellt werden kann.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// Mögliche Typen des Hervorhebungszeichens:
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder->get_Font()->set_EmphasisMark(emphasisMark);

builder->Write(u"Emphasis text");
builder->Writeln();
builder->get_Font()->ClearFormatting();
builder->Write(u"Simple text");

builder->get_Document()->Save(get_ArtifactsDir() + u"Fonts.SetEmphasisMark.docx");
```

## Siehe auch

* Enum [EmphasisMark](../../emphasismark/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
