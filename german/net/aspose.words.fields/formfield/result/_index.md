---
title: FormField.Result
linktitle: Result
articleTitle: Result
second_title: Aspose.Words für .NET
description: Entdecken Sie die FormField-Ergebniseigenschaft, verwalten und passen Sie die Zeichenfolgenausgabe Ihrer Formularfelder einfach an, um das Benutzererlebnis zu verbessern.
type: docs
weight: 170
url: /de/net/aspose.words.fields/formfield/result/
---
## FormField.Result property

Ruft eine Zeichenfolge ab oder legt sie fest, die das Ergebnis dieses Formularfelds darstellt.

```csharp
public string Result { get; set; }
```

## Bemerkungen

Bei einem Textformularfeld ist das Ergebnis der Text, der sich im Feld befindet.

Bei einem Kontrollkästchen-Formularfeld kann das Ergebnis „1“ oder „0“ sein, um anzuzeigen, ob es aktiviert oder deaktiviert ist.

Bei einem Dropdown-Formularfeld ist das Ergebnis die im Dropdown ausgewählte Zeichenfolge.

Einstellung`Result` Für ein Textformularfeld gilt nicht das in[`TextInputFormat`](../textinputformat/) Wenn Sie einen Wert festlegen und das Format anwenden möchten, verwenden Sie die[`SetTextInputValue`](../settextinputvalue/) Verfahren.

Für ein Textformularfeld ist die[`TextInputDefault`](../textinputdefault/) Wert wird angewendet wenn*value* Ist`null`.

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
