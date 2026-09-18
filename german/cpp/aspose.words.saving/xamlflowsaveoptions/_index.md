---
title: "Aspose::Words::Saving::XamlFlowSaveOptions Klasse"
linktitle: "XamlFlowSaveOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::XamlFlowSaveOptions Klasse. Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im XamlFlow- oder XamlFlowPack-Format anzugeben. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 37000
url: /de/cpp/aspose.words.saving/xamlflowsaveoptions/
---
## XamlFlowSaveOptions class


Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im [XamlFlow](../../aspose.words/saveformat/) oder [XamlFlowPack](../../aspose.words/saveformat/) Format anzugeben. Weitere Informationen finden Sie im Dokumentationsartikel [Speicheroptionen angeben](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class XamlFlowSaveOptions : public Aspose::Words::Saving::SaveOptions
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Erstellt ein Speicheroptionen-Objekt einer Klasse, die für das angegebene Speicherformat geeignet ist. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Erstellt ein Speicheroptionen-Objekt einer Klasse, die für die Dateierweiterung geeignet ist, die im angegebenen Dateinamen angegeben ist. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Liest oder setzt einen booleschen Wert, der angibt, ob das Einbetten von Schriften mit PostScript-Umrissen beim Einbetten von TrueType-Schriften in ein Dokument beim Speichern erlaubt ist. Der Standardwert ist **false**. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Liest oder setzt die benutzerdefinierte lokale Zeitzone, die für Datums-/Uhrzeitfelder verwendet wird. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Liest oder setzt den Pfad zur Standardvorlage (einschließlich Dateiname). Der Standardwert für diese Eigenschaft ist **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Liest einen Wert, der bestimmt, wie 3D-Effekte gerendert werden. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Liest oder setzt einen Wert, der bestimmt, wie DrawingML-Effekte gerendert werden. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Liest oder setzt einen Wert, der bestimmt, wie DrawingML-Formen gerendert werden. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | Wenn **true**, wird der Name und die Version von Aspose.Words in die erzeugten Dateien eingebettet. Standardwert ist **true**. |
| [get_ImageSavingCallback](./get_imagesavingcallback/)() const | Ermöglicht die Steuerung, wie Bilder gespeichert werden, wenn ein Dokument nach XAML gespeichert wird. |
| [get_ImagesFolder](./get_imagesfolder/)() const | Gibt den physischen Ordner an, in dem Bilder beim Export eines Dokuments in das XAML-Format gespeichert werden. Standard ist ein leerer String. |
| [get_ImagesFolderAlias](./get_imagesfolderalias/)() const | Gibt den Namen des Ordners an, der zum Erstellen von Bild-URIs verwendet wird, die in ein XAML-Dokument geschrieben werden. Standard ist ein leerer String. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Liest oder setzt einen Wert, der bestimmt, wie Tinten‑ (InkML‑)Objekte gerendert werden. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Liest den Wert, der bestimmt, ob Speicheroptimierung vor dem Speichern des Dokuments durchgeführt werden soll. Der Standardwert für diese Eigenschaft ist **false**. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | Wenn **true**, wird die Ausgabe dort, wo möglich, hübsch formatiert. Standardwert ist **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Wird beim Speichern eines Dokuments aufgerufen und akzeptiert Daten über den Speicherfortschritt. |
| [get_ReplaceBackslashWithYenSign](./get_replacebackslashwithyensign/)() const | Gibt an, ob Rückwärtsschrägstriche durch Yen‑Zeichen ersetzt werden sollen. Standardwert ist **false**. |
| [get_SaveFormat](./get_saveformat/)() override | Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. Kann nur [XamlFlow](../../aspose.words/saveformat/) sein. |
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
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Setter für [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Setter für [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Legt einen Wert fest, der bestimmt, wie 3D‑Effekte gerendert werden. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Setter für [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Setter für [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ImageSavingCallback](./set_imagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IImageSavingCallback\>\&) | Ermöglicht die Steuerung, wie Bilder gespeichert werden, wenn ein Dokument nach XAML gespeichert wird. |
| [set_ImagesFolder](./set_imagesfolder/)(const System::String\&) | Setter für [Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder](./get_imagesfolder/). |
| [set_ImagesFolderAlias](./set_imagesfolderalias/)(const System::String\&) | Setter für [Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias](./get_imagesfolderalias/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Setter für [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Legt den Wert fest, der bestimmt, ob vor dem Speichern des Dokuments eine Speicheroptimierung durchgeführt werden soll. Der Standardwert für diese Eigenschaft ist **false**. |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Setter für [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_ReplaceBackslashWithYenSign](./set_replacebackslashwithyensign/)(bool) | Setter für [Aspose::Words::Saving::XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign](./get_replacebackslashwithyensign/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. Kann nur [XamlFlow](../../aspose.words/saveformat/) sein. |
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
| [XamlFlowSaveOptions](./xamlflowsaveoptions/)() | Initialisiert eine neue Instanz dieser Klasse, die verwendet werden kann, um ein Dokument im [XamlFlow](../../aspose.words/saveformat/) Format zu speichern. |
| [XamlFlowSaveOptions](./xamlflowsaveoptions/)(Aspose::Words::SaveFormat) | Initialisiert eine neue Instanz dieser Klasse, die verwendet werden kann, um ein Dokument im [XamlFlow](../../aspose.words/saveformat/) oder [XamlFlowPack](../../aspose.words/saveformat/) Format zu speichern. |
## Siehe auch

* Class [SaveOptions](../saveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
