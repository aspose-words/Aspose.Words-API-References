---
title: FormField.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „FormField Type“, um verschiedene Formularfeldtypen einfach zu identifizieren und zu verwenden und so die Funktionalität und Benutzererfahrung Ihrer Webformulare zu verbessern.
type: docs
weight: 220
url: /de/net/aspose.words.fields/formfield/type/
---
## FormField.Type property

Gibt den Formularfeldtyp zurück.

```csharp
public FieldType Type { get; }
```

## Beispiele

Zeigt, wie ein Kombinationsfeld eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Fügen Sie ein Kombinationsfeld ein, das es einem Benutzer ermöglicht, eine Option aus einer Sammlung von Zeichenfolgen auszuwählen.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// Das Formularfeld wird in Form eines „Select“-HTML-Tags angezeigt.
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### Siehe auch

* enum [FieldType](../../fieldtype/)
* class [FormField](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
