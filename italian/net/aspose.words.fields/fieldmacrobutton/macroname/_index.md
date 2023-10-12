---
title: FieldMacroButton.MacroName
second_title: Aspose.Words per .NET API Reference
description: FieldMacroButton proprietà. Ottiene o imposta il nome della macro o del comando da eseguire.
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldmacrobutton/macroname/
---
## FieldMacroButton.MacroName property

Ottiene o imposta il nome della macro o del comando da eseguire.

```csharp
public string MacroName { get; set; }
```

### Esempi

Mostra come utilizzare i campi MACROBUTTON per consentirci di eseguire le macro di un documento facendo clic.

```csharp
Document doc = new Document(MyDir + "Macro.docm");
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.IsTrue(doc.HasMacros);

// Inserisci un campo MACROBUTTON e fai riferimento a una delle macro del documento per nome nella proprietà MacroName.
FieldMacroButton field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "MyMacro";
field.DisplayText = "Double click to run macro: " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field.GetFieldCode());

// Utilizza la proprietà per fare riferimento a "ViewZoom200", una macro fornita con Microsoft Word.
// Possiamo trovare tutte le altre macro tramite Visualizza -> Macro (elenco a discesa) -> Visualizza macro.
// In quel menu, seleziona "Comandi Word" dal menu a discesa "Macro in:".
// Se il nostro documento contiene una macro personalizzata con lo stesso nome di una macro stock,
// la nostra macro sarà quella eseguita dal campo MACROBUTTON.
builder.InsertParagraph();
field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "ViewZoom200";
field.DisplayText = "Run " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  ViewZoom200 Run ViewZoom200", field.GetFieldCode());

// Salva il documento come tipo di documento abilitato per le macro.
doc.Save(ArtifactsDir + "Field.MACROBUTTON.docm");
```

### Guarda anche

* class [FieldMacroButton](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldmacrobutton/)
* assemblea [Aspose.Words](../../../)


