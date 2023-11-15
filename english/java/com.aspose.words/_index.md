---
title: com.aspose.words
linktitle: com.aspose.words
second_title: Aspose.Words for Java
description: The com.aspose.words package provides classes for generating converting modifying rendering and printing Microsoft Word documents without utilizing Microsoft Word in Java.
type: docs
weight: 10
url: /java/com.aspose.words/
---


The **com.aspose.words** package provides classes for generating, converting, modifying, rendering and printing Microsoft Word documents without utilizing Microsoft Word.

Aspose.Words is written completely in Java. Microsoft Word is not required in order to use Aspose.Words.

The classes in the **com.aspose.words** package borrow best practices from two well-known frameworks: Microsoft Word Automation and System.Xml. A document in Aspose.Words is represented by a tree of nodes, much like in XML DOM. Where possible, class, method and property names match those found in Microsoft Word Automation.

The main classes in this namespace are:

 *  **Document** is the main class of the object model that represents a Microsoft Word document.
 *  **DocumentBuilder** provides an easy way to insert content and formatting into a document.
 *  **Node** is the base class for all nodes in the document.
 *  **CompositeNode** is the base class for all nodes of the document that can contain other nodes, for example **Paragraph**, **Section** and **Table** and .

The **com.aspose.words** package also contains classes that form the reporting engine of Aspose.Words. The reporting engine allows to quickly and easily populate documents designed in Microsoft Word with data from various data sources such as **java.sql.ResultSet**, **array of ResultSets**, **com.aspose.words.net.System.Data.DataSet** or an **array of values**.

The **MailMerge** object which provides access to the reporting functionality is available via the **Document.MailMerge** property.


## Classes

