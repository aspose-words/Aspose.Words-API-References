---
title: "Aspose::Words::Font::get_EmphasisMark method"
linktitle: "get_EmphasisMark"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_EmphasisMark metod. Hämtar eller anger betoningstecknet som tillämpas på denna formatering i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words/font/get_emphasismark/
---
## Font::get_EmphasisMark method


Hämtar eller anger betoningstecknet som tillämpas på denna formatering.

```cpp
Aspose::Words::EmphasisMark Aspose::Words::Font::get_EmphasisMark()
```


## Exempel



Visar hur man lägger till ett extra tecken som renderas ovanför/under glyf‑tecknet.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// Möjliga typer av betoningstecken:
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder->get_Font()->set_EmphasisMark(emphasisMark);

builder->Write(u"Emphasis text");
builder->Writeln();
builder->get_Font()->ClearFormatting();
builder->Write(u"Simple text");

builder->get_Document()->Save(get_ArtifactsDir() + u"Fonts.SetEmphasisMark.docx");
```

## Se även

* Enum [EmphasisMark](../../emphasismark/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
