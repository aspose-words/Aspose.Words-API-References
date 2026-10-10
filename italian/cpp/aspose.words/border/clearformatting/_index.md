---
title: "Aspose::Words::Border::ClearFormatting metodo"
linktitle: "ClearFormatting"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Border::ClearFormatting metodo. Reimposta le proprietà del bordo ai valori predefiniti in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/border/clearformatting/
---
## Border::ClearFormatting method


Reimposta le proprietà del bordo ai valori predefiniti.

```cpp
void Aspose::Words::Border::ClearFormatting()
```


## Esempi



Mostra come rimuovere i bordi da un paragrafo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Borders.docx");

// Ogni paragrafo ha un insieme individuale di bordi.
// Possiamo accedere alle impostazioni per l'aspetto di questi bordi tramite l'oggetto di formattazione del paragrafo.
System::SharedPtr<Aspose::Words::BorderCollection> borders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), borders->idx_get(0)->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(3.0, borders->idx_get(0)->get_LineWidth());
ASSERT_EQ(Aspose::Words::LineStyle::Single, borders->idx_get(0)->get_LineStyle());
ASSERT_TRUE(borders->idx_get(0)->get_IsVisible());

// Possiamo rimuovere un bordo in una volta eseguendo il metodo ClearFormatting.
// Eseguendo questo metodo su ogni bordo di un paragrafo verranno rimossi tutti i suoi bordi.
for (auto&& border : System::IterateOver(borders))
{
    border->ClearFormatting();
}

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), borders->idx_get(0)->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(0.0, borders->idx_get(0)->get_LineWidth());
ASSERT_EQ(Aspose::Words::LineStyle::None, borders->idx_get(0)->get_LineStyle());
ASSERT_FALSE(borders->idx_get(0)->get_IsVisible());

doc->Save(get_ArtifactsDir() + u"Border.ClearFormatting.docx");
```

## Vedi anche

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
