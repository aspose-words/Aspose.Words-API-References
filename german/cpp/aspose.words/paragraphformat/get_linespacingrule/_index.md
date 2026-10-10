---
title: "Aspose::Words::ParagraphFormat::get_LineSpacingRule-Methode"
linktitle: "get_LineSpacingRule"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ParagraphFormat::get_LineSpacingRule-Methode. Gibt den Zeilenabstand für den Absatz in C++ zurück oder legt ihn fest."
type: docs
weight: 21000
url: /de/cpp/aspose.words/paragraphformat/get_linespacingrule/
---
## ParagraphFormat::get_LineSpacingRule method


Liest oder legt den Zeilenabstand für den Absatz fest.

```cpp
Aspose::Words::LineSpacingRule Aspose::Words::ParagraphFormat::get_LineSpacingRule()
```


## Beispiele



Zeigt, wie man mit Zeilenabstand arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Unten sind drei Zeilenabstandsregeln, die wir mit Hilfe von
// der "LineSpacingRule"‑Eigenschaft des Absatzes, um den Abstand zwischen Absätzen zu konfigurieren.
// 1 -  Legen Sie einen Mindestabstand fest.
// Dies gibt vertikalen Abstand zu Textzeilen jeder Größe.
// der zu klein ist, um die minimale Zeilenhöhe beizubehalten.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::AtLeast);
builder->get_ParagraphFormat()->set_LineSpacing(20);

builder->Writeln(u"Minimum line spacing of 20.");
builder->Writeln(u"Minimum line spacing of 20.");

// 2 -  Legen Sie einen genauen Abstand fest.
// Die Verwendung von Schriftgrößen, die für den Abstand zu groß sind, schneidet den Text ab.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::Exactly);
builder->get_ParagraphFormat()->set_LineSpacing(5);

builder->Writeln(u"Line spacing of exactly 5.");
builder->Writeln(u"Line spacing of exactly 5.");

// 3 -  Legen Sie den Abstand als Vielfaches des Standardzeilenabstands fest, der standardmäßig 12 Punkte beträgt.
// Diese Art von Abstand skaliert mit unterschiedlichen Schriftgrößen.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::Multiple);
builder->get_ParagraphFormat()->set_LineSpacing(18);

builder->Writeln(u"Line spacing of 1.5 default lines.");
builder->Writeln(u"Line spacing of 1.5 default lines.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.LineSpacing.docx");
```

## Siehe auch

* Enum [LineSpacingRule](../../linespacingrule/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
