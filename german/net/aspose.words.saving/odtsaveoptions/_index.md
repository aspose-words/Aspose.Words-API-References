---
title: OdtSaveOptions Class
linktitle: OdtSaveOptions
articleTitle: OdtSaveOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.OdtSaveOptions, um Ihr Dokumentspeichererlebnis zu verbessern. Passen Sie die Einstellungen für ODT/OTT-Formate an und optimieren Sie Ihren Workflow!
type: docs
weight: 6110
url: /de/net/aspose.words.saving/odtsaveoptions/
---
## OdtSaveOptions class

Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments imOdt oder Ott format.

Um mehr zu erfahren, besuchen Sie die[Speicheroptionen festlegen](https://docs.aspose.com/words/net/specify-save-options/) Dokumentationsartikel.

```csharp
public class OdtSaveOptions : SaveOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [OdtSaveOptions](odtsaveoptions/#constructor)() | Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments imOdt format. |
| [OdtSaveOptions](odtsaveoptions/#constructor_1)(*[SaveFormat](../../aspose.words/saveformat/)*) | Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments imOdt oder Ott format. |
| [OdtSaveOptions](odtsaveoptions/#constructor_2)(*string*) | Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments imOdt format mit einem Passwort verschlüsselt. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob das Einbetten von Schriftarten mit PostScript-Konturen beim Einbetten von TrueType-Schriftarten in ein Dokument beim Speichern zulässig ist. Der Standardwert ist`FALSCH` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Ruft die benutzerdefinierte lokale Zeitzone ab, die für Datums-/Uhrzeitfelder verwendet wird, oder legt diese fest. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Ruft den Pfad zur Standardvorlage ab oder legt ihn fest (einschließlich Dateiname). Der Standardwert für diese Eigenschaft ist**leere Zeichenfolge** (Empty ). |
| [DigitalSignatureDetails](../../aspose.words.saving/odtsaveoptions/digitalsignaturedetails/) { get; set; } | Ruft ab oder legt fest[`DigitalSignatureDetails`](../digitalsignaturedetails/) Objekt zum Signieren eines Dokuments. |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie 3D-Effekte gerendert werden. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie DrawingML-Effekte gerendert werden. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie DrawingML-Formen gerendert werden. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Wann`WAHR` , bewirkt, dass der Name und die Version von Aspose.Words in die erstellten Dateien eingebettet werden. Der Standardwert ist`WAHR` . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie InkML-Objekte gerendert werden. |
| [IsStrictSchema11](../../aspose.words.saving/odtsaveoptions/isstrictschema11/) { get; set; } | Gibt an, ob der Export strikt der ODT-Spezifikation 1.1 entsprechen soll. OOo 3.0 zeigt Dateien korrekt an, wenn sie Elemente und Attribute von ODT 1.2 enthalten. Verwenden Sie hierfür "false" oder "true" für strikte Konformität mit Spezifikation 1.1. Der Standardwert ist`FALSCH` . |
| [MeasureUnit](../../aspose.words.saving/odtsaveoptions/measureunit/) { get; set; } | Ermöglicht die Angabe von Maßeinheiten für den Dokumentinhalt. Der Standardwert istCentimeters |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob vor dem Speichern des Dokuments eine Speicheroptimierung durchgeführt werden soll. Der Standardwert für diese Eigenschaft ist`FALSCH` . |
| [Password](../../aspose.words.saving/odtsaveoptions/password/) { get; set; } | Ruft ein Kennwort zum Verschlüsseln des Dokuments ab oder legt es fest. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Wann`WAHR` , formatiert die Ausgabe, wo anwendbar. Der Standardwert ist`FALSCH` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Wird beim Speichern eines Dokuments aufgerufen und akzeptiert Daten zum Speicherfortschritt. |
| override [SaveFormat](../../aspose.words.saving/odtsaveoptions/saveformat/) { get; set; } | Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. Kann seinOdt oderOtt . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Gibt den Ordner für temporäre Dateien an, der beim Speichern in eine DOC- oder DOCX-Datei verwendet wird. Standardmäßig ist diese Eigenschaft`null` und es werden keine temporären Dateien verwendet. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Bestimmt, ob die Schriftattribute entsprechend dem verwendeten Zeichencode geändert werden. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) Eigenschaft wird vor dem Speichern aktualisiert. Der Standardwert ist`FALSCH` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob Felder bestimmter Typen aktualisiert werden sollen, bevor das Dokument in einem festen Seitenformat gespeichert wird. Der Standardwert für diese Eigenschaft ist`WAHR` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) Eigenschaft wird vor dem Speichern aktualisiert. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) Eigenschaft wird vor dem Speichern aktualisiert. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob Anti-Aliasing zum Rendern verwendet werden soll oder nicht. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob qualitativ hochwertige (d. h. langsame) Rendering-Algorithmen verwendet werden sollen oder nicht. |

## Bemerkungen

Zur Zeit bietet nur die[`SaveFormat`](./saveformat/) Eigenschaft, aber in Zukunft werden andere Optionen hinzugefügt, wie etwa ein Verschlüsselungskennwort oder Einstellungen für digitale Signaturen.

## Beispiele

Zeigt, wie ein gespeichertes Dokument an ein älteres ODT-Schema angepasst wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

Zeigt, wie verschiedene Maßeinheiten verwendet werden, um Stilparameter eines gespeicherten ODT-Dokuments zu definieren.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Wenn wir das Dokument in .odt exportieren, können wir ein OdtSaveOptions-Objekt verwenden, um zu ändern, wie wir das Dokument speichern.
// Wir können die Eigenschaft „MeasureUnit“ auf „OdtSaveMeasureUnit.Centimeters“ setzen.
    // um Inhalte wie Stilparameter mithilfe des metrischen Systems zu definieren, das Open Office verwendet.
// Wir können die Eigenschaft „MeasureUnit“ auf „OdtSaveMeasureUnit.Inches“ setzen.
// um Inhalte wie Stilparameter mithilfe des imperialen Systems zu definieren, das von Microsoft Word verwendet wird.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Siehe auch

* class [SaveOptions](../saveoptions/)
* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
