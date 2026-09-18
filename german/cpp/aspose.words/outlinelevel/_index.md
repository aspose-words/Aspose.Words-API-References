---
title: "Aspose::Words::OutlineLevel Aufzählung"
linktitle: "OutlineLevel"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::OutlineLevel enum. Gibt das Gliederungsebenenniveau eines Absatzes im Dokument in C++ an."
type: docs
weight: 105000
url: /de/cpp/aspose.words/outlinelevel/
---
## OutlineLevel enum


Gibt die Gliederungsebene eines Absatzes im Dokument an.

```cpp
enum class OutlineLevel
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Level1 | 0 | Der Absatz befindet sich auf Gliederungsebene 1 (oberste Ebene). |
| Level2 | 1 | Der Absatz befindet sich auf Gliederungsebene 2. |
| Level3 | 2 | Der Absatz befindet sich auf Gliederungsebene 3. |
| Level4 | 3 | Der Absatz befindet sich auf Gliederungsebene 4. |
| Level5 | 4 | Der Absatz befindet sich auf Gliederungsebene 5. |
| Level6 | 5 | Der Absatz befindet sich auf Gliederungsebene 6. |
| Level7 | 6 | Der Absatz befindet sich auf Gliederungsebene 7. |
| Level8 | 7 | Der Absatz befindet sich auf Gliederungsebene 8. |
| Level9 | 8 | Der Absatz befindet sich auf Gliederungsebene 9. |
| BodyText | 9 | Der Absatz befindet sich auf der Ebene des Haupttextes. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
