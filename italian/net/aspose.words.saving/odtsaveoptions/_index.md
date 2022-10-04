---
title: OdtSaveOptions
second_title: Aspose.Words per .NET API Reference
description: Può essere utilizzato per specificare opzioni aggiuntive durante il salvataggio di un documento nel fileOdt o Ott formato.
type: docs
weight: 5050
url: /it/net/aspose.words.saving/odtsaveoptions/
---
## OdtSaveOptions class

Può essere utilizzato per specificare opzioni aggiuntive durante il salvataggio di un documento nel fileOdt o Ott formato.

```csharp
public class OdtSaveOptions : SaveOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [OdtSaveOptions](odtsaveoptions/#constructor)() | Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento nel fileOdt formato. |
| [OdtSaveOptions](odtsaveoptions/#constructor_1)(SaveFormat) | Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento nel fileOdt o Ott formato. |
| [OdtSaveOptions](odtsaveoptions/#constructor_2)(string) | Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento nel fileOdt format crittografato con una password. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Ottiene o imposta un valore booleano che indica se consentire l'incorporamento di caratteri con contorni PostScript quando l'incorporamento di caratteri TrueType in un documento viene salvato. Il valore predefinito è **falso** . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Ottiene o imposta il fuso orario locale personalizzato utilizzato per i campi data/ora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Ottiene o imposta il percorso del modello predefinito (incluso il nome file). Il valore predefinito per questa proprietà è **stringa vuota** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering degli effetti 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering degli effetti DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering delle forme DrawingML. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Se true, fa sì che il nome e la versione di Aspose.Words vengano incorporati nei file prodotti. Il valore predefinito è **VERO** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Ottiene o imposta un valore che determina i formati di documento in base ai quali è consentito mappare[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Solo per impostazione predefinitaFlatOpc il formato del documento può essere mappato. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering degli oggetti Ink (InkML). |
| [IsStrictSchema11](../../aspose.words.saving/odtsaveoptions/isstrictschema11/) { get; set; } | Specifica se l'esportazione deve corrispondere rigorosamente alla specifica ODT 1.1. OOo 3.0 visualizza correttamente i file quando contengono elementi e attributi di ODT 1.2. Utilizzare "false" per questo scopo, o "true" per la stretta conformità alla specifica 1.1. Il valore predefinito è **falso** . |
| [MeasureUnit](../../aspose.words.saving/odtsaveoptions/measureunit/) { get; set; } | Consente di specificare le unità di misura da applicare al contenuto del documento. Il valore predefinito èCentimeters |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Ottiene o imposta il valore che determina se eseguire l'ottimizzazione della memoria prima di salvare il documento. Il valore predefinito per questa proprietà è **falso** . |
| [Password](../../aspose.words.saving/odtsaveoptions/password/) { get; set; } | Ottiene o imposta una password per crittografare il documento. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Quando`VERO` , formati graziosi di output ove applicabile. Il valore predefinito è **falso** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Chiamato durante il salvataggio di un documento e accetta i dati sull'avanzamento del salvataggio. |
| override [SaveFormat](../../aspose.words.saving/odtsaveoptions/saveformat/) { get; set; } | Specifica il formato in cui verrà salvato il documento se viene utilizzato questo oggetto opzioni di salvataggio. Può essereOdt oOtt . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Specifica la cartella per i file temporanei utilizzata durante il salvataggio in un file DOC o DOCX. Per impostazione predefinita questa proprietà è`nullo` e non vengono utilizzati file temporanei. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la proprietà viene aggiornata prima del salvataggio. Il valore predefinito è false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Ottiene o imposta un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato di pagina fisso. Il valore predefinito per questa proprietà è **VERO** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la proprietà viene aggiornata prima del salvataggio. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la proprietà viene aggiornata prima del salvataggio. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Ottiene o imposta il valore che determina se il contenuto di[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) viene aggiornato prima del salvataggio. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno l'anti-alias per il rendering. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno algoritmi di rendering di alta qualità (cioè lenti). |

### Osservazioni

Al momento fornisce solo il[`SaveFormat`](./saveformat/) proprietà, ma in futuro verranno aggiunte altre opzioni, come una password di crittografia o le impostazioni della firma digitale.

### Esempi

Mostra come rendere un documento salvato conforme a uno schema ODT precedente.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

Mostra come utilizzare diverse unità di misura per definire i parametri di stile di un documento ODT salvato.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Quando esportiamo il documento in .odt, possiamo usare un oggetto OdtSaveOptions per modificare il modo in cui salviamo il documento.
// Possiamo impostare la proprietà "MeasureUnit" su "OdtSaveMeasureUnit.Centimeters"
// per definire contenuto come parametri di stile utilizzando il sistema di metriche utilizzato da Open Office. 
// Possiamo impostare la proprietà "MeasureUnit" su "OdtSaveMeasureUnit.Inches"
// per definire contenuto come parametri di stile utilizzando il sistema imperiale, utilizzato da Microsoft Word.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Guarda anche

* class [SaveOptions](../saveoptions/)
* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
