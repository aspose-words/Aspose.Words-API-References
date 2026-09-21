---
title: "Aspose::Words::Border::get_IsVisible metod"
linktitle: "get_IsVisible"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Border::get_IsVisible metod. Returnerar **true** om LineStyle inte är None i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words/border/get_isvisible/
---
## Border::get_IsVisible method


Returnerar **true** om [LineStyle](../get_linestyle/) inte är [None](../../linestyle/).

```cpp
bool Aspose::Words::Border::get_IsVisible()
```


## Exempel



Visar hur man tar bort kanter från ett stycke.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Borders.docx");

// Varje stycke har en egen uppsättning kanter.
// Vi kan komma åt inställningarna för utseendet på dessa kanter via styckeformatobjektet.
System::SharedPtr<Aspose::Words::BorderCollection> borders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), borders->idx_get(0)->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(3.0, borders->idx_get(0)->get_LineWidth());
ASSERT_EQ(Aspose::Words::LineStyle::Single, borders->idx_get(0)->get_LineStyle());
ASSERT_TRUE(borders->idx_get(0)->get_IsVisible());

// Vi kan ta bort en kant på en gång genom att köra ClearFormatting‑metoden.
// Att köra den här metoden på varje kant i ett stycke kommer att ta bort alla dess kanter.
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

## Se även

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
