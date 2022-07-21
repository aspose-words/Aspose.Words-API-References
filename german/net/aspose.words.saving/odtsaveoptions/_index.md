---
title: OdtSaveOptions
second_title: Aspose.Words für .NET-API-Referenz
description: Kann verwendet werden um zusätzliche Optionen beim Speichern eines Dokuments im zu spezifizierenOdt oder Ott format.
type: docs
weight: 5050
url: /de/net/aspose.words.saving/odtsaveoptions/
---
## OdtSaveOptions class

Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im zu spezifizierenOdt oder Ott format.

```csharp
public class OdtSaveOptions : SaveOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [OdtSaveOptions](odtsaveoptions#constructor)() | Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments im verwendet werden kannOdt format. |
| [OdtSaveOptions](odtsaveoptions#constructor_1)(SaveFormat) | Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments im verwendet werden kannOdt oder Ott format. |
| [OdtSaveOptions](odtsaveoptions#constructor_2)(string) | Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments im verwendet werden kannOdt format verschlüsselt mit einem Passwort. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob das Einbetten von Schriftarten mit PostScript-Konturen zulässig ist, wenn TrueType-Schriftarten in ein Dokument eingebettet werden, nachdem es gespeichert wurde. Der Standardwert ist **FALSCH** . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | Ruft eine benutzerdefinierte lokale Zeitzone ab oder legt sie fest, die für Datums-/Uhrzeitfelder verwendet wird. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | Ruft den Pfad zur Standardvorlage (einschließlich Dateiname) ab oder legt ihn fest. Der Standardwert für diese Eigenschaft ist **leerer String** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie 3D-Effekte gerendert werden. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie DrawingML-Effekte gerendert werden. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie DrawingML-Formen gerendert werden. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | Wenn wahr, bewirkt dies, dass der Name und die Version von Aspose.Words in produzierte Dateien eingebettet werden. Der Standardwert ist **Stimmt** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | Erhält oder setzt einen Wert, der festlegt, welche Dokumentformate abgebildet werden dürfen[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping) . Nur standardmäßigFlatOpc Dokumentformat darf gemappt werden. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie Ink-Objekte (InkML) gerendert werden. |
| [IsStrictSchema11](../../aspose.words.saving/odtsaveoptions/isstrictschema11) { get; set; } | Gibt an, ob der Export strikt der ODT-Spezifikation 1.1 entsprechen soll. OOo 3.0 zeigt Dateien korrekt an, wenn sie Elemente und Attribute von ODT 1.2 enthalten. Verwenden Sie "false" für diesen Zweck oder "true" für strikte Konformität mit Spezifikation 1.1. Der Standardwert ist **FALSCH** . |
| [MeasureUnit](../../aspose.words.saving/odtsaveoptions/measureunit) { get; set; } | Ermöglicht die Angabe von Maßeinheiten, die auf den Dokumentinhalt angewendet werden sollen. Der Standardwert istCentimeters |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | Holt oder legt einen Wert fest, der bestimmt, ob eine Speicheroptimierung durchgeführt werden soll, bevor das Dokument gespeichert wird. Der Standardwert für diese Eigenschaft ist **FALSCH** . |
| [Password](../../aspose.words.saving/odtsaveoptions/password) { get; set; } | Ruft ein Passwort ab oder legt es fest, um das Dokument zu verschlüsseln. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | Wann`Stimmt` , gibt gegebenenfalls hübsche Formate aus. Standardwert ist **FALSCH** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | Wird beim Speichern eines Dokuments aufgerufen und akzeptiert Daten zum Speicherfortschritt. |
| override [SaveFormat](../../aspose.words.saving/odtsaveoptions/saveformat) { get; set; } | Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. Kann seinOdt oderOtt . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | Gibt den Ordner für temporäre Dateien an, der beim Speichern in eine DOC- oder DOCX-Datei verwendet wird. Standardmäßig ist diese Eigenschaft`Null` und es werden keine temporären Dateien verwendet. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime) Eigenschaft wird vor dem Speichern aktualisiert. Standardwert ist false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob Felder bestimmter Typen aktualisiert werden sollen, bevor das Dokument in einem festen Seitenformat gespeichert wird. Der Standardwert für diese Eigenschaft ist **Stimmt** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted) Eigenschaft wird vor dem Speichern aktualisiert. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime) Eigenschaft wird vor dem Speichern aktualisiert. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | Erhält oder setzt den Wert, der bestimmt, ob der Inhalt von[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag) wird vor dem Speichern aktualisiert. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob Anti-Aliasing für das Rendern verwendet werden soll oder nicht. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob qualitativ hochwertige (dh langsame) Renderalgorithmen verwendet werden sollen oder nicht. |

### Bemerkungen

Im Moment bietet nur die[`SaveFormat`](./saveformat) -Eigenschaft, aber in Zukunft werden weitere Optionen hinzugefügt, wie z. B. ein Verschlüsselungskennwort oder Einstellungen für digitale Signaturen.

### Beispiele

Zeigt, wie ein gespeichertes Dokument einem älteren ODT-Schema entspricht.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

Zeigt, wie verschiedene Maßeinheiten zum Definieren von Stilparametern eines gespeicherten ODT-Dokuments verwendet werden.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Wenn wir das Dokument in .odt exportieren, können wir ein OdtSaveOptions-Objekt verwenden, um zu ändern, wie wir das Dokument speichern.
// Wir können die Eigenschaft "MeasureUnit" auf "OdtSaveMeasureUnit.Centimeters" setzen
// zum Definieren von Inhalten wie Stilparametern unter Verwendung des metrischen Systems, das Open Office verwendet. 
// Wir können die Eigenschaft "MeasureUnit" auf "OdtSaveMeasureUnit.Inches" setzen
// zum Definieren von Inhalten wie Stilparametern unter Verwendung des imperialen Systems, das Microsoft Word verwendet.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Siehe auch

* class [SaveOptions](../saveoptions)
* namensraum [Aspose.Words.Saving](../../aspose.words.saving)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
