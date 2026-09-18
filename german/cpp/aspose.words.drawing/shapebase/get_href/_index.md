---
title: "Aspose::Words::Drawing::ShapeBase::get_HRef-Methode"
linktitle: "get_HRef"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_HRef-Methode. Ruft die vollständige Hyperlink-Adresse für eine Form ab oder legt sie fest, in C++."
type: docs
weight: 24000
url: /de/cpp/aspose.words.drawing/shapebase/get_href/
---
## ShapeBase::get_HRef method


Liest oder legt die vollständige Hyperlink-Adresse für eine Form fest.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_HRef()
```

## Hinweise


Der Standardwert ist eine leere Zeichenfolge.

Nachfolgend Beispiele für gültige Werte dieser Eigenschaft:

Vollständige URI: **https://www.aspose.com/**.

Vollständiger Dateiname: **C:\\My Documents\\SalesReport.doc**.

Relative URI: **%../../../resource.txt**

Relativer Dateiname: **%..\\My Documents\\SalesReport.doc**.

[Bookmark](../../../aspose.words/bookmark/) within another document: **https://www.aspose.com/Products/Default.aspx::Suites**

[Bookmark](../../../aspose.words/bookmark/) within this document: **%#BookmakName**.

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
