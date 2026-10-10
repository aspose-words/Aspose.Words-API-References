---
title: "Aspose::Words::ParagraphFormat::get_OutlineLevel Methode"
linktitle: "get_OutlineLevel"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ParagraphFormat::get_OutlineLevel Methode. Gibt die Gliederungsebene des Absatzes im Dokument in C++ an."
type: docs
weight: 26000
url: /de/cpp/aspose.words/paragraphformat/get_outlinelevel/
---
## ParagraphFormat::get_OutlineLevel method


Gibt die Gliederungsebene des Absatzes im Dokument an.

```cpp
Aspose::Words::OutlineLevel Aspose::Words::ParagraphFormat::get_OutlineLevel()
```


## Beispiele



Zeigt, wie man Gliederungsebenen von Absätzen konfiguriert, um zusammenklappbaren Text zu erstellen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Jeder Absatz hat ein OutlineLevel, das jede Zahl von 1 bis 9 sein kann oder den Standardwert "BodyText" hat.
// Das Setzen der Eigenschaft auf einen der nummerierten Werte zeigt einen Pfeil links
// am Anfang des Absatzes.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level1);
builder->Writeln(u"Paragraph outline level 1.");

// Ebene 1 ist die höchste Ebene. Wenn es einen Absatz mit einer niedrigeren Ebene unter einem Absatz mit einer höheren Ebene gibt,
// Das Einklappen des Absatzes mit höherer Ebene klappt den Absatz mit niedrigerer Ebene ein.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level2);
builder->Writeln(u"Paragraph outline level 2.");

// Zwei Absätze derselben Ebene klappen nicht gegenseitig ein,
// und die Pfeile klappen die Absätze, auf die sie zeigen, nicht ein.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level3);
builder->Writeln(u"Paragraph outline level 3.");
builder->Writeln(u"Paragraph outline level 3.");

// Der Standardwert "BodyText" ist der niedrigste, den ein Absatz jeder Ebene einklappen kann.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::BodyText);
builder->Writeln(u"Paragraph at main text level.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphOutlineLevel.docx");
```

## Siehe auch

* Enum [OutlineLevel](../../outlinelevel/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
