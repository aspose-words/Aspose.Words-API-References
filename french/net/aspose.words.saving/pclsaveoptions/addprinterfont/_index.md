---
title: PclSaveOptions.AddPrinterFont
linktitle: AddPrinterFont
articleTitle: AddPrinterFont
second_title: Aspose.Words pour .NET
description: PclSaveOptions AddPrinterFont méthode. Ajoute des informations sur la police téléchargée sur limprimante par le fabricant en C#.
type: docs
weight: 50
url: /fr/net/aspose.words.saving/pclsaveoptions/addprinterfont/
---
## PclSaveOptions.AddPrinterFont method

Ajoute des informations sur la police téléchargée sur l'imprimante par le fabricant.

```csharp
public void AddPrinterFont(string fontFullName, string fontPclName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fontFullName | String | Nom complet de la police (par exemple "Times New Roman Bold Italic"). |
| fontPclName | String | Nom de la police utilisée dans le document Pcl. |

## Remarques

Il existe 52 polices qui doivent être intégrées dans n'importe quelle imprimante conformément aux spécifications Pcl. Cependant, les fabricants peuvent ajouter d'autres polices à leurs appareils.

## Exemples

Montre comment demander à une imprimante de remplacer toutes les instances d’une police spécifique par une police différente.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Courier";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.AddPrinterFont("Courier New", "Courier");

// Lors de l'impression de ce document, l'imprimante utilisera la police "Courier New"
// pour accéder aux endroits où notre document utilisait la police "Courier".
doc.Save(ArtifactsDir + "PclSaveOptions.AddPrinterFont.pcl", saveOptions);
```

### Voir également

* class [PclSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
