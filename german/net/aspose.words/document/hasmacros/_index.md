---
title: Document.HasMacros
linktitle: HasMacros
articleTitle: HasMacros
second_title: Aspose.Words für .NET
description: Finden Sie mit der HasMacros-Eigenschaft heraus, ob Ihr Dokument VBA-Projektmakros enthält. Steigern Sie noch heute die Automatisierung und Effizienz Ihrer Workflows!
type: docs
weight: 200
url: /de/net/aspose.words/document/hasmacros/
---
## Document.HasMacros property

Rückgaben`WAHR` wenn das Dokument ein VBA-Projekt (Makros) enthält.

```csharp
public bool HasMacros { get; }
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

* method [RemoveMacros](../removemacros/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
