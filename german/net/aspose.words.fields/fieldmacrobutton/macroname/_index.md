---
title: FieldMacroButton.MacroName
linktitle: MacroName
articleTitle: MacroName
second_title: Aspose.Words für .NET
description: Entdecken Sie die FieldMacroButton MacroName-Eigenschaft, um Ihre Makros oder Befehle einfach zu verwalten und anzupassen und so die Funktionalität und Effizienz zu verbessern.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldmacrobutton/macroname/
---
## FieldMacroButton.MacroName property

Ruft den Namen des auszuführenden Makros oder Befehls ab oder legt ihn fest.

```csharp
public string MacroName { get; set; }
```

## Beispiele

Zeigt, wie MACROBUTTON-Felder verwendet werden, um Makros eines Dokuments durch Klicken auszuführen.

```csharp
Document doc = new Document(MyDir + "Macro.docm");
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.IsTrue(doc.HasMacros);

// Fügen Sie ein MACROBUTTON-Feld ein und verweisen Sie in der MacroName-Eigenschaft mit dem Namen auf eines der Makros des Dokuments.
FieldMacroButton field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "MyMacro";
field.DisplayText = "Double click to run macro: " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field.GetFieldCode());

// Verwenden Sie die Eigenschaft, um auf „ViewZoom200“ zu verweisen, ein Makro, das mit Microsoft Word geliefert wird.
// Alle weiteren Makros finden wir über Ansicht -> Makros (Dropdown) -> Makros anzeigen.
// Wählen Sie in diesem Menü „Word-Befehle“ aus der Dropdown-Liste „Makros in:“ aus.
// Wenn unser Dokument ein benutzerdefiniertes Makro mit demselben Namen wie ein Standardmakro enthält,
// Unser Makro wird dasjenige sein, das das MACROBUTTON-Feld ausführt.
builder.InsertParagraph();
field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "ViewZoom200";
field.DisplayText = "Run " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  ViewZoom200 Run ViewZoom200", field.GetFieldCode());

// Speichern Sie das Dokument als Dokumenttyp mit Makros.
doc.Save(ArtifactsDir + "Field.MACROBUTTON.docm");
```

### Siehe auch

* class [FieldMacroButton](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
