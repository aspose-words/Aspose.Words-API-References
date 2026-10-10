---
title: "Aspose::Words::ConvertUtil::PointToInch method"
linktitle: "PointToInch"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ConvertUtil::PointToInch-Methode. Konvertiert Punkte in Zoll in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words/convertutil/pointtoinch/
---
## ConvertUtil::PointToInch method


Konvertiert Punkte in Zoll.

```cpp
static double Aspose::Words::ConvertUtil::PointToInch(double points)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Punkte | double | Der zu konvertierende Wert. |

## Beispiele



Zeigt, wie man Seiteneigenschaften in Zoll angibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Der \"Page Setup\" eines Abschnitts definiert die Größe der Seitenränder in Punkten.
// Wir können auch die Klasse \"ConvertUtil\" verwenden, um eine vertrautere Maßeinheit zu nutzen,
// wie Zoll beim Definieren von Grenzen.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::InchToPoint(2.0));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::InchToPoint(2.5));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));

// Ein Zoll entspricht 72 Punkten.
ASPOSE_ASSERT_EQ(72.0, Aspose::Words::ConvertUtil::InchToPoint(1));
ASPOSE_ASSERT_EQ(1.0, Aspose::Words::ConvertUtil::PointToInch(72));

// Fügen Sie Inhalt hinzu, um die neuen Ränder zu demonstrieren.
builder->Writeln(System::String::Format(u"This Text is {0} points/{1} inches from the left, ", pageSetup->get_LeftMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_LeftMargin())) + System::String::Format(u"{0} points/{1} inches from the right, ", pageSetup->get_RightMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_RightMargin())) + System::String::Format(u"{0} points/{1} inches from the top, ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_TopMargin())) + System::String::Format(u"and {0} points/{1} inches from the bottom of the page.", pageSetup->get_BottomMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_BottomMargin())));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndInches.docx");
```

## Siehe auch

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
