---
title: Forms2OleControlType Enum
linktitle: Forms2OleControlType
articleTitle: Forms2OleControlType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Drawing.Ole.Forms2OleControlType, che presenta una gamma di tipi di controllo Forms 2.0 per una maggiore automazione dei documenti.
type: docs
weight: 1480
url: /it/net/aspose.words.drawing.ole/forms2olecontroltype/
---
## Forms2OleControlType enumeration

Enumera i tipi di controlli di Forms 2.0.

```csharp
public enum Forms2OleControlType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| OptionButton | `0` | Un controllo a pulsante di scelta. |
| Label | `1` | Un controllo che visualizza il testo. |
| Textbox | `2` | Un controllo che consente all'utente di immettere testo. |
| CheckBox | `3` | Un controllo che consente all'utente di selezionare o deselezionare un'opzione. |
| ToggleButton | `4` | Un controllo che consente all'utente di alternare tra due stati. |
| SpinButton | `5` | Un controllo che consente all'utente di aumentare o diminuire un valore. |
| ComboBox | `6` | Un controllo che consente all'utente di selezionare un elemento da un elenco. |
| Frame | `7` | Un controllo che raggruppa altri controlli. |
| MultiPage | `8` | Un controllo che visualizza più pagine di contenuto. |
| TabStrip | `9` | Un controllo che consente all'utente di passare da una pagina all'altra di contenuto. |
| CommandButton | `10` | Un pulsante che attiva un'azione quando viene cliccato. |
| Image | `11` | Un controllo che visualizza un'immagine. |
| ScrollBar | `12` | Un controllo che consente all'utente di scorrere il contenuto. |
| Form | `13` | Un contenitore per altri controlli. |
| ListBox | `14` | Un controllo che visualizza un elenco di elementi. |

## Esempi

Mostra come modificare lo stato del controllo CheckBox.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
CheckBoxControl checkBoxControl = (CheckBoxControl)shape.OleFormat.OleControl;
checkBoxControl.Checked = true;

Assert.AreEqual(true, checkBoxControl.Checked);
Assert.AreEqual(Forms2OleControlType.CheckBox, checkBoxControl.Type);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* assemblea [Aspose.Words](../../)
