---
title: FormField.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie die Eigenschaft „FormField Name“ einfach verwalten können, um Ihre Formulare für eine bessere Benutzereinbindung und Datenerfassung anzupassen und zu optimieren.
type: docs
weight: 130
url: /de/net/aspose.words.fields/formfield/name/
---
## FormField.Name property

Ruft den Formularfeldnamen ab oder legt ihn fest.

```csharp
public string Name { get; set; }
```

## Bemerkungen

Microsoft Word erlaubt Zeichenfolgen mit maximal 20 Zeichen.

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

* class [FormField](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
