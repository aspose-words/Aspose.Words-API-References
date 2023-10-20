---
title: FormField.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words per .NET
description: FormField Type proprietà. Restituisce il tipo di campo modulo in C#.
type: docs
weight: 220
url: /it/net/aspose.words.fields/formfield/type/
---
## FormField.Type property

Restituisce il tipo di campo modulo.

```csharp
public FieldType Type { get; }
```

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

* enum [FieldType](../../fieldtype/)
* class [FormField](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
