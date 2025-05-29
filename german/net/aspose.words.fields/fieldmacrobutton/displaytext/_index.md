---
title: FieldMacroButton.DisplayText
linktitle: DisplayText
articleTitle: DisplayText
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie die DisplayText-Eigenschaft von FieldMacroButton für eine verbesserte Makroausführung anpassen. Legen Sie den perfekten Schaltflächentext für nahtlose Benutzerbefehle fest!
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldmacrobutton/displaytext/
---
## FieldMacroButton.DisplayText property

Ruft den Text ab oder legt ihn fest, der als „Schaltfläche“ angezeigt werden soll, die zum Ausführen des Makros oder Befehls ausgewählt wird.

```csharp
public string DisplayText { get; set; }
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
