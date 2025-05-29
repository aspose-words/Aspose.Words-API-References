---
title: DocumentBuilder.InsertOleObjectAsIcon
linktitle: InsertOleObjectAsIcon
articleTitle: InsertOleObjectAsIcon
second_title: Aspose.Words pour .NET
description: Insérez facilement des objets OLE sous forme d'icônes dans vos documents avec DocumentBuilder. Personnalisez les icônes et les légendes tout en garantissant une intégration fluide.
type: docs
weight: 430
url: /fr/net/aspose.words/documentbuilder/insertoleobjectasicon/
---
## InsertOleObjectAsIcon(*string, bool, string, string*) {#insertoleobjectasicon_1}

Insère un objet OLE incorporé ou lié comme icône dans le document. Permet de spécifier le fichier et la légende de l'icône. Détecte le type d'objet OLE grâce à l'extension de fichier.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, bool isLinked, string iconFile, 
    string iconCaption)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Chemin complet vers le fichier. |
| isLinked | Boolean | Si`vrai` puis l'objet OLE lié est inséré sinon l'objet OLE incorporé est inséré. |
| iconFile | String | Chemin complet vers le fichier ICO. Si la valeur est`nul` , Aspose.Words utilisera une image prédéfinie. |
| iconCaption | String | Légende de l'icône . Si la valeur est`nul` , Aspose.Words utilisera le nom de fichier. |

### Return_Value

Nœud de forme contenant un objet Ole et inséré à la position actuelle du générateur.

## Exemples

Montre comment insérer un objet OLE dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Les objets OLE sont des liens vers des fichiers de notre système de fichiers local qui peuvent être ouverts par d'autres applications installées.
// Un double-clic sur ces formes lancera l'application, puis utilisez-la pour ouvrir l'objet lié.
// Il existe trois façons d'utiliser la méthode InsertOleObject pour insérer ces formes et configurer leur apparence.
// 1 - Image prise à partir du système de fichiers local :
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // Si 'presentation' est omis et 'asIcon' est défini, cette méthode surchargée sélectionne
    // l'icône selon l'extension de fichier et utilise le nom de fichier pour la légende de l'icône.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// Si 'presentation' est omis et 'asIcon' est défini, cette méthode surchargée sélectionne
// l'icône selon 'progId' et utilise le nom de fichier pour la légende de l'icône.
// 2 - Icône basée sur l'application qui ouvrira l'objet :
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// Si 'iconFile' et 'iconCaption' sont omis, cette méthode surchargée sélectionne
// l'icône selon 'progId' et utilise la légende d'icône prédéfinie.
// 3 - Icône d'image de 32 x 32 pixels ou moins provenant du système de fichiers local, avec une légende personnalisée :
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(*string, string, bool, string, string*) {#insertoleobjectasicon_2}

Insère un objet OLE incorporé ou lié comme icône dans le document. Permet de spécifier le fichier d'icône et la légende. Détecte le type d'objet OLE à l'aide du paramètre progID donné.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, string progId, bool isLinked, string iconFile, 
    string iconCaption)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Chemin complet vers le fichier. |
| progId | String | ProgId de l'objet OLE. |
| isLinked | Boolean | Si`vrai` puis l'objet OLE lié est inséré sinon l'objet OLE incorporé est inséré. |
| iconFile | String | Chemin complet vers le fichier ICO. Si la valeur est`nul` , Aspose.Words utilisera une image prédéfinie. |
| iconCaption | String | Légende de l'icône . Si la valeur est`nul` , Aspose.Words utilisera le nom de fichier. |

### Return_Value

Nœud de forme contenant un objet Ole et inséré à la position actuelle du générateur.

## Exemples

Montre comment insérer un objet OLE incorporé ou lié sous forme d'icône dans le document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si 'iconFile' et 'iconCaption' sont omis, cette méthode surchargée sélectionne
// l'icône selon 'progId' et utilise le nom de fichier pour la légende de l'icône.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // Si 'iconFile' et 'iconCaption' sont omis, cette méthode surchargée sélectionne
    // l'icône selon l'extension de fichier et utilise le nom de fichier pour la légende de l'icône.
    Shape shape = builder.InsertOleObjectAsIcon(stream, "PowerPoint.Application", ImageDir + "Logo icon.ico",
        "My embedded file stream");

    OlePackage setOlePackage = shape.OleFormat.OlePackage;
    setOlePackage.FileName = "Presentation.pptx";
    setOlePackage.DisplayName = "Presentation.pptx";
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjectAsIcon.docx");
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(*Stream, string, string, string*) {#insertoleobjectasicon}

Insère un objet OLE incorporé comme icône depuis un flux dans le document. Permet de spécifier le fichier d'icône et la légende. Détecte le type d'objet OLE à l'aide du paramètre progID donné.

```csharp
public Shape InsertOleObjectAsIcon(Stream stream, string progId, string iconFile, 
    string iconCaption)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| stream | Stream | Flux contenant des données d'application. |
| progId | String | ProgId de l'objet OLE. |
| iconFile | String | Chemin complet vers le fichier ICO. Si la valeur est`nul` , Aspose.Words utilisera une image prédéfinie. |
| iconCaption | String | Légende de l'icône . Si la valeur est`nul` , Aspose.Words utilisera une légende d'icône prédéfinie. |

### Return_Value

Nœud de forme contenant un objet Ole et inséré à la position actuelle du générateur.

## Exemples

Montre comment insérer un objet OLE incorporé ou lié sous forme d'icône dans le document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si 'iconFile' et 'iconCaption' sont omis, cette méthode surchargée sélectionne
// l'icône selon 'progId' et utilise le nom de fichier pour la légende de l'icône.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // Si 'iconFile' et 'iconCaption' sont omis, cette méthode surchargée sélectionne
    // l'icône selon l'extension de fichier et utilise le nom de fichier pour la légende de l'icône.
    Shape shape = builder.InsertOleObjectAsIcon(stream, "PowerPoint.Application", ImageDir + "Logo icon.ico",
        "My embedded file stream");

    OlePackage setOlePackage = shape.OleFormat.OlePackage;
    setOlePackage.FileName = "Presentation.pptx";
    setOlePackage.DisplayName = "Presentation.pptx";
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjectAsIcon.docx");
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
