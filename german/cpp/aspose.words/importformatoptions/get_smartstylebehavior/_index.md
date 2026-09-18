---
title: "Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior-Methode"
linktitle: "get_SmartStyleBehavior"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior-Methode. Gibt einen booleschen Wert zurück oder legt ihn fest, der angibt, wie Stile importiert werden, wenn sie in Quell- und Zieldokumenten denselben Namen haben. Der Standardwert ist false in C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words/importformatoptions/get_smartstylebehavior/
---
## ImportFormatOptions::get_SmartStyleBehavior method


Liest oder setzt einen booleschen Wert, der festlegt, wie Stile importiert werden, wenn sie in Quell‑ und Zieldokumenten denselben Namen haben. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior() const
```

## Hinweise


Wenn diese Option **aktiviert** ist, wird der Quellstil in direkte Attribute innerhalb eines Zieldokuments expandiert, falls der Importmodus [KeepSourceFormatting](../../importformatmode/) verwendet wird.

Wenn diese Option **deaktiviert** ist, wird der Quellstil nur expandiert, wenn er nummeriert ist. Vorhandene Zielattribute werden nicht überschrieben, einschließlich Listen.

## Beispiele



Zeigt, wie doppelte Formatvorlagen beim Einfügen von Dokumenten aufgelöst werden.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);

System::SharedPtr<Aspose::Words::Style> myStyle = builder->get_Document()->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
myStyle->get_Font()->set_Size(14);
myStyle->get_Font()->set_Name(u"Courier New");
myStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

builder->get_ParagraphFormat()->set_StyleName(myStyle->get_Name());
builder->Writeln(u"Hello world!");

// Kopiere das Dokument und bearbeite die "MyStyle"-Formatvorlage der Kopie, sodass sie eine andere Farbe als die des Originals hat.
// Wenn wir die Kopie in das Originaldokument einfügen, führen die beiden Formatvorlagen mit demselben Namen zu einem Konflikt.
System::SharedPtr<Aspose::Words::Document> srcDoc = dstDoc->Clone();
srcDoc->get_Styles()->idx_get(u"MyStyle")->get_Font()->set_Color(System::Drawing::Color::get_Red());

// Wenn wir SmartStyleBehavior aktivieren und den Importformatmodus KeepSourceFormatting verwenden,
// Aspose.Words löst Stilkonflikte, indem es die Formatvorlagen des Quelldokuments konvertiert.
// mit denselben Namen wie Ziel-Formatvorlagen in direkte Absatzattribute umwandelt.
auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_SmartStyleBehavior(true);

builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.SmartStyleBehavior.docx");
```

## Siehe auch

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
