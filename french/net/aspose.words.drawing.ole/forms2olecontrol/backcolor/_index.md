---
title: Forms2OleControl.BackColor
linktitle: BackColor
articleTitle: BackColor
second_title: Aspose.Words pour .NET
description: Découvrez la propriété BackColor de Forms2OleControl pour personnaliser la couleur d'arrière-plan de votre contrôle. Améliorez votre interface utilisateur avec des options de couleurs flexibles dès aujourd'hui !
type: docs
weight: 10
url: /fr/net/aspose.words.drawing.ole/forms2olecontrol/backcolor/
---
## Forms2OleControl.BackColor property

Obtient ou définit une couleur d'arrière-plan du contrôle. La valeur par défaut dépend du type de contrôle.

```csharp
public Color BackColor { get; set; }
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
