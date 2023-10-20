---
title: FormField.Result
linktitle: Result
articleTitle: Result
second_title: Aspose.Words per .NET
description: FormField Result proprietà. Ottiene o imposta una stringa che rappresenta il risultato di questo campo modulo in C#.
type: docs
weight: 170
url: /it/net/aspose.words.fields/formfield/result/
---
## FormField.Result property

Ottiene o imposta una stringa che rappresenta il risultato di questo campo modulo.

```csharp
public string Result { get; set; }
```

## Osservazioni

Per un campo modulo di testo il risultato è il testo presente nel campo.

Per un campo modulo casella di controllo il risultato può essere "1" o "0" per indicare selezionato o deselezionato.

Per un campo modulo a discesa il risultato è la stringa selezionata nel menu a discesa.

Collocamento`Result` per un campo modulo testo non si applica il testo format specificato in[`TextInputFormat`](../textinputformat/) . Se desideri impostare un valore e applicare il formato , utilizza il file[`SetTextInputValue`](../settextinputvalue/) metodo.

Per un campo modulo di testo il[`TextInputDefault`](../textinputdefault/) il valore viene applicato se*value* È`nullo`.

## Esempi

Mostra come inserire una casella combinata.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Inserisce una casella combinata che consentirà all'utente di scegliere un'opzione da una raccolta di stringhe.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// Il campo del modulo apparirà sotto forma di tag html "seleziona".
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### Guarda anche

* class [FormField](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
