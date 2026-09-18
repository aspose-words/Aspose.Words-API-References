---
title: "Aspose::Words::Saving::HtmlSaveOptions Klasse"
linktitle: "HtmlSaveOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions Klasse. Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im Html-, Mhtml-, Epub-, Azw3- oder Mobi-Format anzugeben. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 10000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class


Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) oder [Mobi](../../aspose.words/saveformat/) Format anzugeben. Weitere Informationen finden Sie im Dokumentationsartikel [Speicheroptionen angeben](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class HtmlSaveOptions : public Aspose::Words::Saving::SaveOptions
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Erstellt ein Speicheroptionen-Objekt einer Klasse, die für das angegebene Speicherformat geeignet ist. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Erstellt ein Speicheroptionen-Objekt einer Klasse, die für die Dateierweiterung geeignet ist, die im angegebenen Dateinamen angegeben ist. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Liest oder setzt einen booleschen Wert, der angibt, ob das Einbetten von Schriften mit PostScript-Umrissen beim Einbetten von TrueType-Schriften in ein Dokument beim Speichern erlaubt ist. Der Standardwert ist **false**. |
| [get_AllowNegativeIndent](./get_allownegativeindent/)() const | Gibt an, ob negative linke und rechte Absatzeinzüge beim Speichern in HTML, MHTML oder EPUB normalisiert werden. Der Standardwert ist **false**. |
| [get_CssClassNamePrefix](./get_cssclassnameprefix/)() const | Gibt ein Präfix an, das allen CSS-Klassennamen hinzugefügt wird. Der Standardwert ist eine leere Zeichenkette und generierte CSS-Klassennamen haben kein gemeinsames Präfix. |
| [get_CssSavingCallback](./get_csssavingcallback/)() const | Ermöglicht die Steuerung, wie CSS-Stile gespeichert werden, wenn ein Dokument in HTML, MHTML oder EPUB gespeichert wird. |
| [get_CssStyleSheetFileName](./get_cssstylesheetfilename/)() const | Gibt den Pfad und den Namen der Cascading-[Style](../../aspose.words/style/)-Sheet (CSS)-Datei an, die beim Export eines Dokuments nach HTML geschrieben wird. Der Standardwert ist eine leere Zeichenkette. |
| [get_CssStyleSheetType](./get_cssstylesheettype/)() const | Gibt an, wie CSS (Cascading-[Style](../../aspose.words/style/)-Sheet)-Stile nach HTML, MHTML oder EPUB exportiert werden. Der Standardwert ist [Inline](../cssstylesheettype/) für HTML/MHTML und [External](../cssstylesheettype/) für EPUB. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Liest oder setzt die benutzerdefinierte lokale Zeitzone, die für Datums-/Uhrzeitfelder verwendet wird. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Liest oder setzt den Pfad zur Standardvorlage (einschließlich Dateiname). Der Standardwert für diese Eigenschaft ist **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Liest einen Wert, der bestimmt, wie 3D-Effekte gerendert werden. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Liest oder setzt einen Wert, der bestimmt, wie DrawingML-Effekte gerendert werden. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Liest oder setzt einen Wert, der bestimmt, wie DrawingML-Formen gerendert werden. |
| [get_DocumentPartSavingCallback](./get_documentpartsavingcallback/)() const | Ermöglicht die Steuerung, wie Dokumentteile gespeichert werden, wenn ein Dokument in HTML oder EPUB gespeichert wird. |
| [get_DocumentSplitCriteria](./get_documentsplitcriteria/)() const | Gibt an, wie das Dokument beim Speichern im [Html](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/) oder [Azw3](../../aspose.words/saveformat/) Format aufgeteilt werden soll. Der Standard ist [None](../documentsplitcriteria/) für HTML und [HeadingParagraph](../documentsplitcriteria/) für EPUB und AZW3. |
| [get_DocumentSplitHeadingLevel](./get_documentsplitheadinglevel/)() const | Gibt die maximale Ebene von Überschriften an, bei der das Dokument aufgeteilt werden soll. Der Standardwert ist **%2**. |
| [get_Encoding](./get_encoding/)() const | Gibt die zu verwendende Kodierung beim Export nach HTML, MHTML oder EPUB an. Der Standardwert ist **new UTF8Encoding(false)** (UTF-8 ohne BOM). |
| [get_ExportCidUrlsForMhtmlResources](./get_exportcidurlsformhtmlresources/)() const | Gibt an, ob CID (Content-ID)-URLs verwendet werden sollen, um Ressourcen (Bilder, Schriftarten, CSS) zu referenzieren, die in MHTML-Dokumenten enthalten sind. Standardwert ist **false**. |
| [get_ExportDocumentProperties](./get_exportdocumentproperties/)() const | Gibt an, ob integrierte und benutzerdefinierte Dokumenteigenschaften nach HTML, MHTML oder EPUB exportiert werden sollen. Standardwert ist **false**. |
| [get_ExportDropDownFormFieldAsText](./get_exportdropdownformfieldastext/)() const | Steuert, wie Dropdown-Formularfelder nach HTML oder MHTML gespeichert werden. Standardwert ist **false**. |
| [get_ExportFontResources](./get_exportfontresources/)() const | Gibt an, ob Schriftartressourcen nach HTML, MHTML oder EPUB exportiert werden sollen. Standardwert ist **false**. |
| [get_ExportFontsAsBase64](./get_exportfontsasbase64/)() const | Gibt an, ob Schriftartressourcen in HTML im Base64-Format eingebettet werden sollen. Standardwert ist **false**. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | Wenn **true**, wird der Name und die Version von Aspose.Words in die erzeugten Dateien eingebettet. Standardwert ist **true**. |
| [get_ExportHeadersFootersMode](./get_exportheadersfootersmode/)() const | Gibt an, wie Kopf- und Fußzeilen nach HTML, MHTML oder EPUB ausgegeben werden. Standardwert ist [PerSection](../exportheadersfootersmode/) für HTML/MHTML und [None](../exportheadersfootersmode/) für EPUB. |
| [get_ExportImagesAsBase64](./get_exportimagesasbase64/)() const | Gibt an, ob Bilder im Base64-Format in das Ausgabedokument HTML, MHTML oder EPUB gespeichert werden. Standardwert ist **false**. |
| [get_ExportLanguageInformation](./get_exportlanguageinformation/)() const | Gibt an, ob Sprachinformationen nach HTML, MHTML oder EPUB exportiert werden. Standardwert ist **false**. |
| [get_ExportListLabels](./get_exportlistlabels/)() const | Steuert, wie Listenelemente nach HTML, MHTML oder EPUB ausgegeben werden. Standardwert ist [Auto](../exportlistlabels/). |
| [get_ExportOriginalUrlForLinkedImages](./get_exportoriginalurlforlinkedimages/)() const | Gibt an, ob die ursprüngliche URL als URL der verknüpften Bilder verwendet werden soll. Standardwert ist **false**. |
| [get_ExportPageMargins](./get_exportpagemargins/)() const | Gibt an, ob Seitenränder nach HTML, MHTML oder EPUB exportiert werden. Standardwert ist **false**. |
| [get_ExportPageSetup](./get_exportpagesetup/)() const | Gibt an, ob die Seiteneinrichtung nach HTML, MHTML oder EPUB exportiert wird. Standardwert ist **false**. |
| [get_ExportRelativeFontSize](./get_exportrelativefontsize/)() const | Gibt an, ob Schriftgrößen beim Speichern nach HTML, MHTML oder EPUB in relativen Einheiten ausgegeben werden sollen. Standardwert ist **false**. |
| [get_ExportRoundtripInformation](./get_exportroundtripinformation/)() const | Gibt an, ob die Roundtrip-Informationen beim Speichern nach HTML, MHTML oder EPUB geschrieben werden sollen. Standardwert ist **true** für HTML und **false** für MHTML und EPUB. |
| [get_ExportShapesAsSvg](./get_exportshapesassvg/)() const | Steuert, ob [Shape](../../aspose.words.drawing/shape/)-Knoten beim Speichern nach HTML, MHTML, EPUB oder AZW3 in SVG-Bilder konvertiert werden. Standardwert ist **false**. |
| [get_ExportTextInputFormFieldAsText](./get_exporttextinputformfieldastext/)() const | Steuert, wie Texteingabe-Formularfelder nach HTML oder MHTML gespeichert werden. Standardwert ist **false**. |
| [get_ExportTocPageNumbers](./get_exporttocpagenumbers/)() const | Gibt an, ob Seitenzahlen ins Inhaltsverzeichnis geschrieben werden sollen, wenn HTML, MHTML und EPUB gespeichert werden. Standardwert ist **false**. |
| [get_ExportXhtmlTransitional](./get_exportxhtmltransitional/)() const | Gibt an, ob die DOCTYPE-Deklaration beim Speichern nach HTML oder MHTML geschrieben werden soll. Wenn **true**, wird eine DOCTYPE-Deklaration im Dokument vor dem Root-Element geschrieben. Standardwert ist **false**. Beim Speichern nach EPUB oder HTML5 ([Html5](../htmlversion/)) wird die DOCTYPE-Deklaration immer geschrieben. |
| [get_FontResourcesSubsettingSizeThreshold](./get_fontresourcessubsettingsizethreshold/)() const | Steuert, welche Schriftartressourcen beim Speichern nach HTML, MHTML oder EPUB unterteilt werden müssen. Standardwert ist **%0**. |
| [get_FontSavingCallback](./get_fontsavingcallback/)() const | Ermöglicht die Steuerung, wie Schriftarten gespeichert werden, wenn ein Dokument nach HTML, MHTML oder EPUB gespeichert wird. |
| [get_FontsFolder](./get_fontsfolder/)() const | Gibt den physischen Ordner an, in dem Schriftarten beim Export eines Dokuments nach HTML gespeichert werden. Standardwert ist ein leerer String. |
| [get_FontsFolderAlias](./get_fontsfolderalias/)() const | Gibt den Namen des Ordners an, der zum Erstellen von Schriftart-URIs verwendet wird, die in ein HTML-Dokument geschrieben werden. Standardwert ist ein leerer String. |
| [get_HtmlVersion](./get_htmlversion/)() const | Gibt die Version des HTML-Standards an, die beim Speichern des Dokuments nach HTML oder MHTML verwendet werden soll. Standardwert ist [Xhtml](../htmlversion/). |
| [get_ImageResolution](./get_imageresolution/)() const | Gibt die Ausgabeauflösung für Bilder beim Exportieren nach HTML, MHTML oder EPUB an. Standard ist **%96 dpi**. |
| [get_ImageSavingCallback](./get_imagesavingcallback/)() const | Ermöglicht die Steuerung, wie Bilder gespeichert werden, wenn ein Dokument nach HTML, MHTML oder EPUB gespeichert wird. |
| [get_ImagesFolder](./get_imagesfolder/)() const | Gibt den physischen Ordner an, in dem Bilder beim Exportieren eines Dokuments ins HTML-Format gespeichert werden. Standard ist ein leerer String. |
| [get_ImagesFolderAlias](./get_imagesfolderalias/)() const | Gibt den Namen des Ordners an, der zum Erstellen von Bild-URIs verwendet wird, die in ein HTML-Dokument geschrieben werden. Standard ist ein leerer String. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Liest oder setzt einen Wert, der bestimmt, wie Tinten‑ (InkML‑)Objekte gerendert werden. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Liest den Wert, der bestimmt, ob Speicheroptimierung vor dem Speichern des Dokuments durchgeführt werden soll. Der Standardwert für diese Eigenschaft ist **false**. |
| [get_MetafileFormat](./get_metafileformat/)() const | Gibt an, in welchem Format Metadateien beim Exportieren nach HTML, MHTML oder EPUB gespeichert werden. Der Standardwert ist [Png](../htmlmetafileformat/), was bedeutet, dass Metadateien in Raster‑PNG‑Bilder gerendert werden. |
| [get_NavigationMapLevel](./get_navigationmaplevel/)() const | Gibt die maximale Ebene von Überschriften an, die in die Navigationskarte beim Exportieren in die Formate EPUB, MOBI oder AZW3 übernommen wird. Standardwert ist **%3**. |
| [get_OfficeMathOutputMode](./get_officemathoutputmode/)() const | Steuert, wie OfficeMath‑Objekte nach HTML, MHTML oder EPUB exportiert werden. Der Standardwert ist [Image](../htmlofficemathoutputmode/). |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | Wenn **true**, wird die Ausgabe dort, wo möglich, hübsch formatiert. Standardwert ist **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Wird beim Speichern eines Dokuments aufgerufen und akzeptiert Daten über den Speicherfortschritt. |
| [get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/)() const | Gibt an, ob JavaScript aus Links entfernt wird. Standard ist **false**. |
| [get_ReplaceBackslashWithYenSign](./get_replacebackslashwithyensign/)() const | Gibt an, ob Rückwärtsschrägstriche durch Yen‑Zeichen ersetzt werden sollen. Standardwert ist **false**. |
| [get_ResolveFontNames](./get_resolvefontnames/)() const | Gibt an, ob Schriftfamiliennamen, die im Dokument verwendet werden, beim Schreiben in HTML‑basierte Formate gemäß [FontSettings](../../aspose.words/document/get_fontsettings/) aufgelöst und ersetzt werden. |
| [get_ResourceFolder](./get_resourcefolder/)() const | Gibt einen physischen Ordner an, in dem alle Ressourcen wie Bilder, Schriften und externes CSS gespeichert werden, wenn ein Dokument nach HTML exportiert wird. Standard ist ein leerer String. |
| [get_ResourceFolderAlias](./get_resourcefolderalias/)() const | Gibt den Namen des Ordners an, der zum Erstellen von URIs aller in ein HTML‑Dokument geschriebenen Ressourcen verwendet wird. Standard ist ein leerer String. |
| [get_SaveFormat](./get_saveformat/)() override | Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptions‑Objekt verwendet wird. Kann [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) oder [Mobi](../../aspose.words/saveformat/) sein. |
| [get_ScaleImageToShapeSize](./get_scaleimagetoshapesize/)() const | Gibt an, ob Bilder von Aspose.Words beim Exportieren nach HTML, MHTML oder EPUB auf die Größe der umgebenden Form skaliert werden. Standardwert ist **true**. |
| [get_TableWidthOutputMode](./get_tablewidthoutputmode/)() const | Steuert, wie Tabellen‑, Zeilen‑ und Zellbreiten nach HTML, MHTML oder EPUB exportiert werden. Der Standardwert ist [All](../htmlelementsizeoutputmode/). |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Gibt den Ordner für temporäre Dateien an, die beim Speichern in eine DOC‑ oder DOCX‑Datei verwendet werden. Standardmäßig ist diese Eigenschaft **null** und es werden keine temporären Dateien verwendet. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Bestimmt, ob die Schriftattribute entsprechend dem verwendeten Zeichencode geändert werden. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Liest oder setzt einen Wert, der bestimmt, ob die [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/)‑Eigenschaft vor dem Speichern aktualisiert wird. Standardwert ist **false**; |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Ermittelt einen Wert, der festlegt, ob Felder bestimmter Typen vor dem Speichern des Dokuments in ein festes Seitenformat aktualisiert werden sollen. Der Standardwert für diese Eigenschaft ist **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Ermittelt oder legt einen Wert fest, der bestimmt, ob die [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) Eigenschaft vor dem Speichern aktualisiert wird. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Ermittelt oder legt einen Wert fest, der bestimmt, ob die [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) Eigenschaft vor dem Speichern aktualisiert wird. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | Ermittelt einen Wert, der festlegt, ob das Präsentationsbild von OLE‑Steuerelementen aktualisiert wird. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Ermittelt oder legt einen Wert fest, der bestimmt, ob Antialiasing beim Rendern verwendet werden soll. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Ermittelt oder legt einen Wert fest, der bestimmt, ob hochqualitative (d. h. langsame) Rendering‑Algorithmen verwendet werden sollen. |
| [GetType](./gettype/)() const override |  |
| [HtmlSaveOptions](./htmlsaveoptions/)() | Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments im [Html](../../aspose.words/saveformat/) Format verwendet werden kann. |
| [HtmlSaveOptions](./htmlsaveoptions/)(Aspose::Words::SaveFormat) | Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments im [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) oder [Mobi](../../aspose.words/saveformat/) Format verwendet werden kann. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_AllowNegativeIndent](./set_allownegativeindent/)(bool) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_AllowNegativeIndent](./get_allownegativeindent/). |
| [set_CssClassNamePrefix](./set_cssclassnameprefix/)(const System::String\&) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix](./get_cssclassnameprefix/). |
| [set_CssSavingCallback](./set_csssavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::ICssSavingCallback\>\&) | Ermöglicht die Steuerung, wie CSS-Stile gespeichert werden, wenn ein Dokument in HTML, MHTML oder EPUB gespeichert wird. |
| [set_CssStyleSheetFileName](./set_cssstylesheetfilename/)(const System::String\&) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName](./get_cssstylesheetfilename/). |
| [set_CssStyleSheetType](./set_cssstylesheettype/)(Aspose::Words::Saving::CssStyleSheetType) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType](./get_cssstylesheettype/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Setter für [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Setter für [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Legt einen Wert fest, der bestimmt, wie 3D‑Effekte gerendert werden. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Setter für [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Setter für [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_DocumentPartSavingCallback](./set_documentpartsavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentPartSavingCallback\>\&) | Ermöglicht die Steuerung, wie Dokumentteile gespeichert werden, wenn ein Dokument in HTML oder EPUB gespeichert wird. |
| [set_DocumentSplitCriteria](./set_documentsplitcriteria/)(Aspose::Words::Saving::DocumentSplitCriteria) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria](./get_documentsplitcriteria/). |
| [set_DocumentSplitHeadingLevel](./set_documentsplitheadinglevel/)(int32_t) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel](./get_documentsplitheadinglevel/). |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_Encoding](./get_encoding/). |
| [set_ExportCidUrlsForMhtmlResources](./set_exportcidurlsformhtmlresources/)(bool) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources](./get_exportcidurlsformhtmlresources/). |
| [set_ExportDocumentProperties](./set_exportdocumentproperties/)(bool) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ExportDocumentProperties](./get_exportdocumentproperties/). |
| [set_ExportDropDownFormFieldAsText](./set_exportdropdownformfieldastext/)(bool) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText](./get_exportdropdownformfieldastext/). |
| [set_ExportFontResources](./set_exportfontresources/)(bool) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources](./get_exportfontresources/). |
| [set_ExportFontsAsBase64](./set_exportfontsasbase64/)(bool) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64](./get_exportfontsasbase64/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ExportHeadersFootersMode](./set_exportheadersfootersmode/)(Aspose::Words::Saving::ExportHeadersFootersMode) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode](./get_exportheadersfootersmode/). |
| [set_ExportImagesAsBase64](./set_exportimagesasbase64/)(bool) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ExportImagesAsBase64](./get_exportimagesasbase64/). |
| [set_ExportLanguageInformation](./set_exportlanguageinformation/)(bool) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation](./get_exportlanguageinformation/). |
| [set_ExportListLabels](./set_exportlistlabels/)(Aspose::Words::Saving::ExportListLabels) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ExportListLabels](./get_exportlistlabels/). |
| [set_ExportOriginalUrlForLinkedImages](./set_exportoriginalurlforlinkedimages/)(bool) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages](./get_exportoriginalurlforlinkedimages/). |
| [set_ExportPageMargins](./set_exportpagemargins/)(bool) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins](./get_exportpagemargins/). |
| [set_ExportPageSetup](./set_exportpagesetup/)(bool) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup](./get_exportpagesetup/). |
| [set_ExportRelativeFontSize](./set_exportrelativefontsize/)(bool) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize](./get_exportrelativefontsize/). |
| [set_ExportRoundtripInformation](./set_exportroundtripinformation/)(bool) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation](./get_exportroundtripinformation/). |
| [set_ExportShapesAsSvg](./set_exportshapesassvg/)(bool) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg](./get_exportshapesassvg/). |
| [set_ExportTextInputFormFieldAsText](./set_exporttextinputformfieldastext/)(bool) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText](./get_exporttextinputformfieldastext/). |
| [set_ExportTocPageNumbers](./set_exporttocpagenumbers/)(bool) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers](./get_exporttocpagenumbers/). |
| [set_ExportXhtmlTransitional](./set_exportxhtmltransitional/)(bool) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional](./get_exportxhtmltransitional/). |
| [set_FontResourcesSubsettingSizeThreshold](./set_fontresourcessubsettingsizethreshold/)(int32_t) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold](./get_fontresourcessubsettingsizethreshold/). |
| [set_FontSavingCallback](./set_fontsavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IFontSavingCallback\>\&) | Ermöglicht die Steuerung, wie Schriftarten gespeichert werden, wenn ein Dokument nach HTML, MHTML oder EPUB gespeichert wird. |
| [set_FontsFolder](./set_fontsfolder/)(const System::String\&) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder](./get_fontsfolder/). |
| [set_FontsFolderAlias](./set_fontsfolderalias/)(const System::String\&) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias](./get_fontsfolderalias/). |
| [set_HtmlVersion](./set_htmlversion/)(Aspose::Words::Saving::HtmlVersion) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_HtmlVersion](./get_htmlversion/). |
| [set_ImageResolution](./set_imageresolution/)(int32_t) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution](./get_imageresolution/). |
| [set_ImageSavingCallback](./set_imagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IImageSavingCallback\>\&) | Ermöglicht die Steuerung, wie Bilder gespeichert werden, wenn ein Dokument nach HTML, MHTML oder EPUB gespeichert wird. |
| [set_ImagesFolder](./set_imagesfolder/)(const System::String\&) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder](./get_imagesfolder/). |
| [set_ImagesFolderAlias](./set_imagesfolderalias/)(const System::String\&) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias](./get_imagesfolderalias/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Setter für [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Legt den Wert fest, der bestimmt, ob vor dem Speichern des Dokuments eine Speicheroptimierung durchgeführt werden soll. Der Standardwert für diese Eigenschaft ist **false**. |
| [set_MetafileFormat](./set_metafileformat/)(Aspose::Words::Saving::HtmlMetafileFormat) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_MetafileFormat](./get_metafileformat/). |
| [set_NavigationMapLevel](./set_navigationmaplevel/)(int32_t) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel](./get_navigationmaplevel/). |
| [set_OfficeMathOutputMode](./set_officemathoutputmode/)(Aspose::Words::Saving::HtmlOfficeMathOutputMode) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_OfficeMathOutputMode](./get_officemathoutputmode/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Setter für [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RemoveJavaScriptFromLinks](./set_removejavascriptfromlinks/)(bool) | Gibt an, ob JavaScript aus Links entfernt wird. Standard ist **false**. |
| [set_ReplaceBackslashWithYenSign](./set_replacebackslashwithyensign/)(bool) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign](./get_replacebackslashwithyensign/). |
| [set_ResolveFontNames](./set_resolvefontnames/)(bool) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames](./get_resolvefontnames/). |
| [set_ResourceFolder](./set_resourcefolder/)(const System::String\&) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolder](./get_resourcefolder/). |
| [set_ResourceFolderAlias](./set_resourcefolderalias/)(const System::String\&) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolderAlias](./get_resourcefolderalias/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_ScaleImageToShapeSize](./set_scaleimagetoshapesize/)(bool) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize](./get_scaleimagetoshapesize/). |
| [set_TableWidthOutputMode](./set_tablewidthoutputmode/)(Aspose::Words::Saving::HtmlElementSizeOutputMode) | Setter für [Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode](./get_tablewidthoutputmode/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Setter für [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Legt einen Wert fest, der bestimmt, ob Felder bestimmter Typen vor dem Speichern des Dokuments in ein festes Seitenformat aktualisiert werden sollen. Der Standardwert für diese Eigenschaft ist **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Legt einen Wert fest, der bestimmt, ob das Präsentationsbild von OLE-Steuerelementen aktualisiert wird. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie beim Speichern eines Dokuments als .epub eine bestimmte Kodierung verwendet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Verwenden Sie ein SaveOptions‑Objekt, um die Kodierung für ein Dokument, das wir speichern werden, anzugeben.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Epub);
saveOptions->set_Encoding(System::Text::Encoding::get_UTF8());

// Standardmäßig enthält ein ausgegebenes .epub‑Dokument alle Inhalte in einem HTML‑Teil.
// Ein Aufteilungskriterium ermöglicht es uns, das Dokument in mehrere HTML‑Teile zu segmentieren.
// Wir werden die Kriterien festlegen, um das Dokument in Überschrifts‑Absätze aufzuteilen.
// Dies ist nützlich für Leser, die HTML‑Dateien, die größer als eine bestimmte Größe sind, nicht lesen können.
saveOptions->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);

// Geben Sie an, dass wir Dokumenteigenschaften exportieren möchten.
saveOptions->set_ExportDocumentProperties(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```


Zeigt, wie man den Ordner zum Speichern verknüpfter Bilder nach dem Speichern als .html angibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::String imagesDir = System::IO::Path::Combine(get_ArtifactsDir(), u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// Setzt eine Option, um Formularfelder als Klartext anstelle von HTML-Eingabeelementen zu exportieren.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

## Siehe auch

* Class [SaveOptions](../saveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
