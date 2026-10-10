---
title: "Aspose::Words::Saving::SaveOptions‑Klasse"
linktitle: "SaveOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::SaveOptions‑Klasse. Dies ist eine abstrakte Basisklasse für Klassen, die dem Benutzer ermöglichen, zusätzliche Optionen beim Speichern eines Dokuments in ein bestimmtes Format anzugeben. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 29000
url: /de/cpp/aspose.words.saving/saveoptions/
---
## SaveOptions class


Dies ist eine abstrakte Basisklasse für Klassen, die dem Benutzer ermöglichen, zusätzliche Optionen beim Speichern eines Dokuments in ein bestimmtes Format anzugeben. Weitere Informationen finden Sie im Dokumentationsartikel [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class SaveOptions : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| static [CreateSaveOptions](./createsaveoptions/)(Aspose::Words::SaveFormat) | Erstellt ein Speicheroptionen-Objekt einer Klasse, die für das angegebene Speicherformat geeignet ist. |
| static [CreateSaveOptions](./createsaveoptions/)(const System::String\&) | Erstellt ein Speicheroptionen-Objekt einer Klasse, die für die Dateierweiterung geeignet ist, die im angegebenen Dateinamen angegeben ist. |
| [get_AllowEmbeddingPostScriptFonts](./get_allowembeddingpostscriptfonts/)() const | Liest oder setzt einen booleschen Wert, der angibt, ob das Einbetten von Schriften mit PostScript-Umrissen beim Einbetten von TrueType-Schriften in ein Dokument beim Speichern erlaubt ist. Der Standardwert ist **false**. |
| [get_CustomTimeZoneInfo](./get_customtimezoneinfo/)() const | Liest oder setzt die benutzerdefinierte lokale Zeitzone, die für Datums-/Uhrzeitfelder verwendet wird. |
| [get_DefaultTemplate](./get_defaulttemplate/)() const | Liest oder setzt den Pfad zur Standardvorlage (einschließlich Dateiname). Der Standardwert für diese Eigenschaft ist **empty string**. |
| [get_Dml3DEffectsRenderingMode](./get_dml3deffectsrenderingmode/)() const | Liest einen Wert, der bestimmt, wie 3D-Effekte gerendert werden. |
| virtual [get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/)() | Liest oder setzt einen Wert, der bestimmt, wie DrawingML-Effekte gerendert werden. |
| [get_DmlRenderingMode](./get_dmlrenderingmode/)() const | Liest oder setzt einen Wert, der bestimmt, wie DrawingML-Formen gerendert werden. |
| [get_ExportGeneratorName](./get_exportgeneratorname/)() const | Wenn **true**, wird der Name und die Version von Aspose.Words in die erzeugten Dateien eingebettet. Standardwert ist **true**. |
| [get_ImlRenderingMode](./get_imlrenderingmode/)() const | Liest oder setzt einen Wert, der bestimmt, wie Tinten‑ (InkML‑)Objekte gerendert werden. |
| [get_MemoryOptimization](./get_memoryoptimization/)() const | Liest den Wert, der bestimmt, ob Speicheroptimierung vor dem Speichern des Dokuments durchgeführt werden soll. Der Standardwert für diese Eigenschaft ist **false**. |
| [get_PrettyFormat](./get_prettyformat/)() const | Wenn **true**, wird die Ausgabe dort, wo möglich, hübsch formatiert. Standardwert ist **false**. |
| [get_ProgressCallback](./get_progresscallback/)() const | Wird beim Speichern eines Dokuments aufgerufen und akzeptiert Daten über den Speicherfortschritt. |
| virtual [get_SaveFormat](./get_saveformat/)() | Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses SaveOptions‑Objekt verwendet wird. |
| [get_TempFolder](./get_tempfolder/)() const | Gibt den Ordner für temporäre Dateien an, die beim Speichern in eine DOC‑ oder DOCX‑Datei verwendet werden. Standardmäßig ist diese Eigenschaft **null** und es werden keine temporären Dateien verwendet. |
| [get_UpdateAmbiguousTextFont](./get_updateambiguoustextfont/)() const | Bestimmt, ob die Schriftattribute entsprechend dem verwendeten Zeichencode geändert werden. |
| [get_UpdateCreatedTimeProperty](./get_updatecreatedtimeproperty/)() const | Liest oder setzt einen Wert, der bestimmt, ob die [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/)‑Eigenschaft vor dem Speichern aktualisiert wird. Standardwert ist **false**; |
| [get_UpdateFields](./get_updatefields/)() const | Ermittelt einen Wert, der festlegt, ob Felder bestimmter Typen vor dem Speichern des Dokuments in ein festes Seitenformat aktualisiert werden sollen. Der Standardwert für diese Eigenschaft ist **true**. |
| [get_UpdateLastPrintedProperty](./get_updatelastprintedproperty/)() const | Ermittelt oder legt einen Wert fest, der bestimmt, ob die [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) Eigenschaft vor dem Speichern aktualisiert wird. |
| [get_UpdateLastSavedTimeProperty](./get_updatelastsavedtimeproperty/)() const | Ermittelt oder legt einen Wert fest, der bestimmt, ob die [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) Eigenschaft vor dem Speichern aktualisiert wird. |
| [get_UpdateOleControlImages](./get_updateolecontrolimages/)() const | Ermittelt einen Wert, der festlegt, ob das Präsentationsbild von OLE‑Steuerelementen aktualisiert wird. |
| [get_UseAntiAliasing](./get_useantialiasing/)() const | Ermittelt oder legt einen Wert fest, der bestimmt, ob Antialiasing beim Rendern verwendet werden soll. |
| [get_UseHighQualityRendering](./get_usehighqualityrendering/)() const | Ermittelt oder legt einen Wert fest, der bestimmt, ob hochqualitative (d. h. langsame) Rendering‑Algorithmen verwendet werden sollen. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](./set_allowembeddingpostscriptfonts/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](./get_allowembeddingpostscriptfonts/). |
| [set_CustomTimeZoneInfo](./set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Setter für [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](./get_customtimezoneinfo/). |
| [set_DefaultTemplate](./set_defaulttemplate/)(const System::String\&) | Setter für [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](./get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](./set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Legt einen Wert fest, der bestimmt, wie 3D‑Effekte gerendert werden. |
| virtual [set_DmlEffectsRenderingMode](./set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Setter für [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](./set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Setter für [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](./get_dmlrenderingmode/). |
| [set_ExportGeneratorName](./set_exportgeneratorname/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](./get_exportgeneratorname/). |
| [set_ImlRenderingMode](./set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Setter für [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](./get_imlrenderingmode/). |
| [set_MemoryOptimization](./set_memoryoptimization/)(bool) | Legt den Wert fest, der bestimmt, ob vor dem Speichern des Dokuments eine Speicheroptimierung durchgeführt werden soll. Der Standardwert für diese Eigenschaft ist **false**. |
| [set_PrettyFormat](./set_prettyformat/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](./get_prettyformat/). |
| [set_ProgressCallback](./set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Setter für [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](./get_progresscallback/). |
| virtual [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) | Setter für [Aspose::Words::Saving::SaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_TempFolder](./set_tempfolder/)(const System::String\&) | Setter für [Aspose::Words::Saving::SaveOptions::get_TempFolder](./get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](./set_updateambiguoustextfont/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](./get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](./set_updatecreatedtimeproperty/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](./get_updatecreatedtimeproperty/). |
| [set_UpdateFields](./set_updatefields/)(bool) | Legt einen Wert fest, der bestimmt, ob Felder bestimmter Typen vor dem Speichern des Dokuments in ein festes Seitenformat aktualisiert werden sollen. Der Standardwert für diese Eigenschaft ist **true**. |
| [set_UpdateLastPrintedProperty](./set_updatelastprintedproperty/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](./get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](./set_updatelastsavedtimeproperty/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](./get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](./set_updateolecontrolimages/)(bool) | Legt einen Wert fest, der bestimmt, ob das Präsentationsbild von OLE-Steuerelementen aktualisiert wird. |
| [set_UseAntiAliasing](./set_useantialiasing/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](./get_useantialiasing/). |
| [set_UseHighQualityRendering](./set_usehighqualityrendering/)(bool) | Setter für [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](./get_usehighqualityrendering/). |
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

## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
