---
title: Aspose::Words::ParagraphFormat class
linktitle: ParagraphFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ParagraphFormat class. Represents all the formatting for a paragraph. To learn more, visit the  documentation article in C++.'
type: docs
weight: 49000
url: /cpp/aspose.words/paragraphformat/
---
## ParagraphFormat class


Represents all the formatting for a paragraph. To learn more, visit the [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/) documentation article.

```cpp
class ParagraphFormat : public Aspose::Words::IBorderAttrSource,
                        public Aspose::Words::IShadingAttrSource
```

## Methods

| Method | Description |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Resets to default paragraph formatting. |
| [get_AddSpaceBetweenFarEastAndAlpha](./get_addspacebetweenfareastandalpha/)() | Gets or sets a flag indicating whether inter-character spacing is automatically adjusted between regions of Latin text and regions of East Asian text in the current paragraph. |
| [get_AddSpaceBetweenFarEastAndDigit](./get_addspacebetweenfareastanddigit/)() | Gets or sets a flag indicating whether inter-character spacing is automatically adjusted between regions of numbers and regions of East Asian text in the current paragraph. |
| [get_Alignment](./get_alignment/)() | Gets or sets text alignment for the paragraph. |
| [get_BaselineAlignment](./get_baselinealignment/)() | Gets fonts vertical position on a line. |
| [get_Bidi](./get_bidi/)() | Gets or sets whether this is a right-to-left paragraph. |
| [get_Borders](./get_borders/)() | Gets collection of borders of the paragraph. |
| [get_CharacterUnitFirstLineIndent](./get_characterunitfirstlineindent/)() | Gets or sets the value (in characters) for the first-line or hanging indent. Use positive values to set the first-line indent, and negative values to set the hanging indent. |
| [get_CharacterUnitLeftIndent](./get_characterunitleftindent/)() | Gets or sets the left indent value (in characters) for the specified paragraphs. |
| [get_CharacterUnitRightIndent](./get_characterunitrightindent/)() | Gets or sets the right indent value (in characters) for the specified paragraphs. |
| [get_DropCapPosition](./get_dropcapposition/)() | Gets or sets the position for a drop cap text. |
| [get_FarEastLineBreakControl](./get_fareastlinebreakcontrol/)() | Gets or sets a flag indicating whether East Asian line-breaking rules are applied to the current paragraph. |
| [get_FirstLineIndent](./get_firstlineindent/)() | Gets or sets the value (in points) for a first line or hanging indent. Use positive values to set the first-line indent, and negative values to set the hanging indent. |
| [get_HangingPunctuation](./get_hangingpunctuation/)() | Gets or sets a flag indicating whether hanging punctuation is enabled for the current paragraph. |
| [get_IsHeading](./get_isheading/)() | True when the paragraph style is one of the built-in Heading styles. |
| [get_IsListItem](./get_islistitem/)() | True when the paragraph is an item in a bulleted or numbered list. |
| [get_KeepTogether](./get_keeptogether/)() | True if all lines in the paragraph are to remain on the same page. |
| [get_KeepWithNext](./get_keepwithnext/)() | True if the paragraph is to remains on the same page as the paragraph that follows it. |
| [get_LeftIndent](./get_leftindent/)() | Gets or sets the value (in points) that represents the left indent for paragraph. |
| [get_LineSpacing](./get_linespacing/)() | Gets or sets the line spacing (in points) for the paragraph. |
| [get_LineSpacingRule](./get_linespacingrule/)() | Gets or sets the line spacing for the paragraph. |
| [get_LinesToDrop](./get_linestodrop/)() | Gets or sets the number of lines of the paragraph text used to calculate the drop cap height. |
| [get_LineUnitAfter](./get_lineunitafter/)() | Gets or sets the amount of spacing (in gridlines) after the paragraphs. |
| [get_LineUnitBefore](./get_lineunitbefore/)() | Gets or sets the amount of spacing (in gridlines) before the paragraphs. |
| [get_MirrorIndents](./get_mirrorindents/)() | Gets a flag indicating whether the left and right indents are of the same width. |
| [get_NoSpaceBetweenParagraphsOfSameStyle](./get_nospacebetweenparagraphsofsamestyle/)() | When **true**, [SpaceBefore](./get_spacebefore/) and [SpaceAfter](./get_spaceafter/) will be ignored between the paragraphs of the same style. |
| [get_OutlineLevel](./get_outlinelevel/)() | Specifies the outline level of the paragraph in the document. |
| [get_PageBreakBefore](./get_pagebreakbefore/)() | True if a page break is forced before the paragraph. |
| [get_RightIndent](./get_rightindent/)() | Gets or sets the value (in points) that represents the right indent for paragraph. |
| [get_Shading](./get_shading/)() | Returns a [Shading](../shading/) object that refers to the shading formatting for the paragraph. |
| [get_SnapToGrid](./get_snaptogrid/)() | Specifies whether the current paragraph should use the document grid lines per page settings when laying out the contents in the paragraph. |
| [get_SpaceAfter](./get_spaceafter/)() | Gets or sets the amount of spacing (in points) after the paragraph. |
| [get_SpaceAfterAuto](./get_spaceafterauto/)() | True if the amount of spacing after the paragraph is set automatically. |
| [get_SpaceBefore](./get_spacebefore/)() | Gets or sets the amount of spacing (in points) before the paragraph. |
| [get_SpaceBeforeAuto](./get_spacebeforeauto/)() | True if the amount of spacing before the paragraph is set automatically. |
| [get_Style](./get_style/)() | Gets or sets the paragraph style applied to this formatting. |
| [get_StyleIdentifier](./get_styleidentifier/)() | Gets or sets the locale independent style identifier of the paragraph style applied to this formatting. |
| [get_StyleName](./get_stylename/)() | Gets or sets the name of the paragraph style applied to this formatting. |
| [get_SuppressAutoHyphens](./get_suppressautohyphens/)() | Specifies whether the current paragraph should be exempted from any hyphenation which is applied in the document settings. |
| [get_SuppressLineNumbers](./get_suppresslinenumbers/)() | Specifies whether the current paragraph's lines should be exempted from line numbering which is applied in the parent section. |
| [get_TabStops](./get_tabstops/)() | Gets the collection of custom tab stops defined for this object. |
| [get_WidowControl](./get_widowcontrol/)() | True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph. |
| [get_WordWrap](./get_wordwrap/)() | If this property is **false**, Latin text in the middle of a word can be wrapped for the current paragraph. Otherwise Latin text is wrapped by whole words. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AddSpaceBetweenFarEastAndAlpha](./set_addspacebetweenfareastandalpha/)(bool) | Setter for [Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndAlpha](./get_addspacebetweenfareastandalpha/). |
| [set_AddSpaceBetweenFarEastAndDigit](./set_addspacebetweenfareastanddigit/)(bool) | Setter for [Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndDigit](./get_addspacebetweenfareastanddigit/). |
| [set_Alignment](./set_alignment/)(Aspose::Words::ParagraphAlignment) | Setter for [Aspose::Words::ParagraphFormat::get_Alignment](./get_alignment/). |
| [set_BaselineAlignment](./set_baselinealignment/)(Aspose::Words::BaselineAlignment) | Sets fonts vertical position on a line. |
| [set_Bidi](./set_bidi/)(bool) | Setter for [Aspose::Words::ParagraphFormat::get_Bidi](./get_bidi/). |
| [set_CharacterUnitFirstLineIndent](./set_characterunitfirstlineindent/)(double) | Setter for [Aspose::Words::ParagraphFormat::get_CharacterUnitFirstLineIndent](./get_characterunitfirstlineindent/). |
| [set_CharacterUnitLeftIndent](./set_characterunitleftindent/)(double) | Setter for [Aspose::Words::ParagraphFormat::get_CharacterUnitLeftIndent](./get_characterunitleftindent/). |
| [set_CharacterUnitRightIndent](./set_characterunitrightindent/)(double) | Setter for [Aspose::Words::ParagraphFormat::get_CharacterUnitRightIndent](./get_characterunitrightindent/). |
| [set_DropCapPosition](./set_dropcapposition/)(Aspose::Words::DropCapPosition) | Setter for [Aspose::Words::ParagraphFormat::get_DropCapPosition](./get_dropcapposition/). |
| [set_FarEastLineBreakControl](./set_fareastlinebreakcontrol/)(bool) | Setter for [Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl](./get_fareastlinebreakcontrol/). |
| [set_FirstLineIndent](./set_firstlineindent/)(double) | Setter for [Aspose::Words::ParagraphFormat::get_FirstLineIndent](./get_firstlineindent/). |
| [set_HangingPunctuation](./set_hangingpunctuation/)(bool) | Setter for [Aspose::Words::ParagraphFormat::get_HangingPunctuation](./get_hangingpunctuation/). |
| [set_KeepTogether](./set_keeptogether/)(bool) | Setter for [Aspose::Words::ParagraphFormat::get_KeepTogether](./get_keeptogether/). |
| [set_KeepWithNext](./set_keepwithnext/)(bool) | Setter for [Aspose::Words::ParagraphFormat::get_KeepWithNext](./get_keepwithnext/). |
| [set_LeftIndent](./set_leftindent/)(double) | Setter for [Aspose::Words::ParagraphFormat::get_LeftIndent](./get_leftindent/). |
| [set_LineSpacing](./set_linespacing/)(double) | Setter for [Aspose::Words::ParagraphFormat::get_LineSpacing](./get_linespacing/). |
| [set_LineSpacingRule](./set_linespacingrule/)(Aspose::Words::LineSpacingRule) | Setter for [Aspose::Words::ParagraphFormat::get_LineSpacingRule](./get_linespacingrule/). |
| [set_LinesToDrop](./set_linestodrop/)(int32_t) | Setter for [Aspose::Words::ParagraphFormat::get_LinesToDrop](./get_linestodrop/). |
| [set_LineUnitAfter](./set_lineunitafter/)(double) | Setter for [Aspose::Words::ParagraphFormat::get_LineUnitAfter](./get_lineunitafter/). |
| [set_LineUnitBefore](./set_lineunitbefore/)(double) | Setter for [Aspose::Words::ParagraphFormat::get_LineUnitBefore](./get_lineunitbefore/). |
| [set_MirrorIndents](./set_mirrorindents/)(bool) | Sets a flag indicating whether the left and right indents are of the same width. |
| [set_NoSpaceBetweenParagraphsOfSameStyle](./set_nospacebetweenparagraphsofsamestyle/)(bool) | Setter for [Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle](./get_nospacebetweenparagraphsofsamestyle/). |
| [set_OutlineLevel](./set_outlinelevel/)(Aspose::Words::OutlineLevel) | Setter for [Aspose::Words::ParagraphFormat::get_OutlineLevel](./get_outlinelevel/). |
| [set_PageBreakBefore](./set_pagebreakbefore/)(bool) | Setter for [Aspose::Words::ParagraphFormat::get_PageBreakBefore](./get_pagebreakbefore/). |
| [set_RightIndent](./set_rightindent/)(double) | Setter for [Aspose::Words::ParagraphFormat::get_RightIndent](./get_rightindent/). |
| [set_SnapToGrid](./set_snaptogrid/)(bool) | Setter for [Aspose::Words::ParagraphFormat::get_SnapToGrid](./get_snaptogrid/). |
| [set_SpaceAfter](./set_spaceafter/)(double) | Setter for [Aspose::Words::ParagraphFormat::get_SpaceAfter](./get_spaceafter/). |
| [set_SpaceAfterAuto](./set_spaceafterauto/)(bool) | Setter for [Aspose::Words::ParagraphFormat::get_SpaceAfterAuto](./get_spaceafterauto/). |
| [set_SpaceBefore](./set_spacebefore/)(double) | Setter for [Aspose::Words::ParagraphFormat::get_SpaceBefore](./get_spacebefore/). |
| [set_SpaceBeforeAuto](./set_spacebeforeauto/)(bool) | Setter for [Aspose::Words::ParagraphFormat::get_SpaceBeforeAuto](./get_spacebeforeauto/). |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Setter for [Aspose::Words::ParagraphFormat::get_Style](./get_style/). |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | Setter for [Aspose::Words::ParagraphFormat::get_StyleIdentifier](./get_styleidentifier/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Setter for [Aspose::Words::ParagraphFormat::get_StyleName](./get_stylename/). |
| [set_SuppressAutoHyphens](./set_suppressautohyphens/)(bool) | Setter for [Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens](./get_suppressautohyphens/). |
| [set_SuppressLineNumbers](./set_suppresslinenumbers/)(bool) | Setter for [Aspose::Words::ParagraphFormat::get_SuppressLineNumbers](./get_suppresslinenumbers/). |
| [set_WidowControl](./set_widowcontrol/)(bool) | Setter for [Aspose::Words::ParagraphFormat::get_WidowControl](./get_widowcontrol/). |
| [set_WordWrap](./set_wordwrap/)(bool) | Setter for [Aspose::Words::ParagraphFormat::get_WordWrap](./get_wordwrap/). |
| static [Type](./type/)() |  |

## Examples



Shows how to construct an Aspose.Words document by hand. 
```cpp
auto doc = MakeObject<Document>();

// A blank document contains one section, one body and one paragraph.
// Call the "RemoveAllChildren" method to remove all those nodes,
// and end up with a document node with no children.
doc->RemoveAllChildren();

// This document now has no composite child nodes that we can add content to.
// If we wish to edit it, we will need to repopulate its node collection.
// First, create a new section, and then append it as a child to the root document node.
auto section = MakeObject<Section>(doc);
doc->AppendChild(section);

// Set some page setup properties for the section.
section->get_PageSetup()->set_SectionStart(SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(PaperSize::Letter);

// A section needs a body, which will contain and display all its contents
// on the page between the section's header and footer.
auto body = MakeObject<Body>(doc);
section->AppendChild(body);

// Create a paragraph, set some formatting properties, and then append it as a child to the body.
auto para = MakeObject<Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(ParagraphAlignment::Center);

body->AppendChild(para);

// Finally, add some content to do the document. Create a run,
// set its appearance and contents, and then append it as a child to the paragraph.
auto run = MakeObject<Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(ArtifactsDir + u"Section.CreateManually.docx");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
