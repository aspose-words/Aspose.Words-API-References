---
title: FormField Class
linktitle: FormField
articleTitle: FormField
second_title: Aspose.Words per .NET
description: Aspose.Words.Fields.FormField classe. Rappresenta un singolo campo modulo in C#.
type: docs
weight: 2620
url: /it/net/aspose.words.fields/formfield/
---
## FormField class

Rappresenta un singolo campo modulo.

Per saperne di più, visita il[Lavorare con i campi del modulo](https://docs.aspose.com/words/net/working-with-form-fields/) articolo di documentazione.

```csharp
public class FormField : SpecialChar
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CalculateOnExit](../../aspose.words.fields/formfield/calculateonexit/) { get; set; } | Vero se i riferimenti al campo modulo specificato vengono aggiornati automaticamente ogni volta che si esce dal campo. |
| [CheckBoxSize](../../aspose.words.fields/formfield/checkboxsize/) { get; set; } | Ottiene o imposta la dimensione della casella di controllo in punti. Ha effetto solo quando[`IsCheckBoxExactSize`](./ischeckboxexactsize/) È`VERO` . |
| [Checked](../../aspose.words.fields/formfield/checked/) { get; set; } | Ottiene o imposta lo stato selezionato del campo del modulo della casella di controllo. Il valore predefinito per questa proprietà è`falso` . |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| [Default](../../aspose.words.fields/formfield/default/) { get; set; } | Ottiene o imposta il valore predefinito del campo del modulo della casella di controllo. Il valore predefinito per questa proprietà è`falso` . |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [DropDownItems](../../aspose.words.fields/formfield/dropdownitems/) { get; } | Fornisce l'accesso agli elementi di un campo modulo a discesa. |
| [DropDownSelectedIndex](../../aspose.words.fields/formfield/dropdownselectedindex/) { get; set; } | Ottiene o imposta l'indice specificando l'elemento attualmente selezionato in un campo del modulo a discesa. |
| [Enabled](../../aspose.words.fields/formfield/enabled/) { get; set; } | Vero se un campo modulo è abilitato. |
| [EntryMacro](../../aspose.words.fields/formfield/entrymacro/) { get; set; } | Restituisce o imposta il nome di una macro di voce per il campo modulo. |
| [ExitMacro](../../aspose.words.fields/formfield/exitmacro/) { get; set; } | Restituisce o imposta un nome di macro di uscita per il campo modulo. |
| [Font](../../aspose.words/inline/font/) { get; } | Fornisce l'accesso alla formattazione dei caratteri di questo oggetto. |
| [HelpText](../../aspose.words.fields/formfield/helptext/) { get; set; } | Restituisce o imposta il testo visualizzato in una finestra di messaggio quando il campo del modulo è attivo e l'utente preme F1. |
| [IsCheckBoxExactSize](../../aspose.words.fields/formfield/ischeckboxexactsize/) { get; set; } | Ottiene o imposta il valore booleano che indica se la dimensione della casella di testo è automatica o specificata esplicitamente. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Restituisce`VERO` se questo nodo può contenere altri nodi. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Restituisce vero se questo oggetto è stato eliminato in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Restituisce true se la formattazione dell'oggetto è stata modificata in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Restituisce vero se questo oggetto è stato inserito in Microsoft Word mentre il rilevamento delle modifiche era abilitato. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Restituisce`VERO` se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre il rilevamento delle modifiche era abilitato. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Restituisce`VERO` se questo oggetto è stato spostato (inserito) in Microsoft Word mentre il rilevamento delle modifiche era abilitato. |
| [MaxLength](../../aspose.words.fields/formfield/maxlength/) { get; set; } | Lunghezza massima del campo di testo. Zero quando la lunghezza non è limitata. |
| [Name](../../aspose.words.fields/formfield/name/) { get; set; } | Ottiene o imposta il nome del campo del modulo. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| override [NodeType](../../aspose.words.fields/formfield/nodetype/) { get; } | RestituisceFormField . |
| [OwnHelp](../../aspose.words.fields/formfield/ownhelp/) { get; set; } | Specifica l'origine del testo visualizzato in una finestra di messaggio quando un campo modulo è attivo e l'utente preme F1. |
| [OwnStatus](../../aspose.words.fields/formfield/ownstatus/) { get; set; } | Specifica l'origine del testo visualizzato nella barra di stato quando è attivo un campo modulo. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ottiene il genitore immediato di questo nodo. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Recupera il genitore[`Paragraph`](../../aspose.words/paragraph/) di questo nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ottiene il nodo immediatamente precedente questo nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Restituisce a[`Range`](../../aspose.words/range/) oggetto che rappresenta la porzione di documento contenuta in questo nodo. |
| [Result](../../aspose.words.fields/formfield/result/) { get; set; } | Ottiene o imposta una stringa che rappresenta il risultato di questo campo modulo. |
| [StatusText](../../aspose.words.fields/formfield/statustext/) { get; set; } | Restituisce o imposta il testo visualizzato nella barra di stato quando il focus è su un campo modulo. |
| [TextInputDefault](../../aspose.words.fields/formfield/textinputdefault/) { get; set; } | Ottiene o imposta la stringa predefinita o un'espressione di calcolo di un campo modulo di testo. |
| [TextInputFormat](../../aspose.words.fields/formfield/textinputformat/) { get; set; } | Restituisce o imposta la formattazione del testo per un campo modulo di testo. |
| [TextInputType](../../aspose.words.fields/formfield/textinputtype/) { get; set; } | Ottiene o imposta il tipo di un campo modulo di testo. |
| [Type](../../aspose.words.fields/formfield/type/) { get; } | Restituisce il tipo di campo modulo. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words.fields/formfield/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accetta un visitatore. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicato del nodo. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Ottiene il primo antenato dell'oggetto specificato[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ottiene il primo antenato del tipo di oggetto specificato. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Ottiene il carattere speciale rappresentato da questo nodo. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero di preordine. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ottiene il nodo precedente in base all'algoritmo di attraversamento dell'albero di preordine. |
| [Remove](../../aspose.words/node/remove/)() | Si rimuove dal genitore. |
| [RemoveField](../../aspose.words.fields/formfield/removefield/)() | Rimuove il campo modulo completo, non solo il carattere speciale del campo modulo. |
| [SetTextInputValue](../../aspose.words.fields/formfield/settextinputvalue/)(*object*) | Applica il formato testo specificato in[`TextInputFormat`](./textinputformat/) e memorizza il valore in[`Result`](./result/) . |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

## Osservazioni

Microsoft Word fornisce i seguenti campi modulo: casella di controllo, input di testo e menu a discesa (casella combinata).

`FormField`è un nodo inline e può essere solo un figlio di[`Paragraph`](../../aspose.words/paragraph/).

`FormField` è rappresentato in un documento da un carattere speciale e posizionato come carattere all'interno di una riga di testo.

Un campo modulo completo in un documento Word è una struttura complessa rappresentata da diversi nodi : inizio campo, codice campo come TESTOFORMA, dati campo modulo, separatore campo, risultato campo , fine campo e un segnalibro. Per creare campi modulo a livello di codice in un documento Word use [`InsertCheckBox`](../../aspose.words/documentbuilder/insertcheckbox/) , [`InsertTextInput`](../../aspose.words/documentbuilder/inserttextinput/) e [`InsertComboBox`](../../aspose.words/documentbuilder/insertcombobox/) which assicurati che tutti i nodi dei campi del modulo siano creati nell'ordine corretto e in uno stato adeguato.

## Esempi

Mostra come formattare l'intero FormField, incluso il valore del campo.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

FormField formField = doc.Range.FormFields[0];
formField.Font.Bold = true;
formField.Font.Size = 24;
formField.Font.Color = Color.Red;

formField.Result = "Aspose.FormField";

doc = DocumentHelper.SaveOpen(doc);

Run formFieldRun = doc.FirstSection.Body.FirstParagraph.Runs[1];

Assert.AreEqual("Aspose.FormField", formFieldRun.Text);
Assert.AreEqual(true, formFieldRun.Font.Bold);
Assert.AreEqual(24, formFieldRun.Font.Size);
Assert.AreEqual(Color.Red.ToArgb(), formFieldRun.Font.Color.ToArgb());
```

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

* class [SpecialChar](../../aspose.words/specialchar/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
