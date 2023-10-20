---
title: FieldMacroButton.MacroName
linktitle: MacroName
articleTitle: MacroName
second_title: Aspose.Words für .NET
description: FieldMacroButton MacroName eigendom. Ruft den Namen des auszuführenden Makros oder Befehls ab oder legt diesen fest in C#.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldmacrobutton/macroname/
---
## FieldMacroButton.MacroName property

Ruft den Namen des auszuführenden Makros oder Befehls ab oder legt diesen fest.

```csharp
public string MacroName { get; set; }
```

## Beispiele

Zeigt, wie wir MACROBUTTON-Felder verwenden, um die Makros eines Dokuments durch Klicken auszuführen.

```csharp
Document doc = new Document(MyDir + "Macro.docm");
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.IsTrue(doc.HasMacros);

// Ein MACROBUTTON-Feld einfügen und in der MacroName-Eigenschaft namentlich auf eines der Makros des Dokuments verweisen.
FieldMacroButton field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "MyMacro";
field.DisplayText = "Double click to run macro: " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field.GetFieldCode());

// Verwenden Sie die Eigenschaft, um auf „ViewZoom200“ zu verweisen, ein Makro, das im Lieferumfang von Microsoft Word enthalten ist.
// Alle anderen Makros finden wir über View -> Makros (Dropdown) -> Makros anzeigen.
// Wählen Sie in diesem Menü „Word-Befehle“ aus der Dropdown-Liste „Makros in:“ aus.
// Wenn unser Dokument ein benutzerdefiniertes Makro mit demselben Namen wie ein Standardmakro enthält,
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

* class [FieldMacroButton](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
