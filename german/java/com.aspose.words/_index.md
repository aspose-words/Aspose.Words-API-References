---
title: "com.aspose.words"
linktitle: "com.aspose.words"
second_title: "Aspose.Words für Java"
description: "Das com.aspose.words‑Paket stellt Klassen zum Erzeugen, Konvertieren, Modifizieren, Rendern und Drucken von Microsoft‑Word‑Dokumenten bereit, ohne Microsoft Word in Java zu verwenden."
type: docs
weight: 10
url: /de/java/com.aspose.words/
---


Das **com.aspose.words**‑Paket stellt Klassen zum Erzeugen, Konvertieren, Modifizieren, Rendern und Drucken von Microsoft‑Word‑Dokumenten bereit, ohne Microsoft Word zu verwenden.

Aspose.Words ist vollständig in Java geschrieben. Microsoft Word ist nicht erforderlich, um Aspose.Words zu verwenden.

Die Klassen im **com.aspose.words**‑Paket übernehmen bewährte Praktiken aus zwei bekannten Frameworks: Microsoft Word Automation und System.Xml. Ein Dokument in Aspose.Words wird durch einen Knotenbaum repräsentiert, ähnlich dem XML‑DOM. Wo möglich, stimmen Klassen‑, Methoden‑ und Eigenschaftsnamen mit denen der Microsoft Word Automation überein.

Die wichtigsten Klassen in diesem Namespace sind:

 *  **Document** is the main class of the object model that represents a Microsoft Word document.
 *  **DocumentBuilder** provides an easy way to insert content and formatting into a document.
 *  **Node** is the base class for all nodes in the document.
 *  **CompositeNode** is the base class for all nodes of the document that can contain other nodes, for example **Paragraph**, **Section** and **Table** and .

Das **com.aspose.words**‑Paket enthält außerdem Klassen, die die Reporting‑Engine von Aspose.Words bilden. Die Reporting‑Engine ermöglicht es, Dokumente, die in Microsoft Word entworfen wurden, schnell und einfach mit Daten aus verschiedenen Datenquellen wie **java.sql.ResultSet**, **array of ResultSets**, **com.aspose.words.net.System.Data.DataSet** oder einem **array of values** zu füllen.

Das **MailMerge**‑Objekt, das Zugriff auf die Reporting‑Funktionalität bietet, ist über die **Document.MailMerge**‑Eigenschaft verfügbar.


## Klassen

