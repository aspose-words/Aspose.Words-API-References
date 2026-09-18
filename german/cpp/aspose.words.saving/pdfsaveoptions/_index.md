---
title: "Aspose::Words::Saving::PdfSaveOptions Klasse"
linktitle: "PdfSaveOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PdfSaveOptions Klasse. Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im PDF-Format anzugeben. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 25000
url: /de/cpp/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class


Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im [Pdf](../../aspose.words/saveformat/)‑Format anzugeben. Weitere Informationen finden Sie im Dokumentationsartikel [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class PdfSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Clone](./clone/)() | Erstellt eine tiefe Kopie dieses Objekts. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Erstellt ein Speicheroptionen-Objekt einer Klasse, die für das angegebene Speicherformat geeignet ist. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Erstellt ein Speicheroptionen-Objekt einer Klasse, die für die Dateierweiterung geeignet ist, die im angegebenen Dateinamen angegeben ist. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | Bestimmt, ob das angegebene Objekt im Wert dem aktuellen Objekt entspricht. |
| [get_AdditionalTextPositioning](./get_additionaltextpositioning/)() const | Ein Flag, das angibt, ob zusätzliche Textpositionierungsoperatoren geschrieben werden sollen oder nicht. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Liest oder setzt einen booleschen Wert, der angibt, ob das Einbetten von Schriften mit PostScript-Umrissen beim Einbetten von TrueType-Schriften in ein Dokument beim Speichern erlaubt ist. Der Standardwert ist **false**. |
| [get_AttachmentsEmbeddingMode](./get_attachmentsembeddingmode/)() const | Liest oder legt einen Wert fest, der bestimmt, wie Anhänge in das PDF‑Dokument eingebettet werden. |
| [get_CacheBackgroundGraphics](./get_cachebackgroundgraphics/)() const | Liest oder legt einen Wert fest, der bestimmt, ob Grafiken, die im Hintergrund des Dokuments platziert werden, zwischengespeichert werden sollen oder nicht. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | Ermittelt einen Wert, der bestimmt, wie Farben gerendert werden. |
| [get_Compliance](./get_compliance/)() const | Gibt das Konformitätsniveau der PDF‑Standards für Ausgabedokumente an. |
| [get_CreateNoteHyperlinks](./get_createnotehyperlinks/)() const | Gibt an, ob Fuß‑/Endnoten‑Verweise im Haupttext in aktive Hyperlinks umgewandelt werden sollen. Beim Anklicken führt der Hyperlink zur entsprechenden Fuß‑/Endnote. Standardwert ist **false**. |
| [get_CustomPropertiesExport](./get_custompropertiesexport/)() const | Liest oder legt einen Wert fest, der bestimmt, wie [CustomDocumentProperties](../../aspose.words/document/get_customdocumentproperties/) in die PDF‑Datei exportiert werden. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Liest oder setzt die benutzerdefinierte lokale Zeitzone, die für Datums-/Uhrzeitfelder verwendet wird. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Liest oder setzt den Pfad zur Standardvorlage (einschließlich Dateiname). Der Standardwert für diese Eigenschaft ist **empty string**. |
| [get_DigitalSignatureDetails](./get_digitalsignaturedetails/)() const | Liest oder legt die Details für das Signieren des Ausgabepdf‑Dokuments fest. |
| [get_DisplayDocTitle](./get_displaydoctitle/)() const | Ein Flag, das angibt, ob die Titelleiste des Fensters den Dokumenttitel aus dem Title‑Eintrag des Dokumentinformations‑Dictionaries anzeigen soll. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Liest einen Wert, der bestimmt, wie 3D-Effekte gerendert werden. |
| [get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/)() override | Liest oder setzt einen Wert, der bestimmt, wie DrawingML-Effekte gerendert werden. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Liest oder setzt einen Wert, der bestimmt, wie DrawingML-Formen gerendert werden. |
| [get_DownsampleOptions](./get_downsampleoptions/)() const | Ermöglicht das Angeben von Downsampling‑Optionen. |
| [get_EmbedFullFonts](./get_embedfullfonts/)() const | Steuert, wie Schriftarten in die resultierenden PDF‑Dokumente eingebettet werden. |
| [get_EncryptionDetails](./get_encryptiondetails/)() const | Liest oder legt die Details für die Verschlüsselung des Ausgabepdf‑Dokuments fest. |
| [get_ExportDocumentStructure](./get_exportdocumentstructure/)() const | Liest oder legt einen Wert fest, der bestimmt, ob die Dokumentstruktur exportiert werden soll oder nicht. |
| [get_ExportFloatingShapesAsInlineTag](./get_exportfloatingshapesasinlinetag/)() const | Liest oder legt einen Wert fest, der bestimmt, ob schwebende Formen als Inline‑Tags in der Dokumentstruktur exportiert werden. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | Wenn **true**, wird der Name und die Version von Aspose.Words in die erzeugten Dateien eingebettet. Standardwert ist **true**. |
| [get_ExportLanguageToSpanTag](./get_exportlanguagetospantag/)() const | Liest oder legt einen Wert fest, der bestimmt, ob ein \"Span\"-Tag in der Dokumentstruktur erstellt werden soll, um die Textsprache zu exportieren. |
| [get_ExportParagraphGraphicsToArtifact](./get_exportparagraphgraphicstoartifact/)() const | Liest oder legt einen Wert fest, der bestimmt, ob eine Absatzgrafik als Artefakt markiert werden soll. |
| [get_FontEmbeddingMode](./get_fontembeddingmode/)() const | Gibt den Schriftart‑Einbettungsmodus an. |
| [get_GenerateFormFieldScripts](./get_generateformfieldscripts/)() const | Gibt an, ob Skripte erzeugt werden sollen, die das Verhalten bestimmter Microsoft‑Word‑Formularfeld‑Funktionen in PDF emulieren. Standardwert ist **false**. |
| [get_HeaderFooterBookmarksExportMode](./get_headerfooterbookmarksexportmode/)() const | Bestimmt, wie Lesezeichen in Kopf‑/Fußzeilen exportiert werden. |
| [get_ImageColorSpaceExportMode](./get_imagecolorspaceexportmode/)() const | Gibt an, wie der Farbraum für die Bilder im PDF-Dokument ausgewählt wird. |
| [get_ImageCompression](./get_imagecompression/)() const | Gibt den Kompressionstyp an, der für alle Bilder im Dokument verwendet wird. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Liest oder setzt einen Wert, der bestimmt, wie Tinten‑ (InkML‑)Objekte gerendert werden. |
| [get_InterpolateImages](./get_interpolateimages/)() const | Ein Flag, das angibt, ob Bildinterpolation von einem konformen Reader durchgeführt werden soll. Wenn **false** angegeben wird, wird das Flag nicht in das Ausgabedokument geschrieben und stattdessen das Standardverhalten des Readers verwendet. |
| [get_JpegQuality](./get_jpegquality/)() | Liest oder legt einen Wert fest, der die Qualität der JPEG‑Bilder im PDF‑Dokument bestimmt. |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | Ruft einen Wert ab oder legt ihn fest, der die Qualität der JPEG-Bilder in einem Html-Dokument bestimmt. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Liest den Wert, der bestimmt, ob Speicheroptimierung vor dem Speichern des Dokuments durchgeführt werden soll. Der Standardwert für diese Eigenschaft ist **false**. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | Ermöglicht die Angabe von Metadatei-Renderoptionen. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | Ruft das [NumeralFormat](../numeralformat/) ab, das für die Darstellung von Ziffern verwendet wird. Standardmäßig werden europäische Ziffern verwendet. |
| [get_OpenHyperlinksInNewWindow](./get_openhyperlinksinnewwindow/)() const | Liest oder legt einen Wert fest, der bestimmt, ob Hyperlinks im Ausgabepdf‑Dokument gezwungen werden, in einem neuen Fenster (oder Tab) des Browsers geöffnet zu werden. |
| virtual [get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/)() | Das Flag gibt an, ob eine Optimierung der Ausgabe erforderlich ist. Ist dieses Flag gesetzt, werden redundante verschachtelte Canvas-Elemente und leere Canvas-Elemente entfernt, außerdem werden benachbarte Glyphen mit derselben Formatierung zusammengeführt. Hinweis: Die Genauigkeit der Inhaltsdarstellung kann beeinträchtigt werden, wenn diese Eigenschaft auf **true** gesetzt ist. Standardwert ist **false**. |
| [get_OutlineOptions](./get_outlineoptions/)() const | Ermöglicht die Angabe von Umrissoptionen. |
| [get_PageLayout](./get_pagelayout/)() const | Gibt das Seitenlayout an, das verwendet wird, wenn das Dokument in einem PDF‑Reader geöffnet wird. |
| [get_PageMode](./get_pagemode/)() const | Gibt an, wie das PDF‑Dokument angezeigt werden soll, wenn es in einem PDF‑Reader geöffnet wird. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | Ermöglicht die Steuerung, wie einzelne Seiten gespeichert werden, wenn ein Dokument in ein Fixed-Page-Format exportiert wird. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | Ruft die zu rendernden Seiten ab oder legt sie fest. Standard ist, dass alle Seiten im Dokument gerendert werden. |
| [get_PreblendImages](./get_preblendimages/)() const | Liest oder legt einen Wert fest, der bestimmt, ob transparente Bilder mit schwarzer Hintergrundfarbe vorab gemischt werden sollen oder nicht. |
| [get_PreserveFormFields](./get_preserveformfields/)() const | Gibt an, ob Microsoft Word-Formularfelder als Formularfelder im PDF erhalten bleiben oder in Text konvertiert werden sollen. Standardwert ist **false**. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | Wenn **true**, wird die Ausgabe dort, wo möglich, hübsch formatiert. Standardwert ist **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Wird beim Speichern eines Dokuments aufgerufen und akzeptiert Daten über den Speicherfortschritt. |
| [get_RenderChoiceFormFieldBorder](./get_renderchoiceformfieldborder/)() const | Gibt an, ob die Rahmen von Auswahlformularfeldern im PDF gerendert werden sollen. |
| [get_SaveFormat](./get_saveformat/)() override | Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionen-Objekt verwendet wird. Kann nur [Pdf](../../aspose.words/saveformat/) sein. |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Gibt den Ordner für temporäre Dateien an, die beim Speichern in eine DOC‑ oder DOCX‑Datei verwendet werden. Standardmäßig ist diese Eigenschaft **null** und es werden keine temporären Dateien verwendet. |
| [get_TextCompression](./get_textcompression/)() const | Gibt den Kompressionstyp an, der für alle textuellen Inhalte im Dokument verwendet wird. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Bestimmt, ob die Schriftattribute entsprechend dem verwendeten Zeichencode geändert werden. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Liest oder setzt einen Wert, der bestimmt, ob die [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/)‑Eigenschaft vor dem Speichern aktualisiert wird. Standardwert ist **false**; |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Ermittelt einen Wert, der festlegt, ob Felder bestimmter Typen vor dem Speichern des Dokuments in ein festes Seitenformat aktualisiert werden sollen. Der Standardwert für diese Eigenschaft ist **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Ermittelt oder legt einen Wert fest, der bestimmt, ob die [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) Eigenschaft vor dem Speichern aktualisiert wird. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Ermittelt oder legt einen Wert fest, der bestimmt, ob die [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) Eigenschaft vor dem Speichern aktualisiert wird. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | Ermittelt einen Wert, der festlegt, ob das Präsentationsbild von OLE‑Steuerelementen aktualisiert wird. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Ermittelt oder legt einen Wert fest, der bestimmt, ob Antialiasing beim Rendern verwendet werden soll. |
| [get_UseBookFoldPrintingSettings](./get_usebookfoldprintingsettings/)() const | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob das Dokument mit einem Broschürendrucklayout gespeichert werden soll, falls es über [MultiplePages](../../aspose.words/pagesetup/get_multiplepages/) angegeben ist. |
| [get_UseCoreFonts](./get_usecorefonts/)() const | Liest oder legt einen Wert fest, der bestimmt, ob TrueType-Schriften Arial, Times New Roman, Courier New und Symbol durch Kern-PDF-Type‑1-Schriften ersetzt werden sollen oder nicht. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Ermittelt oder legt einen Wert fest, der bestimmt, ob hochqualitative (d. h. langsame) Rendering‑Algorithmen verwendet werden sollen. |
| [get_UseSdtTagAsFormFieldName](./get_usesdttagasformfieldname/)() const | Gibt an, ob das Tag‑ oder Id‑Eigenschaft des SDT‑Steuerelements als Name eines Formularfelds im PDF verwendet werden soll. |
| [get_ZoomBehavior](./get_zoombehavior/)() const | Liest einen Wert, der bestimmt, welcher Zoomtyp angewendet werden soll, wenn ein Dokument mit einem PDF‑Betrachter geöffnet wird. |
| [get_ZoomFactor](./get_zoomfactor/)() const | Liest einen Wert, der den Zoomfaktor (in Prozent) für ein Dokument bestimmt. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfSaveOptions](./pdfsaveoptions/)() | Initialisiert eine neue Instanz dieser Klasse, die verwendet werden kann, um ein Dokument im [Pdf](../../aspose.words/saveformat/)-Format zu speichern. |
| [set_AdditionalTextPositioning](./set_additionaltextpositioning/)(bool) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_AdditionalTextPositioning](./get_additionaltextpositioning/). |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_AttachmentsEmbeddingMode](./set_attachmentsembeddingmode/)(Aspose::Words::Saving::PdfAttachmentsEmbeddingMode) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_AttachmentsEmbeddingMode](./get_attachmentsembeddingmode/). |
| [set_CacheBackgroundGraphics](./set_cachebackgroundgraphics/)(bool) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics](./get_cachebackgroundgraphics/). |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | Legt einen Wert fest, der bestimmt, wie Farben gerendert werden. |
| [set_Compliance](./set_compliance/)(Aspose::Words::Saving::PdfCompliance) | Gibt das Konformitätsniveau der PDF‑Standards für Ausgabedokumente an. |
| [set_CreateNoteHyperlinks](./set_createnotehyperlinks/)(bool) | Gibt an, ob Fuß‑/Endnoten‑Verweise im Haupttext in aktive Hyperlinks umgewandelt werden sollen. Beim Anklicken führt der Hyperlink zur entsprechenden Fuß‑/Endnote. Standardwert ist **false**. |
| [set_CustomPropertiesExport](./set_custompropertiesexport/)(Aspose::Words::Saving::PdfCustomPropertiesExport) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_CustomPropertiesExport](./get_custompropertiesexport/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Setter für [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Setter für [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_DigitalSignatureDetails](./set_digitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::Saving::PdfDigitalSignatureDetails\>\&) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_DigitalSignatureDetails](./get_digitalsignaturedetails/). |
| [set_DisplayDocTitle](./set_displaydoctitle/)(bool) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_DisplayDocTitle](./get_displaydoctitle/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Legt einen Wert fest, der bestimmt, wie 3D‑Effekte gerendert werden. |
| [set_DmlEffectsRenderingMode](./set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) override | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Setter für [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_DownsampleOptions](./set_downsampleoptions/)(const System::SharedPtr\<Aspose::Words::Saving::DownsampleOptions\>\&) | Ermöglicht das Angeben von Downsampling‑Optionen. |
| [set_EmbedFullFonts](./set_embedfullfonts/)(bool) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts](./get_embedfullfonts/). |
| [set_EncryptionDetails](./set_encryptiondetails/)(const System::SharedPtr\<Aspose::Words::Saving::PdfEncryptionDetails\>\&) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails](./get_encryptiondetails/). |
| [set_ExportDocumentStructure](./set_exportdocumentstructure/)(bool) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_ExportDocumentStructure](./get_exportdocumentstructure/). |
| [set_ExportFloatingShapesAsInlineTag](./set_exportfloatingshapesasinlinetag/)(bool) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag](./get_exportfloatingshapesasinlinetag/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ExportLanguageToSpanTag](./set_exportlanguagetospantag/)(bool) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag](./get_exportlanguagetospantag/). |
| [set_ExportParagraphGraphicsToArtifact](./set_exportparagraphgraphicstoartifact/)(bool) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact](./get_exportparagraphgraphicstoartifact/). |
| [set_FontEmbeddingMode](./set_fontembeddingmode/)(Aspose::Words::Saving::PdfFontEmbeddingMode) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode](./get_fontembeddingmode/). |
| [set_GenerateFormFieldScripts](./set_generateformfieldscripts/)(bool) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts](./get_generateformfieldscripts/). |
| [set_HeaderFooterBookmarksExportMode](./set_headerfooterbookmarksexportmode/)(Aspose::Words::Saving::HeaderFooterBookmarksExportMode) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_HeaderFooterBookmarksExportMode](./get_headerfooterbookmarksexportmode/). |
| [set_ImageColorSpaceExportMode](./set_imagecolorspaceexportmode/)(Aspose::Words::Saving::PdfImageColorSpaceExportMode) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode](./get_imagecolorspaceexportmode/). |
| [set_ImageCompression](./set_imagecompression/)(Aspose::Words::Saving::PdfImageCompression) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression](./get_imagecompression/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Setter für [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_InterpolateImages](./set_interpolateimages/)(bool) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages](./get_interpolateimages/). |
| [set_JpegQuality](./set_jpegquality/)(int32_t) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality](./get_jpegquality/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Legt den Wert fest, der bestimmt, ob vor dem Speichern des Dokuments eine Speicheroptimierung durchgeführt werden soll. Der Standardwert für diese Eigenschaft ist **false**. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | Ermöglicht die Angabe von Metadatei-Renderoptionen. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | Legt das [NumeralFormat](../numeralformat/) fest, das für die Darstellung von Ziffern verwendet wird. Standardmäßig werden europäische Ziffern verwendet. |
| [set_OpenHyperlinksInNewWindow](./set_openhyperlinksinnewwindow/)(bool) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow](./get_openhyperlinksinnewwindow/). |
| virtual [set_OptimizeOutput](../fixedpagesaveoptions/set_optimizeoutput/)(bool) | Setter für [Aspose::Words::Saving::FixedPageSaveOptions::get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/). |
| [set_PageLayout](./set_pagelayout/)(Aspose::Words::Saving::PdfPageLayout) | Gibt das Seitenlayout an, das verwendet wird, wenn das Dokument in einem PDF‑Reader geöffnet wird. |
| [set_PageMode](./set_pagemode/)(Aspose::Words::Saving::PdfPageMode) | Gibt an, wie das PDF‑Dokument angezeigt werden soll, wenn es in einem PDF‑Reader geöffnet wird. |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | Ermöglicht die Steuerung, wie einzelne Seiten gespeichert werden, wenn ein Dokument in ein Fixed-Page-Format exportiert wird. |
| [set_PageSet](../fixedpagesaveoptions/set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | Setter für [Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet](../fixedpagesaveoptions/get_pageset/). |
| [set_PreblendImages](./set_preblendimages/)(bool) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages](./get_preblendimages/). |
| [set_PreserveFormFields](./set_preserveformfields/)(bool) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields](./get_preserveformfields/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Setter für [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RenderChoiceFormFieldBorder](./set_renderchoiceformfieldborder/)(bool) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_RenderChoiceFormFieldBorder](./get_renderchoiceformfieldborder/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionen-Objekt verwendet wird. Kann nur [Pdf](../../aspose.words/saveformat/) sein. |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Setter für [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_TextCompression](./set_textcompression/)(Aspose::Words::Saving::PdfTextCompression) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_TextCompression](./get_textcompression/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Legt einen Wert fest, der bestimmt, ob Felder bestimmter Typen vor dem Speichern des Dokuments in ein festes Seitenformat aktualisiert werden sollen. Der Standardwert für diese Eigenschaft ist **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Legt einen Wert fest, der bestimmt, ob das Präsentationsbild von OLE-Steuerelementen aktualisiert wird. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseBookFoldPrintingSettings](./set_usebookfoldprintingsettings/)(bool) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_UseBookFoldPrintingSettings](./get_usebookfoldprintingsettings/). |
| [set_UseCoreFonts](./set_usecorefonts/)(bool) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts](./get_usecorefonts/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [set_UseSdtTagAsFormFieldName](./set_usesdttagasformfieldname/)(bool) | Setter für [Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName](./get_usesdttagasformfieldname/). |
| [set_ZoomBehavior](./set_zoombehavior/)(Aspose::Words::Saving::PdfZoomBehavior) | Legt einen Wert fest, der bestimmt, welcher Zoomtyp angewendet werden soll, wenn ein Dokument mit einem PDF‑Betrachter geöffnet wird. |
| [set_ZoomFactor](./set_zoomfactor/)(int32_t) | Legt einen Wert fest, der den Zoomfaktor (in Prozent) für ein Dokument bestimmt. |
| static [Type](./type/)() |  |
## Siehe auch

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
