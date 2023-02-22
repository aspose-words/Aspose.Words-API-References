---
title: Enum CompressionLevel
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.CompressionLevel énumération. Niveau de compression des fichiers OOXML.
type: docs
weight: 4610
url: /fr/net/aspose.words.saving/compressionlevel/
---
## CompressionLevel enumeration

Niveau de compression des fichiers OOXML.

(les fichiers DOCX et DOTX sont en interne une archive ZIP, cette propriété contrôle le niveau de compression de l'archive.

Notez que le fichier FlatOpc n'est pas une archive ZIP, par conséquent, cette propriété n'affecte pas les fichiers FlatOpc.)

```csharp
public enum CompressionLevel
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Normal | `0` | Niveau de compression normal. Niveau de compression par défaut utilisé par Aspose.Words. |
| Maximum | `1` | Niveau de compression maximal. |
| Fast | `2` | Niveau de compression rapide. |
| SuperFast | `3` | Niveau de compression ultra rapide. Microsoft Word utilise ce niveau de compression. |

### Exemples

Montre comment spécifier le niveau de compression à utiliser lors de l'enregistrement d'un document OOXML.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Lorsque nous enregistrons le document au format OOXML, nous pouvons créer un objet OoxmlSaveOptions
// puis passez-le à la méthode d'enregistrement du document pour modifier la façon dont nous enregistrons le document.
// Définissez la propriété "CompressionLevel" sur "CompressionLevel.Maximum" pour appliquer la compression la plus forte et la plus lente.
// Définissez la propriété "CompressionLevel" sur "CompressionLevel.Normal" à appliquer
// la compression par défaut utilisée par Aspose.Words lors de l'enregistrement des documents OOXML.
// Définissez la propriété "CompressionLevel" sur "CompressionLevel.Fast" pour appliquer une compression plus rapide et plus faible.
// Définissez la propriété "CompressionLevel" sur "CompressionLevel.SuperFast" à appliquer
// la compression par défaut utilisée par Microsoft Word.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.CompressionLevel = compressionLevel;

Stopwatch st = Stopwatch.StartNew();
doc.Save(ArtifactsDir + "OoxmlSaveOptions.DocumentCompression.docx", saveOptions);
st.Stop();

FileInfo fileInfo = new FileInfo(ArtifactsDir + "OoxmlSaveOptions.DocumentCompression.docx");

Console.WriteLine($"Saving operation done using the \"{compressionLevel}\" compression level:");
Console.WriteLine($"\tDuration:\t{st.ElapsedMilliseconds} ms");
Console.WriteLine($"\tFile Size:\t{fileInfo.Length} bytes");
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)


