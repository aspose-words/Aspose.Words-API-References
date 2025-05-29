---
title: ViewOptions.FormsDesign
linktitle: FormsDesign
articleTitle: FormsDesign
second_title: Aspose.Words per .NET
description: Scopri come ViewOptions FormsDesign migliora l'esperienza dei tuoi documenti attivando e disattivando la modalità di progettazione dei moduli per una modifica e una personalizzazione senza interruzioni.
type: docs
weight: 30
url: /it/net/aspose.words.settings/viewoptions/formsdesign/
---
## ViewOptions.FormsDesign property

Specifica se il documento è in modalità di progettazione moduli.

```csharp
public bool FormsDesign { get; set; }
```

## Osservazioni

Attualmente funziona solo per documenti in formato WordML.

## Esempi

Mostra come abilitare/disabilitare la modalità di progettazione dei moduli.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Impostare la proprietà "FormsDesign" su "false" per mantenere disabilitata la modalità di progettazione dei moduli.
// Impostare la proprietà "FormsDesign" su "true" per abilitare la modalità di progettazione dei moduli.
doc.ViewOptions.FormsDesign = useFormsDesign;

doc.Save(ArtifactsDir + "ViewOptions.FormsDesign.xml");

Assert.AreEqual(useFormsDesign,
    File.ReadAllText(ArtifactsDir + "ViewOptions.FormsDesign.xml").Contains("<w:formsDesign />"));
```

### Guarda anche

* class [ViewOptions](../)
* spazio dei nomi [Aspose.Words.Settings](../../../aspose.words.settings/)
* assemblea [Aspose.Words](../../../)
