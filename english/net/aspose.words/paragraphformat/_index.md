---
title: ParagraphFormat
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 4120
url: /net/aspose.words/paragraphformat/
---
## ParagraphFormat class

Represents all the formatting for a paragraph.

```csharp
public class ParagraphFormat
```

## Public Members

| name | description |
| --- | --- |
| [AddSpaceBetweenFarEastAndAlpha](addspacebetweenfareastandalpha) { get; set; } | Gets or sets a flag indicating whether inter-character spacing is automatically adjusted between regions of Latin text and regions of East Asian text in the current paragraph. |
| [AddSpaceBetweenFarEastAndDigit](addspacebetweenfareastanddigit) { get; set; } | Gets or sets a flag indicating whether inter-character spacing is automatically adjusted between regions of numbers and regions of East Asian text in the current paragraph. |
| [Alignment](alignment) { get; set; } | Gets or sets text alignment for the paragraph. |
| [Bidi](bidi) { get; set; } | Gets or sets whether this is a right-to-left paragraph. |
| [Borders](borders) { get; } | Gets collection of borders of the paragraph. |
| [CharacterUnitFirstLineIndent](characterunitfirstlineindent) { get; set; } | Gets or sets the value (in characters) for the first-line or hanging indent. Use positive values to set the first-line indent, and negative values to set the hanging indent. |
| [CharacterUnitLeftIndent](characterunitleftindent) { get; set; } | Gets or sets the left indent value (in characters) for the specified paragraphs. |
| [CharacterUnitRightIndent](characterunitrightindent) { get; set; } | Gets or sets the right indent value (in characters) for the specified paragraphs. |
| [DropCapPosition](dropcapposition) { get; set; } | Gets or sets the position for a drop cap text. |
| [FarEastLineBreakControl](fareastlinebreakcontrol) { get; set; } | Gets or sets a flag indicating whether East Asian line-breaking rules are applied to the current paragraph. |
| [FirstLineIndent](firstlineindent) { get; set; } | Gets or sets the value (in points) for a first line or hanging indent. Use positive values to set the first-line indent, and negative values to set the hanging indent. |
| [HangingPunctuation](hangingpunctuation) { get; set; } | Gets or sets a flag indicating whether hanging punctuation is enabled for the current paragraph. |
| [IsHeading](isheading) { get; } | True when the paragraph style is one of the built-in Heading styles. |
| [IsListItem](islistitem) { get; } | True when the paragraph is an item in a bulleted or numbered list. |
| [KeepTogether](keeptogether) { get; set; } | True if all lines in the paragraph are to remain on the same page. |
| [KeepWithNext](keepwithnext) { get; set; } | True if the paragraph is to remains on the same page as the paragraph that follows it. |
| [LeftIndent](leftindent) { get; set; } | Gets or sets the value (in points) that represents the left indent for paragraph. |
| [LineSpacing](linespacing) { get; set; } | Gets or sets the line spacing (in points) for the paragraph. |
| [LineSpacingRule](linespacingrule) { get; set; } | Gets or sets the line spacing for the paragraph. |
| [LinesToDrop](linestodrop) { get; set; } | Gets or sets the number of lines of the paragraph text used to calculate the drop cap height. |
| [LineUnitAfter](lineunitafter) { get; set; } | Gets or sets the amount of spacing (in gridlines) after the paragraphs. |
| [LineUnitBefore](lineunitbefore) { get; set; } | Gets or sets the amount of spacing (in gridlines) before the paragraphs. |
| [NoSpaceBetweenParagraphsOfSameStyle](nospacebetweenparagraphsofsamestyle) { get; set; } | When true, [`SpaceBefore`](./spacebefore) and [`SpaceAfter`](./spaceafter) will be ignored between the paragraphs of the same style. |
| [OutlineLevel](outlinelevel) { get; set; } | Specifies the outline level of the paragraph in the document. |
| [PageBreakBefore](pagebreakbefore) { get; set; } | True if a page break is forced before the paragraph. |
| [RightIndent](rightindent) { get; set; } | Gets or sets the value (in points) that represents the right indent for paragraph. |
| [Shading](shading) { get; } | Returns a Shading object that refers to the shading formatting for the paragraph. |
| [SnapToGrid](snaptogrid) { get; set; } | Specifies whether the current paragraph should use the document grid lines per page settings when laying out the contents in the paragraph. |
| [SpaceAfter](spaceafter) { get; set; } | Gets or sets the amount of spacing (in points) after the paragraph. |
| [SpaceAfterAuto](spaceafterauto) { get; set; } | True if the amount of spacing after the paragraph is set automatically. |
| [SpaceBefore](spacebefore) { get; set; } | Gets or sets the amount of spacing (in points) before the paragraph. |
| [SpaceBeforeAuto](spacebeforeauto) { get; set; } | True if the amount of spacing before the paragraph is set automatically. |
| [Style](style) { get; set; } | Gets or sets the paragraph style applied to this formatting. |
| [StyleIdentifier](styleidentifier) { get; set; } | Gets or sets the locale independent style identifier of the paragraph style applied to this formatting. |
| [StyleName](stylename) { get; set; } | Gets or sets the name of the paragraph style applied to this formatting. |
| [SuppressAutoHyphens](suppressautohyphens) { get; set; } | Specifies whether the current paragraph should be exempted from any hyphenation which is applied in the document settings. |
| [SuppressLineNumbers](suppresslinenumbers) { get; set; } | Specifies whether the current paragraph's lines should be exempted from line numbering which is applied in the parent section. |
| [TabStops](tabstops) { get; } | Gets the collection of custom tab stops defined for this object. |
| [WidowControl](widowcontrol) { get; set; } | True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph. |
| [WordWrap](wordwrap) { get; set; } | If this property is false, Latin text in the middle of a word can be wrapped for the current paragraph. Otherwise Latin text is wrapped by whole words. |
| [ClearFormatting](clearformatting)() | Resets to default paragraph formatting. |

### See Also

* namespace [Aspose.Words](../../aspose.words)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
