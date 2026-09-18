---
title: "Aspose::Words::Font::get_NoProofing Methode"
linktitle: "get_NoProofing"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_NoProofing Methode. Wahr, wenn die formatierten Zeichen in C++ nicht rechtschreibgeprüft werden sollen."
type: docs
weight: 30000
url: /de/cpp/aspose.words/font/get_noproofing/
---
## Font::get_NoProofing method


Wahr, wenn die formatierten Zeichen nicht rechtschreibgeprüft werden sollen.

```cpp
bool Aspose::Words::Font::get_NoProofing()
```


## Beispiele



Zeigt, wie man verhindert, dass Text von Microsoft Word rechtschreibgeprüft wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Normalerweise hebt Microsoft Word Rechtschreibfehler mit einer gezackten roten Unterstreichung hervor.
// Wir können das Flag "NoProofing" zurücksetzen, um einen Textabschnitt zu erstellen, der
// den Rechtschreibprüfer umgeht, während er vollständig deaktiviert wird.
builder->get_Font()->set_NoProofing(true);

builder->Writeln(u"Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc->Save(get_ArtifactsDir() + u"Font.NoProofing.docx");
```

## Siehe auch

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
