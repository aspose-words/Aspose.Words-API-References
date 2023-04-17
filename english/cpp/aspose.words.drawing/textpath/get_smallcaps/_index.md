---
title: Aspose::Words::Drawing::TextPath::get_SmallCaps method
linktitle: get_SmallCaps
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::TextPath::get_SmallCaps method. True if the font is formatted as small capital letters in C++.'
type: docs
weight: 14000
url: /cpp/aspose.words.drawing/textpath/get_smallcaps/
---
## TextPath::get_SmallCaps method


True if the font is formatted as small capital letters.

```cpp
bool Aspose::Words::Drawing::TextPath::get_SmallCaps()
```

## Remarks


The default value is **false**.

## Examples



Shows how to work with WordArt. 
```cpp
void InsertTextPaths()
{
    auto doc = MakeObject<Document>();

    // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
    // Provide a "ShapeType" as an argument to set a shape for the WordArt.
    SharedPtr<Shape> shape = AppendWordArt(doc, u"Hello World! This text is bold, and italic.", u"Arial", 480, 24, System::Drawing::Color::get_White(),
                                           System::Drawing::Color::get_Black(), ShapeType::TextPlainText);

    // Apply the "Bold' and "Italic" formatting settings to the text using the respective properties.
    shape->get_TextPath()->set_Bold(true);
    shape->get_TextPath()->set_Italic(true);

    // Below are various other text formatting-related properties.
    ASSERT_FALSE(shape->get_TextPath()->get_Underline());
    ASSERT_FALSE(shape->get_TextPath()->get_Shadow());
    ASSERT_FALSE(shape->get_TextPath()->get_StrikeThrough());
    ASSERT_FALSE(shape->get_TextPath()->get_ReverseRows());
    ASSERT_FALSE(shape->get_TextPath()->get_XScale());
    ASSERT_FALSE(shape->get_TextPath()->get_Trim());
    ASSERT_FALSE(shape->get_TextPath()->get_SmallCaps());

    ASPOSE_ASSERT_EQ(36.0, shape->get_TextPath()->get_Size());
    ASSERT_EQ(u"Hello World! This text is bold, and italic.", shape->get_TextPath()->get_Text());
    ASSERT_EQ(ShapeType::TextPlainText, shape->get_ShapeType());

    // Use the "On" property to show/hide the text.
    shape = AppendWordArt(doc, u"On set to \"true\"", u"Calibri", 150, 24, System::Drawing::Color::get_Yellow(), System::Drawing::Color::get_Red(),
                          ShapeType::TextPlainText);
    shape->get_TextPath()->set_On(true);

    shape = AppendWordArt(doc, u"On set to \"false\"", u"Calibri", 150, 24, System::Drawing::Color::get_Yellow(), System::Drawing::Color::get_Purple(),
                          ShapeType::TextPlainText);
    shape->get_TextPath()->set_On(false);

    // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
    shape = AppendWordArt(doc, u"Kerning: VAV", u"Times New Roman", 90, 24, System::Drawing::Color::get_Orange(), System::Drawing::Color::get_Red(),
                          ShapeType::TextPlainText);
    shape->get_TextPath()->set_Kerning(true);

    shape = AppendWordArt(doc, u"No kerning: VAV", u"Times New Roman", 100, 24, System::Drawing::Color::get_Orange(), System::Drawing::Color::get_Red(),
                          ShapeType::TextPlainText);
    shape->get_TextPath()->set_Kerning(false);

    // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
    shape = AppendWordArt(doc, u"Spacing set to 0.1", u"Calibri", 120, 24, System::Drawing::Color::get_BlueViolet(), System::Drawing::Color::get_Blue(),
                          ShapeType::TextCascadeDown);
    shape->get_TextPath()->set_Spacing(0.1);

    // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
    shape = AppendWordArt(doc, u"RotateLetters", u"Calibri", 200, 36, System::Drawing::Color::get_GreenYellow(), System::Drawing::Color::get_Green(),
                          ShapeType::TextWave);
    shape->get_TextPath()->set_RotateLetters(true);

    // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
    shape = AppendWordArt(doc, u"Same character height for lower and UPPER case", u"Calibri", 300, 24, System::Drawing::Color::get_DeepSkyBlue(),
                          System::Drawing::Color::get_DodgerBlue(), ShapeType::TextSlantUp);
    shape->get_TextPath()->set_SameLetterHeights(true);

    // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
    shape = AppendWordArt(doc, u"FitShape on", u"Calibri", 160, 24, System::Drawing::Color::get_LightBlue(), System::Drawing::Color::get_Blue(),
                          ShapeType::TextPlainText);
    ASSERT_TRUE(shape->get_TextPath()->get_FitShape());
    shape->get_TextPath()->set_Size(24.0);

    // If we set the "FitShape: property to "false", the text will keep the size
    // which the "Size" property specifies regardless of the size of the shape.
    // Use the "TextPathAlignment" property also to align the text to a side of the shape.
    shape = AppendWordArt(doc, u"FitShape off", u"Calibri", 160, 24, System::Drawing::Color::get_LightBlue(), System::Drawing::Color::get_Blue(),
                          ShapeType::TextPlainText);
    shape->get_TextPath()->set_FitShape(false);
    shape->get_TextPath()->set_Size(24.0);
    shape->get_TextPath()->set_TextPathAlignment(TextPathAlignment::Right);

    doc->Save(ArtifactsDir + u"Shape.InsertTextPaths.docx");
}

static SharedPtr<Shape> AppendWordArt(SharedPtr<Document> doc, String text, String textFontFamily, double shapeWidth, double shapeHeight,
                                      System::Drawing::Color wordArtFill, System::Drawing::Color line, ShapeType wordArtShapeType)
{
    // Create an inline Shape, which will serve as a container for our WordArt.
    // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
    // These types will have "WordArt object" in the description,
    // and their enumerator constant names will all start with "Text".
    auto shape = MakeObject<Shape>(doc, wordArtShapeType);
    shape->set_WrapType(WrapType::Inline);
    shape->set_Width(shapeWidth);
    shape->set_Height(shapeHeight);
    shape->set_FillColor(wordArtFill);
    shape->set_StrokeColor(line);

    shape->get_TextPath()->set_Text(text);
    shape->get_TextPath()->set_FontFamily(textFontFamily);

    auto para = System::DynamicCast<Paragraph>(doc->get_FirstSection()->get_Body()->AppendChild(MakeObject<Paragraph>(doc)));
    para->AppendChild(shape);
    return shape;
}
```

## See Also

* Class [TextPath](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
