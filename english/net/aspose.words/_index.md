---
title: Aspose.Words
second_title: Aspose.Words for .NET API Reference
description: The Aspose.Words namespace provides classes for generating, converting, modifying, rendering and printing Microsoft Word documents without utilizing Microsoft Word.Aspose.Words is written completely in C#, CLS compliant and contains only safe managed code. Microsoft Word is not required in order to use Aspose.Words.The classes in the Aspose.Words namespace borrow best practices from two well-known frameworks: Microsoft Word Automation and System.Xml. A document in Aspose.Words is represented by a tree of nodes, much like in XML DOM. Where possible, class, method and property names match those found in Microsoft Word Automation. The main classes in this namespace are:
type: docs
weight: 10
url: /net/aspose.words/
---
The Aspose.Words namespace provides classes for generating, converting, modifying, rendering and printing Microsoft Word documents without utilizing Microsoft Word.Aspose.Words is written completely in C#, CLS compliant and contains only safe managed code. Microsoft Word is not required in order to use Aspose.Words.The classes in the Aspose.Words namespace borrow best practices from two well-known frameworks: Microsoft Word Automation and System.Xml. A document in Aspose.Words is represented by a tree of nodes, much like in XML DOM. Where possible, class, method and property names match those found in Microsoft Word Automation. The main classes in this namespace are:

## Classes

