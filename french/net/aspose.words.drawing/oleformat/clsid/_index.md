---
title: OleFormat.Clsid
linktitle: Clsid
articleTitle: Clsid
second_title: Aspose.Words pour .NET
description: Découvrez la propriété OleFormat Clsid pour récupérer facilement le CLSID des objets OLE, améliorant ainsi les fonctionnalités et les performances de votre application.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing/oleformat/clsid/
---
## OleFormat.Clsid property

Obtient le CLSID de l'objet OLE.

```csharp
public Guid Clsid { get; }
```

## Exemples

Montre comment accéder à un contrôle OLE intégré dans un document et à ses contrôles enfants.

```csharp
Document doc = new Document(MyDir + "OLE ActiveX controls.docm");

// Les formes stockent et affichent les objets OLE dans le corps du document.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual("6e182020-f460-11ce-9bcd-00aa00608e01", shape.OleFormat.Clsid.ToString());

Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;

// Certains contrôles OLE peuvent contenir des contrôles enfants, comme celui de ce document avec trois boutons d'options.
Forms2OleControlCollection oleControlCollection = oleControl.ChildNodes;

Assert.AreEqual(3, oleControlCollection.Count);

Assert.AreEqual("C#", oleControlCollection[0].Caption);
Assert.AreEqual("1", oleControlCollection[0].Value);

Assert.AreEqual("Visual Basic", oleControlCollection[1].Caption);
Assert.AreEqual("0", oleControlCollection[1].Value);

Assert.AreEqual("Delphi", oleControlCollection[2].Caption);
Assert.AreEqual("0", oleControlCollection[2].Value);
```

### Voir également

* class [OleFormat](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
