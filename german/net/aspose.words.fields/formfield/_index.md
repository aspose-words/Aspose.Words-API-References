---
title: FormField
second_title: Aspose.Words für .NET-API-Referenz
description: Stellt ein einzelnes Formularfeld dar.
type: docs
weight: 2460
url: /de/net/aspose.words.fields/formfield/
---
## FormField class

Stellt ein einzelnes Formularfeld dar.

```csharp
public class FormField : SpecialChar
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CalculateOnExit](../../aspose.words.fields/formfield/calculateonexit) { get; set; } | True, wenn Verweise auf das angegebene Formularfeld automatisch aktualisiert werden, wenn das Feld verlassen wird. |
| [CheckBoxSize](../../aspose.words.fields/formfield/checkboxsize) { get; set; } | Holt oder setzt die Größe des Kontrollkästchens in Punkt. Hat nur Wirkung, wenn[`IsCheckBoxExactSize`](./ischeckboxexactsize) ist wahr. |
| [Checked](../../aspose.words.fields/formfield/checked) { get; set; } | Ruft den aktivierten Status des Kontrollkästchen-Formularfelds ab oder legt ihn fest. Der Standardwert für diese Eigenschaft ist **FALSCH** . |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| [Default](../../aspose.words.fields/formfield/default) { get; set; } | Ruft den Standardwert des Kontrollkästchen-Formularfelds ab oder legt ihn fest. Der Standardwert für diese Eigenschaft ist **FALSCH** . |
| virtual [Document](../../aspose.words/node/document) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [DropDownItems](../../aspose.words.fields/formfield/dropdownitems) { get; } | Bietet Zugriff auf die Elemente eines Dropdown-Formularfelds. |
| [DropDownSelectedIndex](../../aspose.words.fields/formfield/dropdownselectedindex) { get; set; } | Ruft den Index ab oder legt ihn fest, der das aktuell ausgewählte Element in einem Dropdown-Formularfeld angibt. |
| [Enabled](../../aspose.words.fields/formfield/enabled) { get; set; } | True, wenn ein Formularfeld aktiviert ist. |
| [EntryMacro](../../aspose.words.fields/formfield/entrymacro) { get; set; } | Gibt einen Eintragsmakronamen für das Formularfeld zurück oder legt ihn fest. |
| [ExitMacro](../../aspose.words.fields/formfield/exitmacro) { get; set; } | Gibt einen Exit-Makronamen für das Formularfeld zurück oder legt ihn fest. |
| [Font](../../aspose.words/inline/font) { get; } | Bietet Zugriff auf die Schriftformatierung dieses Objekts. |
| [HelpText](../../aspose.words.fields/formfield/helptext) { get; set; } | Gibt den Text zurück oder legt ihn fest, der in einem Meldungsfeld angezeigt wird, wenn das Formularfeld den Fokus hat und der Benutzer F1 drückt. |
| [IsCheckBoxExactSize](../../aspose.words.fields/formfield/ischeckboxexactsize) { get; set; } | Ruft den booleschen Wert ab oder legt ihn fest, der angibt, ob die Größe des Textfelds automatisch ist oder explizit angegeben wird. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | Gibt wahr zurück, wenn dieser Knoten andere Knoten enthalten kann. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsnachverfolgung aktiviert war. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision) { get; } | Gibt „true“ zurück, wenn die Formatierung des Objekts in Microsoft Word geändert wurde, während die Änderungsverfolgung aktiviert war. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision) { get; } | gibt zurück **Stimmt** wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsnachverfolgung aktiviert war. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision) { get; } | gibt zurück **Stimmt** wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsnachverfolgung aktiviert war. |
| [MaxLength](../../aspose.words.fields/formfield/maxlength) { get; set; } | Maximale Länge für das Textfeld. Null, wenn die Länge nicht begrenzt ist. |
| [Name](../../aspose.words.fields/formfield/name) { get; set; } | Ruft den Formularfeldnamen ab oder legt ihn fest. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words.fields/formfield/nodetype) { get; } | gibt zurück **NodeType.FormField** . |
| [OwnHelp](../../aspose.words.fields/formfield/ownhelp) { get; set; } | Gibt die Quelle des Textes an, der in einem Meldungsfeld angezeigt wird, wenn ein Formularfeld den Fokus hat und der Benutzer F1 drückt. |
| [OwnStatus](../../aspose.words.fields/formfield/ownstatus) { get; set; } | Gibt die Quelle des Textes an, der in der Statusleiste angezeigt wird, wenn ein Formularfeld den Fokus hat. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph) { get; } | Ruft das übergeordnete Element ab[`Paragraph`](../../aspose.words/paragraph) dieses Knotens. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Ruft den Knoten unmittelbar vor diesem Knoten ab. |
| [Range](../../aspose.words/node/range) { get; } | Gibt a zurück **Bereich** Objekt, das den Teil eines Dokuments darstellt, das in diesem Knoten enthalten ist. |
| [Result](../../aspose.words.fields/formfield/result) { get; set; } | Ruft eine Zeichenfolge ab oder legt sie fest, die das Ergebnis dieses Formularfelds darstellt. |
| [StatusText](../../aspose.words.fields/formfield/statustext) { get; set; } | Gibt den Text zurück oder legt ihn fest, der in der Statusleiste angezeigt wird, wenn ein Formularfeld den Fokus hat. |
| [TextInputDefault](../../aspose.words.fields/formfield/textinputdefault) { get; set; } | Ruft die Standardzeichenfolge oder einen Berechnungsausdruck eines Textformularfelds ab oder legt sie fest. |
| [TextInputFormat](../../aspose.words.fields/formfield/textinputformat) { get; set; } | Gibt die Textformatierung für ein Textformularfeld zurück oder legt sie fest. |
| [TextInputType](../../aspose.words.fields/formfield/textinputtype) { get; set; } | Ruft den Typ eines Textformularfelds ab oder legt ihn fest. |
| [Type](../../aspose.words.fields/formfield/type) { get; } | Gibt den Formularfeldtyp zurück. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words.fields/formfield/accept)(DocumentVisitor) | Akzeptiert einen Besucher. |
| [Clone](../../aspose.words/node/clone)(bool) | Erstellt ein Duplikat des Knotens. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Ruft den ersten Vorfahren der angegebenen ab[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| override [GetText](../../aspose.words/specialchar/gettext)() | Ruft das Sonderzeichen ab, das dieser Knoten darstellt. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ruft den nächsten Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ruft den vorherigen Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [Remove](../../aspose.words/node/remove)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveField](../../aspose.words.fields/formfield/removefield)() | Entfernt das komplette Formularfeld, nicht nur das Sonderzeichen des Formularfelds. |
| [SetTextInputValue](../../aspose.words.fields/formfield/settextinputvalue)(object) | Wendet das in angegebene Textformat an[`TextInputFormat`](./textinputformat) und speichert den Wert in[`Result`](./result) . |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in einen String. |

### Bemerkungen

Microsoft Word stellt folgende Formularfelder zur Verfügung: Checkbox, Texteingabe und Dropdown (Combobox).

**Formularfeld** ist ein Inline-Knoten und kann nur ein Kind von sein **Absatz**.

**Formularfeld** wird in einem Dokument durch ein Sonderzeichen dargestellt und als Zeichen innerhalb einer Textzeile positioniert.

Ein vollständiges Formularfeld in einem Word-Dokument ist eine komplexe Struktur, die durch mehrere Knoten dargestellt wird: Feldanfang, Feldcode wie FORMTEXT, Formularfelddaten, Feldtrennzeichen, Feldergebnis, Feldende und ein Lesezeichen. Verwenden Sie zum programmgesteuerten Erstellen von Formularfeldern in einem Word-Dokument [`DocumentBuilder.InsertCheckBox`](../../aspose.words/documentbuilder/insertcheckbox) , [`DocumentBuilder.InsertTextInput`](../../aspose.words/documentbuilder/inserttextinput) and [`DocumentBuilder.InsertComboBox`](../../aspose.words/documentbuilder/insertcombobox) which Stellen Sie sicher, dass alle Formularfeldknoten in der richtigen Reihenfolge und in einem geeigneten Zustand erstellt werden.

### Beispiele

Zeigt, wie das gesamte FormField formatiert wird, einschließlich des Feldwerts.

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

// Das Formularfeld erscheint in Form eines „select“-HTML-Tags.
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### Siehe auch

* class [SpecialChar](../../aspose.words/specialchar)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