| Class | Description |
| --- | --- |
| class [AbsolutePositionTab](./absolutepositiontab) | An absolute position tab is a character which is used to advance the position on the current line of text when displaying this WordprocessingML content. |
| class [Body](./body) | Represents a container for the main text of a section. |
| class [Bookmark](./bookmark) | Represents a single bookmark. |
| class [BookmarkCollection](./bookmarkcollection) | A collection of [`Bookmark`](aspose.words/bookmark) objects that represent the bookmarks in the specified range. |
| class [BookmarkEnd](./bookmarkend) | Represents an end of a bookmark in a Word document. |
| class [BookmarkStart](./bookmarkstart) | Represents a start of a bookmark in a Word document. |
| class [Border](./border) | Represents a border of an object. |
| class [BorderCollection](./bordercollection) | A collection of Border objects. |
| static class [BuildVersionInfo](./buildversioninfo) | Provides information about the current product name and version. |
| class [CleanupOptions](./cleanupoptions) | Allows to specify options for document cleaning. |
| class [ComHelper](./comhelper) | Provides methods for COM clients to load a document into Aspose.Words. |
| class [Comment](./comment) | Represents a container for text of a comment. |
| class [CommentCollection](./commentcollection) | Provides typed access to a collection of [`Comment`](aspose.words/comment) nodes. |
| class [CommentRangeEnd](./commentrangeend) | Denotes the end of a region of text that has a comment associated with it. |
| class [CommentRangeStart](./commentrangestart) | Denotes the start of a region of text that has a comment associated with it. |
| abstract class [CompositeNode](./compositenode) | Base class for nodes that can contain other nodes. |
| class [ConditionalStyle](./conditionalstyle) | Represents special formatting applied to some area of a table with assigned table style. |
| class [ConditionalStyleCollection](./conditionalstylecollection) | Represents a collection of [`ConditionalStyle`](aspose.words/conditionalstyle) objects. |
| static class [ControlChar](./controlchar) | Control characters often encountered in documents. |
| static class [ConvertUtil](./convertutil) | Provides helper functions to convert between various measurement units. |
| class [Document](./document) | Represents a Word document. |
| abstract class [DocumentBase](./documentbase) | Provides the abstract base class for a main document and a glossary document of a Word document. |
| class [DocumentBuilder](./documentbuilder) | Provides methods to insert text, images and other content, specify font, paragraph and section formatting. |
| class [DocumentReaderPluginLoadException](./documentreaderpluginloadexception) | Thrown during document load, when the plugin required for reading the document format cannot be loaded. |
| abstract class [DocumentVisitor](./documentvisitor) | Base class for custom document visitors. |
| class [EditableRange](./editablerange) | Represents a single editable range. |
| class [EditableRangeEnd](./editablerangeend) | Represents an end of an editable range in a Word document. |
| class [EditableRangeStart](./editablerangestart) | Represents a start of an editable range in a Word document. |
| class [FileCorruptedException](./filecorruptedexception) | Thrown during document load, when the document appears to be corrupted and impossible to load. |
| class [FileFormatInfo](./fileformatinfo) | Contains data returned by [`FileFormatUtil`](aspose.words/fileformatutil) document format detection methods. |
| static class [FileFormatUtil](./fileformatutil) | Provides utility methods for working with file formats, such as detecting file format or converting file extensions to/from file format enums. |
| class [Font](./font) | Contains font attributes (font name, font size, color, and so on) for an object. |
| class [FrameFormat](./frameformat) | Represents frame related formatting for a paragraph. |
| class [HeaderFooter](./headerfooter) | Represents a container for the header or footer text of a section. |
| class [HeaderFooterCollection](./headerfootercollection) | Provides typed access to [`HeaderFooter`](aspose.words/headerfooter) nodes of a Section. |
| static class [Hyphenation](./hyphenation) | Provides methods for working with hyphenation dictionaries. These dictionaries prescribe where words of a specific language can be hyphenated. |
| class [ImageWatermarkOptions](./imagewatermarkoptions) | Contains options that can be specified when adding a watermark with image. |
| class [ImportFormatOptions](./importformatoptions) | Allows to specify various import options to format output. |
| class [IncorrectPasswordException](./incorrectpasswordexception) | Thrown if a document is encrypted with a password and the password specified when opening the document is incorrect or missing. |
| abstract class [Inline](./inline) | Base class for inline-level nodes that can have character formatting associated with them, but cannot have child nodes of their own. |
| abstract class [InlineStory](./inlinestory) | Base class for inline-level nodes that can contain paragraphs and tables. |
| abstract class [InternableComplexAttr](./internablecomplexattr) | Base class for internable complex attribute. Internable complex attribute should notify parent collection when going to be changed. |
| class [License](./license) | Provides methods to license the component. |
| class [Metered](./metered) | Provides methods to set metered key. |
| abstract class [Node](./node) | Base class for all nodes of a Word document. |
| class [NodeChangingArgs](./nodechangingargs) | Provides data for methods of the [`INodeChangingCallback`](aspose.words/inodechangingcallback) interface. |
| class [NodeCollection](./nodecollection) | Represents a collection of nodes of a specific type. |
| class [NodeImporter](./nodeimporter) | Allows to efficiently perform repeated import of nodes from one document to another. |
| class [NodeList](./nodelist) | Represents a collection of nodes matching an XPath query executed using the [`SelectNodes`](aspose.words/compositenode/selectnodes) method. |
| class [PageSetup](./pagesetup) | Represents the page setup properties of a section. |
| class [Paragraph](./paragraph) | Represents a paragraph of text. |
| class [ParagraphCollection](./paragraphcollection) | Provides typed access to a collection of [`Paragraph`](aspose.words/paragraph) nodes. |
| class [ParagraphFormat](./paragraphformat) | Represents all the formatting for a paragraph. |
| class [PlainTextDocument](./plaintextdocument) | Allows to extract plain-text representation of the document's content. |
| class [Range](./range) | Represents a contiguous area in a document. |
| class [Revision](./revision) | Represents a revision (tracked change) in a document node or style. Use [`RevisionType`](aspose.words/revision/revisiontype) to check the type of this revision. |
| class [RevisionCollection](./revisioncollection) | A collection of [`Revision`](aspose.words/revision) objects that represent revisions in the document. |
| class [RevisionGroup](./revisiongroup) | Represents a group of sequential [`Revision`](aspose.words/revision) objects. |
| class [RevisionGroupCollection](./revisiongroupcollection) | A collection of [`RevisionGroup`](aspose.words/revisiongroup) objects that represent revision groups in the document. |
| class [Run](./run) | Represents a run of characters with the same font formatting. |
| class [RunCollection](./runcollection) | Provides typed access to a collection of [`Run`](aspose.words/run) nodes. |
| class [Section](./section) | Represents a single section in a document. |
| class [SectionCollection](./sectioncollection) | A collection of Section objects in the document. |
| class [Shading](./shading) | Contains shading attributes for an object. |
| class [SignatureLineOptions](./signaturelineoptions) | Allows to specify options for signature line being inserted. Used in [`DocumentBuilder`](aspose.words/documentbuilder). |
| class [SpecialChar](./specialchar) | Base class for special characters in the document. |
| abstract class [Story](./story) | Base class for elements that contain block-level nodes [`Paragraph`](aspose.words/paragraph) and [`Table`](aspose.words.tables/table). |
| class [Style](./style) | Represents a single built-in or user-defined style. |
| class [StyleCollection](./stylecollection) | A collection of Style objects that represent both the built-in and user-defined styles in a document. |
| class [SubDocument](./subdocument) | Represents a SubDocument - which is a reference to an externally stored document. |
| class [TableStyle](./tablestyle) | Represents a table style. |
| class [TabStop](./tabstop) | Represents a single custom tab stop. The TabStop object is a member of the [`TabStopCollection`](aspose.words/tabstopcollection) collection. |
| class [TabStopCollection](./tabstopcollection) | A collection of [`TabStop`](aspose.words/tabstop) objects that represent custom tabs for a paragraph or a style. |
| class [TextColumn](./textcolumn) | Represents a single text column. TextColumn is a member of the [`TextColumnCollection`](aspose.words/textcolumncollection) collection. The TextColumns collection includes all the columns in a section of a document. |
| class [TextColumnCollection](./textcolumncollection) | A collection of [`TextColumn`](aspose.words/textcolumn) objects that represent all the columns of text in a section of a document. |
| class [TextWatermarkOptions](./textwatermarkoptions) | Contains options that can be specified when adding a watermark with text. |
| class [UnsupportedFileFormatException](./unsupportedfileformatexception) | Thrown during document load, when the document format is not recognized or not supported by Aspose.Words. |
| class [VariableCollection](./variablecollection) | A collection of document variables. |
| class [WarningInfo](./warninginfo) | Contains information about a warning that Aspose.Words issued during document loading or saving. |
| class [WarningInfoCollection](./warninginfocollection) | Represents a typed collection of [`WarningInfo`](aspose.words/warninginfo) objects. |
| class [Watermark](./watermark) | Represents class to work with document watermark. |
## Interfaces

