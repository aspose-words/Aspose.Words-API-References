---
title: "Aspose::Words::CleanupOptions::get_DuplicateStyle Methode"
linktitle: "get_DuplicateStyle"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::CleanupOptions::get_DuplicateStyle Methode. Liest/setzt ein Flag, das angibt, ob doppelte Stile aus dem Dokument entfernt werden sollen. Der Standardwert ist false in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words/cleanupoptions/get_duplicatestyle/
---
## CleanupOptions::get_DuplicateStyle method


Liest/legt ein Flag fest, das angibt, ob doppelte Formatvorlagen aus dem Dokument entfernt werden sollen. Standardwert ist **false**.

```cpp
bool Aspose::Words::CleanupOptions::get_DuplicateStyle() const
```


## Beispiele



Zeigt, wie doppelte Stile aus dem Dokument entfernt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Fügen Sie dem Dokument zwei Stile mit identischen Eigenschaften hinzu,
// aber unterschiedlichen Namen. Der zweite Stil wird als Duplikat des ersten betrachtet.
System::SharedPtr<Aspose::Words::Style> myStyle = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
myStyle->get_Font()->set_Size(14);
myStyle->get_Font()->set_Name(u"Courier New");
myStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

System::SharedPtr<Aspose::Words::Style> duplicateStyle = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle2");
duplicateStyle->get_Font()->set_Size(14);
duplicateStyle->get_Font()->set_Name(u"Courier New");
duplicateStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

ASSERT_EQ(6, doc->get_Styles()->get_Count());

// Wenden Sie beide Stile auf verschiedene Absätze im Dokument an.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_ParagraphFormat()->set_StyleName(myStyle->get_Name());
builder->Writeln(u"Hello world!");

builder->get_ParagraphFormat()->set_StyleName(duplicateStyle->get_Name());
builder->Writeln(u"Hello again!");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASPOSE_ASSERT_EQ(myStyle, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Style());
ASPOSE_ASSERT_EQ(duplicateStyle, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Style());

// Konfigurieren Sie ein CleanOptions‑Objekt und rufen Sie anschließend die Cleanup‑Methode auf, um alle doppelten Stile zu ersetzen
// durch das Original und entfernen Sie die Duplikate aus dem Dokument.
auto cleanupOptions = System::MakeObject<Aspose::Words::CleanupOptions>();
cleanupOptions->set_DuplicateStyle(true);

doc->Cleanup(cleanupOptions);

ASSERT_EQ(5, doc->get_Styles()->get_Count());
ASPOSE_ASSERT_EQ(myStyle, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Style());
ASPOSE_ASSERT_EQ(myStyle, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Style());
```

## Siehe auch

* Class [CleanupOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
