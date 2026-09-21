---
title: "Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked metod"
linktitle: "get_AspectRatioLocked"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked metod. Anger om figurens bildförhållande är låst i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.drawing/shapebase/get_aspectratiolocked/
---
## ShapeBase::get_AspectRatioLocked method


Anger om formens bildförhållande är låst.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked()
```

## Anmärkningar


Standardvärdet beror på [ShapeType](../../shapetype/), för [Image](../../shapetype/) är det **true** men för de andra figurtyperna är det **false**.

Har effekt endast för former på toppnivå.

## Exempel



Visar hur man låser/upplåser en figurs bildförhållande.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en form. Om vi öppnar detta dokument i Microsoft Word kan vi vänsterklicka på formen för att avslöja
// åtta storlekshandtag runt dess omkrets, som vi kan klicka och dra för att ändra dess storlek.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Ställ in egenskapen \"AspectRatioLocked\" till \"true\" för att bevara figurens bildförhållande
// när du använder någon av de fyra diagonala storlekshandtagen, som ändrar både bildens höjd och bredd.
// Att använda någon ortogonal storlekshandtag som antingen ändrar höjden eller bredden kommer fortfarande att ändra bildförhållandet.
// Ställ in egenskapen \"AspectRatioLocked\" till \"false\" för att låta oss
// fritt ändra bildens bildförhållande med alla storlekshandtag.
shape->set_AspectRatioLocked(lockAspectRatio);

doc->Save(get_ArtifactsDir() + u"Shape.AspectRatio.docx");
```

## Se även

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
