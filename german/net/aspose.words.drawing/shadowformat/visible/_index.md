---
title: ShadowFormat.Visible
second_title: Aspose.Words für .NET-API-Referenz
description: ShadowFormat eigendom. Gibt zurückWAHR wenn die auf diese Instanz angewendete Formatierung sichtbar ist.
type: docs
weight: 20
url: /de/net/aspose.words.drawing/shadowformat/visible/
---
## ShadowFormat.Visible property

Gibt zurück`WAHR` wenn die auf diese Instanz angewendete Formatierung sichtbar ist.

```csharp
public bool Visible { get; }
```

### Bemerkungen

Anders[`Clear`](../clear/) , zuweisen`FALSCH` auf „Sichtbar“ löscht die Formatierung nicht, es verbirgt nur den Formeffekt.

### Beispiele

Zeigt, wie mit einer Schattenformatierung für die Form gearbeitet wird.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];

if (shape.ShadowFormat.Visible && shape.ShadowFormat.Type == ShadowType.Shadow2)                
    shape.ShadowFormat.Type = ShadowType.Shadow7;

if (shape.ShadowFormat.Type == ShadowType.ShadowMixed)            
    shape.ShadowFormat.Clear();
```

### Siehe auch

* class [ShadowFormat](../)
* namensraum [Aspose.Words.Drawing](../../shadowformat/)
* Montage [Aspose.Words](../../../)


