---
title: DocumentBuilder.InsertComboBox
linktitle: InsertComboBox
articleTitle: InsertComboBox
second_title: Aspose.Words per .NET
description: Migliora i tuoi documenti con il metodo InsertComboBox di DocumentBuilder. Aggiungi facilmente campi modulo interattivi con caselle combinate per una migliore esperienza utente.
type: docs
weight: 300
url: /it/net/aspose.words/documentbuilder/insertcombobox/
---
## DocumentBuilder.InsertComboBox method

Inserisce un campo modulo combobox nella posizione corrente.

```csharp
public FormField InsertComboBox(string name, string[] items, int selectedIndex)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | String | Il nome del campo del modulo. Può essere una stringa vuota. I valori più lunghi di 20 caratteri verranno troncati. |
| items | String[] | Gli elementi del ComboBox. Massimo 25 elementi. |
| selectedIndex | Int32 | Indice dell'elemento selezionato nella casella combinata. |

### Valore di ritorno

Il nodo del campo modulo appena inserito.

## Osservazioni

Se si specifica un nome per il campo del modulo, verrà automaticamente creato un segnalibro con lo stesso nome.

## Esempi

Mostra come inserire un campo modulo casella combinata in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserire un modulo che richiede all'utente di scegliere una delle voci dal menu.
builder.Write("Pick a fruit: ");
string[] items = { "Apple", "Banana", "Cherry" };
builder.InsertComboBox("DropDown", items, 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertComboBox.docx");
```

Mostra come creare campi modulo.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// I campi modulo sono oggetti nel documento con cui l'utente può interagire, chiedendogli di immettere valori.
// Possiamo crearli utilizzando un generatore di documenti. Di seguito sono riportati due metodi per farlo.
// 1 - Input di testo di base:
builder.InsertTextInput("My text input", TextFormFieldType.Regular, 
    "", "Enter your name here", 30);

// 2 - Casella combinata con testo di richiesta e un intervallo di valori possibili:
string[] items =
{
    "-- Select your favorite footwear --", "Sneakers", "Oxfords", "Flip-flops", "Other"
};

builder.InsertParagraph();
builder.InsertComboBox("My combo box", items, 0);

builder.Document.Save(ArtifactsDir + "DocumentBuilder.CreateForm.docx");
```

### Guarda anche

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
