---
title: FormField.Result
second_title: Aspose.Words für .NET-API-Referenz
description: FormField eigendom. Ruft eine Zeichenfolge ab die das Ergebnis dieses Formularfelds darstellt oder legt diese fest.
type: docs
weight: 170
url: /de/net/aspose.words.fields/formfield/result/
---
## FormField.Result property

Ruft eine Zeichenfolge ab, die das Ergebnis dieses Formularfelds darstellt, oder legt diese fest.

```csharp
public string Result { get; set; }
```

### Bemerkungen

Bei einem Textformularfeld ist das Ergebnis der Text, der sich im Feld befindet.

Für ein Kontrollkästchen-Formularfeld kann das Ergebnis „1“ oder „0“ sein, um anzuzeigen, ob es aktiviert oder deaktiviert ist.

Bei einem Dropdown-Formularfeld ist das Ergebnis die im Dropdown ausgewählte Zeichenfolge.

Einstellung`Result` Für ein Textformularfeld gilt nicht das in angegebene Textformat [`TextInputFormat`](../textinputformat/) . Wenn Sie einen Wert festlegen und das Format anwenden möchten, verwenden Sie das[`SetTextInputValue`](../settextinputvalue/) Methode.

Für ein Textformularfeld das[`TextInputDefault`](../textinputdefault/) Wert wird angewendet wenn*value* Ist`Null`.

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

* class [FormField](../)
* namensraum [Aspose.Words.Fields](../../formfield/)
* Montage [Aspose.Words](../../../)