| Klasse | Beschreibung |
| --- | --- |
| [AbsolutePositionTab](../com.aspose.words/absolutepositiontab/) | Ein Tabulator mit absoluter Position ist ein Zeichen, das verwendet wird, um die Position in der aktuellen Textzeile beim Anzeigen dieses WordprocessingML‑Inhalts voranzuschieben. |
| [Adjustment](../com.aspose.words/adjustment/) | Stellt Anpassungswerte dar, die auf die angegebene Form angewendet werden. |
| [AdjustmentCollection](../com.aspose.words/adjustmentcollection/) | Stellt eine schreibgeschützte Sammlung von [Adjustment](../com.aspose.words/adjustment/) Anpassungswerten dar, die auf die angegebene Form angewendet werden. |
| [AdvancedCompareOptions](../com.aspose.words/advancedcompareoptions/) | Ermöglicht das Festlegen erweiterter Vergleichsoptionen. |
| [AiModel](../com.aspose.words/aimodel/) | Eine abstrakte Klasse, die die Integration verschiedener KI‑Modelle innerhalb von Aspose.Words darstellt. |
| [AiModelType](../com.aspose.words/aimodeltype/) | Stellt die Typen von [AiModel](../com.aspose.words/aimodel/) dar, die in den Dokumenten‑Verarbeitungs‑Workflow integriert werden können. |
| [AnthropicAiModel](../com.aspose.words/anthropicaimodel/) | Eine abstrakte Klasse, die die Integration mit Anthropic\u2019s KI‑Modellen innerhalb von Aspose.Words darstellt. |
| [ArrowLength](../com.aspose.words/arrowlength/) | Länge des Pfeils am Ende einer Linie. |
| [ArrowType](../com.aspose.words/arrowtype/) | Gibt den Typ eines Pfeils am Zeilenende an. |
| [ArrowWidth](../com.aspose.words/arrowwidth/) | Breite des Pfeils am Ende einer Linie. |
| [AsposeWordsPrintDocument](../com.aspose.words/asposewordsprintdocument/) | Stellt eine Standardimplementierung für das Drucken eines [Document](../com.aspose.words/document/) im Java-Druckframework bereit. |
| [AutoFitBehavior](../com.aspose.words/autofitbehavior/) | Bestimmt, wie Aspose.Words die Tabelle skaliert, wenn Sie die Methode **M:Aspose.Words.Tables.Table.AutoFit(Aspose.Words.Tables.AutoFitBehavior)** aufrufen. |
| [AxisBound](../com.aspose.words/axisbound/) | Stellt den minimalen oder maximalen Grenzwert von Achsenwerten dar. |
| [AxisBuiltInUnit](../com.aspose.words/axisbuiltinunit/) | Gibt die Anzeigeeinheiten für eine Achse an. |
| [AxisCategoryType](../com.aspose.words/axiscategorytype/) | Gibt den Typ einer Kategorieachse an. |
| [AxisCrosses](../com.aspose.words/axiscrosses/) | Gibt die möglichen Schnittpunkte für eine Achse an. |
| [AxisDisplayUnit](../com.aspose.words/axisdisplayunit/) | Stellt Zugriff auf die Skalierungsoptionen der Anzeigeeinheiten für die Werteachse bereit. |
| [AxisGroup](../com.aspose.words/axisgroup/) | Stellt einen Typ einer Diagrammachsgruppe dar. |
| [AxisScaleType](../com.aspose.words/axisscaletype/) | Gibt die möglichen Skalierungstypen für eine Achse an. |
| [AxisScaling](../com.aspose.words/axisscaling/) | Stellt die Skalierungsoptionen der Achse dar. |
| [AxisTickLabelPosition](../com.aspose.words/axisticklabelposition/) | Gibt die möglichen Positionen für Achsenbeschriftungen an. |
| [AxisTickLabels](../com.aspose.words/axisticklabels/) | Stellt Eigenschaften von Achsenmarkierungsbeschriftungen dar. |
| [AxisTickMark](../com.aspose.words/axistickmark/) | Gibt die möglichen Positionen für Achsenmarkierungen an. |
| [AxisTimeUnit](../com.aspose.words/axistimeunit/) | Gibt die Zeiteinheit für Achsen an. |
| [BarcodeParameters](../com.aspose.words/barcodeparameters/) | Containerklasse für Barcode-Parameter, die an BarcodeGenerator weitergereicht werden. |
| [BaseWebExtensionCollection](../com.aspose.words/basewebextensioncollection/) | Basisklasse für die Sammlungen [TaskPaneCollection](../com.aspose.words/taskpanecollection/), [WebExtensionBindingCollection](../com.aspose.words/webextensionbindingcollection/), [WebExtensionPropertyCollection](../com.aspose.words/webextensionpropertycollection/) und [WebExtensionReferenceCollection](../com.aspose.words/webextensionreferencecollection/). |
| [BaselineAlignment](../com.aspose.words/baselinealignment/) | Gibt die vertikale Position von Schriftarten in einer Zeile an. |
| [BasicTextShaperCache](../com.aspose.words/basictextshapercache/) | Implementiert einen einfachen Cache für [ITextShaper](../com.aspose.words/itextshaper/)-Instanzen. |
| [Bibliography](../com.aspose.words/bibliography/) | Stellt die Liste der im Dokument verfügbaren Bibliografienquellen dar. |
| [BlockImportMode](../com.aspose.words/blockimportmode/) | Gibt an, wie Eigenschaften von Block‑Elementen aus HTML‑basierten Dokumenten importiert werden. |
| [Body](../com.aspose.words/body/) | Stellt einen Container für den Haupttext eines Abschnitts dar. |
| [Bookmark](../com.aspose.words/bookmark/) | Stellt ein einzelnes Lesezeichen dar. |
| [BookmarkCollection](../com.aspose.words/bookmarkcollection/) | Eine Sammlung von [Bookmark](../com.aspose.words/bookmark/) Objekten, die die Lesezeichen im angegebenen Bereich darstellen. |
| [BookmarkEnd](../com.aspose.words/bookmarkend/) | Stellt das Ende eines Lesezeichens in einem Word-Dokument dar. |
| [BookmarkStart](../com.aspose.words/bookmarkstart/) | Stellt den Anfang eines Lesezeichens in einem Word-Dokument dar. |
| [BookmarksOutlineLevelCollection](../com.aspose.words/bookmarksoutlinelevelcollection/) | Eine Sammlung von einzelnen Lesezeichen-Gliederungsebenen. |
| [Border](../com.aspose.words/border/) | Stellt einen Rahmen eines Objekts dar. |
| [BorderCollection](../com.aspose.words/bordercollection/) | Eine Sammlung von [Border](../com.aspose.words/border/) Objekten. |
| [BorderType](../com.aspose.words/bordertype/) | Gibt die Seiten eines Rahmens an. |
| [BreakType](../com.aspose.words/breaktype/) | Gibt den Typ eines Umbruchs innerhalb eines Dokuments an. |
| [BubbleSizeCollection](../com.aspose.words/bubblesizecollection/) | Stellt eine Sammlung von Blasengrößen für eine Diagrammreihe dar. |
| [BuildVersionInfo](../com.aspose.words/buildversioninfo/) | Stellt Informationen über den aktuellen Produktnamen und die Version bereit. |
| [BuildingBlock](../com.aspose.words/buildingblock/) | Stellt einen Glossareintrag im Dokument dar, wie z. B. ein Building Block, AutoText oder einen AutoCorrect‑Eintrag. |
| [BuildingBlockBehavior](../com.aspose.words/buildingblockbehavior/) | Gibt das Verhalten an, das auf den Inhalt des Building Blocks angewendet werden soll, wenn er in das Hauptdokument eingefügt wird. |
| [BuildingBlockCollection](../com.aspose.words/buildingblockcollection/) | Eine Sammlung von [BuildingBlock](../com.aspose.words/buildingblock/) Objekten im Dokument. |
| [BuildingBlockGallery](../com.aspose.words/buildingblockgallery/) | Gibt die vordefinierte Galerie an, in die ein Building Block klassifiziert wird. |
| [BuildingBlockType](../com.aspose.words/buildingblocktype/) | Gibt einen Building Block‑Typ an. |
| [BuiltInDocumentProperties](../com.aspose.words/builtindocumentproperties/) | Eine Sammlung von integrierten Dokumenteigenschaften. |
| [CalendarType](../com.aspose.words/calendartype/) | Gibt den Typ eines Kalenders an. |
| [Cell](../com.aspose.words/cell/) | Stellt eine Tabellenzelle dar. |
| [CellCollection](../com.aspose.words/cellcollection/) | Bietet typisierten Zugriff auf eine Sammlung von [Cell](../com.aspose.words/cell/) Knoten. |
| [CellFormat](../com.aspose.words/cellformat/) | Stellt alle Formatierungen für eine Tabellenzelle dar. |
| [CellMerge](../com.aspose.words/cellmerge/) | Gibt an, wie eine Zelle in einer Tabelle mit anderen Zellen zusammengeführt wird. |
| [CellVerticalAlignment](../com.aspose.words/cellverticalalignment/) | Gibt die vertikale Ausrichtung des Textes in einer Tabellenzelle an. |
| [CertificateHolder](../com.aspose.words/certificateholder/) | Stellt einen Halter einer **X509Certificate2**-Instanz dar. |
| [ChapterPageSeparator](../com.aspose.words/chapterpageseparator/) | Definiert das Trennzeichen, das zwischen Kapitel- und Seitenzahl erscheint. |
| [Chart](../com.aspose.words/chart/) | Stellt Zugriff auf die Eigenschaften der Diagrammform bereit. |
| [ChartAxis](../com.aspose.words/chartaxis/) | Stellt die Achsenoptionen des Diagramms dar. |
| [ChartAxisCollection](../com.aspose.words/chartaxiscollection/) | Stellt eine Sammlung von Diagrammachsen dar. |
| [ChartAxisTitle](../com.aspose.words/chartaxistitle/) | Stellt Zugriff auf die Eigenschaften des Achsentitels bereit. |
| [ChartAxisType](../com.aspose.words/chartaxistype/) | Gibt den Typ der Diagrammachse an. |
| [ChartDataLabel](../com.aspose.words/chartdatalabel/) | Stellt eine Datenbeschriftung an einem Diagrammpunkt oder einer Trendlinie dar. |
| [ChartDataLabelCollection](../com.aspose.words/chartdatalabelcollection/) | Stellt eine Sammlung von [ChartDataLabel](../com.aspose.words/chartdatalabel/) dar. |
| [ChartDataLabelLocationMode](../com.aspose.words/chartdatalabellocationmode/) | Gibt an, wie die Werte \\u200b\\u200bdie die Position einer Datenbeschriftung festlegen - die [ChartDataLabel.#getLeft()](../com.aspose.words/chartdatalabel/#getLeft) / [ChartDataLabel.#setLeft(double)](../com.aspose.words/chartdatalabel/#setLeft-double) und [ChartDataLabel.#getTop()](../com.aspose.words/chartdatalabel/#getTop) / [ChartDataLabel.#setTop(double)](../com.aspose.words/chartdatalabel/#setTop-double) Eigenschaften - interpretiert werden. |
| [ChartDataLabelPosition](../com.aspose.words/chartdatalabelposition/) | Gibt die Position für eine Diagrammdatenbeschriftung an. |
| [ChartDataPoint](../com.aspose.words/chartdatapoint/) | Ermöglicht die Angabe der Formatierung eines einzelnen Datenpunkts im Diagramm. |
| [ChartDataPointCollection](../com.aspose.words/chartdatapointcollection/) | Stellt eine Sammlung von [ChartDataPoint](../com.aspose.words/chartdatapoint/) dar. |
| [ChartDataTable](../com.aspose.words/chartdatatable/) | Ermöglicht die Angabe von Eigenschaften einer Diagrammdatentabelle. |
| [ChartFormat](../com.aspose.words/chartformat/) | Stellt die Formatierung eines Diagrammelements dar. |
| [ChartLegend](../com.aspose.words/chartlegend/) | Stellt die Eigenschaften der Diagrammlegende dar. |
| [ChartLegendEntry](../com.aspose.words/chartlegendentry/) | Stellt einen Eintrag der Diagrammlegende dar. |
| [ChartLegendEntryCollection](../com.aspose.words/chartlegendentrycollection/) | Stellt eine Sammlung von Einträgen der Diagrammlegende dar. |
| [ChartMarker](../com.aspose.words/chartmarker/) | Stellt einen Diagrammdatenmarker dar. |
| [ChartMultilevelValue](../com.aspose.words/chartmultilevelvalue/) | Stellt einen Wert für Diagramme dar, die mehrstufige Daten anzeigen. |
| [ChartNumberFormat](../com.aspose.words/chartnumberformat/) | Stellt die Zahlenformatierung des übergeordneten Elements dar. |
| [ChartSeries](../com.aspose.words/chartseries/) | Stellt die Eigenschaften von Diagrammserien dar. |
| [ChartSeriesCollection](../com.aspose.words/chartseriescollection/) | Stellt eine Sammlung von [ChartSeries](../com.aspose.words/chartseries/) dar. |
| [ChartSeriesGroup](../com.aspose.words/chartseriesgroup/) | Stellt die Eigenschaften einer Diagrammseriengruppe dar, d.h. die Eigenschaften von Diagrammserien desselben Typs, die den gleichen Achsen zugeordnet sind. |
| [ChartSeriesGroupCollection](../com.aspose.words/chartseriesgroupcollection/) | Stellt eine Sammlung von [ChartSeriesGroup](../com.aspose.words/chartseriesgroup/) Objekten dar. |
| [ChartSeriesType](../com.aspose.words/chartseriestype/) | Gibt den Typ einer Diagrammserie an. |
| [ChartShapeType](../com.aspose.words/chartshapetype/) | Gibt den Formtyp von Diagrammelementen an. |
| [ChartStyle](../com.aspose.words/chartstyle/) | Gibt vordefinierte Stile eines Diagramms an. |
| [ChartTitle](../com.aspose.words/charttitle/) | Stellt Zugriff auf die Eigenschaften des Diagrammtitels bereit. |
| [ChartType](../com.aspose.words/charttype/) | Gibt den Typ eines Diagramms an. |
| [ChartXValue](../com.aspose.words/chartxvalue/) | Stellt einen X-Wert für eine Diagrammserie dar. |
| [ChartXValueCollection](../com.aspose.words/chartxvaluecollection/) | Stellt eine Sammlung von X-Werten für eine Diagrammserie dar. |
| [ChartXValueType](../com.aspose.words/chartxvaluetype/) | Ermöglicht die Angabe des Typs eines X-Werts einer Diagrammserie. |
| [ChartYValue](../com.aspose.words/chartyvalue/) | Stellt einen Y-Wert für eine Diagrammserie dar. |
| [ChartYValueCollection](../com.aspose.words/chartyvaluecollection/) | Stellt eine Sammlung von Y-Werten für eine Diagrammserie dar. |
| [ChartYValueType](../com.aspose.words/chartyvaluetype/) | Ermöglicht die Angabe des Typs eines Y-Werts einer Diagrammserie. |
| [CheckBoxControl](../com.aspose.words/checkboxcontrol/) | Das CheckBox-Steuerelement schaltet einen Wert um. |
| [CheckGrammarOptions](../com.aspose.words/checkgrammaroptions/) | Ermöglicht die Angabe verschiedener Optionen beim Überprüfen der Grammatik eines Dokuments mit KI. |
| [ChmLoadOptions](../com.aspose.words/chmloadoptions/) | Ermöglicht die Angabe zusätzlicher Optionen beim Laden eines CHM-Dokuments in ein [Document](../com.aspose.words/document/)‑Objekt. |
| [CleanupOptions](../com.aspose.words/cleanupoptions/) | Ermöglicht die Angabe von Optionen für die Dokumentenreinigung. |
| [Cluster](../com.aspose.words/cluster/) | Kapselt Codepunkte und Glyphen, die ein Graphem bilden. |
| [ColorMode](../com.aspose.words/colormode/) | Gibt an, wie Farben gerendert werden. |
| [ColorPrintMode](../com.aspose.words/colorprintmode/) | Gibt an, wie nichtfarbige Seiten gedruckt werden, wenn das Gerät Farbdruck unterstützt. |
| [CommandButtonControl](../com.aspose.words/commandbuttoncontrol/) | Das CommandButton-Steuerelement führt ein Makro aus, das eine Aktion ausführt, wenn ein Benutzer darauf klickt. |
| [Comment](../com.aspose.words/comment/) | Stellt einen Container für den Text eines Kommentars dar. |
| [CommentCollection](../com.aspose.words/commentcollection/) | Stellt typisierten Zugriff auf eine Sammlung von [Comment](../com.aspose.words/comment/)‑Knoten bereit. |
| [CommentDisplayMode](../com.aspose.words/commentdisplaymode/) | Gibt den Rendermodus für Dokumentkommentare an. |
| [CommentRangeEnd](../com.aspose.words/commentrangeend/) | Bezeichnet das Ende eines Textbereichs, dem ein Kommentar zugeordnet ist. |
| [CommentRangeStart](../com.aspose.words/commentrangestart/) | Bezeichnet den Anfang eines Textbereichs, dem ein Kommentar zugeordnet ist. |
| [CompareOptions](../com.aspose.words/compareoptions/) | Ermöglicht die Auswahl zusätzlicher Optionen für den Dokumentvergleichsvorgang. |
| [Comparer](../com.aspose.words/comparer/) | Stellt Methoden zum Vergleich von Dokumenten bereit. |
| [ComparerContext](../com.aspose.words/comparercontext/) | Dokumentvergleichskontext |
| [ComparisonEvaluationResult](../com.aspose.words/comparisonevaluationresult/) | Das Ergebnis der Vergleichsauswertung. |
| [ComparisonExpression](../com.aspose.words/comparisonexpression/) | Der Vergleichsausdruck. |
| [ComparisonTargetType](../com.aspose.words/comparisontargettype/) | Ermöglicht das Angeben des Basisdokuments, das während des Vergleichs verwendet wird. |
| [Compatibility](../com.aspose.words/compatibility/) | Gibt die Namen der Kompatibilitätsoptionen an. |
| [CompatibilityOptions](../com.aspose.words/compatibilityoptions/) | Enthält Kompatibilitätsoptionen (das heißt, die vom Benutzer auf dem **Compatibility**‑Tab des **Options**‑Dialogs in Microsoft Word eingegebenen Einstellungen). |
| [CompositeNode](../com.aspose.words/compositenode/) | Basisklasse für Knoten, die andere Knoten enthalten können. |
| [CompressionLevel](../com.aspose.words/compressionlevel/) | Komprimierungsstufe für OOXML- und XPS-Dateien. |
| [ConditionalStyle](../com.aspose.words/conditionalstyle/) | Stellt spezielle Formatierung dar, die auf einen Bereich einer Tabelle mit zugewiesenem Tabellenstil angewendet wird. |
| [ConditionalStyleCollection](../com.aspose.words/conditionalstylecollection/) | Stellt eine Sammlung von [ConditionalStyle](../com.aspose.words/conditionalstyle/)‑Objekten dar. |
| [ConditionalStyleType](../com.aspose.words/conditionalstyletype/) | Stellt mögliche Tabellenbereiche dar, für die bedingte Formatierung in einem Tabellenstil definiert werden kann. |
| [ContentDisposition](../com.aspose.words/contentdisposition/) | Enumeriert verschiedene Möglichkeiten, das Dokument im Browser des Clients darzustellen. |
| [ContinuousSectionRestart](../com.aspose.words/continuoussectionrestart/) | Stellt unterschiedliche Verhaltensweisen bei der Berechnung von Seitenzahlen in einem fortlaufenden Abschnitt dar, der die Seitennummerierung neu startet. |
| [Contributor](../com.aspose.words/contributor/) | Stellt einen Bibliografie‑Quellenbeitragenden dar. |
| [ContributorCollection](../com.aspose.words/contributorcollection/) | Stellt Bibliografie‑Quellenbeitragende dar. |
| [ControlChar](../com.aspose.words/controlchar/) | Steuerzeichen, die häufig in Dokumenten vorkommen. |
| [ConvertUtil](../com.aspose.words/convertutil/) | Bietet Hilfsfunktionen zum Konvertieren zwischen verschiedenen Maßeinheiten. |
| [Converter](../com.aspose.words/converter/) | Stellt eine Gruppe von Methoden dar, die dazu gedacht sind, verschiedene Dokumenttypen mit einer einzigen Codezeile zu konvertieren. |
| [ConverterContext](../com.aspose.words/convertercontext/) | Kontext des Dokumentkonverters |
| [Corporate](../com.aspose.words/corporate/) | Stellt einen Unternehmens‑ (oder Organisations‑) Bibliografie‑Quellenbeitragenden dar. |
| [CssSavingArgs](../com.aspose.words/csssavingargs/) | Stellt Daten für das Ereignis [ICssSavingCallback.\#cssSaving(com.aspose.words.CssSavingArgs)](../com.aspose.words/icsssavingcallback/\#cssSaving-com.aspose.words.CssSavingArgs) bereit. |
| [CssStyleSheetType](../com.aspose.words/cssstylesheettype/) | Gibt an, wie CSS‑ (Cascading Style Sheet)‑Stile nach HTML exportiert werden. |
| [CsvDataLoadOptions](../com.aspose.words/csvdataloadoptions/) | Stellt Optionen für das Parsen von CSV‑Daten dar. |
| [CsvDataSource](../com.aspose.words/csvdatasource/) | Bietet Zugriff auf die Daten einer CSV‑Datei oder eines Streams, die in einem Bericht verwendet werden sollen. |
| [CurrentThreadSettings](../com.aspose.words/currentthreadsettings/) | Diese Klasse hilft, das thread‑isolierte Gebietsschema und die Zeitzone für eine Aspose.Words‑Anwendung festzulegen. |
| [CustomDocumentProperties](../com.aspose.words/customdocumentproperties/) | Eine Sammlung benutzerdefinierter Dokumenteigenschaften. |
| [CustomPart](../com.aspose.words/custompart/) | Stellt einen benutzerdefinierten (beliebigen Inhalt) Teil dar, der nicht durch den ISO/IEC‑29500‑Standard definiert ist. |
| [CustomPartCollection](../com.aspose.words/custompartcollection/) | Stellt eine Sammlung von [CustomPart](../com.aspose.words/custompart/)‑Objekten dar. |
| [CustomXmlPart](../com.aspose.words/customxmlpart/) | Stellt einen Custom XML Data Storage Part dar (benutzerdefinierte XML‑Daten innerhalb eines Pakets). |
| [CustomXmlPartCollection](../com.aspose.words/customxmlpartcollection/) | Stellt eine Sammlung von Custom XML Parts dar. |
| [CustomXmlProperty](../com.aspose.words/customxmlproperty/) | Stellt ein einzelnes benutzerdefiniertes XML‑Attribut oder eine Smart‑Tag‑Eigenschaft dar. |
| [CustomXmlPropertyCollection](../com.aspose.words/customxmlpropertycollection/) | Stellt eine Sammlung von benutzerdefinierten XML‑Attributen oder Smart‑Tag‑Eigenschaften dar. |
| [CustomXmlSchemaCollection](../com.aspose.words/customxmlschemacollection/) | Eine Sammlung von Zeichenketten, die XML‑Schemata darstellen, die einem benutzerdefinierten XML‑Teil zugeordnet sind. |
| [DashStyle](../com.aspose.words/dashstyle/) | Gestrichelter Linienstil. |
| [DefaultFontSubstitutionRule](../com.aspose.words/defaultfontsubstitutionrule/) | Standardregel für die Schriftart‑Ersetzung. |
| [DigitalSignature](../com.aspose.words/digitalsignature/) | Stellt eine digitale Signatur in einem Dokument und das Ergebnis ihrer Verifizierung dar. |
| [DigitalSignatureCollection](../com.aspose.words/digitalsignaturecollection/) | Bietet eine schreibgeschützte Sammlung digitaler Signaturen, die an ein Dokument angehängt sind. |
| [DigitalSignatureDetails](../com.aspose.words/digitalsignaturedetails/) | Enthält Details zum Signieren eines Dokuments mit einer digitalen Signatur. |
| [DigitalSignatureType](../com.aspose.words/digitalsignaturetype/) | Gibt den Typ einer digitalen Signatur an. |
| [DigitalSignatureUtil](../com.aspose.words/digitalsignatureutil/) | Stellt Methoden zum Signieren von Dokumenten bereit. |
| [Direction](../com.aspose.words/direction/) | Textrichtung. |
| [Dml3DEffectsRenderingMode](../com.aspose.words/dml3deffectsrenderingmode/) | Gibt an, wie 3D‑Formeffekte gerendert werden. |
| [DmlEffectsRenderingMode](../com.aspose.words/dmleffectsrenderingmode/) | Gibt an, wie DrawingML‑Effekte in feste Seitenformate gerendert werden. |
| [DmlRenderingMode](../com.aspose.words/dmlrenderingmode/) | Gibt an, wie DrawingML‑Formen in feste Seitenformate gerendert werden. |
| [DocSaveOptions](../com.aspose.words/docsaveoptions/) | Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im Format [SaveFormat.\#DOC](../com.aspose.words/saveformat/\#DOC) oder [SaveFormat.\#DOT](../com.aspose.words/saveformat/\#DOT) anzugeben. |
| [DoclingSaveOptions](../com.aspose.words/doclingsaveoptions/) | Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im Format [SaveFormat.\#DOCLING](../com.aspose.words/saveformat/\#DOCLING) anzugeben. |
| [Document](../com.aspose.words/document/) | Stellt ein Word‑Dokument dar. |
| [DocumentBase](../com.aspose.words/documentbase/) | Bietet die abstrakte Basisklasse für ein Hauptdokument und ein Glossar‑Dokument eines Word‑Dokuments. |
| [DocumentBuilder](../com.aspose.words/documentbuilder/) | Stellt Methoden zum Einfügen von Text, Bildern und anderem Inhalt sowie zum Festlegen von Schriftart-, Absatz- und Abschnittsformatierungen bereit. |
| [DocumentBuilderOptions](../com.aspose.words/documentbuilderoptions/) | Ermöglicht das Angeben zusätzlicher Optionen für den Dokumenterstellungsprozess. |
| [DocumentDirection](../com.aspose.words/documentdirection/) | Ermöglicht das Festlegen der Fließrichtung des Textes in einem Dokument. |
| [DocumentLoadingArgs](../com.aspose.words/documentloadingargs/) | Ein Argument, das an [IDocumentLoadingCallback.\#notify(com.aspose.words.DocumentLoadingArgs)](../com.aspose.words/idocumentloadingcallback/\#notify-com.aspose.words.DocumentLoadingArgs) übergeben wird. |
| [DocumentPartSavingArgs](../com.aspose.words/documentpartsavingargs/) | Stellt Daten für den [IDocumentPartSavingCallback.\#documentPartSaving(com.aspose.words.DocumentPartSavingArgs)](../com.aspose.words/idocumentpartsavingcallback/\#documentPartSaving-com.aspose.words.DocumentPartSavingArgs) Callback bereit. |
| [DocumentProperty](../com.aspose.words/documentproperty/) | Stellt eine benutzerdefinierte oder integrierte Dokumenteigenschaft dar. |
| [DocumentPropertyCollection](../com.aspose.words/documentpropertycollection/) | Basisklasse für die Sammlungen [BuiltInDocumentProperties](../com.aspose.words/builtindocumentproperties/) und [CustomDocumentProperties](../com.aspose.words/customdocumentproperties/). |
| [DocumentReaderPluginLoadException](../com.aspose.words/documentreaderpluginloadexception/) | Wird beim Laden des Dokuments ausgelöst, wenn das zum Lesen des Dokumentformats erforderliche Plugin nicht geladen werden kann. |
| [DocumentRecoveryMode](../com.aspose.words/documentrecoverymode/) | Gibt die verfügbaren Wiederherstellungsoptionen an, wenn ein Dokument beim Laden auf Fehler stößt. |
| [DocumentSavingArgs](../com.aspose.words/documentsavingargs/) | Ein Argument, das an [IDocumentSavingCallback.\#notify(com.aspose.words.DocumentSavingArgs)](../com.aspose.words/idocumentsavingcallback/\#notify-com.aspose.words.DocumentSavingArgs) übergeben wird. |
| [DocumentSecurity](../com.aspose.words/documentsecurity/) | Wird als Wert für die Eigenschaft [BuiltInDocumentProperties.\#getSecurity()](../com.aspose.words/builtindocumentproperties/\#getSecurity) / [BuiltInDocumentProperties.\#setSecurity(int)](../com.aspose.words/builtindocumentproperties/\#setSecurity-int) verwendet. |
| [DocumentSplitCriteria](../com.aspose.words/documentsplitcriteria/) | Gibt an, wie das Dokument beim Speichern im Format [SaveFormat.\#HTML](../com.aspose.words/saveformat/\#HTML), [SaveFormat.\#EPUB](../com.aspose.words/saveformat/\#EPUB) oder [SaveFormat.\#AZW\_3](../com.aspose.words/saveformat/\#AZW-3) in Teile aufgeteilt wird. |
| [DocumentVisitor](../com.aspose.words/documentvisitor/) | Basisklasse für benutzerdefinierte Dokumentbesucher. |
| [DownsampleOptions](../com.aspose.words/downsampleoptions/) | Ermöglicht das Angeben von Downsample-Optionen. |
| [DropCapPosition](../com.aspose.words/dropcapposition/) | Gibt die Position für einen Initialbuchstaben-Text an. |
| [DropDownItemCollection](../com.aspose.words/dropdownitemcollection/) | Eine Sammlung von Zeichenketten, die alle Elemente in einem Dropdown-Formularfeld darstellen. |
| [EditableRange](../com.aspose.words/editablerange/) | Stellt einen einzelnen bearbeitbaren Bereich dar. |
| [EditableRangeEnd](../com.aspose.words/editablerangeend/) | Stellt das Ende eines bearbeitbaren Bereichs in einem Word-Dokument dar. |
| [EditableRangeStart](../com.aspose.words/editablerangestart/) | Stellt den Anfang eines bearbeitbaren Bereichs in einem Word-Dokument dar. |
| [EditingLanguage](../com.aspose.words/editinglanguage/) | Gibt die Bearbeitungssprache an. |
| [EditorType](../com.aspose.words/editortype/) | Gibt die Menge möglicher Aliase (oder Bearbeitungsgruppen) an, die als Aliase verwendet werden können, um zu bestimmen, ob dem aktuellen Benutzer das Bearbeiten eines einzelnen, durch einen bearbeitbaren Bereich definierten Bereichs innerhalb eines Dokuments erlaubt ist. |
| [EmbeddedFontFormat](../com.aspose.words/embeddedfontformat/) | Gibt das Format einer bestimmten eingebetteten Schriftart im Objekt [FontInfo](../com.aspose.words/fontinfo/) an. |
| [EmbeddedFontStyle](../com.aspose.words/embeddedfontstyle/) | Gibt den Stil einer eingebetteten Schriftart im Objekt [FontInfo](../com.aspose.words/fontinfo/) an. |
| [EmfPlusDualRenderingMode](../com.aspose.words/emfplusdualrenderingmode/) | Gibt an, wie Aspose.Words EMF+ Dual-Metadateien rendern soll. |
| [EmphasisMark](../com.aspose.words/emphasismark/) | Gibt mögliche Typen von Betonungszeichen an. |
| [EndCap](../com.aspose.words/endcap/) | Gibt den Linienstil für Enden an. |
| [EndnoteOptions](../com.aspose.words/endnoteoptions/) | Stellt die Nummerierungsoptionen für Endnoten in einem Dokument oder Abschnitt dar. |
| [EndnotePosition](../com.aspose.words/endnoteposition/) | Definiert die Position der Endnote. |
| [ExportFontFormat](../com.aspose.words/exportfontformat/) | Gibt das Format an, das zum Exportieren von Schriftarten beim Rendern in das feste HTML-Format verwendet wird. |
| [ExportHeadersFootersMode](../com.aspose.words/exportheadersfootersmode/) | Legt fest, wie Kopf- und Fußzeilen nach HTML, MHTML oder EPUB exportiert werden. |
| [ExportListLabels](../com.aspose.words/exportlistlabels/) | Legt fest, wie Listenelemente nach HTML, MHTML und EPUB exportiert werden. |
| [Field](../com.aspose.words/field/) | Stellt ein Microsoft Word-Dokumentfeld dar. |
| [FieldAddIn](../com.aspose.words/fieldaddin/) | Implementiert das ADDIN-Feld. |
| [FieldAddressBlock](../com.aspose.words/fieldaddressblock/) | Implementiert das ADDRESSBLOCK-Feld. |
| [FieldAdvance](../com.aspose.words/fieldadvance/) | Implementiert das ADVANCE-Feld. |
| [FieldArgumentBuilder](../com.aspose.words/fieldargumentbuilder/) | Erstellt ein komplexes Feldargument, das aus Feldern, Knoten und einfachem Text besteht. |
| [FieldAsk](../com.aspose.words/fieldask/) | Implementiert das ASK-Feld. |
| [FieldAuthor](../com.aspose.words/fieldauthor/) | Implementiert das AUTHOR-Feld. |
| [FieldAutoNum](../com.aspose.words/fieldautonum/) | Implementiert das AUTONUM-Feld. |
| [FieldAutoNumLgl](../com.aspose.words/fieldautonumlgl/) | Implementiert das AUTONUMLGL-Feld. |
| [FieldAutoNumOut](../com.aspose.words/fieldautonumout/) | Implementiert das AUTONUMOUT-Feld. |
| [FieldAutoText](../com.aspose.words/fieldautotext/) | Implementiert das AUTOTEXT-Feld. |
| [FieldAutoTextList](../com.aspose.words/fieldautotextlist/) | Implementiert das AUTOTEXTLIST-Feld. |
| [FieldBarcode](../com.aspose.words/fieldbarcode/) | Implementiert das BARCODE-Feld. |
| [FieldBibliography](../com.aspose.words/fieldbibliography/) | Implementiert das BIBLIOGRAPHY-Feld. |
| [FieldBidiOutline](../com.aspose.words/fieldbidioutline/) | Implementiert das BIDIOUTLINE-Feld. |
| [FieldBuilder](../com.aspose.words/fieldbuilder/) | Erstellt ein Feld aus Feldcode‑Token (Argumente und Schalter). |
| [FieldChar](../com.aspose.words/fieldchar/) | Basisklasse für Knoten, die Feldzeichen in einem Dokument darstellen. |
| [FieldCitation](../com.aspose.words/fieldcitation/) | Implementiert das CITATION-Feld. |
| [FieldCollection](../com.aspose.words/fieldcollection/) | Eine Sammlung von [Field](../com.aspose.words/field/)‑Objekten, die die Felder im angegebenen Bereich darstellen. |
| [FieldComments](../com.aspose.words/fieldcomments/) | Implementiert das COMMENTS-Feld. |
| [FieldCompare](../com.aspose.words/fieldcompare/) | Implementiert das COMPARE-Feld. |
| [FieldCreateDate](../com.aspose.words/fieldcreatedate/) | Implementiert das CREATEDATE-Feld. |
| [FieldData](../com.aspose.words/fielddata/) | Implementiert das DATA-Feld. |
| [FieldDatabase](../com.aspose.words/fielddatabase/) | Implementiert das DATABASE-Feld. |
| [FieldDatabaseDataRow](../com.aspose.words/fielddatabasedatarow/) | Stellt Daten für das Ergebnis des [FieldDatabase](../com.aspose.words/fielddatabase/) Feldes bereit. |
| [FieldDatabaseDataTable](../com.aspose.words/fielddatabasedatatable/) | Stellt Daten für das Ergebnis des [FieldDatabase](../com.aspose.words/fielddatabase/) Feldes bereit. |
| [FieldDate](../com.aspose.words/fielddate/) | Implementiert das DATE-Feld. |
| [FieldDde](../com.aspose.words/fielddde/) | Implementiert das DDE-Feld. |
| [FieldDdeAuto](../com.aspose.words/fieldddeauto/) | Implementiert das DDEAUTO-Feld. |
| [FieldDisplayBarcode](../com.aspose.words/fielddisplaybarcode/) | Implementiert das DISPLAYBARCODE-Feld. |
| [FieldDocProperty](../com.aspose.words/fielddocproperty/) | Implementiert das DOCPROPERTY-Feld. |
| [FieldDocVariable](../com.aspose.words/fielddocvariable/) | Implementiert das DOCVARIABLE-Feld. |
| [FieldEQ](../com.aspose.words/fieldeq/) | Implementiert das EQ-Feld. |
| [FieldEditTime](../com.aspose.words/fieldedittime/) | Implementiert das EDITTIME-Feld. |
| [FieldEmbed](../com.aspose.words/fieldembed/) | Implementiert das EMBED-Feld. |
| [FieldEnd](../com.aspose.words/fieldend/) | Stellt das Ende eines Word-Feldes in einem Dokument dar. |
| [FieldFileName](../com.aspose.words/fieldfilename/) | Implementiert das FILENAME-Feld. |
| [FieldFileSize](../com.aspose.words/fieldfilesize/) | Implementiert das FILESIZE-Feld. |
| [FieldFillIn](../com.aspose.words/fieldfillin/) | Implementiert das FILLIN-Feld. |
| [FieldFootnoteRef](../com.aspose.words/fieldfootnoteref/) | Implementiert das FOOTNOTEREF-Feld. |
| [FieldFormCheckBox](../com.aspose.words/fieldformcheckbox/) | Implementiert das FORMCHECKBOX-Feld. |
| [FieldFormDropDown](../com.aspose.words/fieldformdropdown/) | Implementiert das FORMDROPDOWN-Feld. |
| [FieldFormText](../com.aspose.words/fieldformtext/) | Implementiert das FORMTEXT-Feld. |
| [FieldFormat](../com.aspose.words/fieldformat/) | Bietet typisierten Zugriff auf numerische, Datums- und Zeit- sowie allgemeine Formatierung des Feldes. |
| [FieldFormula](../com.aspose.words/fieldformula/) | Implementiert das = (Formel)-Feld. |
| [FieldGlossary](../com.aspose.words/fieldglossary/) | Implementiert das GLOSSARY-Feld. |
| [FieldGoToButton](../com.aspose.words/fieldgotobutton/) | Implementiert das GOTOBUTTON-Feld. |
| [FieldGreetingLine](../com.aspose.words/fieldgreetingline/) | Implementiert das GREETINGLINE-Feld. |
| [FieldHyperlink](../com.aspose.words/fieldhyperlink/) | Implementiert das HYPERLINK-Feld |
| [FieldIf](../com.aspose.words/fieldif/) | Implementiert das IF-Feld. |
| [FieldIfComparisonResult](../com.aspose.words/fieldifcomparisonresult/) | Gibt das Ergebnis der Auswertung der IF-Feldbedingung an. |
| [FieldImport](../com.aspose.words/fieldimport/) | Implementiert das IMPORT-Feld. |
| [FieldInclude](../com.aspose.words/fieldinclude/) | Implementiert das INCLUDE-Feld. |
| [FieldIncludePicture](../com.aspose.words/fieldincludepicture/) | Implementiert das INCLUDEPICTURE-Feld. |
| [FieldIncludeText](../com.aspose.words/fieldincludetext/) | Implementiert das INCLUDETEXT-Feld. |
| [FieldIndex](../com.aspose.words/fieldindex/) | Implementiert das INDEX-Feld. |
| [FieldIndexFormat](../com.aspose.words/fieldindexformat/) | Gibt die Formatierung für die [FieldIndex](../com.aspose.words/fieldindex/) Felder in einem Dokument an. |
| [FieldInfo](../com.aspose.words/fieldinfo/) | Implementiert das INFO-Feld. |
| [FieldKeywords](../com.aspose.words/fieldkeywords/) | Implementiert das KEYWORDS-Feld. |
| [FieldLastSavedBy](../com.aspose.words/fieldlastsavedby/) | Implementiert das LASTSAVEDBY-Feld. |
| [FieldLink](../com.aspose.words/fieldlink/) | Implementiert das LINK-Feld. |
| [FieldListNum](../com.aspose.words/fieldlistnum/) | Implementiert das LISTNUM-Feld. |
| [FieldMacroButton](../com.aspose.words/fieldmacrobutton/) | Implementiert das MACROBUTTON-Feld. |
| [FieldMergeBarcode](../com.aspose.words/fieldmergebarcode/) | Implementiert das MERGEBARCODE-Feld. |
| [FieldMergeField](../com.aspose.words/fieldmergefield/) | Implementiert das MERGEFIELD-Feld. |
| [FieldMergeRec](../com.aspose.words/fieldmergerec/) | Implementiert das MERGEREC-Feld. |
| [FieldMergeSeq](../com.aspose.words/fieldmergeseq/) | Implementiert das MERGESEQ-Feld. |
| [FieldMergingArgs](../com.aspose.words/fieldmergingargs/) | Stellt Daten für das **MergeField**-Ereignis bereit. |
| [FieldMergingArgsBase](../com.aspose.words/fieldmergingargsbase/) | Basisklasse für [FieldMergingArgs](../com.aspose.words/fieldmergingargs/) und [ImageFieldMergingArgs](../com.aspose.words/imagefieldmergingargs/). |
| [FieldNext](../com.aspose.words/fieldnext/) | Implementiert das NEXT-Feld. |
| [FieldNextIf](../com.aspose.words/fieldnextif/) | Implementiert das NEXTIF-Feld. |
| [FieldNoteRef](../com.aspose.words/fieldnoteref/) | Implementiert das NOTEREF-Feld. |
| [FieldNumChars](../com.aspose.words/fieldnumchars/) | Implementiert das NUMCHARS-Feld. |
| [FieldNumPages](../com.aspose.words/fieldnumpages/) | Implementiert das NUMPAGES-Feld. |
| [FieldNumWords](../com.aspose.words/fieldnumwords/) | Implementiert das NUMWORDS-Feld. |
| [FieldOcx](../com.aspose.words/fieldocx/) | Implementiert das OCX-Feld. |
| [FieldOptions](../com.aspose.words/fieldoptions/) | Stellt Optionen zur Steuerung der Feldverarbeitung in einem Dokument dar. |
| [FieldPage](../com.aspose.words/fieldpage/) | Implementiert das PAGE-Feld. |
| [FieldPageRef](../com.aspose.words/fieldpageref/) | Implementiert das PAGEREF-Feld. |
| [FieldPrint](../com.aspose.words/fieldprint/) | Implementiert das PRINT-Feld. |
| [FieldPrintDate](../com.aspose.words/fieldprintdate/) | Implementiert das PRINTDATE-Feld. |
| [FieldPrivate](../com.aspose.words/fieldprivate/) | Implementiert das PRIVATE-Feld. |
| [FieldQuote](../com.aspose.words/fieldquote/) | Implementiert das QUOTE-Feld. |
| [FieldRD](../com.aspose.words/fieldrd/) | Implementiert das RD-Feld. |
| [FieldRef](../com.aspose.words/fieldref/) | Implementiert das REF-Feld. |
| [FieldRevNum](../com.aspose.words/fieldrevnum/) | Implementiert das REVNUM-Feld. |
| [FieldSaveDate](../com.aspose.words/fieldsavedate/) | Implementiert das SAVEDATE-Feld. |
| [FieldSection](../com.aspose.words/fieldsection/) | Implementiert das SECTION-Feld. |
| [FieldSectionPages](../com.aspose.words/fieldsectionpages/) | Implementiert das SECTIONPAGES-Feld. |
| [FieldSeparator](../com.aspose.words/fieldseparator/) | Stellt einen Word-Feldtrenner dar, der den Feldcode vom Feldresultat trennt. |
| [FieldSeq](../com.aspose.words/fieldseq/) | Implementiert das SEQ-Feld. |
| [FieldSet](../com.aspose.words/fieldset/) | Implementiert das SET-Feld. |
| [FieldShape](../com.aspose.words/fieldshape/) | Implementiert das SHAPE-Feld. |
| [FieldSkipIf](../com.aspose.words/fieldskipif/) | Implementiert das SKIPIF-Feld. |
| [FieldStart](../com.aspose.words/fieldstart/) | Stellt den Beginn eines Word-Feldes in einem Dokument dar. |
| [FieldStyleRef](../com.aspose.words/fieldstyleref/) | Implementiert das STYLEREF-Feld. |
| [FieldSubject](../com.aspose.words/fieldsubject/) | Implementiert das SUBJECT-Feld. |
| [FieldSymbol](../com.aspose.words/fieldsymbol/) | Implementiert ein SYMBOL-Feld. |
| [FieldTA](../com.aspose.words/fieldta/) | Implementiert das TA-Feld. |
| [FieldTC](../com.aspose.words/fieldtc/) | Implementiert das TC-Feld. |
| [FieldTemplate](../com.aspose.words/fieldtemplate/) | Implementiert das TEMPLATE-Feld. |
| [FieldTime](../com.aspose.words/fieldtime/) | Implementiert das TIME-Feld. |
| [FieldTitle](../com.aspose.words/fieldtitle/) | Implementiert das TITLE-Feld. |
| [FieldToa](../com.aspose.words/fieldtoa/) | Implementiert das TOA-Feld. |
| [FieldToc](../com.aspose.words/fieldtoc/) | Implementiert das TOC-Feld. |
| [FieldType](../com.aspose.words/fieldtype/) | Gibt Microsoft Word-Feldtypen an. |
| [FieldUnknown](../com.aspose.words/fieldunknown/) | Implementiert ein unbekanntes oder nicht erkanntes Feld. |
| [FieldUpdateCultureSource](../com.aspose.words/fieldupdateculturesource/) | Gibt an, welche Kultur bei der Feldaktualisierung verwendet werden soll. |
| [FieldUpdatingProgressArgs](../com.aspose.words/fieldupdatingprogressargs/) | Stellt Daten für das Ereignis zum Fortschritt der Feldaktualisierung bereit. |
| [FieldUserAddress](../com.aspose.words/fielduseraddress/) | Implementiert das USERADDRESS-Feld. |
| [FieldUserInitials](../com.aspose.words/fielduserinitials/) | Implementiert das USERINITIALS-Feld. |
| [FieldUserName](../com.aspose.words/fieldusername/) | Implementiert das USERNAME-Feld. |
| [FieldXE](../com.aspose.words/fieldxe/) | Implementiert das XE-Feld. |
| [FileCorruptedException](../com.aspose.words/filecorruptedexception/) | Wird beim Laden des Dokuments ausgelöst, wenn das Dokument beschädigt zu sein scheint und nicht geladen werden kann. |
| [FileFontSource](../com.aspose.words/filefontsource/) | Stellt die einzelne TrueType-Schriftdatei dar, die im Dateisystem gespeichert ist. |
| [FileFormatInfo](../com.aspose.words/fileformatinfo/) | Enthält Daten, die von den Dokumentformat-Erkennungsmethoden von [FileFormatUtil](../com.aspose.words/fileformatutil/) zurückgegeben werden. |
| [FileFormatUtil](../com.aspose.words/fileformatutil/) | Stellt Dienstprogrammmethoden für die Arbeit mit Dateiformaten bereit, z. B. zum Erkennen von Dateiformaten oder zum Konvertieren von Dateierweiterungen in/von Dateiformat-Enums. |
| [Fill](../com.aspose.words/fill/) | Stellt die Füllformatierung für ein Objekt dar. |
| [FillType](../com.aspose.words/filltype/) | Gibt den Fülltyp für ein ausfüllbares Objekt an. |
| [FindReplaceDirection](../com.aspose.words/findreplacedirection/) | Gibt die Richtung für Ersetzungsoperationen an. |
| [FindReplaceOptions](../com.aspose.words/findreplaceoptions/) | Gibt Optionen für Suchen/Ersetzen-Operationen an. |
| [FipsUnapprovedOperationException](../com.aspose.words/fipsunapprovedoperationexception/) | Stellt die Ausnahme dar, die ausgelöst wird, wenn versucht wird, Kryptografie unsachgemäß zu verwenden. |
| [FixedPageSaveOptions](../com.aspose.words/fixedpagesaveoptions/) | Enthält gängige Optionen, die beim Speichern eines Dokuments in feste Seitenformate (PDF, XPS, Bilder usw.) angegeben werden können. |
| [FlipOrientation](../com.aspose.words/fliporientation/) | Mögliche Werte für die Ausrichtung einer Form. |
| [FolderFontSource](../com.aspose.words/folderfontsource/) | Stellt den Ordner dar, der TrueType-Schriftdateien enthält. |
| [Font](../com.aspose.words/font/) | Enthält Schriftattribute (Schriftname, Schriftgröße, Farbe usw.) für ein Objekt. |
| [FontConfigSubstitutionRule](../com.aspose.words/fontconfigsubstitutionrule/) | Schriftkonfigurations‑Ersetzungsregel. |
| [FontEmbeddingLicensingRights](../com.aspose.words/fontembeddinglicensingrights/) | Stellt die Einbettungs‑Lizenzrechte für die Schrift dar. |
| [FontEmbeddingUsagePermissions](../com.aspose.words/fontembeddingusagepermissions/) | Stellt die Nutzungsberechtigungen für die Schrift‑Einbettung dar. |
| [FontFallbackSettings](../com.aspose.words/fontfallbacksettings/) | Gibt die Einstellungen für den Schriftfallback‑Mechanismus an. |
| [FontFamily](../com.aspose.words/fontfamily/) | Stellt die Schriftfamilie dar. |
| [FontFeature](../com.aspose.words/fontfeature/) | Funktionen liefern Informationen darüber, wie Glyphen in einer Schrift verwendet werden, um ein Skript darzustellen. |
| [FontInfo](../com.aspose.words/fontinfo/) | Gibt Informationen über eine im Dokument verwendete Schrift an. |
| [FontInfoCollection](../com.aspose.words/fontinfocollection/) | Stellt eine Sammlung von im Dokument verwendeten Schriften dar. |
| [FontInfoSubstitutionRule](../com.aspose.words/fontinfosubstitutionrule/) | Schriftinfo‑Ersetzungsregel. |
| [FontNameSubstitutionRule](../com.aspose.words/fontnamesubstitutionrule/) | Schrift‑Ersetzungsregel zur Verarbeitung des Schriftnamens. |
| [FontPitch](../com.aspose.words/fontpitch/) | Stellt die Schriftbreite dar. |
| [FontSavingArgs](../com.aspose.words/fontsavingargs/) | Stellt Daten für das Ereignis [IFontSavingCallback.#fontSaving(com.aspose.words.FontSavingArgs)](../com.aspose.words/ifontsavingcallback/#fontSaving-com.aspose.words.FontSavingArgs) bereit. |
| [FontSettings](../com.aspose.words/fontsettings/) | Gibt die Schrift‑Einstellungen für ein Dokument an. |
| [FontSourceBase](../com.aspose.words/fontsourcebase/) | Dies ist eine abstrakte Basisklasse für die Klassen, die dem Benutzer ermöglichen, verschiedene Schriftquellen anzugeben. |
| [FontSourceType](../com.aspose.words/fontsourcetype/) | Gibt den Typ der Schriftquelle an. |
| [FontSubstitutionReason](../com.aspose.words/fontsubstitutionreason/) | Gibt den Grund für die Schrift‑Ersetzung an. |
| [FontSubstitutionRule](../com.aspose.words/fontsubstitutionrule/) | Dies ist eine abstrakte Basisklasse für die Schrift‑Ersetzungsregel. |
| [FontSubstitutionSettings](../com.aspose.words/fontsubstitutionsettings/) | Gibt die Einstellungen für den Schrift‑Ersetzungsmechanismus an. |
| [FontSubstitutionWarningInfo](../com.aspose.words/fontsubstitutionwarninginfo/) | Enthält Informationen über eine Schrift‑Ersetzungswarnung, die Aspose.Words beim Laden oder Speichern eines Dokuments ausgegeben hat. |
| [Footnote](../com.aspose.words/footnote/) | Stellt einen Container für den Text einer Fußnote oder Endnote dar. |
| [FootnoteNumberingRule](../com.aspose.words/footnotenumberingrule/) | Bestimmt, wann die automatische Nummerierung von Fußnoten oder Endnoten neu startet. |
| [FootnoteOptions](../com.aspose.words/footnoteoptions/) | Stellt die Optionen für die Fußnotennummerierung eines Dokuments oder Abschnitts dar. |
| [FootnotePosition](../com.aspose.words/footnoteposition/) | Definiert die Position der Fußnote. |
| [FootnoteSeparator](../com.aspose.words/footnoteseparator/) |  |
| [FootnoteSeparatorCollection](../com.aspose.words/footnoteseparatorcollection/) | Bietet typisierten Zugriff auf **T:Aspose.Words.Notes.FootnoteSeparator**-Knoten eines Dokuments. |
| [FootnoteSeparatorType](../com.aspose.words/footnoteseparatortype/) | Gibt den Typ des Fußnoten-/Endnoten-Trennzeichens an. |
| [FootnoteType](../com.aspose.words/footnotetype/) | Gibt an, ob dies eine Fußnote oder eine Endnote ist. |
| [FormField](../com.aspose.words/formfield/) | Stellt ein einzelnes Formularfeld dar. |
| [FormFieldCollection](../com.aspose.words/formfieldcollection/) | Eine Sammlung von [FormField](../com.aspose.words/formfield/)-Objekten, die alle Formularfelder in einem Bereich darstellen. |
| [Forms2OleControl](../com.aspose.words/forms2olecontrol/) | Stellt das Microsoft Forms 2.0 OLE-Steuerelement dar. |
| [Forms2OleControlCollection](../com.aspose.words/forms2olecontrolcollection/) | Stellt eine Sammlung von [Forms2OleControl](../com.aspose.words/forms2olecontrol/)-Objekten dar. |
| [Forms2OleControlType](../com.aspose.words/forms2olecontroltype/) | Enumeriert die Typen von Forms 2.0-Steuerelementen. |
| [FrameFormat](../com.aspose.words/frameformat/) | Stellt die rahmenbezogene Formatierung für einen Absatz dar. |
| [Frameset](../com.aspose.words/frameset/) | Stellt eine Frames-Seite oder einen einzelnen Frame auf einer Frames-Seite dar. |
| [FramesetCollection](../com.aspose.words/framesetcollection/) | Stellt eine Sammlung von Instanzen der Klasse [Frameset](../com.aspose.words/frameset/) dar. |
| [GeneralFormat](../com.aspose.words/generalformat/) | Gibt ein allgemeines Format an, das auf ein numerisches, Text- oder beliebiges Feldresultat angewendet wird. |
| [GeneralFormatCollection](../com.aspose.words/generalformatcollection/) | Stellt eine typisierte Sammlung allgemeiner Formate dar. |
| [GlossaryDocument](../com.aspose.words/glossarydocument/) | Stellt das Wurzelelement für ein Glossar-Dokument innerhalb eines Word-Dokuments dar. |
| [GlowFormat](../com.aspose.words/glowformat/) | Stellt die Leuchteffekt-Formatierung für ein Objekt dar. |
| [Glyph](../com.aspose.words/glyph/) | Stellt ein Glyph dar |
| [GlyphFlags](../com.aspose.words/glyphflags/) |  |
| [GoogleAiModel](../com.aspose.words/googleaimodel/) | Klasse, die die Integration von Google KI-Modellen (Gemini) in Aspose.Words darstellt. |
| [GradientStop](../com.aspose.words/gradientstop/) | Stellt einen Farbverlaufsstopp dar. |
| [GradientStopCollection](../com.aspose.words/gradientstopcollection/) | Enthält eine Sammlung von [GradientStop](../com.aspose.words/gradientstop/)-Objekten. |
| [GradientStyle](../com.aspose.words/gradientstyle/) | Gibt den Stil für eine Farbverlaufsfüllung an. |
| [GradientVariant](../com.aspose.words/gradientvariant/) | Gibt die Variante für eine Farbverlaufsfüllung an. |
| [Granularity](../com.aspose.words/granularity/) | Gibt die Granularität der zu verfolgenden Änderungen beim Vergleich zweier Dokumente an. |
| [GraphicsQualityOptions](../com.aspose.words/graphicsqualityoptions/) | Ermöglicht das Angeben zusätzlicher **java.awt.RenderingHints**. |
| [GroupShape](../com.aspose.words/groupshape/) | Stellt eine Gruppe von Formen in einem Dokument dar. |
| [HeaderFooter](../com.aspose.words/headerfooter/) | Stellt einen Container für den Header- oder Footer-Text eines Abschnitts dar. |
| [HeaderFooterBookmarksExportMode](../com.aspose.words/headerfooterbookmarksexportmode/) | Gibt an, wie Lesezeichen in Headern/Footern exportiert werden. |
| [HeaderFooterCollection](../com.aspose.words/headerfootercollection/) | Bietet typisierten Zugriff auf die Knoten [HeaderFooter](../com.aspose.words/headerfooter/) eines [Section](../com.aspose.words/section/). |
| [HeaderFooterType](../com.aspose.words/headerfootertype/) | Identifiziert den Typ von Header oder Footer, der in einer Word-Datei gefunden wird. |
| [HeightRule](../com.aspose.words/heightrule/) | Legt die Regel zur Bestimmung der Höhe eines Objekts fest. |
| [HorizontalAlignment](../com.aspose.words/horizontalalignment/) | Gibt die horizontale Ausrichtung einer schwebenden Form, eines Textfelds oder einer schwebenden Tabelle an. |
| [HorizontalRuleAlignment](../com.aspose.words/horizontalrulealignment/) | Stellt die Ausrichtung für die angegebene horizontale Linie dar. |
| [HorizontalRuleFormat](../com.aspose.words/horizontalruleformat/) | Stellt die Formatierung der horizontalen Linie dar. |
| [HtmlControlType](../com.aspose.words/htmlcontroltype/) | Typ von Dokumentknoten, die  und  Elemente aus HTML darstellen. |
| [HtmlElementSizeOutputMode](../com.aspose.words/htmlelementsizeoutputmode/) | Gibt an, wie Aspose.Words Breiten und Höhen von Elementen nach HTML, MHTML und EPUB exportiert. |
| [HtmlFixedPageHorizontalAlignment](../com.aspose.words/htmlfixedpagehorizontalalignment/) | Gibt die horizontale Ausrichtung für Seiten im ausgegebenen HTML-Dokument an. |
| [HtmlFixedSaveOptions](../com.aspose.words/htmlfixedsaveoptions/) | Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im Format [SaveFormat.\#HTML\_FIXED](../com.aspose.words/saveformat/\#HTML-FIXED) anzugeben. |
| [HtmlInsertOptions](../com.aspose.words/htmlinsertoptions/) | Gibt Optionen für die Methode **M:Aspose.Words.DocumentBuilder.InsertHtml(System.String,Aspose.Words.HtmlInsertOptions)** an. |
| [HtmlLoadOptions](../com.aspose.words/htmlloadoptions/) | Ermöglicht das Angeben zusätzlicher Optionen beim Laden eines HTML-Dokuments in ein [Document](../com.aspose.words/document/) Objekt. |
| [HtmlMetafileFormat](../com.aspose.words/htmlmetafileformat/) | Gibt das Format an, in dem Metadateien in HTML-Dokumente gespeichert werden. |
| [HtmlOfficeMathOutputMode](../com.aspose.words/htmlofficemathoutputmode/) | Gibt an, wie Aspose.Words OfficeMath nach HTML, MHTML und EPUB exportiert. |
| [HtmlSaveOptions](../com.aspose.words/htmlsaveoptions/) | Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im Format [SaveFormat.\#HTML](../com.aspose.words/saveformat/\#HTML), [SaveFormat.\#MHTML](../com.aspose.words/saveformat/\#MHTML), [SaveFormat.\#EPUB](../com.aspose.words/saveformat/\#EPUB), [SaveFormat.\#AZW\_3](../com.aspose.words/saveformat/\#AZW-3) oder [SaveFormat.\#MOBI](../com.aspose.words/saveformat/\#MOBI) anzugeben. |
| [HtmlVersion](../com.aspose.words/htmlversion/) | Gibt an, welche HTML-Version beim Speichern des Dokuments in die Formate [SaveFormat.\#HTML](../com.aspose.words/saveformat/\#HTML) und [SaveFormat.\#MHTML](../com.aspose.words/saveformat/\#MHTML) verwendet wird. |
| [Hyphenation](../com.aspose.words/hyphenation/) | Stellt Methoden zur Arbeit mit Silbentrennungswörterbüchern bereit. |
| [HyphenationOptions](../com.aspose.words/hyphenationoptions/) | Ermöglicht die Konfiguration von Silbentrennungsoptionen für das Dokument. |
| [ImageBinarizationMethod](../com.aspose.words/imagebinarizationmethod/) | Gibt die Methode an, die zum Binarisieren von Bildern verwendet wird. |
| [ImageColorMode](../com.aspose.words/imagecolormode/) | Gibt den Farbmodus für die erzeugten Bilder der Dokumentseiten an. |
| [ImageData](../com.aspose.words/imagedata/) | Definiert ein Bild für eine Form. |
| [ImageFieldMergingArgs](../com.aspose.words/imagefieldmergingargs/) | Stellt Daten für das Ereignis [IFieldMergingCallback.\#imageFieldMerging(com.aspose.words.ImageFieldMergingArgs)](../com.aspose.words/ifieldmergingcallback/\#imageFieldMerging-com.aspose.words.ImageFieldMergingArgs) bereit. |
| [ImagePixelFormat](../com.aspose.words/imagepixelformat/) | Gibt das Pixel-Format für die erzeugten Bilder der Dokumentseiten an. |
| [ImageSaveOptions](../com.aspose.words/imagesaveoptions/) | Ermöglicht das Angeben zusätzlicher Optionen beim Rendern von Dokumentseiten oder Formen zu Bildern. |
| [ImageSavingArgs](../com.aspose.words/imagesavingargs/) | Stellt Daten für das [IImageSavingCallback.#imageSaving(com.aspose.words.ImageSavingArgs)](../com.aspose.words/iimagesavingcallback/#imageSaving-com.aspose.words.ImageSavingArgs) Ereignis bereit. |
| [ImageSize](../com.aspose.words/imagesize/) | Enthält Informationen über Bildgröße und Auflösung. |
| [ImageType](../com.aspose.words/imagetype/) | Gibt den Typ (Format) eines Bildes in einem Microsoft Word-Dokument an. |
| [ImageWatermarkOptions](../com.aspose.words/imagewatermarkoptions/) | Enthält Optionen, die beim Hinzufügen eines Wasserzeichens mit Bild angegeben werden können. |
| [ImlRenderingMode](../com.aspose.words/imlrenderingmode/) | Gibt an, wie Tintenobjekte (InkML) in feste Seitenformate gerendert werden. |
| [ImportFormatMode](../com.aspose.words/importformatmode/) | Gibt an, wie Formatierungen beim Importieren von Inhalten aus einem anderen Dokument zusammengeführt werden. |
| [ImportFormatOptions](../com.aspose.words/importformatoptions/) | Ermöglicht das Angeben verschiedener Importoptionen zur Formatierung der Ausgabe. |
| [IncorrectPasswordException](../com.aspose.words/incorrectpasswordexception/) | Wird ausgelöst, wenn ein Dokument mit einem Passwort verschlüsselt ist und das beim Öffnen des Dokuments angegebene Passwort falsch oder fehlt. |
| [Inline](../com.aspose.words/inline/) | Basisklasse für Inline-Knoten, die Zeichenformatierungen zugeordnet haben können, aber keine eigenen untergeordneten Knoten besitzen. |
| [InlineStory](../com.aspose.words/inlinestory/) | Basisklasse für Inline-Knoten, die Absätze und Tabellen enthalten können. |
| [InternableComplexAttr](../com.aspose.words/internablecomplexattr/) | Basisklasse für internierbare komplexe Attribute. |
| [JoinRunsOptions](../com.aspose.words/joinrunsoptions/) | Stellt Konfigurationsflags für die Join‑Runs‑Operation bereit. |
| [JoinStyle](../com.aspose.words/joinstyle/) | Linienverbindungsstil. |
| [JsonDataLoadOptions](../com.aspose.words/jsondataloadoptions/) | Stellt Optionen für das Parsen von JSON-Daten dar. |
| [JsonDataSource](../com.aspose.words/jsondatasource/) | Stellt Zugriff auf Daten einer JSON-Datei oder eines Streams bereit, die in einem Bericht verwendet werden. |
| [JsonSimpleValueParseMode](../com.aspose.words/jsonsimplevalueparsemode/) | Gibt einen Modus zum Parsen einfacher JSON‑Werte (null, boolesch, Zahl, Ganzzahl und Zeichenkette) beim Laden von JSON an. |
| [JustificationMode](../com.aspose.words/justificationmode/) | Gibt die Zeichenabstandsanpassung für ein Dokument an. |
| [KnownTypeSet](../com.aspose.words/knowntypeset/) | Stellt eine ungeordnete Menge dar (z.B. |
| [Language](../com.aspose.words/language/) | Gibt die Sprache an, in die der Text mithilfe von KI übersetzt wird.. |
| [LanguagePreferences](../com.aspose.words/languagepreferences/) | Ermöglicht das Einrichten von Spracheinstellungen. |
| [LayoutCollector](../com.aspose.words/layoutcollector/) | Diese Klasse ermöglicht die Berechnung von Seitenzahlen von Dokumentknoten. |
| [LayoutEntityType](../com.aspose.words/layoutentitytype/) | Typen der Layout‑Entitäten. |
| [LayoutEnumerator](../com.aspose.words/layoutenumerator/) | Enumeriert Seitenlayout‑Entitäten eines Dokuments. |
| [LayoutFlow](../com.aspose.words/layoutflow/) | Bestimmt den Fluss des Textlayouts in einem Textfeld. |
| [LayoutOptions](../com.aspose.words/layoutoptions/) | Enthält die Optionen, die die Steuerung des Dokumentlayoutprozesses ermöglichen. |
| [LegendPosition](../com.aspose.words/legendposition/) | Gibt die möglichen Positionen für eine Diagrammlegende an. |
| [License](../com.aspose.words/license/) | Stellt Methoden zur Lizenzierung der Komponente bereit. |
| [LineNumberRestartMode](../com.aspose.words/linenumberrestartmode/) | Bestimmt, wann die automatische Zeilennummerierung neu startet. |
| [LineSpacingRule](../com.aspose.words/linespacingrule/) | Gibt Zeilenabstandswerte für einen Absatz an. |
| [LineStyle](../com.aspose.words/linestyle/) | Gibt den Linienstil eines [Border](../com.aspose.words/border/) an. |
| [List](../com.aspose.words/list/) | Stellt die Formatierung einer Liste dar. |
| [ListCollection](../com.aspose.words/listcollection/) | Speichert und verwaltet die Formatierung von Aufzählungs‑ und nummerierten Listen, die in einem Dokument verwendet werden. |
| [ListFormat](../com.aspose.words/listformat/) | Ermöglicht die Steuerung, welche Listformatierung auf einen Absatz angewendet wird. |
| [ListLabel](../com.aspose.words/listlabel/) | Definiert Eigenschaften, die spezifisch für ein Listenelement sind. |
| [ListLevel](../com.aspose.words/listlevel/) | Definiert die Formatierung für eine Listenebene. |
| [ListLevelAlignment](../com.aspose.words/listlevelalignment/) | Gibt die Ausrichtung für die Listennummer oder das Aufzählungszeichen an. |
| [ListLevelCollection](../com.aspose.words/listlevelcollection/) | Eine Sammlung von Listformatierungen für jede Ebene in einer Liste. |
| [ListTemplate](../com.aspose.words/listtemplate/) | Gibt eines der vordefinierten Listformate an, die in Microsoft Word verfügbar sind. |
| [ListTrailingCharacter](../com.aspose.words/listtrailingcharacter/) | Gibt das Zeichen an, das das Listenelement vom Text des Absatzes trennt. |
| [LoadFormat](../com.aspose.words/loadformat/) | Gibt das Format des zu ladenden Dokuments an. |
| [LoadOptions](../com.aspose.words/loadoptions/) | Ermöglicht das Angeben zusätzlicher Optionen (wie Passwort oder Basis‑URI), wenn ein Dokument in ein [Document](../com.aspose.words/document/)‑Objekt geladen wird. |
| [MailMerge](../com.aspose.words/mailmerge/) | Stellt die Seriendruckfunktionalität dar. |
| [MailMergeCheckErrors](../com.aspose.words/mailmergecheckerrors/) | Gibt an, wie Microsoft Word Fehler meldet, die beim Seriendruck erkannt werden. |
| [MailMergeCleanupOptions](../com.aspose.words/mailmergecleanupoptions/) | Gibt Optionen an, die bestimmen, welche Elemente beim Seriendruck entfernt werden. |
| [MailMergeDataSource](../com.aspose.words/mailmergedatasource/) | Datenquelle für den Seriendruck, die in [MailMergerContext](../com.aspose.words/mailmergercontext/) verwendet wird. |
| [MailMergeDataType](../com.aspose.words/mailmergedatatype/) | Gibt den Typ einer externen Seriendruck‑Datenquelle an. |
| [MailMergeDestination](../com.aspose.words/mailmergedestination/) | Gibt die möglichen Ergebnisse an, die erzeugt werden können, wenn ein Seriendruck in einem Dokument durchgeführt wird. |
| [MailMergeMainDocumentType](../com.aspose.words/mailmergemaindocumenttype/) | Gibt die möglichen Typen für ein Seriendruck‑Quelldokument an. |
| [MailMergeOptions](../com.aspose.words/mailmergeoptions/) | Stellt Optionen für die Seriendruckfunktionalität dar. |
| [MailMergeRegionInfo](../com.aspose.words/mailmergeregioninfo/) | Enthält Informationen über einen Seriendruckbereich. |
| [MailMergeSettings](../com.aspose.words/mailmergesettings/) | Gibt alle Seriendruckinformationen für ein Dokument an. |
| [MailMerger](../com.aspose.words/mailmerger/) | Stellt Methoden bereit, die dazu dienen, Vorlagen mit Daten mittels einfachem Seriendruck und Seriendruck mit Regionen zu füllen. |
| [MailMergerContext](../com.aspose.words/mailmergercontext/) | Seriendruck-Kontext. |
| [MappedDataFieldCollection](../com.aspose.words/mappeddatafieldcollection/) | Ermöglicht das automatische Zuordnen von Feldnamen in Ihrer Datenquelle zu den Namen der Seriendruckfelder im Dokument. |
| [Margins](../com.aspose.words/margins/) | Gibt voreingestellte Ränder an. |
| [MarkdownEmptyParagraphExportMode](../com.aspose.words/markdownemptyparagraphexportmode/) | Gibt an, wie Aspose.Words leere Absätze nach Markdown exportiert. |
| [MarkdownExportAsHtml](../com.aspose.words/markdownexportashtml/) | Ermöglicht die Angabe der Elemente, die als rohes HTML nach Markdown exportiert werden sollen. |
| [MarkdownLinkExportMode](../com.aspose.words/markdownlinkexportmode/) | Gibt an, wie Links nach Markdown exportiert werden. |
| [MarkdownListExportMode](../com.aspose.words/markdownlistexportmode/) | Gibt an, wie Listen nach Markdown exportiert werden. |
| [MarkdownLoadOptions](../com.aspose.words/markdownloadoptions/) | Ermöglicht die Angabe zusätzlicher Optionen beim Laden eines [LoadFormat.\#MARKDOWN](../com.aspose.words/loadformat/\#MARKDOWN)-Dokuments in ein [Document](../com.aspose.words/document/)-Objekt. |
| [MarkdownOfficeMathExportMode](../com.aspose.words/markdownofficemathexportmode/) | Gibt an, wie Aspose.Words OfficeMath nach Markdown exportiert. |
| [MarkdownSaveOptions](../com.aspose.words/markdownsaveoptions/) | Klasse zur Angabe zusätzlicher Optionen beim Speichern eines Dokuments im [SaveFormat.\#MARKDOWN](../com.aspose.words/saveformat/\#MARKDOWN)-Format. |
| [MarkerSymbol](../com.aspose.words/markersymbol/) | Gibt den Stil des Markierungssymbols an. |
| [MarkupLevel](../com.aspose.words/markuplevel/) | Gibt die Ebene im Dokumentenbaum an, in der ein bestimmtes [StructuredDocumentTag](../com.aspose.words/structureddocumenttag/) auftreten kann. |
| [MathObjectType](../com.aspose.words/mathobjecttype/) | Gibt den Typ eines Office Math-Objekts an. |
| [MeasurementUnits](../com.aspose.words/measurementunits/) | Gibt die Maßeinheit an. |
| [MemoryFontSource](../com.aspose.words/memoryfontsource/) | Stellt die einzelne TrueType-Schriftdatei dar, die im Speicher gespeichert ist. |
| [MergeFieldImageDimension](../com.aspose.words/mergefieldimagedimension/) | Stellt eine Bilddimension dar (z. |
| [MergeFieldImageDimensionUnit](../com.aspose.words/mergefieldimagedimensionunit/) | Gibt eine Einheit einer Bilddimension an (z. |
| [MergeFormatMode](../com.aspose.words/mergeformatmode/) | Gibt an, wie Formatierungen beim Zusammenführen mehrerer Dokumente zusammengeführt werden. |
| [Merger](../com.aspose.words/merger/) | Stellt eine Gruppe von Methoden dar, die dazu dienen, verschiedene Dokumenttypen zu einem einzigen Ausgabedokument zusammenzuführen. |
| [MergerContext](../com.aspose.words/mergercontext/) | Dokumentzusammenführungs-Kontext. |
| [MetafileRenderingMode](../com.aspose.words/metafilerenderingmode/) | Gibt an, wie Aspose.Words WMF- und EMF-Metadateien rendern soll. |
| [MetafileRenderingOptions](../com.aspose.words/metafilerenderingoptions/) | Ermöglicht die Angabe zusätzlicher Renderoptionen für Metadateien. |
| [Metered](../com.aspose.words/metered/) | Stellt Methoden zum Festlegen des gemessenen Schlüssels bereit. |
| [MorphDataControl](../com.aspose.words/morphdatacontrol/) | Die MorphDataControl-Struktur ist eine Zusammenstellung von sechs Steuerelementen: CheckBox, ComboBox, ListBox, OptionButton, TextBox und ToggleButton. |
| [MsWordVersion](../com.aspose.words/mswordversion/) | Ermöglicht Aspose.Wods, das versionsspezifische Anwendungsverhalten von MS Word nachzuahmen. |
| [MultiPageLayout](../com.aspose.words/multipagelayout/) | Definiert ein Layout zum Rendern mehrerer Seiten in einer einzigen Ausgabe. |
| [MultiplePagesType](../com.aspose.words/multiplepagestype/) | Gibt an, wie das Dokument gedruckt wird. |
| [MustacheTag](../com.aspose.words/mustachetag/) | Stellt das "mustache"-Tag dar. |
| [NativeLibSettings](../com.aspose.words/nativelibsettings/) | Diese Klasse hilft beim Festlegen verschiedener Optionen, wie z. B. des temporären Ordners für native Bibliotheken von Aspose.Words und ob native Bibliotheken geladen und verwendet werden sollen. |
| [Node](../com.aspose.words/node/) | Basisklasse für alle Knoten eines Word-Dokuments. |
| [NodeChangingAction](../com.aspose.words/nodechangingaction/) | Gibt den Typ der Knotenänderung an. |
| [NodeChangingArgs](../com.aspose.words/nodechangingargs/) | Stellt Daten für Methoden des [INodeChangingCallback](../com.aspose.words/inodechangingcallback/)‑Interfaces bereit. |
| [NodeCollection](../com.aspose.words/nodecollection/) | Stellt eine Sammlung von Knoten eines bestimmten Typs dar. |
| [NodeImporter](../com.aspose.words/nodeimporter/) | Ermöglicht das effiziente wiederholte Importieren von Knoten von einem Dokument in ein anderes. |
| [NodeList](../com.aspose.words/nodelist/) | Stellt eine Sammlung von Knoten dar, die einer mit der Methode [CompositeNode.\#selectNodes(java.lang.String)](../com.aspose.words/compositenode/\#selectNodes-java.lang.String) ausgeführten XPath‑Abfrage entsprechen. |
| [NodeRendererBase](../com.aspose.words/noderendererbase/) | Basisklasse für [ShapeRenderer](../com.aspose.words/shaperenderer/) und [OfficeMathRenderer](../com.aspose.words/officemathrenderer/). |
| [NodeType](../com.aspose.words/nodetype/) | Gibt den Typ eines Word-Dokumentknotens an. |
| [NumSpacing](../com.aspose.words/numspacing/) | Gibt mögliche Werte an, in denen die Ziffernabstände angezeigt werden können. |
| [NumberStyle](../com.aspose.words/numberstyle/) | Gibt den Zahlenstil für eine Liste, Fußnoten und Endnoten sowie Seitenzahlen an. |
| [NumeralFormat](../com.aspose.words/numeralformat/) | Zeigt das Symbolset an, das zur Darstellung von Zahlen beim Rendern in feste Seitenformate verwendet wird. |
| [Odso](../com.aspose.words/odso/) | Gibt die Einstellungen des Office Data Source Object (ODSO) für eine Seriendruck-Datenquelle an. |
| [OdsoDataSourceType](../com.aspose.words/odsodatasourcetype/) | Gibt den Typ der externen Datenquelle an, die im Rahmen der ODSO-Verbindungsinformationen verbunden werden soll. |
| [OdsoFieldMapData](../com.aspose.words/odsofieldmapdata/) | Gibt an, wie eine Spalte in der externen Datenquelle den vordefinierten Seriendruckfeldern im Dokument zugeordnet wird. |
| [OdsoFieldMapDataCollection](../com.aspose.words/odsofieldmapdatacollection/) | Eine typisierte Sammlung der [OdsoFieldMapData](../com.aspose.words/odsofieldmapdata/)‑Objekte. |
| [OdsoFieldMappingType](../com.aspose.words/odsofieldmappingtype/) | Gibt die möglichen Typen an, die verwendet werden, um anzuzeigen, ob ein bestimmtes Seriendruckfeld einer Spalte in der angegebenen externen Datenquelle zugeordnet wurde. |
| [OdsoRecipientData](../com.aspose.words/odsorecipientdata/) | Stellt Informationen über einen einzelnen Datensatz in einer externen Datenquelle dar, der vom Seriendruck ausgeschlossen werden soll. |
| [OdsoRecipientDataCollection](../com.aspose.words/odsorecipientdatacollection/) | Eine typisierte Sammlung von [OdsoRecipientData](../com.aspose.words/odsorecipientdata/) |
| [OdtSaveMeasureUnit](../com.aspose.words/odtsavemeasureunit/) | Angegebene Maßeinheiten, die beim Speichern auf messbaren Dokumentinhalt wie Formen, Breiten und andere angewendet werden. |
| [OdtSaveOptions](../com.aspose.words/odtsaveoptions/) | Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im [SaveFormat.\#ODT](../com.aspose.words/saveformat/\#ODT)- oder [SaveFormat.\#OTT](../com.aspose.words/saveformat/\#OTT)-Format anzugeben. |
| [OfficeMath](../com.aspose.words/officemath/) | Stellt ein Office‑Math‑Objekt dar, wie z. B. eine Funktion, Gleichung, Matrix oder Ähnliches. |
| [OfficeMathDisplayType](../com.aspose.words/officemathdisplaytype/) | Gibt den Anzeigetyp des Gleichungsformats an. |
| [OfficeMathJustification](../com.aspose.words/officemathjustification/) | Gibt die Ausrichtung der Gleichung an. |
| [OfficeMathRenderer](../com.aspose.words/officemathrenderer/) | Stellt Methoden bereit, um ein einzelnes [OfficeMath](../com.aspose.words/officemath/) in ein Raster‑ oder Vektorbild oder in ein Graphics‑Objekt zu rendern. |
| [OleControl](../com.aspose.words/olecontrol/) | Stellt ein OLE‑ActiveX‑Steuerelement dar. |
| [OleFormat](../com.aspose.words/oleformat/) | Bietet Zugriff auf die Daten eines OLE‑Objekts oder ActiveX‑Steuerelements. |
| [OlePackage](../com.aspose.words/olepackage/) | Ermöglicht den Zugriff auf OLE‑Package‑Eigenschaften. |
| [OoxmlCompliance](../com.aspose.words/ooxmlcompliance/) | Ermöglicht die Angabe, welche OOXML‑Spezifikation beim Speichern im DOCX‑Format verwendet wird. |
| [OoxmlSaveOptions](../com.aspose.words/ooxmlsaveoptions/) | Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im [SaveFormat.\#DOCX](../com.aspose.words/saveformat/\#DOCX), [SaveFormat.\#DOCM](../com.aspose.words/saveformat/\#DOCM), [SaveFormat.\#DOTX](../com.aspose.words/saveformat/\#DOTX), [SaveFormat.\#DOTM](../com.aspose.words/saveformat/\#DOTM)‑ oder [SaveFormat.\#FLAT\_OPC](../com.aspose.words/saveformat/\#FLAT-OPC)‑Format anzugeben. |
| [OpenAiModel](../com.aspose.words/openaimodel/) | Klasse, die die Integration von OpenAi‑Modellen in Aspose.Words darstellt. |
| [OptionButtonControl](../com.aspose.words/optionbuttoncontrol/) | Das OptionButton‑Steuerelement ermöglicht eine einzelne Auswahl in einer begrenzten Menge gegenseitig ausschließender Optionen. |
| [Orientation](../com.aspose.words/orientation/) | Gibt die Seitenausrichtung an. |
| [OutlineLevel](../com.aspose.words/outlinelevel/) | Gibt die Gliederungsebene eines Absatzes im Dokument an. |
| [OutlineOptions](../com.aspose.words/outlineoptions/) | Ermöglicht die Angabe von Gliederungsoptionen. |
| [PageBorderAppliesTo](../com.aspose.words/pageborderappliesto/) | Gibt an, auf welchen Seiten der Seitenrand gedruckt wird. |
| [PageBorderDistanceFrom](../com.aspose.words/pageborderdistancefrom/) | Gibt die Position des Seitenrands relativ zum Seitenrand an. |
| [PageExtractOptions](../com.aspose.words/pageextractoptions/) | Ermöglicht die Angabe von Optionen für das Extrahieren von Dokumentseiten. |
| [PageInfo](../com.aspose.words/pageinfo/) | Stellt Informationen über eine bestimmte Dokumentseite dar. |
| [PageLayoutCallbackArgs](../com.aspose.words/pagelayoutcallbackargs/) | Ein Argument, das an [IPageLayoutCallback.\#notify(com.aspose.words.PageLayoutCallbackArgs)](../com.aspose.words/ipagelayoutcallback/\#notify-com.aspose.words.PageLayoutCallbackArgs) übergeben wird. |
| [PageLayoutEvent](../com.aspose.words/pagelayoutevent/) | Ein Ereigniscode, der während des Aufbaus und Renderns des Seitenlayout‑Modells ausgelöst wird. |
| [PageRange](../com.aspose.words/pagerange/) | Stellt einen zusammenhängenden Seitenbereich dar. |
| [PageSavingArgs](../com.aspose.words/pagesavingargs/) | Stellt Daten für das Ereignis [IPageSavingCallback.\#pageSaving(com.aspose.words.PageSavingArgs)](../com.aspose.words/ipagesavingcallback/\#pageSaving-com.aspose.words.PageSavingArgs) bereit. |
| [PageSet](../com.aspose.words/pageset/) | Beschreibt eine zufällige Menge von Seiten. |
| [PageSetup](../com.aspose.words/pagesetup/) | Stellt die Seiteneinrichtungseigenschaften eines Abschnitts dar. |
| [PageVerticalAlignment](../com.aspose.words/pageverticalalignment/) | Gibt die vertikale Ausrichtung des Textes auf jeder Seite an. |
| [PaperSize](../com.aspose.words/papersize/) | Gibt die Papiergröße an. |
| [Paragraph](../com.aspose.words/paragraph/) | Stellt einen Textabsatz dar. |
| [ParagraphAlignment](../com.aspose.words/paragraphalignment/) | Gibt die Textausrichtung in einem Absatz an. |
| [ParagraphCollection](../com.aspose.words/paragraphcollection/) | Bietet typisierten Zugriff auf eine Sammlung von [Paragraph](../com.aspose.words/paragraph/) Knoten. |
| [ParagraphFormat](../com.aspose.words/paragraphformat/) | Stellt die gesamte Formatierung für einen Absatz dar. |
| [PatternType](../com.aspose.words/patterntype/) | Gibt das Füllmuster an, das zum Ausfüllen einer Form verwendet werden soll. |
| [PclSaveOptions](../com.aspose.words/pclsaveoptions/) | Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im [SaveFormat.\#PCL](../com.aspose.words/saveformat/\#PCL)-Format anzugeben. |
| [PdfAttachmentsEmbeddingMode](../com.aspose.words/pdfattachmentsembeddingmode/) | Gibt an, wie Anhänge in ein PDF-Dokument eingebettet werden. |
| [PdfCompliance](../com.aspose.words/pdfcompliance/) | Gibt das Konformitätsniveau der PDF-Standards an. |
| [PdfCustomPropertiesExport](../com.aspose.words/pdfcustompropertiesexport/) | Gibt an, wie [Document.\#getCustomDocumentProperties()](../com.aspose.words/document/\#getCustomDocumentProperties) in eine PDF-Datei exportiert werden. |
| [PdfDigitalSignatureDetails](../com.aspose.words/pdfdigitalsignaturedetails/) | Enthält Details zum Signieren eines PDF-Dokuments mit einer digitalen Signatur. |
| [PdfDigitalSignatureHashAlgorithm](../com.aspose.words/pdfdigitalsignaturehashalgorithm/) | Gibt einen digitalen Hash-Algorithmus an, der von einer digitalen Signatur verwendet wird. |
| [PdfDigitalSignatureTimestampSettings](../com.aspose.words/pdfdigitalsignaturetimestampsettings/) | Enthält Einstellungen des Zeitstempels der digitalen Signatur. |
| [PdfEncryptionDetails](../com.aspose.words/pdfencryptiondetails/) | Enthält Details zur Verschlüsselung und zu Zugriffsberechtigungen für ein PDF-Dokument. |
| [PdfFontEmbeddingMode](../com.aspose.words/pdffontembeddingmode/) | Gibt an, wie Aspose.Words Schriftarten einbetten soll. |
| [PdfImageColorSpaceExportMode](../com.aspose.words/pdfimagecolorspaceexportmode/) | Gibt an, wie der Farbraum für die Bilder im PDF-Dokument ausgewählt wird. |
| [PdfImageCompression](../com.aspose.words/pdfimagecompression/) | Gibt den Kompressionstyp an, der auf Bilder in der PDF-Datei angewendet wird. |
| [PdfLoadOptions](../com.aspose.words/pdfloadoptions/) | Ermöglicht das Angeben zusätzlicher Optionen beim Laden eines PDF-Dokuments in ein [Document](../com.aspose.words/document/)-Objekt. |
| [PdfPageLayout](../com.aspose.words/pdfpagelayout/) | Gibt das Seitenlayout an, das verwendet werden soll, wenn das Dokument in einem PDF‑Reader geöffnet wird. |
| [PdfPageMode](../com.aspose.words/pdfpagemode/) | Gibt an, wie das PDF-Dokument angezeigt werden soll, wenn es im PDF‑Reader geöffnet wird. |
| [PdfPermissions](../com.aspose.words/pdfpermissions/) | Gibt die Vorgänge an, die einem Benutzer bei einem verschlüsselten PDF-Dokument erlaubt sind. |
| [PdfSaveOptions](../com.aspose.words/pdfsaveoptions/) | Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im [SaveFormat.\#PDF](../com.aspose.words/saveformat/\#PDF)-Format anzugeben. |
| [PdfTextCompression](../com.aspose.words/pdftextcompression/) | Gibt einen Kompressionstyp an, der auf alle Inhalte in der PDF-Datei außer Bildern angewendet wird. |
| [PdfZoomBehavior](../com.aspose.words/pdfzoombehavior/) | Gibt den Zoomtyp an, der auf ein PDF‑Dokument angewendet wird, wenn es in einem PDF‑Betrachter geöffnet wird. |
| [Person](../com.aspose.words/person/) | Stellt einen einzelnen (eine Person) Bibliografie‑Quellenbeitragenden dar. |
| [PersonCollection](../com.aspose.words/personcollection/) | Stellt eine Liste von Personen dar, die Bibliografie‑Quellenbeitragende sind. |
| [PhoneticGuide](../com.aspose.words/phoneticguide/) | Stellt die phonetische Anleitung dar. |
| [PhysicalFontInfo](../com.aspose.words/physicalfontinfo/) | Gibt Informationen über physische Schriftarten an, die dem Aspose.Words‑Schrift‑Engine zur Verfügung stehen. |
| [PlainTextDocument](../com.aspose.words/plaintextdocument/) | Ermöglicht das Extrahieren einer Nur‑Text‑Darstellung des Inhalts des Dokuments. |
| [PreferredWidth](../com.aspose.words/preferredwidth/) | Stellt einen Wert und seine Maßeinheit dar, die zur Angabe der bevorzugten Breite einer Tabelle oder einer Zelle verwendet werden. |
| [PreferredWidthType](../com.aspose.words/preferredwidthtype/) | Gibt die Maßeinheit für die bevorzugte Breite einer Tabelle oder Zelle an. |
| [PresetTexture](../com.aspose.words/presettexture/) | Gibt die Textur an, die zum Füllen einer Form verwendet wird. |
| [Processor](../com.aspose.words/processor/) | Prozessor‑Klasse zur Durchführung verschiedener Dokumentenverarbeitungsaktionen. |
| [ProcessorContext](../com.aspose.words/processorcontext/) | Basisklasse für Prozessor‑Kontexte. |
| [PropertyType](../com.aspose.words/propertytype/) | Gibt den Datentyp einer Dokumenteneigenschaft an. |
| [ProtectionType](../com.aspose.words/protectiontype/) | Schutztyp für ein Dokument. |
| [PsSaveOptions](../com.aspose.words/pssaveoptions/) | Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im [SaveFormat.#PS](../com.aspose.words/saveformat/#PS)-Format anzugeben. |
| [Range](../com.aspose.words/range/) | Stellt einen zusammenhängenden Bereich in einem Dokument dar. |
| [ReadabilityStatistics](../com.aspose.words/readabilitystatistics/) | Stellt Informationen über die Lesbarkeitsbewertung eines Dokuments bereit. |
| [ReflectionFormat](../com.aspose.words/reflectionformat/) | Stellt die Reflexionsformatierung für ein Objekt dar. |
| [RelativeHorizontalPosition](../com.aspose.words/relativehorizontalposition/) | Gibt an, worauf sich die horizontale Position einer Form oder eines Textfelds bezieht. |
| [RelativeHorizontalSize](../com.aspose.words/relativehorizontalsize/) | Gibt relativ an, worauf die Breite einer Form oder eines Textfelds horizontal berechnet wird. |
| [RelativeVerticalPosition](../com.aspose.words/relativeverticalposition/) | Gibt an, worauf sich die vertikale Position einer Form oder eines Textfelds bezieht. |
| [RelativeVerticalSize](../com.aspose.words/relativeverticalsize/) | Gibt relativ an, worauf die Höhe einer Form oder eines Textfelds vertikal berechnet wird. |
| [ReplaceAction](../com.aspose.words/replaceaction/) | Ermöglicht dem Benutzer anzugeben, was mit dem aktuellen Treffer während einer Ersetzungsoperation geschieht. |
| [ReplacementFormat](../com.aspose.words/replacementformat/) | Gibt das Ersetzungsformat an. |
| [Replacer](../com.aspose.words/replacer/) | Stellt Methoden bereit, die zum Suchen und Ersetzen von Text im Dokument gedacht sind. |
| [ReplacerContext](../com.aspose.words/replacercontext/) | Kontext der Suchen/Ersetzen‑Operation. |
| [ReplacingArgs](../com.aspose.words/replacingargs/) | Stellt Daten für einen benutzerdefinierten Ersetzungsvorgang bereit. |
| [ReportBuildOptions](../com.aspose.words/reportbuildoptions/) | Gibt Optionen an, die das Verhalten von [ReportingEngine](../com.aspose.words/reportingengine/) beim Erstellen eines Berichts steuern. |
| [ReportBuilder](../com.aspose.words/reportbuilder/) | Stellt Methoden bereit, die dazu dienen, Vorlagen mit Daten mithilfe der LINQ Reporting Engine zu füllen. |
| [ReportBuilderContext](../com.aspose.words/reportbuildercontext/) | LINQ Reporting Engine-Kontext. |
| [ReportBuilderOptions](../com.aspose.words/reportbuilderoptions/) | Stellt Optionen für die Funktionalität der LINQ Reporting Engine dar. |
| [ReportingEngine](../com.aspose.words/reportingengine/) | Stellt Routinen zum Befüllen von Vorlagendokumenten mit Daten sowie eine Reihe von Einstellungen zur Steuerung dieser Routinen bereit. |
| [ResourceLoadingAction](../com.aspose.words/resourceloadingaction/) | Gibt den Modus des Ressourcenladens an. |
| [ResourceLoadingArgs](../com.aspose.words/resourceloadingargs/) | Stellt Daten für die Methode [IResourceLoadingCallback.\#resourceLoading(com.aspose.words.ResourceLoadingArgs)](../com.aspose.words/iresourceloadingcallback/\#resourceLoading-com.aspose.words.ResourceLoadingArgs) bereit. |
| [ResourceSavingArgs](../com.aspose.words/resourcesavingargs/) | Stellt Daten für das Ereignis [IResourceSavingCallback.\#resourceSaving(com.aspose.words.ResourceSavingArgs)](../com.aspose.words/iresourcesavingcallback/\#resourceSaving-com.aspose.words.ResourceSavingArgs) bereit. |
| [ResourceType](../com.aspose.words/resourcetype/) | Typ der geladenen Ressource. |
| [Revision](../com.aspose.words/revision/) | Stellt eine Revision (nachverfolgte Änderung) in einem Dokumentknoten oder Stil dar. |
| [RevisionCollection](../com.aspose.words/revisioncollection/) | Eine Sammlung von [Revision](../com.aspose.words/revision/)-Objekten, die Revisionen im Dokument darstellen. |
| [RevisionColor](../com.aspose.words/revisioncolor/) | Ermöglicht die Angabe der Farbe von Dokumentrevisionen. |
| [RevisionGroup](../com.aspose.words/revisiongroup/) | Stellt eine Gruppe von aufeinanderfolgenden [Revision](../com.aspose.words/revision/)-Objekten dar. |
| [RevisionGroupCollection](../com.aspose.words/revisiongroupcollection/) | Eine Sammlung von [RevisionGroup](../com.aspose.words/revisiongroup/)-Objekten, die Revisionsgruppen im Dokument darstellen. |
| [RevisionOptions](../com.aspose.words/revisionoptions/) | Ermöglicht die Steuerung, wie Dokumentrevisionen während des Layoutvorgangs verarbeitet werden. |
| [RevisionTextEffect](../com.aspose.words/revisiontexteffect/) | Ermöglicht die Angabe eines Dekorationseffekts für Revisionen von Dokumenttext. |
| [RevisionType](../com.aspose.words/revisiontype/) | Gibt den Typ der nachverfolgten Änderung in [Revision](../com.aspose.words/revision/) an. |
| [RevisionsView](../com.aspose.words/revisionsview/) | Ermöglicht die Angabe, ob mit der Original- oder der überarbeiteten Version eines Dokuments gearbeitet werden soll. |
| [Row](../com.aspose.words/row/) | Stellt eine Tabellenzeile dar. |
| [RowCollection](../com.aspose.words/rowcollection/) | Stellt typisierten Zugriff auf eine Sammlung von [Row](../com.aspose.words/row/)-Knoten bereit. |
| [RowFormat](../com.aspose.words/rowformat/) | Stellt die gesamte Formatierung einer Tabellenzeile dar. |
| [RtfLoadOptions](../com.aspose.words/rtfloadoptions/) | Ermöglicht die Angabe zusätzlicher Optionen beim Laden eines [LoadFormat.\#RTF](../com.aspose.words/loadformat/\#RTF)-Dokuments in ein [Document](../com.aspose.words/document/)-Objekt. |
| [RtfSaveOptions](../com.aspose.words/rtfsaveoptions/) | Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im [SaveFormat.\#RTF](../com.aspose.words/saveformat/\#RTF)-Format anzugeben. |
| [Run](../com.aspose.words/run/) | Stellt einen Lauf von Zeichen mit derselben Schriftformatierung dar. |
| [RunCollection](../com.aspose.words/runcollection/) | Bietet typisierten Zugriff auf eine Sammlung von [Run](../com.aspose.words/run/) Knoten. |
| [SaveFormat](../com.aspose.words/saveformat/) | Gibt das Format an, in dem das Dokument gespeichert wird. |
| [SaveOptions](../com.aspose.words/saveoptions/) | Dies ist eine abstrakte Basisklasse für Klassen, die dem Benutzer ermöglichen, zusätzliche Optionen beim Speichern eines Dokuments in einem bestimmten Format anzugeben. |
| [SaveOutputParameters](../com.aspose.words/saveoutputparameters/) | Dieses Objekt wird nach dem Speichern eines Dokuments an den Aufrufer zurückgegeben und enthält zusätzliche Informationen, die während des Speicher‑Vorgangs erzeugt oder berechnet wurden. |
| [ScriptShapingLevel](../com.aspose.words/scriptshapinglevel/) | Beschreibt die vom Skript benötigten Shaping‑Ebenen. |
| [SdtAppearance](../com.aspose.words/sdtappearance/) | Legt das Erscheinungsbild eines strukturierten Dokumenttags fest. |
| [SdtCalendarType](../com.aspose.words/sdtcalendartype/) | Gibt die möglichen Kalendertypen an, die verwendet werden können, um [StructuredDocumentTag.\#getCalendarType()](../com.aspose.words/structureddocumenttag/\#getCalendarType) / [StructuredDocumentTag.\#setCalendarType(int)](../com.aspose.words/structureddocumenttag/\#setCalendarType-int) in einem Office Open XML‑Dokument zu spezifizieren. |
| [SdtDateStorageFormat](../com.aspose.words/sdtdatestorageformat/) | Gibt an, wie das Datum für ein Datums‑SDT gespeichert/abgerufen wird, wenn das SDT an einen XML‑Knoten im Datenspeicher des Dokuments gebunden ist. |
| [SdtListItem](../com.aspose.words/sdtlistitem/) | Dieses Element gibt ein einzelnes Listenelement innerhalb eines übergeordneten [SdtType.\#COMBO\_BOX](../com.aspose.words/sdttype/\#COMBO-BOX) oder [SdtType.\#DROP\_DOWN\_LIST](../com.aspose.words/sdttype/\#DROP-DOWN-LIST) strukturierten Dokumenttags an. |
| [SdtListItemCollection](../com.aspose.words/sdtlistitemcollection/) | Bietet Zugriff auf [SdtListItem](../com.aspose.words/sdtlistitem/)‑Elemente eines strukturierten Dokumenttags. |
| [SdtType](../com.aspose.words/sdttype/) | Gibt den Typ eines strukturierten Dokumenttags‑Knotens (SDT) an. |
| [Section](../com.aspose.words/section/) | Stellt einen einzelnen Abschnitt in einem Dokument dar. |
| [SectionCollection](../com.aspose.words/sectioncollection/) | Eine Sammlung von [Section](../com.aspose.words/section/)‑Objekten im Dokument. |
| [SectionLayoutMode](../com.aspose.words/sectionlayoutmode/) | Legt den Layout‑Modus für einen Abschnitt fest, der die Definition des Dokument‑Gitternetz‑Verhaltens ermöglicht. |
| [SectionStart](../com.aspose.words/sectionstart/) | Der Typ des Umbruchs zu Beginn des Abschnitts. |
| [Shading](../com.aspose.words/shading/) | Enthält Schattierungsattribute für ein Objekt. |
| [ShadowFormat](../com.aspose.words/shadowformat/) | Stellt Schattierungsformatierung für ein Objekt dar. |
| [ShadowType](../com.aspose.words/shadowtype/) | Gibt den Typ eines Formschattens an. |
| [Shape](../com.aspose.words/shape/) | Stellt ein Objekt in der Zeichnungsebene dar, z. B. eine AutoShape, ein Textfeld, eine Freiform, ein OLE‑Objekt, ein ActiveX‑Steuerelement oder ein Bild. |
| [ShapeBase](../com.aspose.words/shapebase/) | Basisklasse für Objekte in der Zeichnungsebene, wie eine AutoShape, Freiform, OLE‑Objekt, ActiveX‑Steuerelement oder Bild. |
| [ShapeLineStyle](../com.aspose.words/shapelinestyle/) | Gibt den zusammengesetzten Linienstil einer [Shape](../com.aspose.words/shape/) an. |
| [ShapeMarkupLanguage](../com.aspose.words/shapemarkuplanguage/) | Gibt die für die Form verwendete Auszeichnungssprache an. |
| [ShapeRenderer](../com.aspose.words/shaperenderer/) | Bietet Methoden zum Rendern einer einzelnen [Shape](../com.aspose.words/shape/) oder [GroupShape](../com.aspose.words/groupshape/) in ein Raster‑ oder Vektorbild bzw. in ein Graphics‑Objekt. |
| [ShapeTextOrientation](../com.aspose.words/shapetextorientation/) | Gibt die Ausrichtung des Textes in Formen an. |
| [ShapeType](../com.aspose.words/shapetype/) | Gibt den Typ einer Form in einem Microsoft‑Word‑Dokument an. |
| [ShowInBalloons](../com.aspose.words/showinballoons/) | Gibt an, welche Revisionen in Ballons dargestellt werden. |
| [SignOptions](../com.aspose.words/signoptions/) | Ermöglicht das Festlegen von Optionen für die Dokumentenunterzeichnung. |
| [SignatureLine](../com.aspose.words/signatureline/) | Stellt Zugriff auf Eigenschaften der Signaturzeile bereit. |
| [SignatureLineOptions](../com.aspose.words/signaturelineoptions/) | Ermöglicht das Festlegen von Optionen für das Einfügen einer Signaturzeile. |
| [SignerContext](../com.aspose.words/signercontext/) | Kontext des Dokumentenunterzeichners |
| [SmartTag](../com.aspose.words/smarttag/) | Dieses Element gibt das Vorhandensein eines SmartTags um ein oder mehrere Inline-Strukturen (Runs, Bilder, Felder usw.) innerhalb eines Absatzes an. |
| [SoftEdgeFormat](../com.aspose.words/softedgeformat/) | Stellt die Weichkant-Formatierung für ein Objekt dar. |
| [Source](../com.aspose.words/source/) | Stellt eine einzelne Quelle dar, z. B. ein Buch, einen Zeitschriftenartikel oder ein Interview. |
| [SourceType](../com.aspose.words/sourcetype/) | Stellt Bibliographie-Quelltypen dar. |
| [SpecialChar](../com.aspose.words/specialchar/) | Basisklasse für Sonderzeichen im Dokument. |
| [SplitCriteria](../com.aspose.words/splitcriteria/) | Gibt an, wie das Dokument in Teile aufgeteilt wird. |
| [SplitOptions](../com.aspose.words/splitoptions/) | Gibt Optionen an, wie das Dokument in Teile aufgeteilt wird. |
| [Splitter](../com.aspose.words/splitter/) | Stellt Methoden bereit, die dazu dienen, Dokumente anhand verschiedener Kriterien in Teile zu splitten. |
| [SplitterContext](../com.aspose.words/splittercontext/) | Kontext des Dokumententeilers. |
| [Story](../com.aspose.words/story/) | Basisklasse für Elemente, die Block‑Ebene‑Knoten [Paragraph](../com.aspose.words/paragraph/) und [Table](../com.aspose.words/table/) enthalten. |
| [StoryType](../com.aspose.words/storytype/) | Der Text eines Word‑Dokuments wird in Stories gespeichert. |
| [StreamFontSource](../com.aspose.words/streamfontsource/) | Basisklasse für benutzerdefinierte Stream‑Schriftquellen. |
| [Stroke](../com.aspose.words/stroke/) | Definiert einen Strich für eine Form. |
| [StructuredDocumentTag](../com.aspose.words/structureddocumenttag/) | Stellt ein strukturiertes Dokument-Tag (SDT oder Inhaltssteuerelement) in einem Dokument dar. |
| [StructuredDocumentTagCollection](../com.aspose.words/structureddocumenttagcollection/) | Eine Sammlung von [IStructuredDocumentTag](../com.aspose.words/istructureddocumenttag/)-Instanzen, die die strukturierten Dokument-Tags im angegebenen Bereich darstellen. |
| [StructuredDocumentTagRangeEnd](../com.aspose.words/structureddocumenttagrangeend/) | Stellt das Ende eines **ranged** strukturierten Dokument-Tags dar, das Inhalte aus mehreren Abschnitten akzeptiert. |
| [StructuredDocumentTagRangeStart](../com.aspose.words/structureddocumenttagrangestart/) | Stellt den Anfang eines **ranged** strukturierten Dokument-Tags dar, das Inhalte aus mehreren Abschnitten akzeptiert. |
| [Style](../com.aspose.words/style/) | Stellt einen einzelnen integrierten oder benutzerdefinierten Stil dar. |
| [StyleCollection](../com.aspose.words/stylecollection/) | Eine Sammlung von [Style](../com.aspose.words/style/)-Objekten, die sowohl die integrierten als auch die benutzerdefinierten Stile in einem Dokument darstellen. |
| [StyleIdentifier](../com.aspose.words/styleidentifier/) | Sprachunabhängiger Stil‑Bezeichner. |
| [StyleType](../com.aspose.words/styletype/) | Stellt den Typ des Stils dar. |
| [SubDocument](../com.aspose.words/subdocument/) | Stellt ein **SubDocument** \- dar, das eine Referenz zu einem extern gespeicherten Dokument ist. |
| [SummarizeOptions](../com.aspose.words/summarizeoptions/) | Ermöglicht das Angeben verschiedener Optionen zum Zusammenfassen des Dokumentinhalts. |
| [SummaryLength](../com.aspose.words/summarylength/) | Enumeriert mögliche Längen der Zusammenfassung. |
| [SuperUserJwtTokenRequestHandler](../com.aspose.words/superuserjwttokenrequesthandler/) | JWT Token Request Handler mit Caching, lokaler Validierung und Circuit Breaker. |
| [SvgSaveOptions](../com.aspose.words/svgsaveoptions/) | Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im [SaveFormat.\#SVG](../com.aspose.words/saveformat/\#SVG)-Format anzugeben. |
| [SvgTextOutputMode](../com.aspose.words/svgtextoutputmode/) | Ermöglicht die Angabe, wie Text innerhalb eines Dokuments beim Speichern im SVG-Format gerendert werden soll. |
| [SystemFontSource](../com.aspose.words/systemfontsource/) | Stellt alle im System installierten TrueType-Schriften dar. |
| [TabAlignment](../com.aspose.words/tabalignment/) | Gibt die Ausrichtung/den Typ eines Tabstopps an. |
| [TabLeader](../com.aspose.words/tableader/) | Gibt den Typ der Führungs‑Linie an, die unter dem Tab‑Zeichen angezeigt wird. |
| [TabStop](../com.aspose.words/tabstop/) | Stellt einen einzelnen benutzerdefinierten Tabstopp dar. |
| [TabStopCollection](../com.aspose.words/tabstopcollection/) | Eine Sammlung von [TabStop](../com.aspose.words/tabstop/)-Objekten, die benutzerdefinierte Tabs für einen Absatz oder einen Stil darstellen. |
| [Table](../com.aspose.words/table/) | Stellt eine Tabelle in einem Word-Dokument dar. |
| [TableAlignment](../com.aspose.words/tablealignment/) | Gibt die Ausrichtung für eine Inline‑Tabelle an. |
| [TableCollection](../com.aspose.words/tablecollection/) | Bietet typisierten Zugriff auf eine Sammlung von [Table](../com.aspose.words/table/)-Knoten. |
| [TableContentAlignment](../com.aspose.words/tablecontentalignment/) | Ermöglicht die Angabe der Ausrichtung des Tabelleninhalts, die beim Exportieren in das Markdown-Format verwendet wird. |
| [TableStyle](../com.aspose.words/tablestyle/) | Stellt einen Tabellenstil dar. |
| [TableStyleOptions](../com.aspose.words/tablestyleoptions/) | Gibt an, wie ein Tabellenstil auf eine Tabelle angewendet wird. |
| [TableSubstitutionRule](../com.aspose.words/tablesubstitutionrule/) | Regel für die Schriftart‑Substitution in Tabellen. |
| [TaskPane](../com.aspose.words/taskpane/) | Stellt ein Add‑In‑Task‑Pane‑Objekt dar. |
| [TaskPaneCollection](../com.aspose.words/taskpanecollection/) | Gibt eine Liste von persistierten Task‑Pane‑Objekten an. |
| [TaskPaneDockState](../com.aspose.words/taskpanedockstate/) | Enumeriert verfügbare Positionen des Task‑Pane‑Objekts. |
| [TextBox](../com.aspose.words/textbox/) | Definiert Attribute, die angeben, wie ein Text innerhalb einer Form angezeigt wird. |
| [TextBoxAnchor](../com.aspose.words/textboxanchor/) | Gibt Werte für die vertikale Ausrichtung von Formtext an. |
| [TextBoxControl](../com.aspose.words/textboxcontrol/) | Das TextBox‑Steuerelement zeigt Text aus einem organisierten Datensatz oder Benutzereingaben an. |
| [TextBoxWrapMode](../com.aspose.words/textboxwrapmode/) | Gibt an, wie Text innerhalb einer Form umbrochen wird. |
| [TextColumn](../com.aspose.words/textcolumn/) | Stellt eine einzelne Textspalte dar. |
| [TextColumnCollection](../com.aspose.words/textcolumncollection/) | Eine Sammlung von [TextColumn](../com.aspose.words/textcolumn/)-Objekten, die alle Textspalten in einem Abschnitt eines Dokuments darstellen. |
| [TextDmlEffect](../com.aspose.words/textdmleffect/) | Dml-Texteffekt für Textläufe. |
| [TextEffect](../com.aspose.words/texteffect/) | Animationseffekt für Textläufe. |
| [TextFormFieldType](../com.aspose.words/textformfieldtype/) | Gibt den Typ eines Textformularfelds an. |
| [TextOrientation](../com.aspose.words/textorientation/) | Gibt die Ausrichtung des Textes auf einer Seite, in einer Tabellenzelle oder einem Textrahmen an. |
| [TextPath](../com.aspose.words/textpath/) | Definiert den Text und die Formatierung des Textpfads (eines WordArt-Objekts). |
| [TextPathAlignment](../com.aspose.words/textpathalignment/) | WordArt-Ausrichtung. |
| [TextWatermarkOptions](../com.aspose.words/textwatermarkoptions/) | Enthält Optionen, die beim Hinzufügen eines Wasserzeichens mit Text angegeben werden können. |
| [TextWrapping](../com.aspose.words/textwrapping/) | Gibt an, wie Text um die Tabelle herumfließt. |
| [TextureAlignment](../com.aspose.words/texturealignment/) | Gibt die Ausrichtung für das Kacheln der Texturfüllung an. |
| [TextureIndex](../com.aspose.words/textureindex/) | Gibt die Schattierungstextur an. |
| [Theme](../com.aspose.words/theme/) | Stellt das Dokumententhema dar und bietet Zugriff auf die wichtigsten Thementeile, einschließlich [Theme.\#getMajorFonts()](../com.aspose.words/theme/\#getMajorFonts), [Theme.\#getMinorFonts()](../com.aspose.words/theme/\#getMinorFonts) und [Theme.\#getColors()](../com.aspose.words/theme/\#getColors). |
| [ThemeColor](../com.aspose.words/themecolor/) | Gibt die Themenfarben für Dokumententhemen an. |
| [ThemeColors](../com.aspose.words/themecolors/) | Stellt das Farbschema des Dokumententhemas dar, das zwölf Farben enthält. |
| [ThemeFont](../com.aspose.words/themefont/) | Gibt die Arten von Themen-Schriftartnamen für Dokumententhemen an. |
| [ThemeFonts](../com.aspose.words/themefonts/) | Stellt eine Sammlung von Schriftarten im Schriftartenschema dar und ermöglicht die Angabe verschiedener Schriftarten für unterschiedliche Sprachen [ThemeFonts.\#getLatin()](../com.aspose.words/themefonts/\#getLatin) / [ThemeFonts.\#setLatin(java.lang.String)](../com.aspose.words/themefonts/\#setLatin-java.lang.String), [ThemeFonts.\#getEastAsian()](../com.aspose.words/themefonts/\#getEastAsian) / [ThemeFonts.\#setEastAsian(java.lang.String)](../com.aspose.words/themefonts/\#setEastAsian-java.lang.String) und [ThemeFonts.\#getComplexScript()](../com.aspose.words/themefonts/\#getComplexScript) / [ThemeFonts.\#setComplexScript(java.lang.String)](../com.aspose.words/themefonts/\#setComplexScript-java.lang.String). |
| [ThumbnailGeneratingOptions](../com.aspose.words/thumbnailgeneratingoptions/) | Kann verwendet werden, um zusätzliche Optionen beim Erzeugen einer Miniaturansicht für ein Dokument anzugeben. |
| [TiffCompression](../com.aspose.words/tiffcompression/) | Gibt an, welche Art von Kompression beim Speichern von Seitenbildern in einer TIFF-Datei angewendet werden soll. |
| [ToaCategories](../com.aspose.words/toacategories/) | Stellt eine Tabelle von Autoritätskategorien dar. |
| [TxtExportHeadersFootersMode](../com.aspose.words/txtexportheadersfootersmode/) | Gibt an, wie Kopf- und Fußzeilen in das Klartextformat exportiert werden. |
| [TxtLeadingSpacesOptions](../com.aspose.words/txtleadingspacesoptions/) | Gibt die verfügbaren Optionen für die Behandlung von führenden Leerzeichen beim Import aus einer [LoadFormat.\#TEXT](../com.aspose.words/loadformat/\#TEXT)-Datei an. |
| [TxtListIndentation](../com.aspose.words/txtlistindentation/) | Gibt an, wie Listenebenen eingerückt werden, wenn das Dokument in das [SaveFormat.\#TEXT](../com.aspose.words/saveformat/\#TEXT)-Format exportiert wird. |
| [TxtLoadOptions](../com.aspose.words/txtloadoptions/) | Ermöglicht die Angabe zusätzlicher Optionen beim Laden eines [LoadFormat.\#TEXT](../com.aspose.words/loadformat/\#TEXT)-Dokuments in ein [Document](../com.aspose.words/document/)-Objekt. |
| [TxtOfficeMathExportMode](../com.aspose.words/txtofficemathexportmode/) | Gibt an, wie Aspose.Words OfficeMath nach [SaveFormat.#TEXT](../com.aspose.words/saveformat/#TEXT) exportiert. |
| [TxtSaveOptions](../com.aspose.words/txtsaveoptions/) | Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im [SaveFormat.#TEXT](../com.aspose.words/saveformat/#TEXT)-Format anzugeben. |
| [TxtSaveOptionsBase](../com.aspose.words/txtsaveoptionsbase/) | Die Basisklasse zum Angeben zusätzlicher Optionen beim Speichern eines Dokuments in textbasierte Formate. |
| [TxtTrailingSpacesOptions](../com.aspose.words/txttrailingspacesoptions/) | Gibt die verfügbaren Optionen für die Behandlung von nachgestellten Leerzeichen beim Import aus einer [LoadFormat.#TEXT](../com.aspose.words/loadformat/#TEXT)-Datei an. |
| [Underline](../com.aspose.words/underline/) | Gibt den Typ der Unterstreichung an, die auf eine Schriftart angewendet wird. |
| [UnicodeScript](../com.aspose.words/unicodescript/) | Unicode Character Database-Eigenschaft: Script (sc). |
| [UnsupportedEncryptionException](../com.aspose.words/unsupportedencryptionexception/) | Wird beim Laden eines Dokuments ausgelöst, wenn das Dokument mit einer nicht unterstützten Methode verschlüsselt ist. |
| [UnsupportedFileFormatException](../com.aspose.words/unsupportedfileformatexception/) | Wird beim Laden eines Dokuments ausgelöst, wenn das Dokumentformat nicht erkannt wird oder von Aspose.Words nicht unterstützt wird. |
| [UserInformation](../com.aspose.words/userinformation/) | Gibt Informationen über den Benutzer an. |
| [VariableCollection](../com.aspose.words/variablecollection/) | Eine Sammlung von Dokumentvariablen. |
| [VariationAxis](../com.aspose.words/variationaxis/) | Stellt das OpenType Design-Variation-Achsen-Tag dar. |
| [VariationAxisCoordinate](../com.aspose.words/variationaxiscoordinate/) | Stellt eine Achsenkoordinate dar. |
| [VbaModule](../com.aspose.words/vbamodule/) | Bietet Zugriff auf das VBA-Projektmodul. |
| [VbaModuleCollection](../com.aspose.words/vbamodulecollection/) | Stellt eine Sammlung von [VbaModule](../com.aspose.words/vbamodule/)‑Objekten dar. |
| [VbaModuleType](../com.aspose.words/vbamoduletype/) | Gibt den Typ eines Modells in einem VBA-Projekt an. |
| [VbaProject](../com.aspose.words/vbaproject/) | Bietet Zugriff auf VBA-Projektinformationen. |
| [VbaReference](../com.aspose.words/vbareference/) | Implementiert eine Referenz auf eine Automation-Typbibliothek oder ein VBA-Projekt. |
| [VbaReferenceCollection](../com.aspose.words/vbareferencecollection/) | Stellt eine Sammlung von [VbaReference](../com.aspose.words/vbareference/)‑Objekten dar. |
| [VbaReferenceType](../com.aspose.words/vbareferencetype/) | Ermöglicht die Angabe des Typs eines [VbaReference](../com.aspose.words/vbareference/)‑Objekts. |
| [VerticalAlignment](../com.aspose.words/verticalalignment/) | Gibt die vertikale Ausrichtung einer schwebenden Form, eines Textfelds oder einer schwebenden Tabelle an. |
| [ViewOptions](../com.aspose.words/viewoptions/) | Bietet verschiedene Optionen, die steuern, wie ein Dokument in Microsoft Word angezeigt wird. |
| [ViewType](../com.aspose.words/viewtype/) | Mögliche Werte für den Ansichtsmodus in Microsoft Word. |
| [VisitorAction](../com.aspose.words/visitoraction/) | Ermöglicht dem Besucher die Steuerung der Aufzählung von Knoten. |
| [WarningInfo](../com.aspose.words/warninginfo/) | Enthält Informationen über eine Warnung, die Aspose.Words beim Laden oder Speichern eines Dokuments ausgegeben hat. |
| [WarningInfoCollection](../com.aspose.words/warninginfocollection/) | Stellt eine typisierte Sammlung von [WarningInfo](../com.aspose.words/warninginfo/)‑Objekten dar. |
| [WarningSource](../com.aspose.words/warningsource/) | Gibt das Modul an, das während des Ladens oder Speicherns eines Dokuments eine Warnung erzeugt. |
| [WarningType](../com.aspose.words/warningtype/) | Gibt den Typ einer Warnung an, die von Aspose.Words beim Laden oder Speichern eines Dokuments ausgegeben wird. |
| [Watermark](../com.aspose.words/watermark/) | Stellt eine Klasse dar, um mit Dokumentwasserzeichen zu arbeiten. |
| [WatermarkLayout](../com.aspose.words/watermarklayout/) | Definiert das Layout des Wasserzeichens relativ zum Zentrum des Wasserzeichens. |
| [WatermarkType](../com.aspose.words/watermarktype/) | Gibt den Wasserzeichentyp an. |
| [Watermarker](../com.aspose.words/watermarker/) | Stellt Methoden bereit, die zum Einfügen von Wasserzeichen in Dokumente vorgesehen sind. |
| [WatermarkerContext](../com.aspose.words/watermarkercontext/) | Dokument-Wasserzeichner-Kontext. |
| [WebExtension](../com.aspose.words/webextension/) | Stellt ein Web-Erweiterungsobjekt dar. |
| [WebExtensionBinding](../com.aspose.words/webextensionbinding/) | Gibt eine Bindungsbeziehung zwischen einer Web-Erweiterung und den Daten im Dokument an. |
| [WebExtensionBindingCollection](../com.aspose.words/webextensionbindingcollection/) | Gibt eine Liste von Web-Erweiterungsbindungen an. |
| [WebExtensionBindingType](../com.aspose.words/webextensionbindingtype/) | Enumeriert verfügbare Bindungstypen zwischen einer Web-Erweiterung und den Daten im Dokument. |
| [WebExtensionProperty](../com.aspose.words/webextensionproperty/) | Gibt eine benutzerdefinierte Eigenschaft einer Web-Erweiterung an. |
| [WebExtensionPropertyCollection](../com.aspose.words/webextensionpropertycollection/) | Gibt ein Set benutzerdefinierter Eigenschaften einer Web-Erweiterung an. |
| [WebExtensionReference](../com.aspose.words/webextensionreference/) | Stellt die Referenz auf eine Web-Erweiterung dar. |
| [WebExtensionReferenceCollection](../com.aspose.words/webextensionreferencecollection/) | Gibt eine Liste von Web-Erweiterungsreferenzen an. |
| [WebExtensionStoreType](../com.aspose.words/webextensionstoretype/) | Enumeriert verfügbare Typen eines Web-Erweiterungsstores. |
| [WordML2003SaveOptions](../com.aspose.words/wordml2003saveoptions/) | Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im [SaveFormat.\#WORD\_ML](../com.aspose.words/saveformat/\#WORD-ML)-Format anzugeben. |
| [WrapSide](../com.aspose.words/wrapside/) | Gibt an, an welcher Seite(n) der Form oder des Bildes der Text umfließt. |
| [WrapType](../com.aspose.words/wraptype/) | Gibt an, wie Text um eine Form oder ein Bild herumfließt. |
| [WriteProtection](../com.aspose.words/writeprotection/) | Gibt die Schreibschutz-Einstellungen für ein Dokument an. |
| [X509Certificate2Wrapper](../com.aspose.words/x509certificate2wrapper/) | Von JAVA hinzugefügter öffentlicher Wrapper um unser internes X509Certificate2. |
| [XamlFixedSaveOptions](../com.aspose.words/xamlfixedsaveoptions/) | Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im [SaveFormat.\#XAML\_FIXED](../com.aspose.words/saveformat/\#XAML-FIXED)-Format anzugeben. |
| [XamlFlowSaveOptions](../com.aspose.words/xamlflowsaveoptions/) | Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im [SaveFormat.\#XAML\_FLOW](../com.aspose.words/saveformat/\#XAML-FLOW)- oder im [SaveFormat.\#XAML\_FLOW\_PACK](../com.aspose.words/saveformat/\#XAML-FLOW-PACK)-Format anzugeben. |
| [XlsxDateTimeParsingMode](../com.aspose.words/xlsxdatetimeparsingmode/) | Gibt an, wie Dokumenttext geparst wird, um Datums- und Zeitwerte zu identifizieren. |
| [XlsxSaveOptions](../com.aspose.words/xlsxsaveoptions/) | Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im [SaveFormat.\#XLSX](../com.aspose.words/saveformat/\#XLSX)-Format anzugeben. |
| [XlsxSectionMode](../com.aspose.words/xlsxsectionmode/) | Gibt an, wie Abschnitte beim Speichern eines Dokuments im XLSX-Format behandelt werden. |
| [XmlDataLoadOptions](../com.aspose.words/xmldataloadoptions/) | Stellt Optionen für das Laden von XML-Daten dar. |
| [XmlDataSource](../com.aspose.words/xmldatasource/) | Stellt Zugriff auf Daten einer XML-Datei oder eines Streams bereit, die innerhalb eines Berichts verwendet werden. |
| [XmlDsigLevel](../com.aspose.words/xmldsiglevel/) | Gibt das Niveau einer digitalen Signatur basierend auf dem XML-DSig-Standard an. |
| [XmlMapping](../com.aspose.words/xmlmapping/) | Gibt die Informationen an, die verwendet werden, um eine Zuordnung zwischen dem übergeordneten strukturierten Dokument-Tag und einem XML-Element, das in einem benutzerdefinierten XML-Datenpart im Dokument gespeichert ist, herzustellen. |
| [XpsSaveOptions](../com.aspose.words/xpssaveoptions/) | Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im [SaveFormat.\#XPS](../com.aspose.words/saveformat/\#XPS)-Format anzugeben. |
| [Zip64Mode](../com.aspose.words/zip64mode/) | Gibt an, wann ZIP64-Format-Erweiterungen für OOXML-Dateien verwendet werden sollen. |
| [ZoomType](../com.aspose.words/zoomtype/) | Mögliche Werte dafür, wie groß oder klein das Dokument in Microsoft Word auf dem Bildschirm angezeigt wird. |

## Schnittstellen

| Schnittstelle | Beschreibung |
| --- | --- |
| [IBarcodeGenerator](../com.aspose.words/ibarcodegenerator/) | Öffentliche Schnittstelle für benutzerdefinierten Barcode-Generator. |
| [IBibliographyStylesProvider](../com.aspose.words/ibibliographystylesprovider/) | Implementieren Sie diese Schnittstelle, um den Bibliografiestil für die Felder [FieldBibliography](../com.aspose.words/fieldbibliography/) und [FieldCitation](../com.aspose.words/fieldcitation/) bereitzustellen, wenn sie aktualisiert werden. |
| [IChartDataPoint](../com.aspose.words/ichartdatapoint/) | Enthält Eigenschaften eines einzelnen Datenpunkts im Diagramm. |
| [IComparisonExpressionEvaluator](../com.aspose.words/icomparisonexpressionevaluator/) | Ermöglicht, wenn implementiert, die Überschreibung der Standardauswertung von Vergleichsausdrücken für die Felder [FieldIf](../com.aspose.words/fieldif/) und [FieldCompare](../com.aspose.words/fieldcompare/). |
| [ICssSavingCallback](../com.aspose.words/icsssavingcallback/) | Implementieren Sie diese Schnittstelle, wenn Sie steuern möchten, wie Aspose.Words CSS (Cascading Style Sheet) beim Speichern eines Dokuments als HTML speichert. |
| [IDocumentConverterPlugin](../com.aspose.words/idocumentconverterplugin/) | Definiert eine Schnittstelle für ein externes Konverter-Plugin. |
| [IDocumentLoadingCallback](../com.aspose.words/idocumentloadingcallback/) | Implementieren Sie diese Schnittstelle, wenn Sie eine eigene benutzerdefinierte Methode beim Laden eines Dokuments aufrufen möchten. |
| [IDocumentMergerPlugin](../com.aspose.words/idocumentmergerplugin/) | Definiert eine Schnittstelle für ein externes Merge-Plugin, das PDF-Dokumente zusammenführen kann. |
| [IDocumentPartSavingCallback](../com.aspose.words/idocumentpartsavingcallback/) | Implementieren Sie diese Schnittstelle, wenn Sie Benachrichtigungen erhalten und steuern möchten, wie Aspise.Words Dokumentteile speichert, wenn ein Dokument in das [SaveFormat.\#HTML](../com.aspose.words/saveformat/\#HTML)- oder [SaveFormat.\#EPUB](../com.aspose.words/saveformat/\#EPUB)-Format exportiert wird. |
| [IDocumentProcessorPlugin](../com.aspose.words/idocumentprocessorplugin/) | Definiert eine Schnittstelle für ein externes Dokumentverarbeitungs-Plugin. |
| [IDocumentReaderPlugin](../com.aspose.words/idocumentreaderplugin/) | Definiert eine Schnittstelle für externe Reader-Plugins, die eine Datei in ein Dokument einlesen können. |
| [IDocumentSavingCallback](../com.aspose.words/idocumentsavingcallback/) | Implementieren Sie diese Schnittstelle, wenn Sie eine eigene benutzerdefinierte Methode beim Speichern eines Dokuments aufrufen möchten. |
| [IFieldDatabaseProvider](../com.aspose.words/ifielddatabaseprovider/) | Implementieren Sie diese Schnittstelle, um Daten für das Feld [FieldDatabase](../com.aspose.words/fielddatabase/) bereitzustellen, wenn es aktualisiert wird. |
| [IFieldMergingCallback](../com.aspose.words/ifieldmergingcallback/) | Implementieren Sie diese Schnittstelle, wenn Sie steuern möchten, wie Daten während eines Seriendruckvorgangs in Merge-Felder eingefügt werden. |
| [IFieldResultFormatter](../com.aspose.words/ifieldresultformatter/) | Implementieren Sie diese Schnittstelle, wenn Sie steuern möchten, wie das Feld Ergebnis formatiert wird. |
| [IFieldUpdateCultureProvider](../com.aspose.words/ifieldupdatecultureprovider/) | Wenn implementiert, stellt ein [CultureInfo](../com.aspose.words.net.system.globalization/cultureinfo/) Objekt bereit, das während der Aktualisierung eines bestimmten Feldes verwendet werden sollte. |
| [IFieldUpdatingCallback](../com.aspose.words/ifieldupdatingcallback/) | Implementieren Sie dieses Interface, wenn Sie eigene benutzerdefinierte Methoden während einer Feldaktualisierung aufrufen lassen möchten. |
| [IFieldUpdatingProgressCallback](../com.aspose.words/ifieldupdatingprogresscallback/) | Implementieren Sie dieses Interface, wenn Sie den Fortschritt der Feldaktualisierung verfolgen möchten. |
| [IFieldUserPromptRespondent](../com.aspose.words/ifielduserpromptrespondent/) | Stellt den Befragten für Benutzeraufforderungen während der Feldaktualisierung dar. |
| [IFontSavingCallback](../com.aspose.words/ifontsavingcallback/) | Implementieren Sie dieses Interface, wenn Sie Benachrichtigungen erhalten und steuern möchten, wie **Aspose.Words** Schriftarten speichert, wenn ein Dokument in das HTML-Format exportiert wird. |
| [IHyphenationCallback](../com.aspose.words/ihyphenationcallback/) | Wird von Klassen implementiert, die Silbentrennungswörterbücher registrieren können. |
| [IImageSavingCallback](../com.aspose.words/iimagesavingcallback/) | Implementieren Sie dieses Interface, wenn Sie steuern möchten, wie **Aspose.Words** Bilder speichert, wenn ein Dokument als HTML gespeichert wird. |
| [IIndexFilter](../com.aspose.words/iindexfilter/) | Definiert einen Filter zum Überspringen von Elementen basierend auf deren Indizes. |
| [IMailMergeCallback](../com.aspose.words/imailmergecallback/) | Implementieren Sie dieses Interface, wenn Sie Benachrichtigungen erhalten möchten, während ein Seriendruck durchgeführt wird. |
| [IMailMergeDataSource](../com.aspose.words/imailmergedatasource/) | Implementieren Sie dieses Interface, um einen Seriendruck aus einer benutzerdefinierten Datenquelle zu ermöglichen, z. B. einer Objektliste. |
| [IMailMergeDataSourceRoot](../com.aspose.words/imailmergedatasourceroot/) | Implementieren Sie dieses Interface, um einen Seriendruck aus einer benutzerdefinierten Datenquelle mit Master-Detail-Daten zu ermöglichen. |
| [INodeChangingCallback](../com.aspose.words/inodechangingcallback/) | Implementieren Sie dieses Interface, wenn Sie Benachrichtigungen erhalten möchten, wenn Knoten im Dokument eingefügt oder entfernt werden. |
| [IPageLayoutCallback](../com.aspose.words/ipagelayoutcallback/) | Implementieren Sie dieses Interface, wenn Sie eine eigene benutzerdefinierte Methode während des Aufbaus und Renderns des Seitenlayoutmodells aufrufen lassen möchten. |
| [IPageSavingCallback](../com.aspose.words/ipagesavingcallback/) | Implementieren Sie dieses Interface, wenn Sie steuern möchten, wie **Aspose.Words** einzelne Seiten speichert, wenn ein Dokument in feste Seitenformate gespeichert wird. |
| [IReplacingCallback](../com.aspose.words/ireplacingcallback/) | Implementieren Sie dieses Interface, wenn Sie eine eigene benutzerdefinierte Methode während einer Suchen‑und‑Ersetzen‑Operation aufrufen lassen möchten. |
| [IResourceLoadingCallback](../com.aspose.words/iresourceloadingcallback/) | Implementieren Sie dieses Interface, wenn Sie steuern möchten, wie **Aspose.Words** externe Ressourcen lädt, wenn ein Dokument importiert und Bilder mit [DocumentBuilder](../com.aspose.words/documentbuilder/) eingefügt werden. |
| [IResourceSavingCallback](../com.aspose.words/iresourcesavingcallback/) | Implementieren Sie dieses Interface, wenn Sie steuern möchten, wie **Aspose.Words** externe Ressourcen (Bilder, Schriftarten und CSS) speichert, wenn ein Dokument als festes Seiten‑HTML oder SVG gespeichert wird. |
| [IRevisionCriteria](../com.aspose.words/irevisioncriteria/) | Implementieren Sie dieses Interface, wenn Sie steuern möchten, wann bestimmte [Revision](../com.aspose.words/revision/) von den Methoden [RevisionCollection.\#accept(com.aspose.words.IRevisionCriteria)](../com.aspose.words/revisioncollection/\#accept-com.aspose.words.IRevisionCriteria)/[RevisionCollection.\#reject(com.aspose.words.IRevisionCriteria)](../com.aspose.words/revisioncollection/\#reject-com.aspose.words.IRevisionCriteria) akzeptiert/abgelehnt werden sollen. |
| [IStructuredDocumentTag](../com.aspose.words/istructureddocumenttag/) | Interface zur Definition gemeinsamer Daten für [StructuredDocumentTag](../com.aspose.words/structureddocumenttag/) und [StructuredDocumentTagRangeStart](../com.aspose.words/structureddocumenttagrangestart/). |
| [ITextShaper](../com.aspose.words/itextshaper/) | Stellt Methoden zur Textformung bereit. |
| [ITextShaperFactory](../com.aspose.words/itextshaperfactory/) | Ein Interface einer Fabrik zum Erzeugen von Implementierungen von [ITextShaper](../com.aspose.words/itextshaper/). |
| [IWarningCallback](../com.aspose.words/iwarningcallback/) | Implementieren Sie dieses Interface, wenn Sie eine eigene benutzerdefinierte Methode aufrufen lassen möchten, um Verlust‑der‑Genauigkeit‑Warnungen zu erfassen, die beim Laden oder Speichern eines Dokuments auftreten können. |
