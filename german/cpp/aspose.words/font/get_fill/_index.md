---
title: "Aspose::Words::Font::get_Fill Methode"
linktitle: "get_Fill"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_Fill Methode. Ruft die Füllformatierung für die Schrift in C++ ab."
type: docs
weight: 15000
url: /de/cpp/aspose.words/font/get_fill/
---
## Font::get_Fill method


Ruft die Füllformatierung für die [Font](../) ab.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Fill> Aspose::Words::Font::get_Fill()
```


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

* Class [Fill](../../../aspose.words.drawing/fill/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
