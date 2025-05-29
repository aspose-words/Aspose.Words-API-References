---
title: CommandButtonControl Class
linktitle: CommandButtonControl
articleTitle: CommandButtonControl
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.Ole.CommandButtonControl per creare facilmente pulsanti interattivi che eseguono macro, migliorando il coinvolgimento degli utenti nelle tue applicazioni.
type: docs
weight: 1450
url: /it/net/aspose.words.drawing.ole/commandbuttoncontrol/
---
## CommandButtonControl class

Il controllo CommandButton esegue una macro che esegue un'azione quando un utente fa clic su di esso.

```csharp
public class CommandButtonControl : Forms2OleControl
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [CommandButtonControl](commandbuttoncontrol/)() | Inizializza una nuova istanza di`CommandButtonControl` classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BackColor](../../aspose.words.drawing.ole/forms2olecontrol/backcolor/) { get; set; } | Ottiene o imposta un colore di sfondo del controllo. Il valore predefinito dipende dal tipo di controllo. |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; set; } | Ottiene o imposta una proprietà Caption del controllo. Il valore predefinito è una stringa vuota. |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Ottiene la raccolta di controlli figlio immediati. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Restituisce`VERO` se il controllo è nello stato abilitato. |
| [ForeColor](../../aspose.words.drawing.ole/forms2olecontrol/forecolor/) { get; set; } | Ottiene o imposta un colore di primo piano del controllo. Il valore predefinito dipende dal tipo di controllo. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Ottiene o imposta una stringa che specifica un gruppo di controlli reciprocamente esclusivi. Il valore predefinito è una stringa vuota. |
| [Height](../../aspose.words.drawing.ole/forms2olecontrol/height/) { get; set; } | Ottiene o imposta l'altezza del controllo in punti. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Restituisce`VERO` se il controllo è un[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Ottiene o imposta il nome del controllo ActiveX. |
| override [Type](../../aspose.words.drawing.ole/commandbuttoncontrol/type/) { get; } | Ottiene il tipo di controllo Forms 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Ottiene la proprietà Value sottostante che spesso rappresenta lo stato di controllo. Ad esempio, il pulsante di opzione selezionato ha valore '1' mentre quello non selezionato ha valore '0'. Il valore predefinito è una stringa vuota. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Ottiene o imposta la larghezza del controllo in punti. |

## Esempi

Mostra come inserire un controllo ActiveX.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### Guarda anche

* class [Forms2OleControl](../forms2olecontrol/)
* spazio dei nomi [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* assemblea [Aspose.Words](../../)
