---
title: Class Forms2OleControlCollection
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.Ole.Forms2OleControlCollection klas. Stellt eine Sammlung von darForms2OleControl Objekte.
type: docs
weight: 1120
url: /de/net/aspose.words.drawing.ole/forms2olecontrolcollection/
---
## Forms2OleControlCollection class

Stellt eine Sammlung von dar[`Forms2OleControl`](../forms2olecontrol/) Objekte.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Ole-Objekten](https://docs.aspose.com/words/net/working-with-ole-objects/) Dokumentationsartikel.

```csharp
public class Forms2OleControlCollection : IEnumerable<Forms2OleControl>
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [Forms2OleControlCollection](forms2olecontrolcollection/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.drawing.ole/forms2olecontrolcollection/count/) { get; } | Ruft die Anzahl der Objekte in der Sammlung ab. |
| [Item](../../aspose.words.drawing.ole/forms2olecontrolcollection/item/) { get; } | Ruft ab[`Forms2OleControl`](../forms2olecontrol/) Objekt an einem angegebenen Index. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.ole/forms2olecontrolcollection/getenumerator/)() | Ruft den Enumerator ab. |

### Beispiele

Zeigt, wie auf ein in ein Dokument eingebettetes OLE-Steuerelement und seine untergeordneten Steuerelemente zugegriffen wird.

```csharp
Document doc = new Document(MyDir + "OLE ActiveX controls.docm");

// Formen speichern und zeigen OLE-Objekte im Hauptteil des Dokuments an.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual("6e182020-f460-11ce-9bcd-00aa00608e01", shape.OleFormat.Clsid.ToString());

Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;

// Einige OLE-Steuerelemente enthalten möglicherweise untergeordnete Steuerelemente, z. B. das in diesem Dokument mit drei Optionsschaltflächen.
Forms2OleControlCollection oleControlCollection = oleControl.ChildNodes;

Assert.AreEqual(3, oleControlCollection.Count);

Assert.AreEqual("C#", oleControlCollection[0].Caption);
Assert.AreEqual("1", oleControlCollection[0].Value);

Assert.AreEqual("Visual Basic", oleControlCollection[1].Caption);
Assert.AreEqual("0", oleControlCollection[1].Value);

Assert.AreEqual("Delphi", oleControlCollection[2].Caption);
Assert.AreEqual("0", oleControlCollection[2].Value);
```

### Siehe auch

* class [Forms2OleControl](../forms2olecontrol/)
* namensraum [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* Montage [Aspose.Words](../../)


