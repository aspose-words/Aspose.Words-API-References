---
title: "Aspose::Words::EmphasisMark enum"
linktitle: "EmphasisMark"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::EmphasisMark enum. Anger möjliga typer av betoningstecken i C++."
type: docs
weight: 89000
url: /sv/cpp/aspose.words/emphasismark/
---
## EmphasisMark enum


Anger möjliga typer av betoningstecken.

```cpp
enum class EmphasisMark
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | 0 | Ingen betoningstecken. |
| OverSolidCircle | 1 | Betoningstecken är en solid svart cirkel som visas ovanför text. |
| OverComma | 2 | Betoningstecken är ett kommatecken som visas ovanför text. |
| OverWhiteCircle | 3 | Betoningstecken är en tom vit cirkel som visas ovanför text. |
| UnderSolidCircle | 4 | Betoningstecken är en solid svart cirkel som visas under text. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
