---
title: "Aspose::Words::ConvertUtil::MillimeterToPoint Methode"
linktitle: "MillimeterToPoint"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ConvertUtil::MillimeterToPoint Methode. Konvertiert Millimeter zu Punkten in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words/convertutil/millimetertopoint/
---
## ConvertUtil::MillimeterToPoint method


Konvertiert Millimeter in Punkte.

```cpp
static double Aspose::Words::ConvertUtil::MillimeterToPoint(double millimeters)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Millimeter | double | Der zu konvertierende Wert. |

## Beispiele



Zeigt, wie man Seiten‑eigenschaften in Millimetern angibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Der \"Page Setup\" eines Abschnitts definiert die Größe der Seitenränder in Punkten.
// Wir können auch die Klasse \"ConvertUtil\" verwenden, um eine vertrautere Maßeinheit zu nutzen,
// wie Millimeter beim Definieren von Grenzen.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(30));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(50));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(80));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(40));

// Ein Zentimeter entspricht ungefähr 28,3 Punkten.
ASSERT_NEAR(28.34, Aspose::Words::ConvertUtil::MillimeterToPoint(10), 0.01);

// Fügen Sie Inhalt hinzu, um die neuen Ränder zu demonstrieren.
builder->Writeln(System::String::Format(u"This Text is {0} points from the left, ", pageSetup->get_LeftMargin()) + System::String::Format(u"{0} points from the right, ", pageSetup->get_RightMargin()) + System::String::Format(u"{0} points from the top, ", pageSetup->get_TopMargin()) + System::String::Format(u"and {0} points from the bottom of the page.", pageSetup->get_BottomMargin()));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndMillimeters.docx");
```

## Siehe auch

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
