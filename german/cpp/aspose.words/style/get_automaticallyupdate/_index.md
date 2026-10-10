---
title: "Aspose::Words::Style::get_AutomaticallyUpdate Methode"
linktitle: "get_AutomaticallyUpdate"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Style::get_AutomaticallyUpdate Methode. Gibt an, ob dieser Stil automatisch basierend auf dem entsprechenden Wert in C++ neu definiert wird."
type: docs
weight: 4000
url: /de/cpp/aspose.words/style/get_automaticallyupdate/
---
## Style::get_AutomaticallyUpdate method


Gibt an, ob dieser Stil basierend auf dem entsprechenden Wert automatisch neu definiert wird.

```cpp
bool Aspose::Words::Style::get_AutomaticallyUpdate() const
```

## Hinweise


Wenn der Eigenschaftswert auf true gesetzt ist, definiert MS Word den aktuellen Stil automatisch neu, wenn die entsprechende Absatzformatierung geändert wurde.

Die AutomaticallyUpdate‑Eigenschaft gilt nur für Absatzstile.

Der Standardwert ist **false**.

## Beispiele



Zeigt, wie man einen benutzerdefinierten Stil erstellt und anwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
style->get_Font()->set_Name(u"Times New Roman");
style->get_Font()->set_Size(16);
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
// Stil automatisch neu definieren.
style->set_AutomaticallyUpdate(true);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Wendet einen der Stile aus dem Dokument auf den Absatz an, den der Dokumenten-Builder erstellt.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Style> firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

ASPOSE_ASSERT_EQ(style, firstParagraphStyle);

// Entfernt unseren benutzerdefinierten Stil aus der Stilsammlung des Dokuments.
doc->get_Styles()->idx_get(u"MyStyle")->Remove();

firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

// Jeglicher Text, der einen entfernten Stil verwendet hat, wird zur Standardformatierung zurückkehren.
ASSERT_FALSE(doc->get_Styles()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Style>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Style> s)>>([](System::SharedPtr<Aspose::Words::Style> s) -> bool
{
    return s->get_Name() == u"MyStyle";
}))));
ASSERT_EQ(u"Times New Roman", firstParagraphStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(12.0, firstParagraphStyle->get_Font()->get_Size());
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), firstParagraphStyle->get_Font()->get_Color().ToArgb());
```

## Siehe auch

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
