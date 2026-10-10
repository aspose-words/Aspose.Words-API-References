---
title: "Aspose::Words::Border::get_IsVisible Methode"
linktitle: "get_IsVisible"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Border::get_IsVisible Methode. Gibt true zurück, wenn der LineStyle nicht None ist in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words/border/get_isvisible/
---
## Border::get_IsVisible method


Gibt **true** zurück, wenn der [LineStyle](../get_linestyle/) nicht [None](../../linestyle/) ist.

```cpp
bool Aspose::Words::Border::get_IsVisible()
```


## Beispiele



Zeigt, wie man Rahmen aus einem Absatz entfernt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Borders.docx");

// Jeder Absatz hat einen eigenen Satz von Rahmen.
// Wir können über das Absatzformat-Objekt auf die Einstellungen für das Aussehen dieser Rahmen zugreifen.
System::SharedPtr<Aspose::Words::BorderCollection> borders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), borders->idx_get(0)->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(3.0, borders->idx_get(0)->get_LineWidth());
ASSERT_EQ(Aspose::Words::LineStyle::Single, borders->idx_get(0)->get_LineStyle());
ASSERT_TRUE(borders->idx_get(0)->get_IsVisible());

// Wir können einen Rahmen auf einmal entfernen, indem wir die ClearFormatting‑Methode ausführen.
// Wenn diese Methode für jeden Rahmen eines Absatzes ausgeführt wird, werden alle seine Rahmen entfernt.
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

## Siehe auch

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
