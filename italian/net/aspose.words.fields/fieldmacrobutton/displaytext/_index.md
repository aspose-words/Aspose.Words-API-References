---
title: FieldMacroButton.DisplayText
linktitle: DisplayText
articleTitle: DisplayText
second_title: Aspose.Words per .NET
description: Scopri come personalizzare la proprietà DisplayText di FieldMacroButton per un'esecuzione macro ottimizzata. Imposta il testo perfetto per i pulsanti, per comandi utente fluidi!
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldmacrobutton/displaytext/
---
## FieldMacroButton.DisplayText property

Ottiene o imposta il testo da visualizzare come "pulsante" selezionato per eseguire la macro o il comando.

```csharp
public string DisplayText { get; set; }
```

## Esempi

Mostra come utilizzare i campi MACROBUTTON per consentire di eseguire le macro di un documento mediante clic.

```csharp
Document doc = new Document(MyDir + "Macro.docm");
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.IsTrue(doc.HasMacros);

// Inserire un campo MACROBUTTON e fare riferimento a una delle macro del documento tramite il nome nella proprietà MacroName.
FieldMacroButton field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "MyMacro";
field.DisplayText = "Double click to run macro: " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field.GetFieldCode());

// Utilizzare la proprietà per fare riferimento a "ViewZoom200", una macro fornita con Microsoft Word.
// Possiamo trovare tutte le altre macro tramite Visualizza -> Macro (menu a discesa) -> Visualizza macro.
// In quel menu, seleziona "Comandi Word" dal menu a discesa "Macro in:".
// Se il nostro documento contiene una macro personalizzata con lo stesso nome di una macro standard,
// la nostra macro sarà quella che eseguirà il campo MACROBUTTON.
builder.InsertParagraph();
field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "ViewZoom200";
field.DisplayText = "Run " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  ViewZoom200 Run ViewZoom200", field.GetFieldCode());

// Salva il documento come tipo di documento con macro abilitate.
doc.Save(ArtifactsDir + "Field.MACROBUTTON.docm");
```

### Guarda anche

* class [FieldMacroButton](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
