---
title: "Aspose::Words::Font::get_ComplexScript-metod"
linktitle: "get_ComplexScript"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_ComplexScript-metod. Anger om innehållet i detta körsegment ska behandlas som komplex skripttext oavsett deras Unicode-teckenvärden när formateringen för detta körsegment bestäms i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words/font/get_complexscript/
---
## Font::get_ComplexScript method


Anger om innehållet i detta körningssegment ska behandlas som komplex skripttext oavsett deras Unicode-teckenvärden när formateringen för segmentet bestäms.

```cpp
bool Aspose::Words::Font::get_ComplexScript()
```


## Exempel



Visar hur man lägger till text som alltid behandlas som komplex skript.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_ComplexScript(true);

builder->Writeln(u"Text treated as complex script.");

doc->Save(get_ArtifactsDir() + u"Font.ComplexScript.docx");
```

## Se även

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
