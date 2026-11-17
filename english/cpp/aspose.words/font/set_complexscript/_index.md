---
title: Aspose::Words::Font::set_ComplexScript method
linktitle: set_ComplexScript
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::set_ComplexScript method. Specifies whether the contents of this run shall be treated as complex script text regardless of their Unicode character values when determining the formatting for this run in C++.'
type: docs
weight: 65000
url: /cpp/aspose.words/font/set_complexscript/
---
## Font::set_ComplexScript method


Specifies whether the contents of this run shall be treated as complex script text regardless of their Unicode character values when determining the formatting for this run.

```cpp
void Aspose::Words::Font::set_ComplexScript(bool value)
```

## Examples


Shows how to add text that is always treated as complex script.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_ComplexScript(true);

builder->Writeln(u"Text treated as complex script.");

doc->Save(get_ArtifactsDir() + u"Font.ComplexScript.docx");
```
## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
