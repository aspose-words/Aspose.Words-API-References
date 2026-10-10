---
title: "Aspose::Words::Drawing::ShapeBase::get_HRef metod"
linktitle: "get_HRef"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_HRef metod. Hämtar eller anger den fullständiga hyperlänkadressen för en form i C++."
type: docs
weight: 24000
url: /sv/cpp/aspose.words.drawing/shapebase/get_href/
---
## ShapeBase::get_HRef method


Hämtar eller anger den fullständiga hyperlänkadressen för en form.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_HRef()
```

## Anmärkningar


Standardvärdet är en tom sträng.

Nedan följer exempel på giltiga värden för denna egenskap:

Fullständig URI: **https://www.aspose.com/**.

Fullständigt filnamn: **C:\\My Documents\\SalesReport.doc**.

Relativ URI: **%../../../resource.txt**

Relativt filnamn: **%..\\My Documents\\SalesReport.doc**.

[Bookmark](../../../aspose.words/bookmark/) within another document: **https://www.aspose.com/Products/Default.aspx::Suites**

[Bookmark](../../../aspose.words/bookmark/) within this document: **%#BookmakName**.

## Exempel



Visar hur man infogar en form som innehåller en bild och också är en hyperlänk.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_HRef(u"https://forum.aspose.com/");
shape->set_Target(u"New Window");
shape->set_ScreenTip(u"Aspose.Words Support Forums");

// Ctrl + vänsterklick på formen i Microsoft Word öppnar ett nytt webbläsarfönster
// och tar oss till hyperlänken i egenskapen "HRef".
doc->Save(get_ArtifactsDir() + u"Image.InsertImageWithHyperlink.docx");
```

## Se även

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
