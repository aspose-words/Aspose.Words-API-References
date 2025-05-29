---
title: Document.HasMacros
linktitle: HasMacros
articleTitle: HasMacros
second_title: Aspose.Words för .NET
description: Ta reda på om ditt dokument innehåller VBA-projektmakron med egenskapen HasMacros. Förbättra automatiseringen och effektiviteten i dina arbetsflöden idag!
type: docs
weight: 200
url: /sv/net/aspose.words/document/hasmacros/
---
## Document.HasMacros property

Returer`sann` om dokumentet har ett VBA-projekt (makron).

```csharp
public bool HasMacros { get; }
```

## Exempel

Visar hur man använder MACROBUTTON-fält för att köra ett dokuments makron genom att klicka.

```csharp
Document doc = new Document(MyDir + "Macro.docm");
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.IsTrue(doc.HasMacros);

// Infoga ett MAKROKNAPP-fält och referera till ett av dokumentets makron med namn i egenskapen Makronamn.
FieldMacroButton field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "MyMacro";
field.DisplayText = "Double click to run macro: " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field.GetFieldCode());

// Använd egenskapen för att referera till "ViewZoom200", ett makro som medföljer Microsoft Word.
// Vi kan hitta alla andra makron via Visa -> Makron (rullgardinsmeny) -> Visa makron.
// I den menyn väljer du "Word-kommandon" från rullgardinsmenyn "Makron i:".
// Om vårt dokument innehåller ett anpassat makro med samma namn som ett standardmakro,
// vårt makro kommer att vara det som MACROBUTTON-fältet kör.
builder.InsertParagraph();
field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "ViewZoom200";
field.DisplayText = "Run " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  ViewZoom200 Run ViewZoom200", field.GetFieldCode());

// Spara dokumentet som en makroaktiverad dokumenttyp.
doc.Save(ArtifactsDir + "Field.MACROBUTTON.docm");
```

### Se även

* method [RemoveMacros](../removemacros/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
