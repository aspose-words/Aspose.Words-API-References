---
title: "Aspose::Words::Font::get_StyleName Methode"
linktitle: "get_StyleName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_StyleName Methode. Gibt den Namen des Zeichenstils zurück oder legt ihn fest, der auf diese Formatierung in C++ angewendet wird."
type: docs
weight: 44000
url: /de/cpp/aspose.words/font/get_stylename/
---
## Font::get_StyleName method


Liest oder legt den Namen des auf diese Formatierung angewendeten Zeichenstils fest.

```cpp
System::String Aspose::Words::Font::get_StyleName()
```


## Beispiele



Zeigt, wie der Stil von vorhandenem Text geändert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Unten sind zwei Möglichkeiten, Stile zu referenzieren.
// 1 -  Verwendung des Stilsnamens:
builder->get_Font()->set_StyleName(u"Emphasis");
builder->Writeln(u"Text originally in \"Emphasis\" style");

// 2 -  Verwendung eines integrierten Stilidentifikators:
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::IntenseEmphasis);
builder->Writeln(u"Text originally in \"Intense Emphasis\" style");

// Konvertiere alle Verwendungen eines Stils in einen anderen,
// unter Verwendung der obigen Methoden, um alte und neue Stile zu referenzieren.
for (auto&& run : System::IterateOver<Aspose::Words::Run>(doc->GetChildNodes(Aspose::Words::NodeType::Run, true)))
{
    if (run->get_Font()->get_StyleName() == u"Emphasis")
    {
        run->get_Font()->set_StyleName(u"Strong");
    }

    if (run->get_Font()->get_StyleIdentifier() == Aspose::Words::StyleIdentifier::IntenseEmphasis)
    {
        run->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Strong);
    }
}

doc->Save(get_ArtifactsDir() + u"Font.ChangeStyle.docx");
```

## Siehe auch

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
