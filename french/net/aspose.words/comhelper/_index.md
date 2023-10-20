---
title: ComHelper Class
linktitle: ComHelper
articleTitle: ComHelper
second_title: Aspose.Words pour .NET
description: Aspose.Words.ComHelper classe. Fournit des méthodes permettant aux clients COM de charger un document dans Aspose.Words en C#.
type: docs
weight: 220
url: /fr/net/aspose.words/comhelper/
---
## ComHelper class

Fournit des méthodes permettant aux clients COM de charger un document dans Aspose.Words.

```csharp
public class ComHelper
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [ComHelper](comhelper/)() | Initialise une nouvelle instance de cette classe. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Open](../../aspose.words/comhelper/open/#open)(*Stream*) | Permet de charger une application COM[`Document`](../document/) à partir d'un flux. |
| [Open](../../aspose.words/comhelper/open/#open_1)(*string*) | Permet à une application COM de charger un[`Document`](../document/) à partir d'un fichier. |
| [OpenIStream](../../aspose.words/comhelper/openistream/)(*IStream*) | Permet à une application COM de charger un[`Document`](../document/) à partir d'un objet IStream. |

## Remarques

Utilisez le`ComHelper` classe pour charger un document à partir d'un fichier ou d'un flux dans un [`Document`](../document/) objet dans une application COM.

Le[`Document`](../document/) La classe fournit un constructeur par défaut pour créer un nouveau document et fournit également des constructeurs surchargés pour charger un document à partir d'un fichier ou d'un flux. Si vous utilisez Aspose.Words à partir d'une application .NET, vous pouvez utiliser tous les[`Document`](../document/) directement les constructeurs, mais si vous utilisez Aspose.Words à partir d'une application COM, uniquement la valeur par défaut[`Document`](../document/) Le constructeur est disponible.

## Exemples

```csharp
[VBScript]

Dim helper
Set helper = CreateObject("Aspose.Words.ComHelper")

Dim doc
Set doc = helper.Open(fileName)
```

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

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
