---
title: "Aspose::Words::Style::get_ParagraphFormat Methode"
linktitle: "get_ParagraphFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Style::get_ParagraphFormat Methode. Gibt die Absatzformatierung des Stils in C++ zurück."
type: docs
weight: 16000
url: /de/cpp/aspose.words/style/get_paragraphformat/
---
## Style::get_ParagraphFormat method


Liest die Absatzformatierung des Stils.

```cpp
System::SharedPtr<Aspose::Words::ParagraphFormat> Aspose::Words::Style::get_ParagraphFormat()
```

## Hinweise


Für Zeichen- und Listenstile gibt diese Eigenschaft **null** zurück.

## Beispiele



Zeigt, wie man einen Absatzstil mit Listformatierung erstellt und verwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstelle einen benutzerdefinierten Absatzstil.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Erstelle eine Liste und stelle sicher, dass die Absätze, die diesen Stil verwenden, diese Liste verwenden.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Wende den Absatzstil auf den aktuellen Absatz des DocumentBuilder an und füge dann etwas Text hinzu.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Ändere den Stil des DocumentBuilder zu einem, das keine Listformatierung hat, und schreibe einen weiteren Absatz.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## Siehe auch

* Class [ParagraphFormat](../../paragraphformat/)
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
