---
title: ComHelper
linktitle: ComHelper
articleTitle: ComHelper
second_title: Aspose.Words pour .NET
description: ComHelper constructeur. Initialise une nouvelle instance de cette classe en C#.
type: docs
weight: 10
url: /fr/net/aspose.words/comhelper/comhelper/
---
## ComHelper constructor

Initialise une nouvelle instance de cette classe.

```csharp
public ComHelper()
```

## Exemples

Montre comment ouvrir des documents à l’aide de la classe ComHelper.

```csharp
// La classe ComHelper nous permet de charger des documents depuis des clients COM.
ComHelper comHelper = new ComHelper();

// 1 - Utilisation d'un nom de fichier système local :
Document doc = comHelper.Open(MyDir + "Document.docx");

Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 2 - Depuis un flux :
using (FileStream stream = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    doc = comHelper.Open(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

### Voir également

* class [ComHelper](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
