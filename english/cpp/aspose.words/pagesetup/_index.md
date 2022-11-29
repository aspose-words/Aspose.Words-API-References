---
title: PageSetup
second_title: Aspose.Words for C++ API Reference
description: Represents the page setup properties of a section.
type: docs
weight: 586
url: /cpp/aspose.words/pagesetup/
---
## PageSetup class


Represents the page setup properties of a section.

```cpp
class PageSetup : public Aspose::Words::IBorderAttrSource
```

## Methods

| Method | Description |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Resets page setup to default paper size, margins and orientation. |
| [get_Bidi](./get_bidi/)() | Specifies that this section contains bidirectional (complex scripts) text. |
| [get_BorderAlwaysInFront](./get_borderalwaysinfront/)() | Specifies where the page border is positioned relative to intersecting texts and objects. |
| [get_BorderAppliesTo](./get_borderappliesto/)() | Specifies which pages the page border is printed on. |
| [get_BorderDistanceFrom](./get_borderdistancefrom/)() | Gets or sets a value that indicates whether the specified page border is measured from the edge of the page or from the text it surrounds. |
| [get_Borders](./get_borders/)() | Gets a collection of the page borders. |
| [get_BorderSurroundsFooter](./get_bordersurroundsfooter/)() | Specifies whether the page border includes or excludes the footer. |
| [get_BorderSurroundsHeader](./get_bordersurroundsheader/)() | Specifies whether the page border includes or excludes the header. |
| [get_BottomMargin](./get_bottommargin/)() | Returns or sets the distance (in points) between the bottom edge of the page and the bottom boundary of the body text. |
| [get_ChapterPageSeparator](./get_chapterpageseparator/)() | Gets the separator character that appears between the chapter number and the page number. |
| [get_CharactersPerLine](./get_charactersperline/)() | Gets or sets the number of characters per line in the document grid. |
| [get_DifferentFirstPageHeaderFooter](./get_differentfirstpageheaderfooter/)() | **True** if a different header or footer is used on the first page. |
| [get_EndnoteOptions](./get_endnoteoptions/)() | Provides options that control numbering and positioning of endnotes in this section. |
| [get_FirstPageTray](./get_firstpagetray/)() | Gets the paper tray (bin) to use for the first page of a section. The value is implementation (printer) specific. |
| [get_FooterDistance](./get_footerdistance/)() | Returns or sets the distance (in points) between the footer and the bottom of the page. |
| [get_FootnoteOptions](./get_footnoteoptions/)() | Provides options that control numbering and positioning of footnotes in this section. |
| [get_Gutter](./get_gutter/)() | Gets or sets the amount of extra space added to the margin for document binding. |
| [get_HeaderDistance](./get_headerdistance/)() | Returns or sets the distance (in points) between the header and the top of the page. |
| [get_HeadingLevelForChapter](./get_headinglevelforchapter/)() | Gets or sets the heading level style that is applied to the chapter titles in the document. |
| [get_LayoutMode](./get_layoutmode/)() | Gets or sets the layout mode of this section. |
| [get_LeftMargin](./get_leftmargin/)() | Returns or sets the distance (in points) between the left edge of the page and the left boundary of the body text. |
| [get_LineNumberCountBy](./get_linenumbercountby/)() | Returns or sets the numeric increment for line numbers. |
| [get_LineNumberDistanceFromText](./get_linenumberdistancefromtext/)() | Gets or sets distance between the right edge of line numbers and the left edge of the document. |
| [get_LineNumberRestartMode](./get_linenumberrestartmode/)() | Gets or sets the way line numbering runs that is, whether it starts over at the beginning of a new page or section or runs continuously. |
| [get_LinesPerPage](./get_linesperpage/)() | Gets or sets the number of lines per page in the document grid. |
| [get_LineStartingNumber](./get_linestartingnumber/)() | Gets or sets the starting line number. |
| [get_MultiplePages](./get_multiplepages/)() const | For multiple page documents, gets or sets how a document is printed or rendered so that it can be bound as a booklet. |
| [get_OddAndEvenPagesHeaderFooter](./get_oddandevenpagesheaderfooter/)() const | **True** if the document has different headers and footers for odd-numbered and even-numbered pages. |
| [get_Orientation](./get_orientation/)() | Returns or sets the orientation of the page. |
| [get_OtherPagesTray](./get_otherpagestray/)() | Gets the paper tray (bin) to be used for all but the first page of a section. The value is implementation (printer) specific. |
| [get_PageHeight](./get_pageheight/)() | Returns or sets the height of the page in points. |
| [get_PageNumberStyle](./get_pagenumberstyle/)() | Gets or sets the page number format. |
| [get_PageStartingNumber](./get_pagestartingnumber/)() | Gets or sets the starting page number of the section. |
| [get_PageWidth](./get_pagewidth/)() | Returns or sets the width of the page in points. |
| [get_PaperSize](./get_papersize/)() | Returns or sets the paper size. |
| [get_RestartPageNumbering](./get_restartpagenumbering/)() | **True** if page numbering restarts at the beginning of the section. |
| [get_RightMargin](./get_rightmargin/)() | Returns or sets the distance (in points) between the right edge of the page and the right boundary of the body text. |
| [get_RtlGutter](./get_rtlgutter/)() | Gets or sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language. |
| [get_SectionStart](./get_sectionstart/)() | Returns or sets the type of section break for the specified object. |
| [get_SheetsPerBooklet](./get_sheetsperbooklet/)() const | Returns or sets the number of pages to be included in each booklet. |
| [get_SuppressEndnotes](./get_suppressendnotes/)() | **True** if endnotes are printed at the end of the next section that doesn't suppress endnotes. Suppressed endnotes are printed before the endnotes in that section. |
| [get_TextColumns](./get_textcolumns/)() | Returns a collection that represents the set of text columns. |
| [get_TextOrientation](./get_textorientation/)() | Allows to specify [TextOrientation](./get_textorientation/) for the whole page. Default value is [Horizontal](../textorientation/) |
| [get_TopMargin](./get_topmargin/)() | Returns or sets the distance (in points) between the top edge of the page and the top boundary of the body text. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Returns or sets the vertical alignment of text on each page in a document or section. |
| [set_Bidi](./set_bidi/)(bool) | Setter for [Aspose::Words::PageSetup::get_Bidi](./get_bidi/). |
| [set_BorderAlwaysInFront](./set_borderalwaysinfront/)(bool) | Setter for [Aspose::Words::PageSetup::get_BorderAlwaysInFront](./get_borderalwaysinfront/). |
| [set_BorderAppliesTo](./set_borderappliesto/)(Aspose::Words::PageBorderAppliesTo) | Setter for [Aspose::Words::PageSetup::get_BorderAppliesTo](./get_borderappliesto/). |
| [set_BorderDistanceFrom](./set_borderdistancefrom/)(Aspose::Words::PageBorderDistanceFrom) | Setter for [Aspose::Words::PageSetup::get_BorderDistanceFrom](./get_borderdistancefrom/). |
| [set_BorderSurroundsFooter](./set_bordersurroundsfooter/)(bool) | Setter for [Aspose::Words::PageSetup::get_BorderSurroundsFooter](./get_bordersurroundsfooter/). |
| [set_BorderSurroundsHeader](./set_bordersurroundsheader/)(bool) | Setter for [Aspose::Words::PageSetup::get_BorderSurroundsHeader](./get_bordersurroundsheader/). |
| [set_BottomMargin](./set_bottommargin/)(double) | Setter for [Aspose::Words::PageSetup::get_BottomMargin](./get_bottommargin/). |
| [set_ChapterPageSeparator](./set_chapterpageseparator/)(Aspose::Words::ChapterPageSeparator) | Sets the separator character that appears between the chapter number and the page number. |
| [set_CharactersPerLine](./set_charactersperline/)(int32_t) | Setter for [Aspose::Words::PageSetup::get_CharactersPerLine](./get_charactersperline/). |
| [set_DifferentFirstPageHeaderFooter](./set_differentfirstpageheaderfooter/)(bool) | Setter for [Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter](./get_differentfirstpageheaderfooter/). |
| [set_FirstPageTray](./set_firstpagetray/)(int32_t) | Sets the paper tray (bin) to use for the first page of a section. The value is implementation (printer) specific. |
| [set_FooterDistance](./set_footerdistance/)(double) | Setter for [Aspose::Words::PageSetup::get_FooterDistance](./get_footerdistance/). |
| [set_Gutter](./set_gutter/)(double) | Setter for [Aspose::Words::PageSetup::get_Gutter](./get_gutter/). |
| [set_HeaderDistance](./set_headerdistance/)(double) | Setter for [Aspose::Words::PageSetup::get_HeaderDistance](./get_headerdistance/). |
| [set_HeadingLevelForChapter](./set_headinglevelforchapter/)(int32_t) | Setter for [Aspose::Words::PageSetup::get_HeadingLevelForChapter](./get_headinglevelforchapter/). |
| [set_LayoutMode](./set_layoutmode/)(Aspose::Words::SectionLayoutMode) | Setter for [Aspose::Words::PageSetup::get_LayoutMode](./get_layoutmode/). |
| [set_LeftMargin](./set_leftmargin/)(double) | Setter for [Aspose::Words::PageSetup::get_LeftMargin](./get_leftmargin/). |
| [set_LineNumberCountBy](./set_linenumbercountby/)(int32_t) | Setter for [Aspose::Words::PageSetup::get_LineNumberCountBy](./get_linenumbercountby/). |
| [set_LineNumberDistanceFromText](./set_linenumberdistancefromtext/)(double) | Setter for [Aspose::Words::PageSetup::get_LineNumberDistanceFromText](./get_linenumberdistancefromtext/). |
| [set_LineNumberRestartMode](./set_linenumberrestartmode/)(Aspose::Words::LineNumberRestartMode) | Setter for [Aspose::Words::PageSetup::get_LineNumberRestartMode](./get_linenumberrestartmode/). |
| [set_LinesPerPage](./set_linesperpage/)(int32_t) | Setter for [Aspose::Words::PageSetup::get_LinesPerPage](./get_linesperpage/). |
| [set_LineStartingNumber](./set_linestartingnumber/)(int32_t) | Setter for [Aspose::Words::PageSetup::get_LineStartingNumber](./get_linestartingnumber/). |
| [set_MultiplePages](./set_multiplepages/)(Aspose::Words::Settings::MultiplePagesType) | Setter for [Aspose::Words::PageSetup::get_MultiplePages](./get_multiplepages/). |
| [set_OddAndEvenPagesHeaderFooter](./set_oddandevenpagesheaderfooter/)(bool) | Setter for [Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter](./get_oddandevenpagesheaderfooter/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::Orientation) | Setter for [Aspose::Words::PageSetup::get_Orientation](./get_orientation/). |
| [set_OtherPagesTray](./set_otherpagestray/)(int32_t) | Sets the paper tray (bin) to be used for all but the first page of a section. The value is implementation (printer) specific. |
| [set_PageHeight](./set_pageheight/)(double) | Setter for [Aspose::Words::PageSetup::get_PageHeight](./get_pageheight/). |
| [set_PageNumberStyle](./set_pagenumberstyle/)(Aspose::Words::NumberStyle) | Setter for [Aspose::Words::PageSetup::get_PageNumberStyle](./get_pagenumberstyle/). |
| [set_PageStartingNumber](./set_pagestartingnumber/)(int32_t) | Setter for [Aspose::Words::PageSetup::get_PageStartingNumber](./get_pagestartingnumber/). |
| [set_PageWidth](./set_pagewidth/)(double) | Setter for [Aspose::Words::PageSetup::get_PageWidth](./get_pagewidth/). |
| [set_PaperSize](./set_papersize/)(Aspose::Words::PaperSize) | Setter for [Aspose::Words::PageSetup::get_PaperSize](./get_papersize/). |
| [set_RestartPageNumbering](./set_restartpagenumbering/)(bool) | Setter for [Aspose::Words::PageSetup::get_RestartPageNumbering](./get_restartpagenumbering/). |
| [set_RightMargin](./set_rightmargin/)(double) | Setter for [Aspose::Words::PageSetup::get_RightMargin](./get_rightmargin/). |
| [set_RtlGutter](./set_rtlgutter/)(bool) | Setter for [Aspose::Words::PageSetup::get_RtlGutter](./get_rtlgutter/). |
| [set_SectionStart](./set_sectionstart/)(Aspose::Words::SectionStart) | Setter for [Aspose::Words::PageSetup::get_SectionStart](./get_sectionstart/). |
| [set_SheetsPerBooklet](./set_sheetsperbooklet/)(int32_t) | Setter for [Aspose::Words::PageSetup::get_SheetsPerBooklet](./get_sheetsperbooklet/). |
| [set_SuppressEndnotes](./set_suppressendnotes/)(bool) | Setter for [Aspose::Words::PageSetup::get_SuppressEndnotes](./get_suppressendnotes/). |
| [set_TextOrientation](./set_textorientation/)(Aspose::Words::TextOrientation) | Setter for [Aspose::Words::PageSetup::get_TextOrientation](./get_textorientation/). |
| [set_TopMargin](./set_topmargin/)(double) | Setter for [Aspose::Words::PageSetup::get_TopMargin](./get_topmargin/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::PageVerticalAlignment) | Setter for [Aspose::Words::PageSetup::get_VerticalAlignment](./get_verticalalignment/). |
## Remarks


**PageSetup** object contains all the page setup attributes of a section (left margin, bottom margin, paper size, and so on) as properties.

## Examples



Shows how to apply and revert page setup settings to sections in a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Modify the page setup properties for the builder's current section and add text.
builder->get_PageSetup()->set_Orientation(Orientation::Landscape);
builder->get_PageSetup()->set_VerticalAlignment(PageVerticalAlignment::Center);
builder->Writeln(u"This is the first section, which landscape oriented with vertically centered text.");

// If we start a new section using a document builder,
// it will inherit the builder's current page setup properties.
builder->InsertBreak(BreakType::SectionBreakNewPage);

ASSERT_EQ(Orientation::Landscape, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(PageVerticalAlignment::Center, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

// We can revert its page setup properties to their default values using the "ClearFormatting" method.
builder->get_PageSetup()->ClearFormatting();

ASSERT_EQ(Orientation::Portrait, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(PageVerticalAlignment::Top, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

builder->Writeln(u"This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc->Save(ArtifactsDir + u"PageSetup.ClearFormatting.docx");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words](../../)
