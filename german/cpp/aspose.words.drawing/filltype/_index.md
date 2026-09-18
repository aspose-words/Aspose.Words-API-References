---
title: "Aspose::Words::Drawing::FillType enum"
linktitle: "FillType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::FillType enum. Gibt den Fülltyp für ein ausfüllbares Objekt in C++ an."
type: docs
weight: 22000
url: /de/cpp/aspose.words.drawing/filltype/
---
## FillType enum


Gibt den Fülltyp für ein füllbares Objekt an.

```cpp
enum class FillType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Durchgezogen | 1 | Solide Füllung. |
| Patterned | 2 | Gemusterte Füllung. |
| Gradient | 3 | Verlaufsfüllung. |
| Textured | 4 | Texturierte Füllung. |
| Background | 5 | [Fill](../fill/) ist dasselbe wie der Hintergrund. |
| Bild | 6 | Bildfüllung. |


## Beispiele



Zeigt, wie man beliebige Füllungen zurück in eine solide Füllung konvertiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Two color gradient.docx");

// Hole das Fill-Objekt für die Schriftart des ersten Runs.
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_Font()->get_Fill();

// Überprüfe die Fill-Eigenschaften der Schriftart.
std::cout << System::String::Format(u"The type of the fill is: {0}", fill->get_FillType()) << std::endl;
std::cout << "The foreground color of the fill is: " << fill->get_ForeColor() << std::endl;
std::cout << "The fill is transparent at " << (fill->get_Transparency() * 100) << "%" << std::endl;

// Ändere den Typ der Füllung zu Solid mit einheitlicher grüner Farbe.
fill->Solid();
std::cout << "\nThe fill is changed:" << std::endl;
std::cout << System::String::Format(u"The type of the fill is: {0}", fill->get_FillType()) << std::endl;
std::cout << "The foreground color of the fill is: " << fill->get_ForeColor() << std::endl;
std::cout << "The fill transparency is " << (fill->get_Transparency() * 100) << "%" << std::endl;

doc->Save(get_ArtifactsDir() + u"Drawing.FillSolid.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
