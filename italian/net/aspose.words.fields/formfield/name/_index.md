---
title: FormField.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words per .NET
description: Scopri come gestire facilmente la proprietà Nome del FormField per personalizzare e ottimizzare i tuoi moduli, migliorando il coinvolgimento degli utenti e la raccolta dei dati.
type: docs
weight: 130
url: /it/net/aspose.words.fields/formfield/name/
---
## FormField.Name property

Ottiene o imposta il nome del campo del modulo.

```csharp
public string Name { get; set; }
```

## Osservazioni

Microsoft Word consente stringhe con un massimo di 20 caratteri.

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

// Il campo del modulo apparirà sotto forma di tag HTML "select".
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### Guarda anche

* class [FormField](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