| Interface | Description |
| --- | --- |
| interface [IDocumentReaderPlugin](./idocumentreaderplugin) | Defines an interface for external reader plugins that can read a file into a document. |
| interface [IHyphenationCallback](./ihyphenationcallback) | Implemented by classes which can register hyphenation dictionaries. |
| interface [INodeChangingCallback](./inodechangingcallback) | Implement this interface if you want to receive notifications when nodes are inserted or removed in the document. |
| interface [IWarningCallback](./iwarningcallback) | Implement this interface if you want to have your own custom method called to capture loss of fidelity warnings that can occur during document loading or saving. |
## Enumeration

| Enumeration | Description |
| --- | --- |
| enum [BorderType](./bordertype) | Specifies sides of a border. |
| enum [BreakType](./breaktype) | Specifies type of a break inside a document. |
| enum [CalendarType](./calendartype) | Specifies the type of a calendar. |
| enum [ConditionalStyleType](./conditionalstyletype) | Represents possible table areas to which conditional formatting may be defined in a table style. |
| enum [ContentDisposition](./contentdisposition) | Enumerates different ways of presenting the document at the client browser. |
| enum [DropCapPosition](./dropcapposition) | Specifies the position for a drop cap text. |
| enum [EditorType](./editortype) | Specifies the set of possible aliases (or editing groups) which can be used as aliases to determine if the current user shall be allowed to edit a single range defined by an editable range within a document. |
| enum [EmphasisMark](./emphasismark) | Specifies possible types of emphasis mark. |
| enum [HeaderFooterType](./headerfootertype) | Identifies the type of header or footer found in a Word file. |
| enum [HeightRule](./heightrule) | Specifies the rule for determining the height of an object. |
| [Flags] enum [HtmlInsertOptions](./htmlinsertoptions) | Specifies options for the [`InsertHtml`](aspose.words/documentbuilder/inserthtml) method. |
| enum [ImportFormatMode](./importformatmode) | Specifies how formatting is merged when importing content from another document. |
| enum [LineNumberRestartMode](./linenumberrestartmode) | Determines when automatic line numbering restarts. |
| enum [LineSpacingRule](./linespacingrule) | Specifies line spacing values for a paragraph. |
| enum [LineStyle](./linestyle) | Specifies line style of a [`Border`](aspose.words/border). |
| enum [LoadFormat](./loadformat) | Indicates the format of the document that is to be loaded. |
| enum [MeasurementUnits](./measurementunits) | Specifies the unit of measurement. |
| enum [NodeChangingAction](./nodechangingaction) | Specifies the type of node change. |
| enum [NodeType](./nodetype) | Specifies the type of a Word document node. |
| enum [NumberStyle](./numberstyle) | Specifies the number style for a list, footnotes and endnotes, page numbers. |
| enum [Orientation](./orientation) | Specifies page orientation. |
| enum [OutlineLevel](./outlinelevel) | Specifies the outline level of a paragraph in the document. |
| enum [PageBorderAppliesTo](./pageborderappliesto) | Specifies which pages the page border is printed on. |
| enum [PageBorderDistanceFrom](./pageborderdistancefrom) | Specifies the positioning of the page border relative to the page margin. |
| enum [PageVerticalAlignment](./pageverticalalignment) | Specifies vertical justification of text on each page. |
| enum [PaperSize](./papersize) | Specifies paper size. |
| enum [ParagraphAlignment](./paragraphalignment) | Specifies text alignment in a paragraph. |
| enum [ProtectionType](./protectiontype) | Protection type for a document. |
| enum [RevisionsView](./revisionsview) | Allows to specify whether to work with the original or revised version of a document. |
| enum [RevisionType](./revisiontype) | Specifies the type of change being tracked in [`Revision`](aspose.words/revision). |
| enum [SaveFormat](./saveformat) | Indicates the format in which the document is saved. |
| enum [SectionLayoutMode](./sectionlayoutmode) | Specifies the layout mode for a section allowing to define the document grid behavior. |
| enum [SectionStart](./sectionstart) | The type of break at the beginning of the section. |
| enum [StoryType](./storytype) | Text of a Word document is stored in stories. StoryType identifies a story. |
| enum [StyleIdentifier](./styleidentifier) | Locale independent style identifier. |
| enum [StyleType](./styletype) | Represents type of the style. |
| enum [TabAlignment](./tabalignment) | Specifies the alignment/type of a tab stop. |
| enum [TabLeader](./tableader) | Specifies the type of the leader line displayed under the tab character. |
| enum [TextDmlEffect](./textdmleffect) | Dml text effect for text runs. |
| enum [TextEffect](./texteffect) | Animation effect for text runs. |
| enum [TextOrientation](./textorientation) | Specifies orientation of text on a page, in a table cell or a text frame. |
| enum [TextureIndex](./textureindex) | Specifies shading texture. |
| enum [Underline](./underline) | Indicates type of the underline applied to a font. |
| enum [VisitorAction](./visitoraction) | Allows the visitor to control the enumeration of nodes. |
| enum [WarningSource](./warningsource) | Specifies the module that produces a warning during document loading or saving. |
| [Flags] enum [WarningType](./warningtype) | Specifies the type of a warning that is issued by Aspose.Words during document loading or saving. |
| enum [WatermarkLayout](./watermarklayout) | Defines layout of the watermark relative to the watermark center. |
| enum [WatermarkType](./watermarktype) | Specifies the watermark type. |

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
