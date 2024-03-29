---
title: SaveOptions.FlatOpcXmlMappingOnly
second_title: Aspose.Words per .NET API Reference
description: SaveOptions proprietà. Ottiene o imposta un valore che determina i formati di documento in base ai quali è consentito mappareXmlMapping . Solo per impostazione predefinitaFlatOpc il formato del documento può essere mappato.
type: docs
weight: 90
url: /it/net/aspose.words.saving/saveoptions/flatopcxmlmappingonly/
---
## SaveOptions.FlatOpcXmlMappingOnly property

Ottiene o imposta un valore che determina i formati di documento in base ai quali è consentito mappare[`XmlMapping`](../../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Solo per impostazione predefinitaFlatOpc il formato del documento può essere mappato.

```csharp
public bool FlatOpcXmlMappingOnly { get; set; }
```

### Osservazioni

Questa opzione è associata a[`FlatOpcXmlMappingOnly`](../../../aspose.words.loading/loadoptions/flatopcxmlmappingonly/) . In genere è necessario impostarli entrambi su false per consentire la mappatura di un formato di documento arbitrario.

### Esempi

Mostra come associare tag di documenti strutturati a qualsiasi formato.

```csharp
// Se true - SDT conterrà testo HTML non elaborato.
// Se false, l'HTML mappato verrà analizzato e il documento risultante verrà inserito nel contenuto SDT.
LoadOptions loadOptions = new LoadOptions { FlatOpcXmlMappingOnly = isFlatOpcXmlMappingOnly };
Document doc = new Document(MyDir + "Structured document tag with HTML content.docx", loadOptions);

SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);
saveOptions.FlatOpcXmlMappingOnly = isFlatOpcXmlMappingOnly;

doc.Save(ArtifactsDir + "LoadOptions.FlatOpcXmlMappingOnly.pdf", saveOptions);
```

### Guarda anche

* class [SaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../saveoptions/)
* assemblea [Aspose.Words](../../../)


