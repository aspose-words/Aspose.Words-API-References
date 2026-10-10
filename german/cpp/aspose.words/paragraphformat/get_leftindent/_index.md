---
title: "Aspose::Words::ParagraphFormat::get_LeftIndent-Methode"
linktitle: "get_LeftIndent"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ParagraphFormat::get_LeftIndent-Methode. Gibt den Wert (in Punkten) zurück oder legt ihn fest, der den linken Einzug für einen Absatz in C++ darstellt."
type: docs
weight: 19000
url: /de/cpp/aspose.words/paragraphformat/get_leftindent/
---
## ParagraphFormat::get_LeftIndent method


Liest oder legt den Wert (in Punkten) fest, der den linken Einzug für den Absatz darstellt.

```cpp
double Aspose::Words::ParagraphFormat::get_LeftIndent()
```


## Beispiele



Zeigt, wie man Absatzformatierung konfiguriert, um nicht zentrierten Text zu erzeugen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Zentrieren Sie den gesamten Text, den der Dokumenten-Builder schreibt, und richten Sie Einzüge ein.
// Die nachstehende Einzugs-Konfiguration erzeugt einen Textkörper, der asymmetrisch auf der Seite positioniert wird.
// Das "Zentrum", an dem wir den Text ausrichten, ist die Mitte des Textkörpers, nicht die Mitte der Seite.
System::SharedPtr<Aspose::Words::ParagraphFormat> paragraphFormat = builder->get_ParagraphFormat();
paragraphFormat->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
paragraphFormat->set_LeftIndent(100);
paragraphFormat->set_RightIndent(50);
paragraphFormat->set_SpaceAfter(25);

builder->Writeln(u"This paragraph demonstrates how left and right indentation affects word wrapping.");
builder->Writeln(u"The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetParagraphFormatting.docx");
```

## Siehe auch

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
