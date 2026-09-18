---
title: "Aspose::Words::Font::get_ComplexScript-Methode"
linktitle: "get_ComplexScript"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_ComplexScript-Methode. Gibt an, ob der Inhalt dieses Laufs als komplexer Skripttext behandelt werden soll, unabhängig von seinen Unicode-Zeichenwerten, wenn die Formatierung dieses Laufs in C++ bestimmt wird."
type: docs
weight: 10000
url: /de/cpp/aspose.words/font/get_complexscript/
---
## Font::get_ComplexScript method


Gibt an, ob der Inhalt dieses Laufs als komplexer Skripttext behandelt werden soll, unabhängig von den Unicode‑Zeichenwerten, wenn die Formatierung dieses Laufs bestimmt wird.

```cpp
bool Aspose::Words::Font::get_ComplexScript()
```


## Beispiele



Zeigt, wie Text hinzugefügt wird, der immer als komplexes Skript behandelt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_ComplexScript(true);

builder->Writeln(u"Text treated as complex script.");

doc->Save(get_ArtifactsDir() + u"Font.ComplexScript.docx");
```

## Siehe auch

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
