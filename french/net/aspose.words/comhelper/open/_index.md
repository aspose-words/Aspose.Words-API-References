---
title: ComHelper.Open
second_title: Référence de l'API Aspose.Words pour .NET
description: ComHelper méthode. Permet à une application COM de charger unDocument à partir dun fichier.
type: docs
weight: 20
url: /fr/net/aspose.words/comhelper/open/
---
## Open(string) {#open_1}

Permet à une application COM de charger un[`Document`](../../document/) à partir d'un fichier.

```csharp
public Document Open(string fileName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Nom de fichier du document à charger. |

### Return_Value

UN[`Document`](../../document/) objet qui représente un document Word.

### Remarques

Cette méthode revient à appeler le[`Document`](../../document/) constructeur avec un paramètre de nom de fichier.

### Exemples

```csharp
[VBScript]

Dim helper
Set helper = CreateObject("Aspose.Words.ComHelper")

Dim doc
Set doc = helper.Open(fileName)
```

Montre comment ouvrir des documents à l'aide de la classe ComHelper.

```csharp
// La classe ComHelper nous permet de charger des documents depuis des clients COM.
ComHelper comHelper = new ComHelper();

// 1 - Utilisation d'un nom de fichier système local :
Document doc = comHelper.Open(MyDir + "Document.docx");

Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 2 - Depuis un flux :
using (FileStream stream = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    doc = comHelper.Open(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

### Voir également

* class [Document](../../document/)
* class [ComHelper](../)
* espace de noms [Aspose.Words](../../comhelper/)
* Assemblée [Aspose.Words](../../../)

---

## Open(Stream) {#open}

Autorise le chargement d'une application COM[`Document`](../../document/) à partir d'un flux.

```csharp
public Document Open(Stream stream)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| stream | Stream | Un objet de flux .NET qui contient le document à charger. |

### Return_Value

UN[`Document`](../../document/) objet qui représente un document Word.

### Remarques

Cette méthode revient à appeler le[`Document`](../../document/) constructeur avec un paramètre de flux.

### Exemples

Montre comment ouvrir des documents à l'aide de la classe ComHelper.

```csharp
// La classe ComHelper nous permet de charger des documents depuis des clients COM.
ComHelper comHelper = new ComHelper();

// 1 - Utilisation d'un nom de fichier système local :
Document doc = comHelper.Open(MyDir + "Document.docx");

Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 2 - Depuis un flux :
using (FileStream stream = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    doc = comHelper.Open(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

### Voir également

* class [Document](../../document/)
* class [ComHelper](../)
* espace de noms [Aspose.Words](../../comhelper/)
* Assemblée [Aspose.Words](../../../)


