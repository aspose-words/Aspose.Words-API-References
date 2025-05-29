---
title: Forms2OleControl.Height
linktitle: Height
articleTitle: Height
second_title: Aspose.Words pour .NET
description: Ajustez facilement la hauteur du contrôle Forms2OleControl en points pour un affichage et des fonctionnalités optimales. Améliorez votre interface utilisateur avec des dimensions de contrôle précises !
type: docs
weight: 70
url: /fr/net/aspose.words.drawing.ole/forms2olecontrol/height/
---
## Forms2OleControl.Height property

Obtient ou définit la hauteur du contrôle en points.

```csharp
public double Height { get; set; }
```

## Exemples

Montre comment définir les propriétés du contrôle ActiveX.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;
oleControl.ForeColor = Color.FromArgb(0x17, 0xE1, 0x35);
oleControl.BackColor = Color.FromArgb(0x33, 0x97, 0xF4);
oleControl.Height = 100.54;
oleControl.Width = 201.06;
```

### Voir également

* class [Forms2OleControl](../)
* espace de noms [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* Assemblée [Aspose.Words](../../../)
