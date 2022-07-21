---
title: InsertOleObject
second_title: Référence de l'API Aspose.Words pour .NET
description: Insère un objet OLE incorporé à partir dun flux dans le document.
type: docs
weight: 370
url: /fr/net/aspose.words/documentbuilder/insertoleobject/
---
## InsertOleObject(Stream, string, bool, Stream) {#insertoleobject}

Insère un objet OLE incorporé à partir d'un flux dans le document.

```csharp
public Shape InsertOleObject(Stream stream, string progId, bool asIcon, Stream presentation)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| stream | Stream | Flux contenant des données d'application. |
| progId | String | Identifiant programmatique de l'objet OLE. |
| asIcon | Boolean | Spécifie le mode iconique ou normal de l'objet OLE en cours d'insertion. |
| presentation | Stream | Présentation de l'image de l'objet OLE. Si la valeur est nulle, Aspose.Words utilisera l'une des images prédéfinies. |

### Return_Value

Nœud de forme contenant l'objet Ole et inséré à la position actuelle du générateur.

### Exemples

Montre comment utiliser le générateur de documents pour incorporer des objets OLE dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer une feuille de calcul Microsoft Excel à partir du système de fichiers local
// dans le document tout en gardant son apparence par défaut.
using (Stream spreadsheetStream = File.Open(MyDir + "Spreadsheet.xlsx", FileMode.Open))
{
    builder.Writeln("Spreadsheet Ole object:");
    // Si 'presentation' est omis et 'asIcon' est défini, cette méthode surchargée sélectionne
    // l'icône selon 'progId' et utilise la légende d'icône prédéfinie.
    builder.InsertOleObject(spreadsheetStream, "OleObject.xlsx", false, null);
}

// Insère une présentation Microsoft Powerpoint en tant qu'objet OLE.
// Cette fois, il aura une image téléchargée sur le Web pour une icône.
using (Stream powerpointStream = File.Open(MyDir + "Presentation.pptx", FileMode.Open))
{
    using (WebClient webClient = new WebClient())
    {
        byte[] imgBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

        using (MemoryStream imageStream = new MemoryStream(imgBytes))
        {
            builder.InsertParagraph();
            builder.Writeln("Powerpoint Ole object:");
            builder.InsertOleObject(powerpointStream, "OleObject.pptx", true, imageStream);
        }
    }
}

// Double-cliquez sur ces objets dans Microsoft Word pour ouvrir
// les fichiers liés en utilisant leurs applications respectives.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjects.docx");
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* espace de noms [Aspose.Words](../../documentbuilder)
* Assemblée [Aspose.Words](../../../)

---

## InsertOleObject(string, bool, bool, Stream) {#insertoleobject_1}

Insère un objet OLE incorporé ou lié à partir d'un fichier dans le document. Détecte le type d'objet OLE à l'aide de l'extension de fichier.

```csharp
public Shape InsertOleObject(string fileName, bool isLinked, bool asIcon, Stream presentation)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Chemin d'accès complet au fichier. |
| isLinked | Boolean | Si true, l'objet OLE lié est inséré, sinon l'objet OLE intégré est inséré. |
| asIcon | Boolean | Spécifie le mode iconique ou normal de l'objet OLE en cours d'insertion. |
| presentation | Stream | Présentation de l'image de l'objet OLE. Si la valeur est nulle, Aspose.Words utilisera l'une des images prédéfinies. |

### Return_Value

Nœud de forme contenant l'objet Ole et inséré à la position actuelle du générateur.

### Exemples

Montre comment insérer un objet OLE dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Les objets OLE sont des liens vers des fichiers de notre système de fichiers local qui peuvent être ouverts par d'autres applications installées.
// Double-cliquer sur ces formes lancera l'application, puis l'utilisera pour ouvrir l'objet lié.
// Il existe trois façons d'utiliser la méthode InsertOleObject pour insérer ces formes et configurer leur apparence.
// 1 - Image extraite du système de fichiers local :
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
// 3 - Icône d'image de 32 x 32 pixels ou moins du système de fichiers local, avec une légende personnalisée :
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* espace de noms [Aspose.Words](../../documentbuilder)
* Assemblée [Aspose.Words](../../../)

---

## InsertOleObject(string, string, bool, bool, Stream) {#insertoleobject_2}

Insère un objet OLE incorporé ou lié à partir d'un fichier dans le document. Détecte le type d'objet OLE à l'aide du paramètre progID donné.

```csharp
public Shape InsertOleObject(string fileName, string progId, bool isLinked, bool asIcon, 
    Stream presentation)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Chemin d'accès complet au fichier. |
| progId | String | ProgId de l'objet OLE. |
| isLinked | Boolean | Si true, l'objet OLE lié est inséré, sinon l'objet OLE intégré est inséré. |
| asIcon | Boolean | Spécifie le mode iconique ou normal de l'objet OLE en cours d'insertion. |
| presentation | Stream | Présentation de l'image de l'objet OLE. Si la valeur est nulle, Aspose.Words utilisera l'une des images prédéfinies. |

### Return_Value

Nœud de forme contenant l'objet Ole et inséré à la position actuelle du générateur.

### Exemples

Montre comment insérer un objet OLE dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Les objets OLE sont des liens vers des fichiers de notre système de fichiers local qui peuvent être ouverts par d'autres applications installées.
// Double-cliquer sur ces formes lancera l'application, puis l'utilisera pour ouvrir l'objet lié.
// Il existe trois façons d'utiliser la méthode InsertOleObject pour insérer ces formes et configurer leur apparence.
// 1 - Image extraite du système de fichiers local :
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
// 3 - Icône d'image de 32 x 32 pixels ou moins du système de fichiers local, avec une légende personnalisée :
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* espace de noms [Aspose.Words](../../documentbuilder)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
