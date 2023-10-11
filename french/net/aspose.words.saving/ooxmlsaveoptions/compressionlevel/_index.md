---
title: OoxmlSaveOptions.CompressionLevel
second_title: Référence de l'API Aspose.Words pour .NET
description: OoxmlSaveOptions propriété. Spécifie le niveau de compression utilisé pour enregistrer le document. La valeur par défaut estNormal .
type: docs
weight: 30
url: /fr/net/aspose.words.saving/ooxmlsaveoptions/compressionlevel/
---
## OoxmlSaveOptions.CompressionLevel property

Spécifie le niveau de compression utilisé pour enregistrer le document. La valeur par défaut estNormal .

```csharp
public CompressionLevel CompressionLevel { get; set; }
```

### Exemples

Montre comment spécifier le niveau de compression à utiliser lors de l'enregistrement d'un document OOXML.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Lorsque nous enregistrons le document au format OOXML, nous pouvons créer un objet OoxmlSaveOptions
// puis transmettez-le à la méthode de sauvegarde du document pour modifier la façon dont nous enregistrons le document.
// Définissez la propriété "CompressionLevel" sur "CompressionLevel.Maximum" pour appliquer la compression la plus forte et la plus lente.
// Définissez la propriété "CompressionLevel" sur "CompressionLevel.Normal" pour appliquer
// la compression par défaut utilisée par Aspose.Words lors de l'enregistrement des documents OOXML.
// Définissez la propriété "CompressionLevel" sur "CompressionLevel.Fast" pour appliquer une compression plus rapide et plus faible.
// Définissez la propriété "CompressionLevel" sur "CompressionLevel.SuperFast" pour appliquer
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

* enum [CompressionLevel](../../compressionlevel/)
* class [OoxmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../ooxmlsaveoptions/)
* Assemblée [Aspose.Words](../../../)


