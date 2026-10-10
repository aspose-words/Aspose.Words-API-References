---
title: "Aspose::Words::Font::get_Border Methode"
linktitle: "get_Border"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_Border Methode. Gibt ein Border-Objekt zurück, das den Rand für die Schriftart in C++ angibt."
type: docs
weight: 8000
url: /de/cpp/aspose.words/font/get_border/
---
## Font::get_Border method


Gibt ein [Border](../../border/) Objekt zurück, das den Rand für die Schriftart angibt.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::Font::get_Border()
```


## Beispiele



Zeigt, wie man eine von einem Rahmen umgebene Zeichenkette in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```

## Siehe auch

* Class [Border](../../border/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
