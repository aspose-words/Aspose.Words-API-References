---
title: Document.HasMacros
linktitle: HasMacros
articleTitle: HasMacros
second_title: Aspose.Words per .NET
description: Scopri se il tuo documento contiene macro di progetto VBA con la proprietà HasMacros. Migliora l'automazione e l'efficienza dei tuoi flussi di lavoro oggi stesso!
type: docs
weight: 200
url: /it/net/aspose.words/document/hasmacros/
---
## Document.HasMacros property

Restituisce`VERO` se il documento ha un progetto VBA (macro).

```csharp
public bool HasMacros { get; }
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

* method [RemoveMacros](../removemacros/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
