---
title: "Aspose::Words::DropCapPosition enum"
linktitle: "DropCapPosition"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DropCapPosition enum. Anger positionen för en drop cap-text i C++."
type: docs
weight: 87000
url: /sv/cpp/aspose.words/dropcapposition/
---
## DropCapPosition enum


Anger positionen för en inledande versal (drop cap)-text.

```cpp
enum class DropCapPosition
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | 0 | Stycket har ingen drop cap. |
| Normal | 1 | Drop capen är placerad innanför textmarginalen på ankarestycket. |
| Marginal | 2 | Drop capen är placerad utanför textmarginalen på ankarestycket. |


## Exempel



Visar hur man skapar en drop cap.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga ett stycke med en stor bokstav som texten i det andra och tredje stycket börjar med.
builder->get_Font()->set_Size(54);
builder->Writeln(u"L");

builder->get_Font()->set_Size(18);
builder->Writeln(System::String(u"orem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder->Writeln(System::String(u"Ut enim ad minim veniam, quis nostrud exercitation ") + u"ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// För närvarande kommer det andra och tredje stycket att visas under det första.
// Vi kan konvertera det första stycket till en drop cap för de andra styckena via dess "ParagraphFormat"-objekt.
// Ställ in egenskapen "DropCapPosition" till "DropCapPosition.Margin" för att placera drop capen
// utanför vänstra sidmarginalen om vår text är vänster-till-höger.
// Ställ in egenskapen "DropCapPosition" till "DropCapPosition.Normal" för att placera drop capen inom sidmarginalerna
// och för att låta resten av texten flöda runt den.
// "DropCapPosition.None" är standardtillståndet för alla stycken.
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();
format->set_DropCapPosition(dropCapPosition);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.DropCap.docx");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
