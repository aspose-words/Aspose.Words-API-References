---
title: "Aspose::Words::Drawing::ShapeBase::get_ScreenTip Methode"
linktitle: "get_ScreenTip"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_ScreenTip Methode. Definiert den Text, der angezeigt wird, wenn der Mauszeiger über die Form bewegt wird in C++."
type: docs
weight: 46000
url: /de/cpp/aspose.words.drawing/shapebase/get_screentip/
---
## ShapeBase::get_ScreenTip method


Definiert den Text, der angezeigt wird, wenn der Mauszeiger über die Form bewegt wird.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_ScreenTip()
```

## Hinweise


Der Standardwert ist eine leere Zeichenfolge.

## Beispiele



Zeigt, wie man eine Form einfügt, die ein Bild enthält und zudem ein Hyperlink ist.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_HRef(u"https://forum.aspose.com/");
shape->set_Target(u"New Window");
shape->set_ScreenTip(u"Aspose.Words Support Forums");

// Strg + Linksklick auf die Form in Microsoft Word öffnet ein neues Webbrowser-Fenster
// und führt uns zum Hyperlink in der "HRef"-Eigenschaft.
doc->Save(get_ArtifactsDir() + u"Image.InsertImageWithHyperlink.docx");
```

## Siehe auch

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
