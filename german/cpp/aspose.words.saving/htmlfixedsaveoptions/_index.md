---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions Klasse"
linktitle: "HtmlFixedSaveOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions Klasse. Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im HtmlFixed‑Format anzugeben. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words.saving/htmlfixedsaveoptions/
---
## HtmlFixedSaveOptions class


Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im [HtmlFixed](../../aspose.words/saveformat/)‑Format anzugeben. Weitere Informationen finden Sie im Artikel [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) der Dokumentation.

```cpp
class HtmlFixedSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Erstellt ein Speicheroptionen-Objekt einer Klasse, die für das angegebene Speicherformat geeignet ist. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Erstellt ein Speicheroptionen-Objekt einer Klasse, die für die Dateierweiterung geeignet ist, die im angegebenen Dateinamen angegeben ist. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | Bestimmt, ob das angegebene Objekt im Wert dem aktuellen Objekt entspricht. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Liest oder setzt einen booleschen Wert, der angibt, ob das Einbetten von Schriften mit PostScript-Umrissen beim Einbetten von TrueType-Schriften in ein Dokument beim Speichern erlaubt ist. Der Standardwert ist **false**. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | Ermittelt einen Wert, der bestimmt, wie Farben gerendert werden. |
| [get_CssClassNamesPrefix](./get_cssclassnamesprefix/)() const | Gibt das Präfix an, das allen Klassennamen in der style.css‑Datei hinzugefügt wird. Standardwert ist **%\"aw\"**. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Liest oder setzt die benutzerdefinierte lokale Zeitzone, die für Datums-/Uhrzeitfelder verwendet wird. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Liest oder setzt den Pfad zur Standardvorlage (einschließlich Dateiname). Der Standardwert für diese Eigenschaft ist **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Liest einen Wert, der bestimmt, wie 3D-Effekte gerendert werden. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Liest oder setzt einen Wert, der bestimmt, wie DrawingML-Effekte gerendert werden. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Liest oder setzt einen Wert, der bestimmt, wie DrawingML-Formen gerendert werden. |
| [get_Encoding](./get_encoding/)() const | Gibt die zu verwendende Kodierung beim Exportieren nach HTML an. Standardwert ist **new UTF8Encoding(true)** (UTF-8 mit BOM). |
| [get_ExportEmbeddedCss](./get_exportembeddedcss/)() const | Gibt an, ob das CSS (Cascading [Style](../../aspose.words/style/) Sheet) in das Html‑Dokument eingebettet werden soll. |
| [get_ExportEmbeddedFonts](./get_exportembeddedfonts/)() const | Gibt an, ob Schriftarten im Base64‑Format in das Html‑Dokument eingebettet werden sollen. Hinweis: Das Setzen dieses Flags kann die Größe der ausgegebenen Html‑Datei erheblich vergrößern. |
| [get_ExportEmbeddedImages](./get_exportembeddedimages/)() const | Gibt an, ob Bilder in das Html-Dokument im Base64-Format eingebettet werden sollen. Hinweis: Das Setzen dieses Flags kann die Größe der ausgegebenen Html-Datei erheblich erhöhen. |
| [get_ExportEmbeddedSvg](./get_exportembeddedsvg/)() const | Gibt an, ob SVG-Ressourcen in das Html-Dokument eingebettet werden sollen. Standardwert ist **true**. |
| [get_ExportFormFields](./get_exportformfields/)() const | Liest oder legt die Angabe fest, ob Formularfelder als interaktive Elemente (als 'input'-Tag) exportiert werden, anstatt in Text oder Grafiken konvertiert zu werden. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | Wenn **true**, wird der Name und die Version von Aspose.Words in die erzeugten Dateien eingebettet. Standardwert ist **true**. |
| [get_FontFormat](./get_fontformat/)() const | Liest oder legt das für den Schriftart-Export verwendete [ExportFontFormat](../exportfontformat/) fest. Standardwert ist [Woff](../exportfontformat/). |
| [get_IdPrefix](./get_idprefix/)() const | Gibt ein Präfix an, das allen erzeugten Element-IDs im Ausgabedokument vorangestellt wird. Standardwert ist null und es wird kein Präfix vorangestellt. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Liest oder setzt einen Wert, der bestimmt, wie Tinten‑ (InkML‑)Objekte gerendert werden. |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | Ruft einen Wert ab oder legt ihn fest, der die Qualität der JPEG-Bilder in einem Html-Dokument bestimmt. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Liest den Wert, der bestimmt, ob Speicheroptimierung vor dem Speichern des Dokuments durchgeführt werden soll. Der Standardwert für diese Eigenschaft ist **false**. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | Ermöglicht die Angabe von Metadatei-Renderoptionen. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | Ruft das [NumeralFormat](../numeralformat/) ab, das für die Darstellung von Ziffern verwendet wird. Standardmäßig werden europäische Ziffern verwendet. |
| [get_OptimizeOutput](./get_optimizeoutput/)() override | Das Flag gibt an, ob eine Optimierung der Ausgabe erforderlich ist. Ist dieses Flag gesetzt, werden redundante verschachtelte Canvas-Elemente und leere Canvas-Elemente entfernt, außerdem werden benachbarte Glyphen mit derselben Formatierung zusammengeführt. Hinweis: Die Genauigkeit der Inhaltsdarstellung kann beeinträchtigt werden, wenn diese Eigenschaft auf **true** gesetzt ist. Standardwert ist **true**. |
| [get_PageHorizontalAlignment](./get_pagehorizontalalignment/)() const | Gibt die horizontale Ausrichtung der Seiten in einem HTML-Dokument an. Standardwert ist [Center](../htmlfixedpagehorizontalalignment/). |
| [get_PageMargins](./get_pagemargins/)() const | Gibt die Ränder um die Seiten in einem HTML-Dokument an. Der Randwert wird in Punkten gemessen und muss größer oder gleich 0 sein. Standardwert ist 10 Punkte. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | Ermöglicht die Steuerung, wie einzelne Seiten gespeichert werden, wenn ein Dokument in ein Fixed-Page-Format exportiert wird. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | Ruft die zu rendernden Seiten ab oder legt sie fest. Standard ist, dass alle Seiten im Dokument gerendert werden. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | Wenn **true**, wird die Ausgabe dort, wo möglich, hübsch formatiert. Standardwert ist **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Wird beim Speichern eines Dokuments aufgerufen und akzeptiert Daten über den Speicherfortschritt. |
| [get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/)() const | Gibt an, ob JavaScript aus Links entfernt wird. Standard ist **false**. |
| [get_ResourceSavingCallback](./get_resourcesavingcallback/)() const | Ermöglicht die Steuerung, wie Ressourcen (Bilder, Schriftarten und CSS) gespeichert werden, wenn ein Dokument in das feste Seiten‑Html-Format exportiert wird. |
| [get_ResourcesFolder](./get_resourcesfolder/)() const | Gibt den physischen Ordner an, in dem Ressourcen (Bilder, Schriftarten, CSS) beim Export eines Dokuments in das Html-Format gespeichert werden. Standardwert ist **null**. |
| [get_ResourcesFolderAlias](./get_resourcesfolderalias/)() const | Gibt den Namen des Ordners an, der zum Erstellen von Bild‑URIs verwendet wird, die in ein Html-Dokument geschrieben werden. Standardwert ist **null**. |
| [get_SaveFontFaceCssSeparately](./get_savefontfacecssseparately/)() const | Das Flag gibt an, ob "@font-face"-CSS‑Regeln in eine separate Datei "fontFaces.css" geschrieben werden sollen, wenn ein Dokument mit externem Stylesheet gespeichert wird (d. h., wenn [ExportEmbeddedCss](./get_exportembeddedcss/) **false** ist). Standardwert ist **false**, alle CSS‑Regeln werden in die einzelne Datei "styles.css" geschrieben. |
| [get_SaveFormat](./get_saveformat/)() override | Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroption‑Objekt verwendet wird. Kann nur [HtmlFixed](../../aspose.words/saveformat/) sein. |
| [get_ShowPageBorder](./get_showpageborder/)() const | Gibt an, ob ein Rand um die Seiten angezeigt werden soll. Standardwert ist **true**. |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Gibt den Ordner für temporäre Dateien an, die beim Speichern in eine DOC‑ oder DOCX‑Datei verwendet werden. Standardmäßig ist diese Eigenschaft **null** und es werden keine temporären Dateien verwendet. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Bestimmt, ob die Schriftattribute entsprechend dem verwendeten Zeichencode geändert werden. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Liest oder setzt einen Wert, der bestimmt, ob die [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/)‑Eigenschaft vor dem Speichern aktualisiert wird. Standardwert ist **false**; |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Ermittelt einen Wert, der festlegt, ob Felder bestimmter Typen vor dem Speichern des Dokuments in ein festes Seitenformat aktualisiert werden sollen. Der Standardwert für diese Eigenschaft ist **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Ermittelt oder legt einen Wert fest, der bestimmt, ob die [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) Eigenschaft vor dem Speichern aktualisiert wird. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Ermittelt oder legt einen Wert fest, der bestimmt, ob die [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) Eigenschaft vor dem Speichern aktualisiert wird. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | Ermittelt einen Wert, der festlegt, ob das Präsentationsbild von OLE‑Steuerelementen aktualisiert wird. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Ermittelt oder legt einen Wert fest, der bestimmt, ob Antialiasing beim Rendern verwendet werden soll. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Ermittelt oder legt einen Wert fest, der bestimmt, ob hochqualitative (d. h. langsame) Rendering‑Algorithmen verwendet werden sollen. |
| [get_UseTargetMachineFonts](./get_usetargetmachinefonts/)() const | Das Flag gibt an, ob Schriftarten vom Zielsystem verwendet werden müssen, um das Dokument darzustellen. Ist dieses Flag auf **true** gesetzt, haben die Eigenschaften [FontFormat](./get_fontformat/) und [ExportEmbeddedFonts](./get_exportembeddedfonts/) keine Wirkung, zudem wird [ResourceSavingCallback](./get_resourcesavingcallback/) für Schriftarten nicht ausgelöst. Standardwert ist **false**. |
| [GetType](./gettype/)() const override |  |
| [HtmlFixedSaveOptions](./htmlfixedsaveoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | Legt einen Wert fest, der bestimmt, wie Farben gerendert werden. |
| [set_CssClassNamesPrefix](./set_cssclassnamesprefix/)(const System::String\&) | Gibt das Präfix an, das allen Klassennamen in der style.css‑Datei hinzugefügt wird. Standardwert ist **%\"aw\"**. |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Setter für [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Setter für [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Legt einen Wert fest, der bestimmt, wie 3D‑Effekte gerendert werden. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Setter für [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Setter für [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Setter für [Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding](./get_encoding/). |
| [set_ExportEmbeddedCss](./set_exportembeddedcss/)(bool) | Setter für [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss](./get_exportembeddedcss/). |
| [set_ExportEmbeddedFonts](./set_exportembeddedfonts/)(bool) | Setter für [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts](./get_exportembeddedfonts/). |
| [set_ExportEmbeddedImages](./set_exportembeddedimages/)(bool) | Setter für [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages](./get_exportembeddedimages/). |
| [set_ExportEmbeddedSvg](./set_exportembeddedsvg/)(bool) | Setter für [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg](./get_exportembeddedsvg/). |
| [set_ExportFormFields](./set_exportformfields/)(bool) | Setter für [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields](./get_exportformfields/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_FontFormat](./set_fontformat/)(Aspose::Words::Saving::ExportFontFormat) | Setter für [Aspose::Words::Saving::HtmlFixedSaveOptions::get_FontFormat](./get_fontformat/). |
| [set_IdPrefix](./set_idprefix/)(const System::String\&) | Setter für [Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix](./get_idprefix/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Setter für [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_JpegQuality](../fixedpagesaveoptions/set_jpegquality/)(int32_t) | Setter für [Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Legt den Wert fest, der bestimmt, ob vor dem Speichern des Dokuments eine Speicheroptimierung durchgeführt werden soll. Der Standardwert für diese Eigenschaft ist **false**. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | Ermöglicht die Angabe von Metadatei-Renderoptionen. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | Legt das [NumeralFormat](../numeralformat/) fest, das für die Darstellung von Ziffern verwendet wird. Standardmäßig werden europäische Ziffern verwendet. |
| [set_OptimizeOutput](./set_optimizeoutput/)(bool) override | Setter für [Aspose::Words::Saving::HtmlFixedSaveOptions::get_OptimizeOutput](./get_optimizeoutput/). |
| [set_PageHorizontalAlignment](./set_pagehorizontalalignment/)(Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment) | Setter für [Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageHorizontalAlignment](./get_pagehorizontalalignment/). |
| [set_PageMargins](./set_pagemargins/)(double) | Setter für [Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins](./get_pagemargins/). |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | Ermöglicht die Steuerung, wie einzelne Seiten gespeichert werden, wenn ein Dokument in ein Fixed-Page-Format exportiert wird. |
| [set_PageSet](../fixedpagesaveoptions/set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | Setter für [Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet](../fixedpagesaveoptions/get_pageset/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Setter für [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RemoveJavaScriptFromLinks](./set_removejavascriptfromlinks/)(bool) | Setter für [Aspose::Words::Saving::HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/). |
| [set_ResourceSavingCallback](./set_resourcesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IResourceSavingCallback\>\&) | Ermöglicht die Steuerung, wie Ressourcen (Bilder, Schriftarten und CSS) gespeichert werden, wenn ein Dokument in das feste Seiten‑Html-Format exportiert wird. |
| [set_ResourcesFolder](./set_resourcesfolder/)(const System::String\&) | Setter für [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder](./get_resourcesfolder/). |
| [set_ResourcesFolderAlias](./set_resourcesfolderalias/)(const System::String\&) | Setter für [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolderAlias](./get_resourcesfolderalias/). |
| [set_SaveFontFaceCssSeparately](./set_savefontfacecssseparately/)(bool) | Setter für [Aspose::Words::Saving::HtmlFixedSaveOptions::get_SaveFontFaceCssSeparately](./get_savefontfacecssseparately/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroption‑Objekt verwendet wird. Kann nur [HtmlFixed](../../aspose.words/saveformat/) sein. |
| [set_ShowPageBorder](./set_showpageborder/)(bool) | Gibt an, ob ein Rand um die Seiten angezeigt werden soll. Standardwert ist **true**. |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Setter für [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Legt einen Wert fest, der bestimmt, ob Felder bestimmter Typen vor dem Speichern des Dokuments in ein festes Seitenformat aktualisiert werden sollen. Der Standardwert für diese Eigenschaft ist **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Legt einen Wert fest, der bestimmt, ob das Präsentationsbild von OLE-Steuerelementen aktualisiert wird. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [set_UseTargetMachineFonts](./set_usetargetmachinefonts/)(bool) | Setter für [Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts](./get_usetargetmachinefonts/). |
| static [Type](./type/)() |  |
## Siehe auch

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
