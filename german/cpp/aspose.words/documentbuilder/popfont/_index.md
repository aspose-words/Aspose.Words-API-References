---
title: "Aspose::Words::DocumentBuilder::PopFont Methode"
linktitle: "PopFont"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::PopFont Methode. Ruft die zuvor auf dem Stack gespeicherte Zeichenformatierung in C++ ab."
type: docs
weight: 62000
url: /de/cpp/aspose.words/documentbuilder/popfont/
---
## DocumentBuilder::PopFont method


Ruft die zuvor auf dem Stack gespeicherte Zeichenformatierung ab.

```cpp
void Aspose::Words::DocumentBuilder::PopFont()
```


## Beispiele



Zeigt, wie man den Formatierungsstapel eines Document Builders verwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Richten Sie die Schriftformatierung ein und schreiben Sie dann den Text, der vor dem Hyperlink steht.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(24);
builder->Write(u"To visit Google, hold Ctrl and click ");

// Behalte unsere aktuelle Formatierungskonfiguration im Stack bei.
builder->PushFont();

// Ändere die aktuelle Formatierung des Builders, indem du einen neuen Stil anwendest.
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Hyperlink);
builder->InsertHyperlink(u"here", u"http://www.google.com", false);

ASSERT_EQ(System::Drawing::Color::get_Blue().ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::Single, builder->get_Font()->get_Underline());

// Stelle die zuvor gespeicherte Schriftformatierung wieder her und entferne das Element aus dem Stack.
builder->PopFont();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::None, builder->get_Font()->get_Underline());

builder->Write(u". We hope you enjoyed the example.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.PushPopFont.docx");
```

## Siehe auch

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
