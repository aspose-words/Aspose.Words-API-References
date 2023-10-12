---
title: FormField.Type
second_title: Aspose.Words für .NET-API-Referenz
description: FormField eigendom. Gibt den Formularfeldtyp zurück.
type: docs
weight: 220
url: /de/net/aspose.words.fields/formfield/type/
---
## FormField.Type property

Gibt den Formularfeldtyp zurück.

```csharp
public FieldType Type { get; }
```

### Beispiele

Zeigt, wie ein Kombinationsfeld eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Ein Kombinationsfeld einfügen, das es einem Benutzer ermöglicht, eine Option aus einer Sammlung von Zeichenfolgen auszuwählen.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// Das Formularfeld wird in Form eines „select“-HTML-Tags angezeigt.
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### Siehe auch

* enum [FieldType](../../fieldtype/)
* class [FormField](../)
* namensraum [Aspose.Words.Fields](../../formfield/)
* Montage [Aspose.Words](../../../)


