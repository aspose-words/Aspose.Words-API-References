---
title: ComHelper.Open
linktitle: Open
articleTitle: Open
second_title: Aspose.Words pour .NET
description: Bénéficiez d'une intégration transparente avec la méthode Open de ComHelper, permettant un chargement de documents sans effort à partir de fichiers pour vos applications COM.
type: docs
weight: 20
url: /fr/net/aspose.words/comhelper/open/
---
## Open(*string*) {#open_1}

Permet à une application COM de charger un[`Document`](../../document/) à partir d'un fichier.

```csharp
public Document Open(string fileName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Nom de fichier du document à charger. |

### Return_Value

UN[`Document`](../../document/) objet qui représente un document Word.

## Remarques

Cette méthode est la même que l'appel de[`Document`](../../document/) constructeur avec un paramètre de nom de fichier.

## Exemples

```csharp
[VBScript]

Dim helper
Set helper = CreateObject("Aspose.Words.ComHelper")

Dim doc
Set doc = helper.Open(fileName)
```

Montre comment ouvrir des documents à l'aide de la classe ComHelper.

```csharp
// La classe ComHelper nous permet de charger des documents à partir de clients COM.
ComHelper comHelper = new ComHelper();

// 1 - Utilisation d'un nom de fichier système local :
Document doc = comHelper.Open(MyDir + "Document.docx");

Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 2 - À partir d'un flux :
using (FileStream stream = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    doc = comHelper.Open(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

### Voir également

* class [Document](../../document/)
* class [ComHelper](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## Open(*Stream*) {#open}

Permet à une application COM de se charger[`Document`](../../document/) à partir d'un flux.

```csharp
public Document Open(Stream stream)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| stream | Stream | Un objet de flux .NET qui contient le document à charger. |

### Return_Value

UN[`Document`](../../document/) objet qui représente un document Word.

## Remarques

Cette méthode est la même que l'appel de[`Document`](../../document/) constructeur avec un paramètre de flux.

## Exemples

Montre comment ouvrir des documents à l'aide de la classe ComHelper.

```csharp
// La classe ComHelper nous permet de charger des documents à partir de clients COM.
ComHelper comHelper = new ComHelper();

// 1 - Utilisation d'un nom de fichier système local :
Document doc = comHelper.Open(MyDir + "Document.docx");

Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 2 - À partir d'un flux :
using (FileStream stream = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    doc = comHelper.Open(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

### Voir également

* class [Document](../../document/)
* class [ComHelper](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
