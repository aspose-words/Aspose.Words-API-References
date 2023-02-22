---
title: PlainTextDocument.PlainTextDocument
second_title: Référence de l'API Aspose.Words pour .NET
description: PlainTextDocument constructeur. Crée un document en texte brut à partir dun fichier. Détecte automatiquement le format de fichier.
type: docs
weight: 10
url: /fr/net/aspose.words/plaintextdocument/plaintextdocument/
---
## PlainTextDocument(string) {#constructor_2}

Crée un document en texte brut à partir d'un fichier. Détecte automatiquement le format de fichier.

```csharp
public PlainTextDocument(string fileName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Nom du fichier à partir duquel extraire le texte. |

### Exceptions

| exception | condition |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Le format du document n'est pas reconnu ou n'est pas pris en charge. |
| [FileCorruptedException](../../filecorruptedexception/) | Le document semble être corrompu et ne peut pas être chargé. |
| Exception | Il y a un problème avec le document et il doit être signalé aux développeurs Aspose.Words. |
| IOException | Il y a une exception d'entrée/sortie. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Le document est crypté et nécessite un mot de passe pour s'ouvrir, mais vous avez fourni un mot de passe incorrect. |
| ArgumentException | Le nom du fichier ne peut pas être nul ou une chaîne vide. |

### Exemples

Montre comment charger le contenu d'un document Microsoft Word en texte brut.

```csharp
Document doc = new Document(); 
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PlainTextDocument.Load.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.Load.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### Voir également

* class [PlainTextDocument](../)
* espace de noms [Aspose.Words](../../plaintextdocument/)
* Assemblée [Aspose.Words](../../../)

---

## PlainTextDocument(string, LoadOptions) {#constructor_3}

Crée un document en texte brut à partir d'un fichier. Permet de spécifier des options supplémentaires telles qu'un mot de passe de chiffrement.

```csharp
public PlainTextDocument(string fileName, LoadOptions loadOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Nom du fichier à partir duquel extraire le texte. |
| loadOptions | LoadOptions | Options supplémentaires à utiliser lors du chargement d'un document. Peut être nul. |

### Exceptions

| exception | condition |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Le format du document n'est pas reconnu ou n'est pas pris en charge. |
| [FileCorruptedException](../../filecorruptedexception/) | Le document semble être corrompu et ne peut pas être chargé. |
| Exception | Il y a un problème avec le document et il doit être signalé aux développeurs Aspose.Words. |
| IOException | Il y a une exception d'entrée/sortie. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Le document est crypté et nécessite un mot de passe pour s'ouvrir, mais vous avez fourni un mot de passe incorrect. |
| ArgumentException | Le nom du fichier ne peut pas être nul ou une chaîne vide. |

### Exemples

Montre comment charger le contenu d'un document Microsoft Word chiffré en texte clair.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "PlainTextDocument.LoadEncrypted.docx", saveOptions);

LoadOptions loadOptions = new LoadOptions();
loadOptions.Password = "MyPassword";

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.LoadEncrypted.docx", loadOptions);

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### Voir également

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [PlainTextDocument](../)
* espace de noms [Aspose.Words](../../plaintextdocument/)
* Assemblée [Aspose.Words](../../../)

---

## PlainTextDocument(Stream) {#constructor}

Crée un document en texte brut à partir d'un flux. Détecte automatiquement le format de fichier.

```csharp
public PlainTextDocument(Stream stream)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| stream | Stream | Le flux d'où extraire le texte. |

### Exceptions

| exception | condition |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Le format du document n'est pas reconnu ou n'est pas pris en charge. |
| [FileCorruptedException](../../filecorruptedexception/) | Le document semble être corrompu et ne peut pas être chargé. |
| Exception | Il y a un problème avec le document et il doit être signalé aux développeurs Aspose.Words. |
| IOException | Il y a une exception d'entrée/sortie. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Le document est crypté et nécessite un mot de passe pour s'ouvrir, mais vous avez fourni un mot de passe incorrect. |
| ArgumentNullException | Le flux ne peut pas être nul. |
| NotSupportedException | Le flux ne prend pas en charge la lecture ou la recherche. |
| ObjectDisposedException | Le flux est un objet disposé. |

### Remarques

Le document doit être stocké au début du flux. Le flux doit prendre en charge le positionnement aléatoire.

### Exemples

Montre comment charger le contenu d'un document Microsoft Word en texte brut à l'aide de stream.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
doc.Save(ArtifactsDir + "PlainTextDocument.LoadFromStream.docx");

using (FileStream stream = new FileStream(ArtifactsDir + "PlainTextDocument.LoadFromStream.docx", FileMode.Open))
{
    PlainTextDocument plaintext = new PlainTextDocument(stream);

    Assert.AreEqual("Hello world!", plaintext.Text.Trim());
}
```

### Voir également

* class [PlainTextDocument](../)
* espace de noms [Aspose.Words](../../plaintextdocument/)
* Assemblée [Aspose.Words](../../../)

---

## PlainTextDocument(Stream, LoadOptions) {#constructor_1}

Crée un document en texte brut à partir d'un flux. Permet de spécifier des options supplémentaires telles qu'un mot de passe de chiffrement.

```csharp
public PlainTextDocument(Stream stream, LoadOptions loadOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| stream | Stream | Le flux d'où extraire le texte. |
| loadOptions | LoadOptions | Options supplémentaires à utiliser lors du chargement d'un document. Peut être nul. |

### Exceptions

| exception | condition |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Le format du document n'est pas reconnu ou n'est pas pris en charge. |
| [FileCorruptedException](../../filecorruptedexception/) | Le document semble être corrompu et ne peut pas être chargé. |
| Exception | Il y a un problème avec le document et il doit être signalé aux développeurs Aspose.Words. |
| IOException | Il y a une exception d'entrée/sortie. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Le document est crypté et nécessite un mot de passe pour s'ouvrir, mais vous avez fourni un mot de passe incorrect. |
| ArgumentNullException | Le flux ne peut pas être nul. |
| NotSupportedException | Le flux ne prend pas en charge la lecture ou la recherche. |
| ObjectDisposedException | Le flux est un objet disposé. |

### Remarques

Le document doit être stocké au début du flux. Le flux doit prendre en charge le positionnement aléatoire.

### Exemples

Montre comment charger le contenu d'un document Microsoft Word chiffré en texte brut à l'aide de stream.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "PlainTextDocument.LoadFromStreamWithOptions.docx", saveOptions);

LoadOptions loadOptions = new LoadOptions();
loadOptions.Password = "MyPassword";

using (FileStream stream = new FileStream(ArtifactsDir + "PlainTextDocument.LoadFromStreamWithOptions.docx", FileMode.Open))
{
    PlainTextDocument plaintext = new PlainTextDocument(stream, loadOptions);

    Assert.AreEqual("Hello world!", plaintext.Text.Trim());
}
```

### Voir également

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [PlainTextDocument](../)
* espace de noms [Aspose.Words](../../plaintextdocument/)
* Assemblée [Aspose.Words](../../../)


