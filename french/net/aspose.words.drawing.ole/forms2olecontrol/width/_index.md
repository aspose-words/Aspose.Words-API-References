---
title: Forms2OleControl.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words pour .NET
description: Découvrez comment ajuster facilement la propriété Width de Forms2OleControl pour un contrôle précis de la taille en points. Améliorez votre interface utilisateur sans effort !
type: docs
weight: 100
url: /fr/net/aspose.words.drawing.ole/forms2olecontrol/width/
---
## Forms2OleControl.Width property

Obtient ou définit une largeur du contrôle en points.

```csharp
public double Width { get; set; }
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
