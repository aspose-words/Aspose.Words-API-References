---
title: "Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked method"
linktitle: "get_AspectRatioLocked"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked method. Gibt an, ob das Seitenverhältnis der Form in C++ gesperrt ist."
type: docs
weight: 6000
url: /de/cpp/aspose.words.drawing/shapebase/get_aspectratiolocked/
---
## ShapeBase::get_AspectRatioLocked method


Gibt an, ob das Seitenverhältnis der Form gesperrt ist.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked()
```

## Hinweise


Der Standardwert hängt vom [ShapeType](../../shapetype/) ab; für das [Image](../../shapetype/) ist er **true**, für die anderen Formtypen ist er **false**.

Wirkt nur auf Formen der obersten Ebene.

## Beispiele



Zeigt, wie das Seitenverhältnis einer Form gesperrt/entsperrt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie eine Form ein. Wenn wir dieses Dokument in Microsoft Word öffnen, können wir die Form linksklicken, um
// acht Größengriffe um ihren Umfang zu sehen, die wir anklicken und ziehen können, um ihre Größe zu ändern.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Setzen Sie die Eigenschaft "AspectRatioLocked" auf "true", um das Seitenverhältnis der Form beizubehalten
// wenn Sie einen der vier diagonalen Größengriffe verwenden, die sowohl die Höhe als auch die Breite des Bildes ändern.
// Die Verwendung orthogonaler Größengriffe, die entweder die Höhe oder die Breite ändern, wird das Seitenverhältnis dennoch ändern.
// Setzen Sie die Eigenschaft "AspectRatioLocked" auf "false", um uns zu ermöglichen,
// das Seitenverhältnis des Bildes mit allen Größengriffen frei zu ändern.
shape->set_AspectRatioLocked(lockAspectRatio);

doc->Save(get_ArtifactsDir() + u"Shape.AspectRatio.docx");
```

## Siehe auch

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
