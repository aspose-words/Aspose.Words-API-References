---
title: "Aspose::Words::EmphasisMark‑Enum"
linktitle: "EmphasisMark"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::EmphasisMark‑Enum. Gibt die möglichen Typen von Hervorhebungszeichen in C++ an."
type: docs
weight: 89000
url: /de/cpp/aspose.words/emphasismark/
---
## EmphasisMark enum


Gibt mögliche Typen von Hervorhebungszeichen an.

```cpp
enum class EmphasisMark
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | 0 | Kein Hervorhebungszeichen. |
| OverSolidCircle | 1 | Das Hervorhebungszeichen ist ein durchgehend schwarzer Kreis, der über dem Text angezeigt wird. |
| OverComma | 2 | Das Hervorhebungszeichen ist ein Komma‑Zeichen, das über dem Text angezeigt wird. |
| OverWhiteCircle | 3 | Das Hervorhebungszeichen ist ein leerer weißer Kreis, der über dem Text angezeigt wird. |
| UnderSolidCircle | 4 | Das Hervorhebungszeichen ist ein durchgehend schwarzer Kreis, der unter dem Text angezeigt wird. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