| Class | Description |
| --- | --- |
| [AbsolutePositionTab](../com.aspose.words/absolutepositiontab/) | An absolute position tab is a character which is used to advance the position on the current line of text when displaying this WordprocessingML content. |
| [ArrowLength](../com.aspose.words/arrowlength/) | Length of the arrow at the end of a line. |
| [ArrowType](../com.aspose.words/arrowtype/) | Specifies the type of an arrow at a line end. |
| [ArrowWidth](../com.aspose.words/arrowwidth/) | Width of the arrow at the end of a line. |
| [AsposeWordsPrintDocument](../com.aspose.words/asposewordsprintdocument/) | Provides a default implementation for printing of a [Document](../com.aspose.words/document/) within the Java printing framework. |
| [AutoFitBehavior](../com.aspose.words/autofitbehavior/) | Determines how Aspose.Words resizes the table when you invoke the **M:Aspose.Words.Tables.Table.AutoFit(Aspose.Words.Tables.AutoFitBehavior)** method. |
| [AxisBound](../com.aspose.words/axisbound/) | Represents minimum or maximum bound of axis values. |
| [AxisBuiltInUnit](../com.aspose.words/axisbuiltinunit/) | Specifies the display units for an axis. |
| [AxisCategoryType](../com.aspose.words/axiscategorytype/) | Specifies type of a category axis. |
| [AxisCrosses](../com.aspose.words/axiscrosses/) | Specifies the possible crossing points for an axis. |
| [AxisDisplayUnit](../com.aspose.words/axisdisplayunit/) | Provides access to the scaling options of the display units for the value axis. |
| [AxisScaleType](../com.aspose.words/axisscaletype/) | Specifies the possible scale types for an axis. |
| [AxisScaling](../com.aspose.words/axisscaling/) | Represents the scaling options of the axis. |
| [AxisTickLabelPosition](../com.aspose.words/axisticklabelposition/) | Specifies the possible positions for tick labels. |
| [AxisTickMark](../com.aspose.words/axistickmark/) | Specifies the possible positions for tick marks. |
| [AxisTimeUnit](../com.aspose.words/axistimeunit/) | Specifies the unit of time for axes. |
| [BarcodeParameters](../com.aspose.words/barcodeparameters/) | Container class for barcode parameters to pass-through to BarcodeGenerator. |
| [BaseWebExtensionCollection](../com.aspose.words/basewebextensioncollection/) | Base class for [TaskPaneCollection](../com.aspose.words/taskpanecollection/), [WebExtensionBindingCollection](../com.aspose.words/webextensionbindingcollection/), [WebExtensionPropertyCollection](../com.aspose.words/webextensionpropertycollection/) and [WebExtensionReferenceCollection](../com.aspose.words/webextensionreferencecollection/) collections. |
| [BaselineAlignment](../com.aspose.words/baselinealignment/) | Specifies fonts vertical position on a line. |
| [BasicTextShaperCache](../com.aspose.words/basictextshapercache/) | Implements basic cache for [ITextShaper](../com.aspose.words/itextshaper/) instances. |
| [BlockImportMode](../com.aspose.words/blockimportmode/) | Specifies how properties of block-level elements are imported from HTML-based documents. |
| [Body](../com.aspose.words/body/) | Represents a container for the main text of a section. |
| [Bookmark](../com.aspose.words/bookmark/) | Represents a single bookmark. |
| [BookmarkCollection](../com.aspose.words/bookmarkcollection/) | A collection of [Bookmark](../com.aspose.words/bookmark/) objects that represent the bookmarks in the specified range. |
| [BookmarkEnd](../com.aspose.words/bookmarkend/) | Represents an end of a bookmark in a Word document. |
| [BookmarkStart](../com.aspose.words/bookmarkstart/) | Represents a start of a bookmark in a Word document. |
| [BookmarksOutlineLevelCollection](../com.aspose.words/bookmarksoutlinelevelcollection/) | A collection of individual bookmarks outline level. |
| [Border](../com.aspose.words/border/) | Represents a border of an object. |
| [BorderCollection](../com.aspose.words/bordercollection/) | A collection of [Border](../com.aspose.words/border/) objects. |
| [BorderType](../com.aspose.words/bordertype/) | Specifies sides of a border. |
| [BreakType](../com.aspose.words/breaktype/) | Specifies type of a break inside a document. |
| [BubbleSizeCollection](../com.aspose.words/bubblesizecollection/) | Represents a collection of bubble sizes for a chart series. |
| [BuildVersionInfo](../com.aspose.words/buildversioninfo/) | Provides information about the current product name and version. |
| [BuildingBlock](../com.aspose.words/buildingblock/) | Represents a glossary document entry such as a Building Block, AutoText or an AutoCorrect entry. |
| [BuildingBlockBehavior](../com.aspose.words/buildingblockbehavior/) | Specifies the behavior that shall be applied to the contents of the building block when it is inserted into the main document. |
| [BuildingBlockCollection](../com.aspose.words/buildingblockcollection/) | A collection of [BuildingBlock](../com.aspose.words/buildingblock/) objects in the document. |
| [BuildingBlockGallery](../com.aspose.words/buildingblockgallery/) | Specifies the predefined gallery into which a building block is classified. |
| [BuildingBlockType](../com.aspose.words/buildingblocktype/) | Specifies a building block type. |
| [BuiltInDocumentProperties](../com.aspose.words/builtindocumentproperties/) | A collection of built-in document properties. |
| [CalendarType](../com.aspose.words/calendartype/) | Specifies the type of a calendar. |
| [Cell](../com.aspose.words/cell/) | Represents a table cell. |
| [CellCollection](../com.aspose.words/cellcollection/) | Provides typed access to a collection of [Cell](../com.aspose.words/cell/) nodes. |
| [CellFormat](../com.aspose.words/cellformat/) | Represents all formatting for a table cell. |
| [CellMerge](../com.aspose.words/cellmerge/) | Specifies how a cell in a table is merged with other cells. |
| [CellVerticalAlignment](../com.aspose.words/cellverticalalignment/) | Specifies vertical justification of text inside a table cell. |
| [CertificateHolder](../com.aspose.words/certificateholder/) | Represents a holder of **X509Certificate2** instance. |
| [ChapterPageSeparator](../com.aspose.words/chapterpageseparator/) | Defines the separator character that appears between the chapter and page number. |
| [Chart](../com.aspose.words/chart/) | Provides access to the chart shape properties. |
| [ChartAxis](../com.aspose.words/chartaxis/) | Represents the axis options of the chart. |
| [ChartAxisCollection](../com.aspose.words/chartaxiscollection/) | Represents a collection of chart axes. |
| [ChartAxisTitle](../com.aspose.words/chartaxistitle/) | Provides access to the axis title properties. |
| [ChartAxisType](../com.aspose.words/chartaxistype/) | Specifies type of chart axis. |
| [ChartDataLabel](../com.aspose.words/chartdatalabel/) | Represents data label on a chart point or trendline. |
| [ChartDataLabelCollection](../com.aspose.words/chartdatalabelcollection/) | Represents a collection of [ChartDataLabel](../com.aspose.words/chartdatalabel/). |
| [ChartDataPoint](../com.aspose.words/chartdatapoint/) | Allows to specify formatting of a single data point on the chart. |
| [ChartDataPointCollection](../com.aspose.words/chartdatapointcollection/) | Represents collection of a [ChartDataPoint](../com.aspose.words/chartdatapoint/). |
| [ChartFormat](../com.aspose.words/chartformat/) | Represents the formatting of a chart element. |
| [ChartLegend](../com.aspose.words/chartlegend/) | Represents chart legend properties. |
| [ChartLegendEntry](../com.aspose.words/chartlegendentry/) | Represents a chart legend entry. |
| [ChartLegendEntryCollection](../com.aspose.words/chartlegendentrycollection/) | Represents a collection of chart legend entries. |
| [ChartMarker](../com.aspose.words/chartmarker/) | Represents a chart data marker. |
| [ChartMultilevelValue](../com.aspose.words/chartmultilevelvalue/) | Represents a value for charts that display multilevel data. |
| [ChartNumberFormat](../com.aspose.words/chartnumberformat/) | Represents number formatting of the parent element. |
| [ChartSeries](../com.aspose.words/chartseries/) | Represents chart series properties. |
| [ChartSeriesCollection](../com.aspose.words/chartseriescollection/) | Represents collection of a [ChartSeries](../com.aspose.words/chartseries/). |
| [ChartSeriesType](../com.aspose.words/chartseriestype/) | Specifies a type of a chart series. |
| [ChartShapeType](../com.aspose.words/chartshapetype/) | Specifies the shape type of chart elements. |
| [ChartTitle](../com.aspose.words/charttitle/) | Provides access to the chart title properties. |
| [ChartType](../com.aspose.words/charttype/) | Specifies type of a chart. |
| [ChartXValue](../com.aspose.words/chartxvalue/) | Represents an X value for a chart series. |
| [ChartXValueCollection](../com.aspose.words/chartxvaluecollection/) | Represents a collection of X values for a chart series. |
| [ChartXValueType](../com.aspose.words/chartxvaluetype/) | Allows to specify type of an X value of a chart series. |
| [ChartYValue](../com.aspose.words/chartyvalue/) | Represents an Y value for a chart series. |
| [ChartYValueCollection](../com.aspose.words/chartyvaluecollection/) | Represents a collection of Y values for a chart series. |
| [ChartYValueType](../com.aspose.words/chartyvaluetype/) | Allows to specify type of an Y value of a chart series. |
| [ChmLoadOptions](../com.aspose.words/chmloadoptions/) | Allows to specify additional options when loading CHM document into a [Document](../com.aspose.words/document/) object. |
| [CleanupOptions](../com.aspose.words/cleanupoptions/) | Allows to specify options for document cleaning. |
| [Cluster](../com.aspose.words/cluster/) | Encapsulates code points and glyphs composing a grapheme. |
| [ColorMode](../com.aspose.words/colormode/) | Specifies how colors are rendered. |
| [ColorPrintMode](../com.aspose.words/colorprintmode/) | Specifies how non-colored pages are printed if the device supports color printing. |
| [Comment](../com.aspose.words/comment/) | Represents a container for text of a comment. |
| [CommentCollection](../com.aspose.words/commentcollection/) | Provides typed access to a collection of [Comment](../com.aspose.words/comment/) nodes. |
| [CommentDisplayMode](../com.aspose.words/commentdisplaymode/) | Specifies the rendering mode for document comments. |
| [CommentRangeEnd](../com.aspose.words/commentrangeend/) | Denotes the end of a region of text that has a comment associated with it. |
| [CommentRangeStart](../com.aspose.words/commentrangestart/) | Denotes the start of a region of text that has a comment associated with it. |
| [CompareOptions](../com.aspose.words/compareoptions/) | Allows to choose advanced options for document comparison operation. |
| [ComparisonEvaluationResult](../com.aspose.words/comparisonevaluationresult/) | The comparison evaluation result. |
| [ComparisonExpression](../com.aspose.words/comparisonexpression/) | The comparison expression. |
| [ComparisonTargetType](../com.aspose.words/comparisontargettype/) | Allows to specify base document which will be used during comparison. |
| [Compatibility](../com.aspose.words/compatibility/) | Specifies names of compatibility options. |
| [CompatibilityOptions](../com.aspose.words/compatibilityoptions/) | Contains compatibility options (that is, the user preferences entered on the **Compatibility** tab of the **Options** dialog in Microsoft Word). |
| [CompositeNode](../com.aspose.words/compositenode/) | Base class for nodes that can contain other nodes. |
| [CompressionLevel](../com.aspose.words/compressionlevel/) | Compression level for OOXML files. |
| [ConditionalStyle](../com.aspose.words/conditionalstyle/) | Represents special formatting applied to some area of a table with assigned table style. |
| [ConditionalStyleCollection](../com.aspose.words/conditionalstylecollection/) | Represents a collection of [ConditionalStyle](../com.aspose.words/conditionalstyle/) objects. |
| [ConditionalStyleType](../com.aspose.words/conditionalstyletype/) | Represents possible table areas to which conditional formatting may be defined in a table style. |
| [ContentDisposition](../com.aspose.words/contentdisposition/) | Enumerates different ways of presenting the document at the client browser. |
| [ContinuousSectionRestart](../com.aspose.words/continuoussectionrestart/) | Represents different behaviors when computing page numbers in a continuous section that restarts page numbering. |
| [ControlChar](../com.aspose.words/controlchar/) | Control characters often encountered in documents. |
| [ConvertUtil](../com.aspose.words/convertutil/) | Provides helper functions to convert between various measurement units. |
| [CssSavingArgs](../com.aspose.words/csssavingargs/) | Provides data for the [ICssSavingCallback.\#cssSaving(com.aspose.words.CssSavingArgs)](../com.aspose.words/icsssavingcallback/\#cssSaving-com.aspose.words.CssSavingArgs) event. |
| [CssStyleSheetType](../com.aspose.words/cssstylesheettype/) | Specifies how CSS (Cascading Style Sheet) styles are exported to HTML. |
| [CsvDataLoadOptions](../com.aspose.words/csvdataloadoptions/) | Represents options for parsing CSV data. |
| [CsvDataSource](../com.aspose.words/csvdatasource/) | Provides access to data of a CSV file or stream to be used within a report. |
| [CurrentThreadSettings](../com.aspose.words/currentthreadsettings/) | This class helps to set thread-isolated Locale and Time Zone for a Aspose.Words application. |
| [CustomDocumentProperties](../com.aspose.words/customdocumentproperties/) | A collection of custom document properties. |
| [CustomPart](../com.aspose.words/custompart/) | Represents a custom (arbitrary content) part, that is not defined by the ISO/IEC 29500 standard. |
| [CustomPartCollection](../com.aspose.words/custompartcollection/) | Represents a collection of [CustomPart](../com.aspose.words/custompart/) objects. |
| [CustomXmlPart](../com.aspose.words/customxmlpart/) | Represents a Custom XML Data Storage Part (custom XML data within a package). |
| [CustomXmlPartCollection](../com.aspose.words/customxmlpartcollection/) | Represents a collection of Custom XML Parts. |
| [CustomXmlProperty](../com.aspose.words/customxmlproperty/) | Represents a single custom XML attribute or a smart tag property. |
| [CustomXmlPropertyCollection](../com.aspose.words/customxmlpropertycollection/) | Represents a collection of custom XML attributes or smart tag properties. |
| [CustomXmlSchemaCollection](../com.aspose.words/customxmlschemacollection/) | A collection of strings that represent XML schemas that are associated with a custom XML part. |
| [DashStyle](../com.aspose.words/dashstyle/) | Dashed line style. |
| [DefaultFontSubstitutionRule](../com.aspose.words/defaultfontsubstitutionrule/) | Default font substitution rule. |
| [DigitalSignature](../com.aspose.words/digitalsignature/) | Represents a digital signature on a document and the result of its verification. |
| [DigitalSignatureCollection](../com.aspose.words/digitalsignaturecollection/) | Provides a read-only collection of digital signatures attached to a document. |
| [DigitalSignatureType](../com.aspose.words/digitalsignaturetype/) | Specifies the type of a digital signature. |
| [DigitalSignatureUtil](../com.aspose.words/digitalsignatureutil/) | Provides methods for signing document. |
| [Direction](../com.aspose.words/direction/) | Text direction. |
| [Dml3DEffectsRenderingMode](../com.aspose.words/dml3deffectsrenderingmode/) | Specifies how 3D shape effects are rendered. |
| [DmlEffectsRenderingMode](../com.aspose.words/dmleffectsrenderingmode/) | Specifies how DrawingML effects are rendered to fixed page formats. |
| [DmlRenderingMode](../com.aspose.words/dmlrenderingmode/) | Specifies how DrawingML shapes are rendered to fixed page formats. |
| [DocSaveOptions](../com.aspose.words/docsaveoptions/) | Can be used to specify additional options when saving a document into the [SaveFormat.\#DOC](../com.aspose.words/saveformat/\#DOC) or [SaveFormat.\#DOT](../com.aspose.words/saveformat/\#DOT) format. |
| [Document](../com.aspose.words/document/) | Represents a Word document. |
| [DocumentBase](../com.aspose.words/documentbase/) | Provides the abstract base class for a main document and a glossary document of a Word document. |
| [DocumentBuilder](../com.aspose.words/documentbuilder/) | Provides methods to insert text, images and other content, specify font, paragraph and section formatting. |
| [DocumentDirection](../com.aspose.words/documentdirection/) | Allows to specify the direction to flow the text in a document. |
| [DocumentLoadingArgs](../com.aspose.words/documentloadingargs/) | An argument passed into [IDocumentLoadingCallback.\#notify(com.aspose.words.DocumentLoadingArgs)](../com.aspose.words/idocumentloadingcallback/\#notify-com.aspose.words.DocumentLoadingArgs). |
| [DocumentPartSavingArgs](../com.aspose.words/documentpartsavingargs/) | Provides data for the [IDocumentPartSavingCallback.\#documentPartSaving(com.aspose.words.DocumentPartSavingArgs)](../com.aspose.words/idocumentpartsavingcallback/\#documentPartSaving-com.aspose.words.DocumentPartSavingArgs) callback. |
| [DocumentProperty](../com.aspose.words/documentproperty/) | Represents a custom or built-in document property. |
| [DocumentPropertyCollection](../com.aspose.words/documentpropertycollection/) | Base class for [BuiltInDocumentProperties](../com.aspose.words/builtindocumentproperties/) and [CustomDocumentProperties](../com.aspose.words/customdocumentproperties/) collections. |
| [DocumentReaderPluginLoadException](../com.aspose.words/documentreaderpluginloadexception/) | Thrown during document load, when the plugin required for reading the document format cannot be loaded. |
| [DocumentSavingArgs](../com.aspose.words/documentsavingargs/) | An argument passed into [IDocumentSavingCallback.\#notify(com.aspose.words.DocumentSavingArgs)](../com.aspose.words/idocumentsavingcallback/\#notify-com.aspose.words.DocumentSavingArgs). |
| [DocumentSecurity](../com.aspose.words/documentsecurity/) | Used as a value for the [BuiltInDocumentProperties.\#getSecurity()](../com.aspose.words/builtindocumentproperties/\#getSecurity) / [BuiltInDocumentProperties.\#setSecurity(int)](../com.aspose.words/builtindocumentproperties/\#setSecurity-int) property. |
| [DocumentSplitCriteria](../com.aspose.words/documentsplitcriteria/) | Specifies how the document is split into parts when saving to [SaveFormat.\#HTML](../com.aspose.words/saveformat/\#HTML), [SaveFormat.\#EPUB](../com.aspose.words/saveformat/\#EPUB) or [SaveFormat.\#AZW\_3](../com.aspose.words/saveformat/\#AZW-3) format. |
| [DocumentVisitor](../com.aspose.words/documentvisitor/) | Base class for custom document visitors. |
| [DownsampleOptions](../com.aspose.words/downsampleoptions/) | Allows to specify downsample options. |
| [DropCapPosition](../com.aspose.words/dropcapposition/) | Specifies the position for a drop cap text. |
| [DropDownItemCollection](../com.aspose.words/dropdownitemcollection/) | A collection of strings that represent all the items in a drop-down form field. |
| [EditableRange](../com.aspose.words/editablerange/) | Represents a single editable range. |
| [EditableRangeEnd](../com.aspose.words/editablerangeend/) | Represents an end of an editable range in a Word document. |
| [EditableRangeStart](../com.aspose.words/editablerangestart/) | Represents a start of an editable range in a Word document. |
| [EditingLanguage](../com.aspose.words/editinglanguage/) | Specifies the editing language. |
| [EditorType](../com.aspose.words/editortype/) | Specifies the set of possible aliases (or editing groups) which can be used as aliases to determine if the current user shall be allowed to edit a single range defined by an editable range within a document. |
| [EmbeddedFontFormat](../com.aspose.words/embeddedfontformat/) | Specifies format of particular embedded font inside [FontInfo](../com.aspose.words/fontinfo/) object. |
| [EmbeddedFontStyle](../com.aspose.words/embeddedfontstyle/) | Specifies the style of an embedded font inside a [FontInfo](../com.aspose.words/fontinfo/) object. |
| [EmfPlusDualRenderingMode](../com.aspose.words/emfplusdualrenderingmode/) | Specifies how Aspose.Words should render EMF+ Dual metafiles. |
| [EmphasisMark](../com.aspose.words/emphasismark/) | Specifies possible types of emphasis mark. |
| [EndCap](../com.aspose.words/endcap/) | Specifies line cap style. |
| [EndnoteOptions](../com.aspose.words/endnoteoptions/) | Represents the endnote numbering options for a document or section. |
| [EndnotePosition](../com.aspose.words/endnoteposition/) | Defines the endnote position. |
| [ExportFontFormat](../com.aspose.words/exportfontformat/) | Indicates the format that is used to export fonts while rendering to HTML fixed format. |
| [ExportHeadersFootersMode](../com.aspose.words/exportheadersfootersmode/) | Specifies how headers and footers are exported to HTML, MHTML or EPUB. |
| [ExportListLabels](../com.aspose.words/exportlistlabels/) | Specifies how list labels are exported to HTML, MHTML and EPUB. |
| [Field](../com.aspose.words/field/) | Represents a Microsoft Word document field. |
| [FieldAddIn](../com.aspose.words/fieldaddin/) | Implements the ADDIN field. |
| [FieldAddressBlock](../com.aspose.words/fieldaddressblock/) | Implements the ADDRESSBLOCK field. |
| [FieldAdvance](../com.aspose.words/fieldadvance/) | Implements the ADVANCE field. |
| [FieldArgumentBuilder](../com.aspose.words/fieldargumentbuilder/) | Builds a complex field argument consisting of fields, nodes, and plain text. |
| [FieldAsk](../com.aspose.words/fieldask/) | Implements the ASK field. |
| [FieldAuthor](../com.aspose.words/fieldauthor/) | Implements the AUTHOR field. |
| [FieldAutoNum](../com.aspose.words/fieldautonum/) | Implements the AUTONUM field. |
| [FieldAutoNumLgl](../com.aspose.words/fieldautonumlgl/) | Implements the AUTONUMLGL field. |
| [FieldAutoNumOut](../com.aspose.words/fieldautonumout/) | Implements the AUTONUMOUT field. |
| [FieldAutoText](../com.aspose.words/fieldautotext/) | Implements the AUTOTEXT field. |
| [FieldAutoTextList](../com.aspose.words/fieldautotextlist/) | Implements the AUTOTEXTLIST field. |
| [FieldBarcode](../com.aspose.words/fieldbarcode/) | Implements the BARCODE field. |
| [FieldBibliography](../com.aspose.words/fieldbibliography/) | Implements the BIBLIOGRAPHY field. |
| [FieldBidiOutline](../com.aspose.words/fieldbidioutline/) | Implements the BIDIOUTLINE field. |
| [FieldBuilder](../com.aspose.words/fieldbuilder/) | Builds a field from field code tokens (arguments and switches). |
| [FieldChar](../com.aspose.words/fieldchar/) | Base class for nodes that represent field characters in a document. |
| [FieldCitation](../com.aspose.words/fieldcitation/) | Implements the CITATION field. |
| [FieldCollection](../com.aspose.words/fieldcollection/) | A collection of [Field](../com.aspose.words/field/) objects that represents the fields in the specified range. |
| [FieldComments](../com.aspose.words/fieldcomments/) | Implements the COMMENTS field. |
| [FieldCompare](../com.aspose.words/fieldcompare/) | Implements the COMPARE field. |
| [FieldCreateDate](../com.aspose.words/fieldcreatedate/) | Implements the CREATEDATE field. |
| [FieldData](../com.aspose.words/fielddata/) | Implements the DATA field. |
| [FieldDatabase](../com.aspose.words/fielddatabase/) | Implements the DATABASE field. |
| [FieldDatabaseDataRow](../com.aspose.words/fielddatabasedatarow/) | Provides data for the [FieldDatabase](../com.aspose.words/fielddatabase/) field result. |
| [FieldDatabaseDataTable](../com.aspose.words/fielddatabasedatatable/) | Provides data for the [FieldDatabase](../com.aspose.words/fielddatabase/) field result. |
| [FieldDate](../com.aspose.words/fielddate/) | Implements the DATE field. |
| [FieldDde](../com.aspose.words/fielddde/) | Implements the DDE field. |
| [FieldDdeAuto](../com.aspose.words/fieldddeauto/) | Implements the DDEAUTO field. |
| [FieldDisplayBarcode](../com.aspose.words/fielddisplaybarcode/) | Implements the DISPLAYBARCODE field. |
| [FieldDocProperty](../com.aspose.words/fielddocproperty/) | Implements the DOCPROPERTY field. |
| [FieldDocVariable](../com.aspose.words/fielddocvariable/) | Implements DOCVARIABLE field. |
| [FieldEQ](../com.aspose.words/fieldeq/) | Implements the EQ field. |
| [FieldEditTime](../com.aspose.words/fieldedittime/) | Implements the EDITTIME field. |
| [FieldEmbed](../com.aspose.words/fieldembed/) | Implements the EMBED field. |
| [FieldEnd](../com.aspose.words/fieldend/) | Represents an end of a Word field in a document. |
| [FieldFileName](../com.aspose.words/fieldfilename/) | Implements the FILENAME field. |
| [FieldFileSize](../com.aspose.words/fieldfilesize/) | Implements the FILESIZE field. |
| [FieldFillIn](../com.aspose.words/fieldfillin/) | Implements the FILLIN field. |
| [FieldFootnoteRef](../com.aspose.words/fieldfootnoteref/) | Implements the FOOTNOTEREF field. |
| [FieldFormCheckBox](../com.aspose.words/fieldformcheckbox/) | Implements the FORMCHECKBOX field. |
| [FieldFormDropDown](../com.aspose.words/fieldformdropdown/) | Implements the FORMDROPDOWN field. |
| [FieldFormText](../com.aspose.words/fieldformtext/) | Implements the FORMTEXT field. |
| [FieldFormat](../com.aspose.words/fieldformat/) | Provides typed access to field's numeric, date and time, and general formatting. |
| [FieldFormula](../com.aspose.words/fieldformula/) | Implements the = (formula) field. |
| [FieldGlossary](../com.aspose.words/fieldglossary/) | Implements the GLOSSARY field. |
| [FieldGoToButton](../com.aspose.words/fieldgotobutton/) | Implements the GOTOBUTTON field. |
| [FieldGreetingLine](../com.aspose.words/fieldgreetingline/) | Implements the GREETINGLINE field. |
| [FieldHyperlink](../com.aspose.words/fieldhyperlink/) | Implements the HYPERLINK field |
| [FieldIf](../com.aspose.words/fieldif/) | Implements the IF field. |
| [FieldIfComparisonResult](../com.aspose.words/fieldifcomparisonresult/) | Specifies the result of the IF field condition evaluation. |
| [FieldImport](../com.aspose.words/fieldimport/) | Implements the IMPORT field. |
| [FieldInclude](../com.aspose.words/fieldinclude/) | Implements the INCLUDE field. |
| [FieldIncludePicture](../com.aspose.words/fieldincludepicture/) | Implements the INCLUDEPICTURE field. |
| [FieldIncludeText](../com.aspose.words/fieldincludetext/) | Implements the INCLUDETEXT field. |
| [FieldIndex](../com.aspose.words/fieldindex/) | Implements the INDEX field. |
| [FieldIndexFormat](../com.aspose.words/fieldindexformat/) | Specifies the formatting for the [FieldIndex](../com.aspose.words/fieldindex/) fields in a document. |
| [FieldInfo](../com.aspose.words/fieldinfo/) | Implements the INFO field. |
| [FieldKeywords](../com.aspose.words/fieldkeywords/) | Implements the KEYWORDS field. |
| [FieldLastSavedBy](../com.aspose.words/fieldlastsavedby/) | Implements the LASTSAVEDBY field. |
| [FieldLink](../com.aspose.words/fieldlink/) | Implements the LINK field. |
| [FieldListNum](../com.aspose.words/fieldlistnum/) | Implements the LISTNUM field. |
| [FieldMacroButton](../com.aspose.words/fieldmacrobutton/) | Implements the MACROBUTTON field. |
| [FieldMergeBarcode](../com.aspose.words/fieldmergebarcode/) | Implements the MERGEBARCODE field. |
| [FieldMergeField](../com.aspose.words/fieldmergefield/) | Implements the MERGEFIELD field. |
| [FieldMergeRec](../com.aspose.words/fieldmergerec/) | Implements the MERGEREC field. |
| [FieldMergeSeq](../com.aspose.words/fieldmergeseq/) | Implements the MERGESEQ field. |
| [FieldMergingArgs](../com.aspose.words/fieldmergingargs/) | Provides data for the **MergeField** event. |
| [FieldMergingArgsBase](../com.aspose.words/fieldmergingargsbase/) | Base class for [FieldMergingArgs](../com.aspose.words/fieldmergingargs/) and [ImageFieldMergingArgs](../com.aspose.words/imagefieldmergingargs/). |
| [FieldNext](../com.aspose.words/fieldnext/) | Implements the NEXT field. |
| [FieldNextIf](../com.aspose.words/fieldnextif/) | Implements the NEXTIF field. |
| [FieldNoteRef](../com.aspose.words/fieldnoteref/) | Implements the NOTEREF field. |
| [FieldNumChars](../com.aspose.words/fieldnumchars/) | Implements the NUMCHARS field. |
| [FieldNumPages](../com.aspose.words/fieldnumpages/) | Implements the NUMPAGES field. |
| [FieldNumWords](../com.aspose.words/fieldnumwords/) | Implements the NUMWORDS field. |
| [FieldOcx](../com.aspose.words/fieldocx/) | Implements the OCX field. |
| [FieldOptions](../com.aspose.words/fieldoptions/) | Represents options to control field handling in a document. |
| [FieldPage](../com.aspose.words/fieldpage/) | Implements the PAGE field. |
| [FieldPageRef](../com.aspose.words/fieldpageref/) | Implements the PAGEREF field. |
| [FieldPrint](../com.aspose.words/fieldprint/) | Implements the PRINT field. |
| [FieldPrintDate](../com.aspose.words/fieldprintdate/) | Implements the PRINTDATE field. |
| [FieldPrivate](../com.aspose.words/fieldprivate/) | Implements the PRIVATE field. |
| [FieldQuote](../com.aspose.words/fieldquote/) | Implements the QUOTE field. |
| [FieldRD](../com.aspose.words/fieldrd/) | Implements the RD field. |
| [FieldRef](../com.aspose.words/fieldref/) | Implements the REF field. |
| [FieldRevNum](../com.aspose.words/fieldrevnum/) | Implements the REVNUM field. |
| [FieldSaveDate](../com.aspose.words/fieldsavedate/) | Implements the SAVEDATE field. |
| [FieldSection](../com.aspose.words/fieldsection/) | Implements the SECTION field. |
| [FieldSectionPages](../com.aspose.words/fieldsectionpages/) | Implements the SECTIONPAGES field. |
| [FieldSeparator](../com.aspose.words/fieldseparator/) | Represents a Word field separator that separates the field code from the field result. |
| [FieldSeq](../com.aspose.words/fieldseq/) | Implements the SEQ field. |
| [FieldSet](../com.aspose.words/fieldset/) | Implements the SET field. |
| [FieldShape](../com.aspose.words/fieldshape/) | Implements the SHAPE field. |
| [FieldSkipIf](../com.aspose.words/fieldskipif/) | Implements the SKIPIF field. |
| [FieldStart](../com.aspose.words/fieldstart/) | Represents a start of a Word field in a document. |
| [FieldStyleRef](../com.aspose.words/fieldstyleref/) | Implements the STYLEREF field. |
| [FieldSubject](../com.aspose.words/fieldsubject/) | Implements the SUBJECT field. |
| [FieldSymbol](../com.aspose.words/fieldsymbol/) | Implements a SYMBOL field. |
| [FieldTA](../com.aspose.words/fieldta/) | Implements the TA field. |
| [FieldTC](../com.aspose.words/fieldtc/) | Implements the TC field. |
| [FieldTemplate](../com.aspose.words/fieldtemplate/) | Implements the TEMPLATE field. |
| [FieldTime](../com.aspose.words/fieldtime/) | Implements the TIME field. |
| [FieldTitle](../com.aspose.words/fieldtitle/) | Implements the TITLE field. |
| [FieldToa](../com.aspose.words/fieldtoa/) | Implements the TOA field. |
| [FieldToc](../com.aspose.words/fieldtoc/) | Implements the TOC field. |
| [FieldType](../com.aspose.words/fieldtype/) | Specifies Microsoft Word field types. |
| [FieldUnknown](../com.aspose.words/fieldunknown/) | Implements an unknown or unrecognized field. |
| [FieldUpdateCultureSource](../com.aspose.words/fieldupdateculturesource/) | Indicates what culture to use during field update. |
| [FieldUpdatingProgressArgs](../com.aspose.words/fieldupdatingprogressargs/) | Provides data for the field updating progress event. |
| [FieldUserAddress](../com.aspose.words/fielduseraddress/) | Implements the USERADDRESS field. |
| [FieldUserInitials](../com.aspose.words/fielduserinitials/) | Implements the USERINITIALS field. |
| [FieldUserName](../com.aspose.words/fieldusername/) | Implements the USERNAME field. |
| [FieldXE](../com.aspose.words/fieldxe/) | Implements the XE field. |
| [FileCorruptedException](../com.aspose.words/filecorruptedexception/) | Thrown during document load, when the document appears to be corrupted and impossible to load. |
| [FileFontSource](../com.aspose.words/filefontsource/) | Represents the single TrueType font file stored in the file system. |
| [FileFormatInfo](../com.aspose.words/fileformatinfo/) | Contains data returned by [FileFormatUtil](../com.aspose.words/fileformatutil/) document format detection methods. |
| [FileFormatUtil](../com.aspose.words/fileformatutil/) | Provides utility methods for working with file formats, such as detecting file format or converting file extensions to/from file format enums. |
| [Fill](../com.aspose.words/fill/) | Represents fill formatting for an object. |
| [FillType](../com.aspose.words/filltype/) | Specifies fill type for a fillable object. |
| [FindReplaceDirection](../com.aspose.words/findreplacedirection/) | Specifies direction for replace operations. |
| [FindReplaceOptions](../com.aspose.words/findreplaceoptions/) | Specifies options for find/replace operations. |
| [FipsUnapprovedOperationException](../com.aspose.words/fipsunapprovedoperationexception/) | Represents the exception that is thrown when incorrectly trying to use cryptography. |
| [FixedPageSaveOptions](../com.aspose.words/fixedpagesaveoptions/) | Contains common options that can be specified when saving a document into fixed page formats (PDF, XPS, images etc). |
| [FlipOrientation](../com.aspose.words/fliporientation/) | Possible values for the orientation of a shape. |
| [FolderFontSource](../com.aspose.words/folderfontsource/) | Represents the folder that contains TrueType font files. |
| [Font](../com.aspose.words/font/) | Contains font attributes (font name, font size, color, and so on) for an object. |
| [FontConfigSubstitutionRule](../com.aspose.words/fontconfigsubstitutionrule/) | Font config substitution rule. |
| [FontFallbackSettings](../com.aspose.words/fontfallbacksettings/) | Specifies font fallback mechanism settings. |
| [FontFamily](../com.aspose.words/fontfamily/) | Represents the font family. |
| [FontFeature](../com.aspose.words/fontfeature/) | Features provide information about how glyphs are used in a font to render a script. |
| [FontInfo](../com.aspose.words/fontinfo/) | Specifies information about a font used in the document. |
| [FontInfoCollection](../com.aspose.words/fontinfocollection/) | Represents a collection of fonts used in a document. |
| [FontInfoSubstitutionRule](../com.aspose.words/fontinfosubstitutionrule/) | Font info substitution rule. |
| [FontNameSubstitutionRule](../com.aspose.words/fontnamesubstitutionrule/) | Font substitution rule for processing font name. |
| [FontPitch](../com.aspose.words/fontpitch/) | Represents the font pitch. |
| [FontSavingArgs](../com.aspose.words/fontsavingargs/) | Provides data for the [IFontSavingCallback.\#fontSaving(com.aspose.words.FontSavingArgs)](../com.aspose.words/ifontsavingcallback/\#fontSaving-com.aspose.words.FontSavingArgs) event. |
| [FontSettings](../com.aspose.words/fontsettings/) | Specifies font settings for a document. |
| [FontSourceBase](../com.aspose.words/fontsourcebase/) | This is an abstract base class for the classes that allow the user to specify various font sources. |
| [FontSourceType](../com.aspose.words/fontsourcetype/) | Specifies the type of a font source. |
| [FontSubstitutionRule](../com.aspose.words/fontsubstitutionrule/) | This is an abstract base class for the font substitution rule. |
| [FontSubstitutionSettings](../com.aspose.words/fontsubstitutionsettings/) | Specifies font substitution mechanism settings. |
| [Footnote](../com.aspose.words/footnote/) | Represents a container for text of a footnote or endnote. |
| [FootnoteNumberingRule](../com.aspose.words/footnotenumberingrule/) | Determines when automatic footnote or endnote numbering restarts. |
| [FootnoteOptions](../com.aspose.words/footnoteoptions/) | Represents the footnote numbering options for a document or section. |
| [FootnotePosition](../com.aspose.words/footnoteposition/) | Defines the footnote position. |
| [FootnoteType](../com.aspose.words/footnotetype/) | Specifies whether this is a footnote or an endnote. |
| [FormField](../com.aspose.words/formfield/) | Represents a single form field. |
| [FormFieldCollection](../com.aspose.words/formfieldcollection/) | A collection of [FormField](../com.aspose.words/formfield/) objects that represent all the form fields in a range. |
| [Forms2OleControl](../com.aspose.words/forms2olecontrol/) | Represents Microsoft Forms 2.0 OLE control. |
| [Forms2OleControlCollection](../com.aspose.words/forms2olecontrolcollection/) | Represents collection of [Forms2OleControl](../com.aspose.words/forms2olecontrol/) objects. |
| [Forms2OleControlType](../com.aspose.words/forms2olecontroltype/) | Enumerates types of Forms 2.0 controls. |
| [FrameFormat](../com.aspose.words/frameformat/) | Represents frame related formatting for a paragraph. |
| [Frameset](../com.aspose.words/frameset/) | Represents a frames page or a single frame on a frames page. |
| [FramesetCollection](../com.aspose.words/framesetcollection/) | Represents a collection of instances of the [Frameset](../com.aspose.words/frameset/) class. |
| [GeneralFormat](../com.aspose.words/generalformat/) | Specifies a general format that is applied to a numeric, text, or any field result. |
| [GeneralFormatCollection](../com.aspose.words/generalformatcollection/) | Represents a typed collection of general formats. |
| [GlossaryDocument](../com.aspose.words/glossarydocument/) | Represents the root element for a glossary document within a Word document. |
| [Glyph](../com.aspose.words/glyph/) | Represents a glyph |
| [GradientStop](../com.aspose.words/gradientstop/) | Represents one gradient stop. |
| [GradientStopCollection](../com.aspose.words/gradientstopcollection/) | Contains a collection of [GradientStop](../com.aspose.words/gradientstop/) objects. |
| [GradientStyle](../com.aspose.words/gradientstyle/) | Specifies the style for a gradient fill. |
| [GradientVariant](../com.aspose.words/gradientvariant/) | Specifies the variant for a gradient fill. |
| [Granularity](../com.aspose.words/granularity/) | Specifies the granularity of changes to track when comparing two documents. |
| [GraphicsQualityOptions](../com.aspose.words/graphicsqualityoptions/) | Allows to specify additional **java.awt.RenderingHints**. |
| [GroupShape](../com.aspose.words/groupshape/) | Represents a group of shapes in a document. |
| [HeaderFooter](../com.aspose.words/headerfooter/) | Represents a container for the header or footer text of a section. |
| [HeaderFooterBookmarksExportMode](../com.aspose.words/headerfooterbookmarksexportmode/) | Specifies how bookmarks in headers/footers are exported. |
| [HeaderFooterCollection](../com.aspose.words/headerfootercollection/) | Provides typed access to [HeaderFooter](../com.aspose.words/headerfooter/) nodes of a [Section](../com.aspose.words/section/). |
| [HeaderFooterType](../com.aspose.words/headerfootertype/) | Identifies the type of header or footer found in a Word file. |
| [HeightRule](../com.aspose.words/heightrule/) | Specifies the rule for determining the height of an object. |
| [HorizontalAlignment](../com.aspose.words/horizontalalignment/) | Specifies horizontal alignment of a floating shape, text frame or floating table. |
| [HorizontalRuleAlignment](../com.aspose.words/horizontalrulealignment/) | Represents the alignment for the specified horizontal rule. |
| [HorizontalRuleFormat](../com.aspose.words/horizontalruleformat/) | Represents horizontal rule formatting. |
| [HtmlControlType](../com.aspose.words/htmlcontroltype/) | Type of document nodes that represent  and  elements imported from HTML. |
| [HtmlElementSizeOutputMode](../com.aspose.words/htmlelementsizeoutputmode/) | Specifies how Aspose.Words exports element widths and heights to HTML, MHTML and EPUB. |
| [HtmlFixedPageHorizontalAlignment](../com.aspose.words/htmlfixedpagehorizontalalignment/) | Specifies the horizontal alignment for pages in output HTML document. |
| [HtmlFixedSaveOptions](../com.aspose.words/htmlfixedsaveoptions/) | Can be used to specify additional options when saving a document into the [SaveFormat.\#HTML\_FIXED](../com.aspose.words/saveformat/\#HTML-FIXED) format. |
| [HtmlInsertOptions](../com.aspose.words/htmlinsertoptions/) | Specifies options for the **M:Aspose.Words.DocumentBuilder.InsertHtml(System.String,Aspose.Words.HtmlInsertOptions)** method. |
| [HtmlLoadOptions](../com.aspose.words/htmlloadoptions/) | Allows to specify additional options when loading HTML document into a [Document](../com.aspose.words/document/) object. |
| [HtmlMetafileFormat](../com.aspose.words/htmlmetafileformat/) | Indicates the format in which metafiles are saved to HTML documents. |
| [HtmlOfficeMathOutputMode](../com.aspose.words/htmlofficemathoutputmode/) | Specifies how Aspose.Words exports OfficeMath to HTML, MHTML and EPUB. |
| [HtmlSaveOptions](../com.aspose.words/htmlsaveoptions/) | Can be used to specify additional options when saving a document into the [SaveFormat.\#HTML](../com.aspose.words/saveformat/\#HTML), [SaveFormat.\#MHTML](../com.aspose.words/saveformat/\#MHTML), [SaveFormat.\#EPUB](../com.aspose.words/saveformat/\#EPUB), [SaveFormat.\#AZW\_3](../com.aspose.words/saveformat/\#AZW-3) or [SaveFormat.\#MOBI](../com.aspose.words/saveformat/\#MOBI) format. |
| [HtmlVersion](../com.aspose.words/htmlversion/) | Indicates the version of HTML is used when saving the document to [SaveFormat.\#HTML](../com.aspose.words/saveformat/\#HTML) and [SaveFormat.\#MHTML](../com.aspose.words/saveformat/\#MHTML) formats. |
| [Hyphenation](../com.aspose.words/hyphenation/) | Provides methods for working with hyphenation dictionaries. |
| [HyphenationOptions](../com.aspose.words/hyphenationoptions/) | Allows to configure document hyphenation options. |
| [ImageBinarizationMethod](../com.aspose.words/imagebinarizationmethod/) | Specifies the method used to binarize image. |
| [ImageColorMode](../com.aspose.words/imagecolormode/) | Specifies the color mode for the generated images of document pages. |
| [ImageData](../com.aspose.words/imagedata/) | Defines an image for a shape. |
| [ImageFieldMergingArgs](../com.aspose.words/imagefieldmergingargs/) | Provides data for the [IFieldMergingCallback.\#imageFieldMerging(com.aspose.words.ImageFieldMergingArgs)](../com.aspose.words/ifieldmergingcallback/\#imageFieldMerging-com.aspose.words.ImageFieldMergingArgs) event. |
| [ImagePixelFormat](../com.aspose.words/imagepixelformat/) | Specifies the pixel format for the generated images of document pages. |
| [ImageSaveOptions](../com.aspose.words/imagesaveoptions/) | Allows to specify additional options when rendering document pages or shapes to images. |
| [ImageSavingArgs](../com.aspose.words/imagesavingargs/) | Provides data for the [IImageSavingCallback.\#imageSaving(com.aspose.words.ImageSavingArgs)](../com.aspose.words/iimagesavingcallback/\#imageSaving-com.aspose.words.ImageSavingArgs) event. |
| [ImageSize](../com.aspose.words/imagesize/) | Contains information about image size and resolution. |
| [ImageType](../com.aspose.words/imagetype/) | Specifies the type (format) of an image in a Microsoft Word document. |
| [ImageWatermarkOptions](../com.aspose.words/imagewatermarkoptions/) | Contains options that can be specified when adding a watermark with image. |
| [ImlRenderingMode](../com.aspose.words/imlrenderingmode/) | Specifies how ink (InkML) objects are rendered to fixed page formats. |
| [ImportFormatMode](../com.aspose.words/importformatmode/) | Specifies how formatting is merged when importing content from another document. |
| [ImportFormatOptions](../com.aspose.words/importformatoptions/) | Allows to specify various import options to format output. |
| [IncorrectPasswordException](../com.aspose.words/incorrectpasswordexception/) | Thrown if a document is encrypted with a password and the password specified when opening the document is incorrect or missing. |
| [Inline](../com.aspose.words/inline/) | Base class for inline-level nodes that can have character formatting associated with them, but cannot have child nodes of their own. |
| [InlineStory](../com.aspose.words/inlinestory/) | Base class for inline-level nodes that can contain paragraphs and tables. |
| [InternableComplexAttr](../com.aspose.words/internablecomplexattr/) | Base class for internable complex attribute. |
| [JoinStyle](../com.aspose.words/joinstyle/) | Line join style. |
| [JsonDataLoadOptions](../com.aspose.words/jsondataloadoptions/) | Represents options for parsing JSON data. |
| [JsonDataSource](../com.aspose.words/jsondatasource/) | Provides access to data of a JSON file or stream to be used within a report. |
| [JsonSimpleValueParseMode](../com.aspose.words/jsonsimplevalueparsemode/) | Specifies a mode for parsing JSON simple values (null, boolean, number, integer, and string) while loading JSON. |
| [JustificationMode](../com.aspose.words/justificationmode/) | Specifies the character spacing adjustment for a document. |
| [KnownTypeSet](../com.aspose.words/knowntypeset/) | Represents an unordered set (i.e. |
| [LanguagePreferences](../com.aspose.words/languagepreferences/) | Allows to set up language preferences. |
| [LayoutCollector](../com.aspose.words/layoutcollector/) | This class allows to compute page numbers of document nodes. |
| [LayoutEntityType](../com.aspose.words/layoutentitytype/) | Types of the layout entities. |
| [LayoutEnumerator](../com.aspose.words/layoutenumerator/) | Enumerates page layout entities of a document. |
| [LayoutFlow](../com.aspose.words/layoutflow/) | Determines the flow of the text layout in a textbox. |
| [LayoutOptions](../com.aspose.words/layoutoptions/) | Holds the options that allow controlling the document layout process. |
| [LegendPosition](../com.aspose.words/legendposition/) | Specifies the possible positions for a chart legend. |
| [License](../com.aspose.words/license/) | Provides methods to license the component. |
| [LineNumberRestartMode](../com.aspose.words/linenumberrestartmode/) | Determines when automatic line numbering restarts. |
| [LineSpacingRule](../com.aspose.words/linespacingrule/) | Specifies line spacing values for a paragraph. |
| [LineStyle](../com.aspose.words/linestyle/) | Specifies line style of a [Border](../com.aspose.words/border/). |
| [List](../com.aspose.words/list/) | Represents formatting of a list. |
| [ListCollection](../com.aspose.words/listcollection/) | Stores and manages formatting of bulleted and numbered lists used in a document. |
| [ListFormat](../com.aspose.words/listformat/) | Allows to control what list formatting is applied to a paragraph. |
| [ListLabel](../com.aspose.words/listlabel/) | Defines properties specific to a list label. |
| [ListLevel](../com.aspose.words/listlevel/) | Defines formatting for a list level. |
| [ListLevelAlignment](../com.aspose.words/listlevelalignment/) | Specifies alignment for the list number or bullet. |
| [ListLevelCollection](../com.aspose.words/listlevelcollection/) | A collection of list formatting for each level in a list. |
| [ListTemplate](../com.aspose.words/listtemplate/) | Specifies one of the predefined list formats available in Microsoft Word. |
| [ListTrailingCharacter](../com.aspose.words/listtrailingcharacter/) | Specifies the character that separates the list label from the text of the paragraph. |
| [LoadFormat](../com.aspose.words/loadformat/) | Indicates the format of the document that is to be loaded. |
| [LoadOptions](../com.aspose.words/loadoptions/) | Allows to specify additional options (such as password or base URI) when loading a document into a [Document](../com.aspose.words/document/) object. |
| [MailMerge](../com.aspose.words/mailmerge/) | Represents the mail merge functionality. |
| [MailMergeCheckErrors](../com.aspose.words/mailmergecheckerrors/) | Specifies how Microsoft Word will report errors detected during mail merge. |
| [MailMergeCleanupOptions](../com.aspose.words/mailmergecleanupoptions/) | Specifies options that determine what items are removed during mail merge. |
| [MailMergeDataType](../com.aspose.words/mailmergedatatype/) | Specifies the type of an external mail merge data source. |
| [MailMergeDestination](../com.aspose.words/mailmergedestination/) | Specifies the possible results which may be generated when a mail merge is carried out on a document. |
| [MailMergeMainDocumentType](../com.aspose.words/mailmergemaindocumenttype/) | Specifies the possible types for a mail merge source document. |
| [MailMergeRegionInfo](../com.aspose.words/mailmergeregioninfo/) | Contains information about a mail merge region. |
| [MailMergeSettings](../com.aspose.words/mailmergesettings/) | Specifies all of the mail merge information for a document. |
| [MappedDataFieldCollection](../com.aspose.words/mappeddatafieldcollection/) | Allows to automatically map between names of fields in your data source and names of mail merge fields in the document. |
| [Margins](../com.aspose.words/margins/) | Specifies preset margins. |
| [MarkdownLinkExportMode](../com.aspose.words/markdownlinkexportmode/) | The mode of exporting links to a target document. |
| [MarkdownListExportMode](../com.aspose.words/markdownlistexportmode/) | Specifies how lists are exported into Markdown. |
| [MarkdownSaveOptions](../com.aspose.words/markdownsaveoptions/) | Class to specify additional options when saving a document into the [SaveFormat.\#MARKDOWN](../com.aspose.words/saveformat/\#MARKDOWN) format. |
| [MarkerSymbol](../com.aspose.words/markersymbol/) | Specifies marker symbol style. |
| [MarkupLevel](../com.aspose.words/markuplevel/) | Specifies the level in the document tree where a particular [StructuredDocumentTag](../com.aspose.words/structureddocumenttag/) can occur. |
| [MathObjectType](../com.aspose.words/mathobjecttype/) | Specifies type of an Office Math object. |
| [MeasurementUnits](../com.aspose.words/measurementunits/) | Specifies the unit of measurement. |
| [MemoryFontSource](../com.aspose.words/memoryfontsource/) | Represents the single TrueType font file stored in memory. |
| [MergeFieldImageDimension](../com.aspose.words/mergefieldimagedimension/) | Represents an image dimension (i.e. |
| [MergeFieldImageDimensionUnit](../com.aspose.words/mergefieldimagedimensionunit/) | Specifies an unit of an image dimension (i.e. |
| [MergeFormatMode](../com.aspose.words/mergeformatmode/) | Specifies how formatting is merged when combining multiple documents. |
| [Merger](../com.aspose.words/merger/) | Represents a group of methods intended to merge a variety of different types of documents into a single output document. |
| [MetafileRenderingMode](../com.aspose.words/metafilerenderingmode/) | Specifies how Aspose.Words should render WMF and EMF metafiles. |
| [MetafileRenderingOptions](../com.aspose.words/metafilerenderingoptions/) | Allows to specify additional metafile rendering options. |
| [Metered](../com.aspose.words/metered/) | Provides methods to set metered key. |
| [MsWordVersion](../com.aspose.words/mswordversion/) | Allows Aspose.Wods to mimic MS Word version-specific application behavior. |
| [MultiplePagesType](../com.aspose.words/multiplepagestype/) | Specifies how document is printed out. |
| [MustacheTag](../com.aspose.words/mustachetag/) | Represents "mustache" tag. |
| [NativeLibSettings](../com.aspose.words/nativelibsettings/) | This class helps to set various options such as temporary folder for Aspose.Words native libraries and whether native libraries should be loaded and used. |
| [Node](../com.aspose.words/node/) | Base class for all nodes of a Word document. |
| [NodeChangingAction](../com.aspose.words/nodechangingaction/) | Specifies the type of node change. |
| [NodeChangingArgs](../com.aspose.words/nodechangingargs/) | Provides data for methods of the [INodeChangingCallback](../com.aspose.words/inodechangingcallback/) interface. |
| [NodeCollection](../com.aspose.words/nodecollection/) | Represents a collection of nodes of a specific type. |
| [NodeImporter](../com.aspose.words/nodeimporter/) | Allows to efficiently perform repeated import of nodes from one document to another. |
| [NodeList](../com.aspose.words/nodelist/) | Represents a collection of nodes matching an XPath query executed using the [CompositeNode.\#selectNodes(java.lang.String)](../com.aspose.words/compositenode/\#selectNodes-java.lang.String) method. |
| [NodeRendererBase](../com.aspose.words/noderendererbase/) | Base class for [ShapeRenderer](../com.aspose.words/shaperenderer/) and [OfficeMathRenderer](../com.aspose.words/officemathrenderer/). |
| [NodeType](../com.aspose.words/nodetype/) | Specifies the type of a Word document node. |
| [NumberStyle](../com.aspose.words/numberstyle/) | Specifies the number style for a list, footnotes and endnotes, page numbers. |
| [NumeralFormat](../com.aspose.words/numeralformat/) | Indicates the symbol set that is used to represent numbers while rendering to fixed page formats. |
| [Odso](../com.aspose.words/odso/) | Specifies the Office Data Source Object (ODSO) settings for a mail merge data source. |
| [OdsoDataSourceType](../com.aspose.words/odsodatasourcetype/) | Specifies the type of the external data source to be connected to as part of the ODSO connection information. |
| [OdsoFieldMapData](../com.aspose.words/odsofieldmapdata/) | Specifies how a column in the external data source shall be mapped to the predefined merge fields within the document. |
| [OdsoFieldMapDataCollection](../com.aspose.words/odsofieldmapdatacollection/) | A typed collection of the [OdsoFieldMapData](../com.aspose.words/odsofieldmapdata/) objects. |
| [OdsoFieldMappingType](../com.aspose.words/odsofieldmappingtype/) | Specifies the possible types used to indicate if a given mail merge field has been mapped to a column in the given external data source. |
| [OdsoRecipientData](../com.aspose.words/odsorecipientdata/) | Represents information about a single record within an external data source that is to be excluded from the mail merge. |
| [OdsoRecipientDataCollection](../com.aspose.words/odsorecipientdatacollection/) | A typed collection of [OdsoRecipientData](../com.aspose.words/odsorecipientdata/) |
| [OdtSaveMeasureUnit](../com.aspose.words/odtsavemeasureunit/) | Specified units of measure to apply to measurable document content such as shape, widths and other during saving. |
| [OdtSaveOptions](../com.aspose.words/odtsaveoptions/) | Can be used to specify additional options when saving a document into the [SaveFormat.\#ODT](../com.aspose.words/saveformat/\#ODT) or [SaveFormat.\#OTT](../com.aspose.words/saveformat/\#OTT) format. |
| [OfficeMath](../com.aspose.words/officemath/) | Represents an Office Math object such as function, equation, matrix or alike. |
| [OfficeMathDisplayType](../com.aspose.words/officemathdisplaytype/) | Specifies the display format type of the equation. |
| [OfficeMathJustification](../com.aspose.words/officemathjustification/) | Specifies the justification of the equation. |
| [OfficeMathRenderer](../com.aspose.words/officemathrenderer/) | Provides methods to render an individual [OfficeMath](../com.aspose.words/officemath/) to a raster or vector image or to a Graphics object. |
| [OleControl](../com.aspose.words/olecontrol/) | Represents OLE ActiveX control. |
| [OleFormat](../com.aspose.words/oleformat/) | Provides access to the data of an OLE object or ActiveX control. |
| [OlePackage](../com.aspose.words/olepackage/) | Allows to access OLE Package properties. |
| [OoxmlCompliance](../com.aspose.words/ooxmlcompliance/) | Allows to specify which OOXML specification will be used when saving in the DOCX format. |
| [OoxmlSaveOptions](../com.aspose.words/ooxmlsaveoptions/) | Can be used to specify additional options when saving a document into the [SaveFormat.\#DOCX](../com.aspose.words/saveformat/\#DOCX), [SaveFormat.\#DOCM](../com.aspose.words/saveformat/\#DOCM), [SaveFormat.\#DOTX](../com.aspose.words/saveformat/\#DOTX), [SaveFormat.\#DOTM](../com.aspose.words/saveformat/\#DOTM) or [SaveFormat.\#FLAT\_OPC](../com.aspose.words/saveformat/\#FLAT-OPC) format. |
| [Orientation](../com.aspose.words/orientation/) | Specifies page orientation. |
| [OutlineLevel](../com.aspose.words/outlinelevel/) | Specifies the outline level of a paragraph in the document. |
| [OutlineOptions](../com.aspose.words/outlineoptions/) | Allows to specify outline options. |
| [PageBorderAppliesTo](../com.aspose.words/pageborderappliesto/) | Specifies which pages the page border is printed on. |
| [PageBorderDistanceFrom](../com.aspose.words/pageborderdistancefrom/) | Specifies the positioning of the page border relative to the page margin. |
| [PageInfo](../com.aspose.words/pageinfo/) | Represents information about a particular document page. |
| [PageLayoutCallbackArgs](../com.aspose.words/pagelayoutcallbackargs/) | An argument passed into [IPageLayoutCallback.\#notify(com.aspose.words.PageLayoutCallbackArgs)](../com.aspose.words/ipagelayoutcallback/\#notify-com.aspose.words.PageLayoutCallbackArgs) |
| [PageLayoutEvent](../com.aspose.words/pagelayoutevent/) | A code of event raised during page layout model build and rendering. |
| [PageRange](../com.aspose.words/pagerange/) | Represents a continuous range of pages. |
| [PageSavingArgs](../com.aspose.words/pagesavingargs/) | Provides data for the [IPageSavingCallback.\#pageSaving(com.aspose.words.PageSavingArgs)](../com.aspose.words/ipagesavingcallback/\#pageSaving-com.aspose.words.PageSavingArgs) event. |
| [PageSet](../com.aspose.words/pageset/) | Describes a random set of pages. |
| [PageSetup](../com.aspose.words/pagesetup/) | Represents the page setup properties of a section. |
| [PageVerticalAlignment](../com.aspose.words/pageverticalalignment/) | Specifies vertical justification of text on each page. |
| [PaperSize](../com.aspose.words/papersize/) | Specifies paper size. |
| [Paragraph](../com.aspose.words/paragraph/) | Represents a paragraph of text. |
| [ParagraphAlignment](../com.aspose.words/paragraphalignment/) | Specifies text alignment in a paragraph. |
| [ParagraphCollection](../com.aspose.words/paragraphcollection/) | Provides typed access to a collection of [Paragraph](../com.aspose.words/paragraph/) nodes. |
| [ParagraphFormat](../com.aspose.words/paragraphformat/) | Represents all the formatting for a paragraph. |
| [PatternType](../com.aspose.words/patterntype/) | Specifies the fill pattern to be used to fill a shape. |
| [PclSaveOptions](../com.aspose.words/pclsaveoptions/) | Can be used to specify additional options when saving a document into the [SaveFormat.\#PCL](../com.aspose.words/saveformat/\#PCL) format. |
| [PdfCompliance](../com.aspose.words/pdfcompliance/) | Specifies the PDF standards compliance level. |
| [PdfCustomPropertiesExport](../com.aspose.words/pdfcustompropertiesexport/) | Specifies the way [Document.\#getCustomDocumentProperties()](../com.aspose.words/document/\#getCustomDocumentProperties) are exported to PDF file. |
| [PdfDigitalSignatureDetails](../com.aspose.words/pdfdigitalsignaturedetails/) | Contains details for signing a PDF document with a digital signature. |
| [PdfDigitalSignatureHashAlgorithm](../com.aspose.words/pdfdigitalsignaturehashalgorithm/) | Specifies a digital hash algorithm used by a digital signature. |
| [PdfDigitalSignatureTimestampSettings](../com.aspose.words/pdfdigitalsignaturetimestampsettings/) | Contains settings of the digital signature timestamp. |
| [PdfEncryptionDetails](../com.aspose.words/pdfencryptiondetails/) | Contains details for encrypting and access permissions for a PDF document. |
| [PdfFontEmbeddingMode](../com.aspose.words/pdffontembeddingmode/) | Specifies how Aspose.Words should embed fonts. |
| [PdfImageColorSpaceExportMode](../com.aspose.words/pdfimagecolorspaceexportmode/) | Specifies how the color space will be selected for the images in PDF document. |
| [PdfImageCompression](../com.aspose.words/pdfimagecompression/) | Specifies the type of compression applied to images in the PDF file. |
| [PdfLoadOptions](../com.aspose.words/pdfloadoptions/) | Allows to specify additional options when loading Pdf document into a [Document](../com.aspose.words/document/) object. |
| [PdfPageMode](../com.aspose.words/pdfpagemode/) | Specifies how the PDF document should be displayed when opened in the PDF reader. |
| [PdfPermissions](../com.aspose.words/pdfpermissions/) | Specifies the operations that are allowed to a user on an encrypted PDF document. |
| [PdfSaveOptions](../com.aspose.words/pdfsaveoptions/) | Can be used to specify additional options when saving a document into the [SaveFormat.\#PDF](../com.aspose.words/saveformat/\#PDF) format. |
| [PdfTextCompression](../com.aspose.words/pdftextcompression/) | Specifies a type of compression applied to all content in the PDF file except images. |
| [PdfZoomBehavior](../com.aspose.words/pdfzoombehavior/) | Specifies the type of zoom applied to a PDF document when it is opened in a PDF viewer. |
| [PhoneticGuide](../com.aspose.words/phoneticguide/) | Represents Phonetic Guide. |
| [PhysicalFontInfo](../com.aspose.words/physicalfontinfo/) | Specifies information about physical font available to Aspose.Words font engine. |
| [PlainTextDocument](../com.aspose.words/plaintextdocument/) | Allows to extract plain-text representation of the document's content. |
| [PreferredWidth](../com.aspose.words/preferredwidth/) | Represents a value and its unit of measure that is used to specify the preferred width of a table or a cell. |
| [PreferredWidthType](../com.aspose.words/preferredwidthtype/) | Specifies the unit of measurement for the preferred width of a table or cell. |
| [PresetTexture](../com.aspose.words/presettexture/) | Specifies texture to be used to fill a shape. |
| [PropertyType](../com.aspose.words/propertytype/) | Specifies data type of a document property. |
| [ProtectionType](../com.aspose.words/protectiontype/) | Protection type for a document. |
| [PsSaveOptions](../com.aspose.words/pssaveoptions/) | Can be used to specify additional options when saving a document into the [SaveFormat.\#PS](../com.aspose.words/saveformat/\#PS) format. |
| [Range](../com.aspose.words/range/) | Represents a contiguous area in a document. |
| [RelativeHorizontalPosition](../com.aspose.words/relativehorizontalposition/) | Specifies to what the horizontal position of a shape or text frame is relative. |
| [RelativeHorizontalSize](../com.aspose.words/relativehorizontalsize/) | Specifies relatively to what the width of a shape or a text frame is calculated horizontally. |
| [RelativeVerticalPosition](../com.aspose.words/relativeverticalposition/) | Specifies to what the vertical position of a shape or text frame is relative. |
| [RelativeVerticalSize](../com.aspose.words/relativeverticalsize/) | Specifies relatively to what the height of a shape or a text frame is calculated vertically. |
| [ReplaceAction](../com.aspose.words/replaceaction/) | Allows the user to specify what happens to the current match during a replace operation. |
| [ReplacingArgs](../com.aspose.words/replacingargs/) | Provides data for a custom replace operation. |
| [ReportBuildOptions](../com.aspose.words/reportbuildoptions/) | Specifies options controlling behavior of [ReportingEngine](../com.aspose.words/reportingengine/) while building a report. |
| [ReportingEngine](../com.aspose.words/reportingengine/) | Provides routines to populate template documents with data and a set of settings to control these routines. |
| [ResourceLoadingAction](../com.aspose.words/resourceloadingaction/) | Specifies the mode of resource loading. |
| [ResourceLoadingArgs](../com.aspose.words/resourceloadingargs/) | Provides data for the [IResourceLoadingCallback.\#resourceLoading(com.aspose.words.ResourceLoadingArgs)](../com.aspose.words/iresourceloadingcallback/\#resourceLoading-com.aspose.words.ResourceLoadingArgs) method. |
| [ResourceSavingArgs](../com.aspose.words/resourcesavingargs/) | Provides data for the [IResourceSavingCallback.\#resourceSaving(com.aspose.words.ResourceSavingArgs)](../com.aspose.words/iresourcesavingcallback/\#resourceSaving-com.aspose.words.ResourceSavingArgs) event. |
| [ResourceType](../com.aspose.words/resourcetype/) | Type of loaded resource. |
| [Revision](../com.aspose.words/revision/) | Represents a revision (tracked change) in a document node or style. |
| [RevisionCollection](../com.aspose.words/revisioncollection/) | A collection of [Revision](../com.aspose.words/revision/) objects that represent revisions in the document. |
| [RevisionColor](../com.aspose.words/revisioncolor/) | Allows to specify color of document revisions. |
| [RevisionGroup](../com.aspose.words/revisiongroup/) | Represents a group of sequential [Revision](../com.aspose.words/revision/) objects. |
| [RevisionGroupCollection](../com.aspose.words/revisiongroupcollection/) | A collection of [RevisionGroup](../com.aspose.words/revisiongroup/) objects that represent revision groups in the document. |
| [RevisionOptions](../com.aspose.words/revisionoptions/) | Allows to control how document revisions are handled during layout process. |
| [RevisionTextEffect](../com.aspose.words/revisiontexteffect/) | Allows to specify decoration effect for revisions of document text. |
| [RevisionType](../com.aspose.words/revisiontype/) | Specifies the type of change being tracked in [Revision](../com.aspose.words/revision/). |
| [RevisionsView](../com.aspose.words/revisionsview/) | Allows to specify whether to work with the original or revised version of a document. |
| [Row](../com.aspose.words/row/) | Represents a table row. |
| [RowCollection](../com.aspose.words/rowcollection/) | Provides typed access to a collection of [Row](../com.aspose.words/row/) nodes. |
| [RowFormat](../com.aspose.words/rowformat/) | Represents all formatting for a table row. |
| [RtfLoadOptions](../com.aspose.words/rtfloadoptions/) | Allows to specify additional options when loading [LoadFormat.\#RTF](../com.aspose.words/loadformat/\#RTF) document into a [Document](../com.aspose.words/document/) object. |
| [RtfSaveOptions](../com.aspose.words/rtfsaveoptions/) | Can be used to specify additional options when saving a document into the [SaveFormat.\#RTF](../com.aspose.words/saveformat/\#RTF) format. |
| [Run](../com.aspose.words/run/) | Represents a run of characters with the same font formatting. |
| [RunCollection](../com.aspose.words/runcollection/) | Provides typed access to a collection of [Run](../com.aspose.words/run/) nodes. |
| [SaveFormat](../com.aspose.words/saveformat/) | Indicates the format in which the document is saved. |
| [SaveOptions](../com.aspose.words/saveoptions/) | This is an abstract base class for classes that allow the user to specify additional options when saving a document into a particular format. |
| [SaveOutputParameters](../com.aspose.words/saveoutputparameters/) | This object is returned to the caller after a document is saved and contains additional information that has been generated or calculated during the save operation. |
| [ScriptShapingLevel](../com.aspose.words/scriptshapinglevel/) | Describes shaping levels required by a script. |
| [SdtAppearance](../com.aspose.words/sdtappearance/) | Specifies the appearance of a structured document tag. |
| [SdtCalendarType](../com.aspose.words/sdtcalendartype/) | Specifies the possible types of calendars which can be used to specify [StructuredDocumentTag.\#getCalendarType()](../com.aspose.words/structureddocumenttag/\#getCalendarType) / [StructuredDocumentTag.\#setCalendarType(int)](../com.aspose.words/structureddocumenttag/\#setCalendarType-int) in an Office Open XML document. |
| [SdtDateStorageFormat](../com.aspose.words/sdtdatestorageformat/) | Specifies how the date for a date SDT is stored/retrieved when the SDT is bound to an XML node in the document's data store. |
| [SdtListItem](../com.aspose.words/sdtlistitem/) | This element specifies a single list item within a parent [SdtType.\#COMBO\_BOX](../com.aspose.words/sdttype/\#COMBO-BOX) or [SdtType.\#DROP\_DOWN\_LIST](../com.aspose.words/sdttype/\#DROP-DOWN-LIST) structured document tag. |
| [SdtListItemCollection](../com.aspose.words/sdtlistitemcollection/) | Provides access to [SdtListItem](../com.aspose.words/sdtlistitem/) elements of a structured document tag. |
| [SdtType](../com.aspose.words/sdttype/) | Specifies the type of a structured document tag (SDT) node. |
| [Section](../com.aspose.words/section/) | Represents a single section in a document. |
| [SectionCollection](../com.aspose.words/sectioncollection/) | A collection of [Section](../com.aspose.words/section/) objects in the document. |
| [SectionLayoutMode](../com.aspose.words/sectionlayoutmode/) | Specifies the layout mode for a section allowing to define the document grid behavior. |
| [SectionStart](../com.aspose.words/sectionstart/) | The type of break at the beginning of the section. |
| [Shading](../com.aspose.words/shading/) | Contains shading attributes for an object. |
| [ShadowFormat](../com.aspose.words/shadowformat/) | Represents shadow formatting for an object. |
| [ShadowType](../com.aspose.words/shadowtype/) | Specifies the type of a shape shadow. |
| [Shape](../com.aspose.words/shape/) | Represents an object in the drawing layer, such as an AutoShape, textbox, freeform, OLE object, ActiveX control, or picture. |
| [ShapeBase](../com.aspose.words/shapebase/) | Base class for objects in the drawing layer, such as an AutoShape, freeform, OLE object, ActiveX control, or picture. |
| [ShapeLineStyle](../com.aspose.words/shapelinestyle/) | Specifies the compound line style of a [Shape](../com.aspose.words/shape/). |
| [ShapeMarkupLanguage](../com.aspose.words/shapemarkuplanguage/) | Specifies Markup language used for the shape. |
| [ShapeRenderer](../com.aspose.words/shaperenderer/) | Provides methods to render an individual [Shape](../com.aspose.words/shape/) or [GroupShape](../com.aspose.words/groupshape/) to a raster or vector image or to a Graphics object. |
| [ShapeType](../com.aspose.words/shapetype/) | Specifies the type of shape in a Microsoft Word document. |
| [ShowInBalloons](../com.aspose.words/showinballoons/) | Specifies which revisions are rendered in balloons. |
| [SignOptions](../com.aspose.words/signoptions/) | Allows to specify options for document signing. |
| [SignatureLine](../com.aspose.words/signatureline/) | Provides access to signature line properties. |
| [SignatureLineOptions](../com.aspose.words/signaturelineoptions/) | Allows to specify options for signature line being inserted. |
| [SmartTag](../com.aspose.words/smarttag/) | This element specifies the presence of a smart tag around one or more inline structures (runs, images, fields,etc.) within a paragraph. |
| [SpecialChar](../com.aspose.words/specialchar/) | Base class for special characters in the document. |
| [Story](../com.aspose.words/story/) | Base class for elements that contain block-level nodes [Paragraph](../com.aspose.words/paragraph/) and [Table](../com.aspose.words/table/). |
| [StoryType](../com.aspose.words/storytype/) | Text of a Word document is stored in stories. |
| [StreamFontSource](../com.aspose.words/streamfontsource/) | Base class for user-defined stream font source. |
| [Stroke](../com.aspose.words/stroke/) | Defines a stroke for a shape. |
| [StructuredDocumentTag](../com.aspose.words/structureddocumenttag/) | Represents a structured document tag (SDT or content control) in a document. |
| [StructuredDocumentTagCollection](../com.aspose.words/structureddocumenttagcollection/) | A collection of [IStructuredDocumentTag](../com.aspose.words/istructureddocumenttag/) instances that represent the structured document tags in the specified range. |
| [StructuredDocumentTagRangeEnd](../com.aspose.words/structureddocumenttagrangeend/) | Represents an end of **ranged** structured document tag which accepts multi-sections content. |
| [StructuredDocumentTagRangeStart](../com.aspose.words/structureddocumenttagrangestart/) | Represents a start of **ranged** structured document tag which accepts multi-sections content. |
| [Style](../com.aspose.words/style/) | Represents a single built-in or user-defined style. |
| [StyleCollection](../com.aspose.words/stylecollection/) | A collection of [Style](../com.aspose.words/style/) objects that represent both the built-in and user-defined styles in a document. |
| [StyleIdentifier](../com.aspose.words/styleidentifier/) | Locale independent style identifier. |
| [StyleType](../com.aspose.words/styletype/) | Represents type of the style. |
| [SubDocument](../com.aspose.words/subdocument/) | Represents a **SubDocument** \- which is a reference to an externally stored document. |
| [SvgSaveOptions](../com.aspose.words/svgsaveoptions/) | Can be used to specify additional options when saving a document into the [SaveFormat.\#SVG](../com.aspose.words/saveformat/\#SVG) format. |
| [SvgTextOutputMode](../com.aspose.words/svgtextoutputmode/) | Allows to specify how text inside a document should be rendered when saving in SVG format. |
| [SystemFontSource](../com.aspose.words/systemfontsource/) | Represents all TrueType fonts installed to the system. |
| [TabAlignment](../com.aspose.words/tabalignment/) | Specifies the alignment/type of a tab stop. |
| [TabLeader](../com.aspose.words/tableader/) | Specifies the type of the leader line displayed under the tab character. |
| [TabStop](../com.aspose.words/tabstop/) | Represents a single custom tab stop. |
| [TabStopCollection](../com.aspose.words/tabstopcollection/) | A collection of [TabStop](../com.aspose.words/tabstop/) objects that represent custom tabs for a paragraph or a style. |
| [Table](../com.aspose.words/table/) | Represents a table in a Word document. |
| [TableAlignment](../com.aspose.words/tablealignment/) | Specifies alignment for an inline table. |
| [TableCollection](../com.aspose.words/tablecollection/) | Provides typed access to a collection of [Table](../com.aspose.words/table/) nodes. |
| [TableContentAlignment](../com.aspose.words/tablecontentalignment/) | Allows to specify the alignment of the content of the table to be used when exporting into Markdown format. |
| [TableStyle](../com.aspose.words/tablestyle/) | Represents a table style. |
| [TableStyleOptions](../com.aspose.words/tablestyleoptions/) | Specifies how table style is applied to a table. |
| [TableSubstitutionRule](../com.aspose.words/tablesubstitutionrule/) | Table font substitution rule. |
| [TaskPane](../com.aspose.words/taskpane/) | Represents an add-in task pane object. |
| [TaskPaneCollection](../com.aspose.words/taskpanecollection/) | Specifies a list of persisted task pane objects. |
| [TaskPaneDockState](../com.aspose.words/taskpanedockstate/) | Enumerates available locations of task pane object. |
| [TextBox](../com.aspose.words/textbox/) | Defines attributes that specify how a text is displayed inside a shape. |
| [TextBoxAnchor](../com.aspose.words/textboxanchor/) | Specifies values used for shape text vertical alignment. |
| [TextBoxWrapMode](../com.aspose.words/textboxwrapmode/) | Specifies how text wraps inside a shape. |
| [TextColumn](../com.aspose.words/textcolumn/) | Represents a single text column. |
| [TextColumnCollection](../com.aspose.words/textcolumncollection/) | A collection of [TextColumn](../com.aspose.words/textcolumn/) objects that represent all the columns of text in a section of a document. |
| [TextDmlEffect](../com.aspose.words/textdmleffect/) | Dml text effect for text runs. |
| [TextEffect](../com.aspose.words/texteffect/) | Animation effect for text runs. |
| [TextFormFieldType](../com.aspose.words/textformfieldtype/) | Specifies the type of a text form field. |
| [TextOrientation](../com.aspose.words/textorientation/) | Specifies orientation of text on a page, in a table cell or a text frame. |
| [TextPath](../com.aspose.words/textpath/) | Defines the text and formatting of the text path (of a WordArt object). |
| [TextPathAlignment](../com.aspose.words/textpathalignment/) | WordArt alignment. |
| [TextWatermarkOptions](../com.aspose.words/textwatermarkoptions/) | Contains options that can be specified when adding a watermark with text. |
| [TextWrapping](../com.aspose.words/textwrapping/) | Specifies how text is wrapped around the table. |
| [TextureAlignment](../com.aspose.words/texturealignment/) | Specifies the alignment for the tiling of the texture fill. |
| [TextureIndex](../com.aspose.words/textureindex/) | Specifies shading texture. |
| [Theme](../com.aspose.words/theme/) | Represents document Theme, and provides access to main theme parts including [Theme.\#getMajorFonts()](../com.aspose.words/theme/\#getMajorFonts), [Theme.\#getMinorFonts()](../com.aspose.words/theme/\#getMinorFonts) and [Theme.\#getColors()](../com.aspose.words/theme/\#getColors) |
| [ThemeColor](../com.aspose.words/themecolor/) | Specifies the theme colors for document themes. |
| [ThemeColors](../com.aspose.words/themecolors/) | Represents the color scheme of the document theme which contains twelve colors. |
| [ThemeFont](../com.aspose.words/themefont/) | Specifies the types of theme font names for document themes. |
| [ThemeFonts](../com.aspose.words/themefonts/) | Represents a collection of fonts in the font scheme, allowing to specify different fonts for different languages [ThemeFonts.\#getLatin()](../com.aspose.words/themefonts/\#getLatin) / [ThemeFonts.\#setLatin(java.lang.String)](../com.aspose.words/themefonts/\#setLatin-java.lang.String), [ThemeFonts.\#getEastAsian()](../com.aspose.words/themefonts/\#getEastAsian) / [ThemeFonts.\#setEastAsian(java.lang.String)](../com.aspose.words/themefonts/\#setEastAsian-java.lang.String) and [ThemeFonts.\#getComplexScript()](../com.aspose.words/themefonts/\#getComplexScript) / [ThemeFonts.\#setComplexScript(java.lang.String)](../com.aspose.words/themefonts/\#setComplexScript-java.lang.String). |
| [ThumbnailGeneratingOptions](../com.aspose.words/thumbnailgeneratingoptions/) | Can be used to specify additional options when generating thumbnail for a document. |
| [TiffCompression](../com.aspose.words/tiffcompression/) | Specifies what type of compression to apply when saving page images into a TIFF file. |
| [ToaCategories](../com.aspose.words/toacategories/) | Represents a table of authorities categories. |
| [TxtExportHeadersFootersMode](../com.aspose.words/txtexportheadersfootersmode/) | Specifies the way headers and footers are exported to plain text format. |
| [TxtLeadingSpacesOptions](../com.aspose.words/txtleadingspacesoptions/) | Specifies available options for leading space handling during import from [LoadFormat.\#TEXT](../com.aspose.words/loadformat/\#TEXT) file. |
| [TxtListIndentation](../com.aspose.words/txtlistindentation/) | Specifies how list levels are indented when document is exporting to [SaveFormat.\#TEXT](../com.aspose.words/saveformat/\#TEXT) format. |
| [TxtLoadOptions](../com.aspose.words/txtloadoptions/) | Allows to specify additional options when loading [LoadFormat.\#TEXT](../com.aspose.words/loadformat/\#TEXT) document into a [Document](../com.aspose.words/document/) object. |
| [TxtSaveOptions](../com.aspose.words/txtsaveoptions/) | Can be used to specify additional options when saving a document into the [SaveFormat.\#TEXT](../com.aspose.words/saveformat/\#TEXT) format. |
| [TxtSaveOptionsBase](../com.aspose.words/txtsaveoptionsbase/) | The base class for specifying additional options when saving a document into a text based formats. |
| [TxtTrailingSpacesOptions](../com.aspose.words/txttrailingspacesoptions/) | Specifies available options for trailing spaces handling during import from [LoadFormat.\#TEXT](../com.aspose.words/loadformat/\#TEXT) file. |
| [Underline](../com.aspose.words/underline/) | Indicates type of the underline applied to a font. |
| [UnicodeScript](../com.aspose.words/unicodescript/) | Unicode Character Database property: Script (sc). |
| [UnsupportedFileFormatException](../com.aspose.words/unsupportedfileformatexception/) | Thrown during document load, when the document format is not recognized or not supported by Aspose.Words. |
| [UserInformation](../com.aspose.words/userinformation/) | Specifies information about the user. |
| [VariableCollection](../com.aspose.words/variablecollection/) | A collection of document variables. |
| [VbaModule](../com.aspose.words/vbamodule/) | Provides access to VBA project module. |
| [VbaModuleCollection](../com.aspose.words/vbamodulecollection/) | Represents a collection of [VbaModule](../com.aspose.words/vbamodule/) objects. |
| [VbaModuleType](../com.aspose.words/vbamoduletype/) | Specifies the type of a model in a VBA project. |
| [VbaProject](../com.aspose.words/vbaproject/) | Provides access to VBA project information. |
| [VbaReference](../com.aspose.words/vbareference/) | Implements a reference to an Automation type library or VBA project. |
| [VbaReferenceCollection](../com.aspose.words/vbareferencecollection/) | Represents a collection of [VbaReference](../com.aspose.words/vbareference/) objects. |
| [VbaReferenceType](../com.aspose.words/vbareferencetype/) | Allows to specify the type of a [VbaReference](../com.aspose.words/vbareference/) object. |
| [VerticalAlignment](../com.aspose.words/verticalalignment/) | Specifies vertical alignment of a floating shape, text frame or a floating table. |
| [ViewOptions](../com.aspose.words/viewoptions/) | Provides various options that control how a document is shown in Microsoft Word. |
| [ViewType](../com.aspose.words/viewtype/) | Possible values for the view mode in Microsoft Word. |
| [VisitorAction](../com.aspose.words/visitoraction/) | Allows the visitor to control the enumeration of nodes. |
| [WarningInfo](../com.aspose.words/warninginfo/) | Contains information about a warning that Aspose.Words issued during document loading or saving. |
| [WarningInfoCollection](../com.aspose.words/warninginfocollection/) | Represents a typed collection of [WarningInfo](../com.aspose.words/warninginfo/) objects. |
| [WarningSource](../com.aspose.words/warningsource/) | Specifies the module that produces a warning during document loading or saving. |
| [WarningType](../com.aspose.words/warningtype/) | Specifies the type of a warning that is issued by Aspose.Words during document loading or saving. |
| [Watermark](../com.aspose.words/watermark/) | Represents class to work with document watermark. |
| [WatermarkLayout](../com.aspose.words/watermarklayout/) | Defines layout of the watermark relative to the watermark center. |
| [WatermarkType](../com.aspose.words/watermarktype/) | Specifies the watermark type. |
| [WebExtension](../com.aspose.words/webextension/) | Represents a web extension object. |
| [WebExtensionBinding](../com.aspose.words/webextensionbinding/) | Specifies a binding relationship between a web extension and the data in the document. |
| [WebExtensionBindingCollection](../com.aspose.words/webextensionbindingcollection/) | Specifies a list of web extension bindings. |
| [WebExtensionBindingType](../com.aspose.words/webextensionbindingtype/) | Enumerates available types of binding between a web extension and the data in the document. |
| [WebExtensionProperty](../com.aspose.words/webextensionproperty/) | Specifies a web extension custom property. |
| [WebExtensionPropertyCollection](../com.aspose.words/webextensionpropertycollection/) | Specifies a set of web extension custom properties. |
| [WebExtensionReference](../com.aspose.words/webextensionreference/) | Represents the reference to a web extension. |
| [WebExtensionReferenceCollection](../com.aspose.words/webextensionreferencecollection/) | Specifies a list of web extension references. |
| [WebExtensionStoreType](../com.aspose.words/webextensionstoretype/) | Enumerates available types of a web extension store. |
| [WordML2003SaveOptions](../com.aspose.words/wordml2003saveoptions/) | Can be used to specify additional options when saving a document into the [SaveFormat.\#WORD\_ML](../com.aspose.words/saveformat/\#WORD-ML) format. |
| [WrapSide](../com.aspose.words/wrapside/) | Specifies what side(s) of the shape or picture the text wraps around. |
| [WrapType](../com.aspose.words/wraptype/) | Specifies how text is wrapped around a shape or picture. |
| [WriteProtection](../com.aspose.words/writeprotection/) | Specifies write protection settings for a document. |
| [X509Certificate2Wrapper](../com.aspose.words/x509certificate2wrapper/) | JAVA-added public wrapper around ours internal X509Certificate2. |
| [XamlFixedSaveOptions](../com.aspose.words/xamlfixedsaveoptions/) | Can be used to specify additional options when saving a document into the [SaveFormat.\#XAML\_FIXED](../com.aspose.words/saveformat/\#XAML-FIXED) format. |
| [XamlFlowSaveOptions](../com.aspose.words/xamlflowsaveoptions/) | Can be used to specify additional options when saving a document into the [SaveFormat.\#XAML\_FLOW](../com.aspose.words/saveformat/\#XAML-FLOW) or [SaveFormat.\#XAML\_FLOW\_PACK](../com.aspose.words/saveformat/\#XAML-FLOW-PACK) format. |
| [XlsxSaveOptions](../com.aspose.words/xlsxsaveoptions/) | Can be used to specify additional options when saving a document into the [SaveFormat.\#XLSX](../com.aspose.words/saveformat/\#XLSX) format. |
| [XlsxSectionMode](../com.aspose.words/xlsxsectionmode/) | Specifies how sections are handled when saving a document in the XLSX format. |
| [XmlDataLoadOptions](../com.aspose.words/xmldataloadoptions/) | Represents options for XML data loading. |
| [XmlDataSource](../com.aspose.words/xmldatasource/) | Provides access to data of an XML file or stream to be used within a report. |
| [XmlMapping](../com.aspose.words/xmlmapping/) | Specifies the information that is used to establish a mapping between the parent structured document tag and an XML element stored within a custom XML data part in the document. |
| [XpsSaveOptions](../com.aspose.words/xpssaveoptions/) | Can be used to specify additional options when saving a document into the [SaveFormat.\#XPS](../com.aspose.words/saveformat/\#XPS) format. |
| [ZoomType](../com.aspose.words/zoomtype/) | Possible values for how large or small the document appears on the screen in Microsoft Word. |

## Interfaces

| Interface | Description |
| --- | --- |
| [IBarcodeGenerator](../com.aspose.words/ibarcodegenerator/) | Public interface for barcode custom generator. |
| [IBibliographyStylesProvider](../com.aspose.words/ibibliographystylesprovider/) | Implement this interface to provide bibliography style for the [FieldBibliography](../com.aspose.words/fieldbibliography/) and [FieldCitation](../com.aspose.words/fieldcitation/) fields when they're updated. |
| [IChartDataPoint](../com.aspose.words/ichartdatapoint/) | Contains properties of a single data point on the chart. |
| [IComparisonExpressionEvaluator](../com.aspose.words/icomparisonexpressionevaluator/) | When implemented, allows to override default comparison expressions evaluation for the [FieldIf](../com.aspose.words/fieldif/) and [FieldCompare](../com.aspose.words/fieldcompare/) fields. |
| [ICssSavingCallback](../com.aspose.words/icsssavingcallback/) | Implement this interface if you want to control how Aspose.Words saves CSS (Cascading Style Sheet) when saving a document to HTML. |
| [IDocumentConverterPlugin](../com.aspose.words/idocumentconverterplugin/) | Defines an interface for external converter plugin. |
| [IDocumentLoadingCallback](../com.aspose.words/idocumentloadingcallback/) | Implement this interface if you want to have your own custom method called during loading a document. |
| [IDocumentMergerPlugin](../com.aspose.words/idocumentmergerplugin/) | Defines an interface for external merger plugin that can merge Pdf documents. |
| [IDocumentPartSavingCallback](../com.aspose.words/idocumentpartsavingcallback/) | Implement this interface if you want to receive notifications and control how Aspose.Words saves document parts when exporting a document to [SaveFormat.\#HTML](../com.aspose.words/saveformat/\#HTML) or [SaveFormat.\#EPUB](../com.aspose.words/saveformat/\#EPUB) format. |
| [IDocumentReaderPlugin](../com.aspose.words/idocumentreaderplugin/) | Defines an interface for external reader plugins that can read a file into a document. |
| [IDocumentSavingCallback](../com.aspose.words/idocumentsavingcallback/) | Implement this interface if you want to have your own custom method called during saving a document. |
| [IFieldDatabaseProvider](../com.aspose.words/ifielddatabaseprovider/) | Implement this interface to provide data for the [FieldDatabase](../com.aspose.words/fielddatabase/) field when it's updated. |
| [IFieldMergingCallback](../com.aspose.words/ifieldmergingcallback/) | Implement this interface if you want to control how data is inserted into merge fields during a mail merge operation. |
| [IFieldResultFormatter](../com.aspose.words/ifieldresultformatter/) | Implement this interface if you want to control how the field result is formatted. |
| [IFieldUpdateCultureProvider](../com.aspose.words/ifieldupdatecultureprovider/) | When implemented, provides a [CultureInfo](../com.aspose.words.net.system.globalization/cultureinfo/) object that should be used during the update of a particular field. |
| [IFieldUpdatingCallback](../com.aspose.words/ifieldupdatingcallback/) | Implement this interface if you want to have your own custom methods called during a field update. |
| [IFieldUpdatingProgressCallback](../com.aspose.words/ifieldupdatingprogresscallback/) | Implement this interface if you want to track field updating progress. |
| [IFieldUserPromptRespondent](../com.aspose.words/ifielduserpromptrespondent/) | Represents the respondent to user prompts during field update. |
| [IFontSavingCallback](../com.aspose.words/ifontsavingcallback/) | Implement this interface if you want to receive notifications and control how Aspose.Words saves fonts when exporting a document to HTML format. |
| [IHyphenationCallback](../com.aspose.words/ihyphenationcallback/) | Implemented by classes which can register hyphenation dictionaries. |
| [IImageSavingCallback](../com.aspose.words/iimagesavingcallback/) | Implement this interface if you want to control how Aspose.Words saves images when saving a document to HTML. |
| [IMailMergeCallback](../com.aspose.words/imailmergecallback/) | Implement this interface if you want to receive notifications while mail merge is performed. |
| [IMailMergeDataSource](../com.aspose.words/imailmergedatasource/) | Implement this interface to allow mail merge from a custom data source, such as a list of objects. |
| [IMailMergeDataSourceRoot](../com.aspose.words/imailmergedatasourceroot/) | Implement this interface to allow mail merge from a custom data source with master-detail data. |
| [INodeChangingCallback](../com.aspose.words/inodechangingcallback/) | Implement this interface if you want to receive notifications when nodes are inserted or removed in the document. |
| [IPageLayoutCallback](../com.aspose.words/ipagelayoutcallback/) | Implement this interface if you want to have your own custom method called during build and rendering of page layout model. |
| [IPageSavingCallback](../com.aspose.words/ipagesavingcallback/) | Implement this interface if you want to control how Aspose.Words saves separate pages when saving a document to fixed page formats. |
| [IReplacingCallback](../com.aspose.words/ireplacingcallback/) | Implement this interface if you want to have your own custom method called during a find and replace operation. |
| [IResourceLoadingCallback](../com.aspose.words/iresourceloadingcallback/) | Implement this interface if you want to control how Aspose.Words loads external resource when importing a document and inserting images using [DocumentBuilder](../com.aspose.words/documentbuilder/). |
| [IResourceSavingCallback](../com.aspose.words/iresourcesavingcallback/) | Implement this interface if you want to control how Aspose.Words saves external resources (images, fonts and css) when saving a document to fixed page HTML or SVG. |
| [IRevisionCriteria](../com.aspose.words/irevisioncriteria/) | Implement this interface if you want to control when certain [Revision](../com.aspose.words/revision/) should be accepted/rejected or not by the [RevisionCollection.\#accept(com.aspose.words.IRevisionCriteria)](../com.aspose.words/revisioncollection/\#accept-com.aspose.words.IRevisionCriteria)/ [RevisionCollection.\#reject(com.aspose.words.IRevisionCriteria)](../com.aspose.words/revisioncollection/\#reject-com.aspose.words.IRevisionCriteria) methods. |
| [IStructuredDocumentTag](../com.aspose.words/istructureddocumenttag/) | Interface to define a common data for [StructuredDocumentTag](../com.aspose.words/structureddocumenttag/) and [StructuredDocumentTagRangeStart](../com.aspose.words/structureddocumenttagrangestart/). |
| [ITextShaper](../com.aspose.words/itextshaper/) | Provides methods for text shaping. |
| [ITextShaperFactory](../com.aspose.words/itextshaperfactory/) | An interface of a factory for constructing [ITextShaper](../com.aspose.words/itextshaper/) implementations. |
| [IWarningCallback](../com.aspose.words/iwarningcallback/) | Implement this interface if you want to have your own custom method called to capture loss of fidelity warnings that can occur during document loading or saving. |
