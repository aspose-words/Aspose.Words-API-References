---
title: Document.HasMacros
second_title: Aspose.Words für .NET-API-Referenz
description: Document eigendom. gibt zurück Stimmt wenn das Dokument ein VBAProjekt Makros hat.
type: docs
weight: 190
url: /de/net/aspose.words/document/hasmacros/
---
## Document.HasMacros property

gibt zurück **Stimmt** wenn das Dokument ein VBA-Projekt (Makros) hat.

```csharp
public bool HasMacros { get; }
```

### Beispiele

Zeigt, wie MACROBUTTON-Felder verwendet werden, damit wir die Makros eines Dokuments durch Klicken ausführen können.

```csharp
Document doc = new Document(MyDir + "Macro.docm");
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.IsTrue(doc.HasMacros);

// Fügen Sie ein Feld MACROBUTTON ein und referenzieren Sie eines der Makros des Dokuments anhand des Namens in der Eigenschaft MacroName.
FieldMacroButton field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "MyMacro";
field.DisplayText = "Double click to run macro: " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field.GetFieldCode());

// Verwenden Sie die Eigenschaft, um auf "ViewZoom200" zu verweisen, ein Makro, das mit Microsoft Word geliefert wird.
// Alle anderen Makros finden wir über Ansicht -> Makros (Dropdown) -> Makros anzeigen.
// Wählen Sie in diesem Menü "Word-Befehle" aus der Dropdown-Liste "Makros in:".
// Wenn unser Dokument ein benutzerdefiniertes Makro mit demselben Namen wie ein Aktienmakro enthält,
// Unser Makro wird dasjenige sein, das das MACROBUTTON-Feld ausführt.
builder.InsertParagraph();
field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "ViewZoom200";
field.DisplayText = "Run " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  ViewZoom200 Run ViewZoom200", field.GetFieldCode());

// Speichern Sie das Dokument als makrofähigen Dokumenttyp.
doc.Save(ArtifactsDir + "Field.MACROBUTTON.docm");
```

### Siehe auch

* method [RemoveMacros](../removemacros/)
* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)


