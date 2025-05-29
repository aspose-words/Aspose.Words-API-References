---
title: MailMerger.Execute
linktitle: Execute
articleTitle: Execute
second_title: Aspose.Words pour .NET
description: Optimisez votre flux de travail avec la méthode MailMerger Execute, en fusionnant sans effort les données pour des enregistrements uniques afin d'améliorer l'efficacité et la précision.
type: docs
weight: 20
url: /fr/net/aspose.words.lowcode/mailmerger/execute/
---
## Execute(*string, string, string[], object[]*) {#execute_14}

Effectue une opération de publipostage pour un seul enregistrement.

```csharp
public static void Execute(string inputFileName, string outputFileName, string[] fieldNames, 
    object[] fieldValues)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| fieldNames | String[] | Tableau de noms de champs de fusion. Les noms de champs ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |
| fieldValues | Object[] | Tableau de valeurs à insérer dans les champs de fusion. Le nombre d'éléments de ce tableau doit être identique à celui de fieldNames. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

## Exemples

Montre comment effectuer une opération de publipostage pour un seul enregistrement.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage :
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### Voir également

* class [MailMerger](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveFormat](../../../aspose.words/saveformat/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#execute_8}

Effectue une opération de publipostage pour un seul enregistrement.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde de la sortie. |
| fieldNames | String[] | Tableau de noms de champs de fusion. Les noms de champs ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |
| fieldValues | Object[] | Tableau de valeurs à insérer dans les champs de fusion. Le nombre d'éléments de ce tableau doit être identique à celui de fieldNames. |
| mailMergeOptions | MailMergeOptions | Options de publipostage. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

## Exemples

Montre comment effectuer une opération de publipostage pour un seul enregistrement.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage :
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#execute_11}

Effectue une opération de publipostage pour un seul enregistrement.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde de la sortie. |
| fieldNames | String[] | Tableau de noms de champs de fusion. Les noms de champs ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |
| fieldValues | Object[] | Tableau de valeurs à insérer dans les champs de fusion. Le nombre d'éléments de ce tableau doit être identique à celui de fieldNames. |
| mailMergeOptions | MailMergeOptions | Options de publipostage. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#execute_2}

Effectue une opération de publipostage pour un seul enregistrement.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux du fichier d'entrée. |
| outputStream | Stream | Le flux de fichiers de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde de la sortie. |
| fieldNames | String[] | Tableau de noms de champs de fusion. Les noms de champs ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |
| fieldValues | Object[] | Tableau de valeurs à insérer dans les champs de fusion. Le nombre d'éléments de ce tableau doit être identique à celui de fieldNames. |
| mailMergeOptions | MailMergeOptions | Options de publipostage. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images dans le flux spécifié.

## Exemples

Montre comment effectuer une opération de publipostage pour un seul enregistrement du flux.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage à l'aide de documents du flux :
string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Execute(streamIn, streamOut, SaveFormat.Docx, fieldNames, fieldValues);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
    {
        MailMergeOptions mailMergeOptions = new MailMergeOptions();
        mailMergeOptions.TrimWhitespaces = true;
        MailMerger.Execute(streamIn, streamOut, SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
    }
}
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#execute_5}

Effectue une opération de publipostage pour un seul enregistrement.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux du fichier d'entrée. |
| outputStream | Stream | Le flux de fichiers de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde de la sortie. |
| fieldNames | String[] | Tableau de noms de champs de fusion. Les noms de champs ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |
| fieldValues | Object[] | Tableau de valeurs à insérer dans les champs de fusion. Le nombre d'éléments de ce tableau doit être identique à celui de fieldNames. |
| mailMergeOptions | MailMergeOptions | Options de publipostage. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images dans le flux spécifié.

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Execute(*string, string, DataRow*) {#execute_12}

Effectue un publipostage à partir d'un DataRow dans le document.

```csharp
public static void Execute(string inputFileName, string outputFileName, DataRow dataRow)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| dataRow | DataRow | Ligne contenant les données à insérer dans les champs de publipostage. Les noms de champs ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

## Exemples

Montre comment effectuer une opération de publipostage à partir d'un DataRow.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage à partir d'un DataRow :
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataRow.1.docx", dataRow);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataRow.2.docx", SaveFormat.Docx, dataRow);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataRow.3.docx", SaveFormat.Docx, dataRow, new MailMergeOptions() { TrimWhitespaces = true });
```

### Voir également

* class [MailMerger](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveFormat](../../../aspose.words/saveformat/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_6}

Effectue un publipostage à partir d'un DataRow dans le document.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde de la sortie. |
| dataRow | DataRow | Ligne contenant les données à insérer dans les champs de publipostage. Les noms de champs ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |
| mailMergeOptions | MailMergeOptions | Options de publipostage. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

## Exemples

Montre comment effectuer une opération de publipostage à partir d'un DataRow.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage à partir d'un DataRow :
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataRow.1.docx", dataRow);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataRow.2.docx", SaveFormat.Docx, dataRow);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataRow.3.docx", SaveFormat.Docx, dataRow, new MailMergeOptions() { TrimWhitespaces = true });
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_9}

Effectue un publipostage à partir d'un DataRow dans le document.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde de la sortie. |
| dataRow | DataRow | Ligne contenant les données à insérer dans les champs de publipostage. Les noms de champs ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |
| mailMergeOptions | MailMergeOptions | Options de publipostage. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#execute}

Effectue une opération de publipostage pour un seul enregistrement.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux du fichier d'entrée. |
| outputStream | Stream | Le flux de fichiers de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde de la sortie. |
| dataRow | DataRow | Ligne contenant les données à insérer dans les champs de publipostage. Les noms de champs ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |
| mailMergeOptions | MailMergeOptions | Options de publipostage. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images dans le flux spécifié.

## Exemples

Montre comment effectuer une opération de publipostage à partir d'un DataRow en utilisant des documents du flux.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage à partir d'un DataRow en utilisant des documents du flux :
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStreamDataRow.1.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Execute(streamIn, streamOut, SaveFormat.Docx, dataRow);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStreamDataRow.2.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Execute(streamIn, streamOut, SaveFormat.Docx, dataRow, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_3}

Effectue une opération de publipostage pour un seul enregistrement.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux du fichier d'entrée. |
| outputStream | Stream | Le flux de fichiers de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde de la sortie. |
| dataRow | DataRow | Ligne contenant les données à insérer dans les champs de publipostage. Les noms de champs ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |
| mailMergeOptions | MailMergeOptions | Options de publipostage. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images dans le flux spécifié.

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Execute(*string, string, DataTable*) {#execute_13}

Effectue un publipostage à partir d'un DataTable vers le document.

```csharp
public static void Execute(string inputFileName, string outputFileName, DataTable dataTable)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| dataTable | DataTable | Tableau contenant les données à insérer dans les champs de publipostage. Les noms de champs ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

## Exemples

Montre comment effectuer une opération de publipostage à partir d'un DataTable.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage à partir d'une table de données :
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataTable.1.docx", dataTable);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataTable.2.docx", SaveFormat.Docx, dataTable);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataTable.3.docx", SaveFormat.Docx, dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### Voir également

* class [MailMerger](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveFormat](../../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_7}

Effectue un publipostage à partir d'un DataRow dans le document.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde de la sortie. |
| dataTable | DataTable | Tableau contenant les données à insérer dans les champs de publipostage. Les noms de champs ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |
| mailMergeOptions | MailMergeOptions | Options de publipostage. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

## Exemples

Montre comment effectuer une opération de publipostage à partir d'un DataTable.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage à partir d'une table de données :
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataTable.1.docx", dataTable);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataTable.2.docx", SaveFormat.Docx, dataTable);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataTable.3.docx", SaveFormat.Docx, dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_10}

Effectue un publipostage à partir d'un DataRow dans le document.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde de la sortie. |
| dataTable | DataTable | Tableau contenant les données à insérer dans les champs de publipostage. Les noms de champs ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |
| mailMergeOptions | MailMergeOptions | Options de publipostage. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_1}

Effectue une opération de publipostage pour un seul enregistrement.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux du fichier d'entrée. |
| outputStream | Stream | Le flux de fichiers de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde de la sortie. |
| dataTable | DataTable | Tableau contenant les données à insérer dans les champs de publipostage. Les noms de champs ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |
| mailMergeOptions | MailMergeOptions | Options de publipostage. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images dans le flux spécifié.

## Exemples

Montre comment effectuer une opération de publipostage à partir d'un DataTable à l'aide de documents du flux.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage à partir d'un DataTable en utilisant des documents du flux :
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeDataTable.1.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Execute(streamIn, streamOut, SaveFormat.Docx, dataTable);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeDataTable.2.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Execute(streamIn, streamOut, SaveFormat.Docx, dataTable, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_4}

Effectue une opération de publipostage pour un seul enregistrement.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux du fichier d'entrée. |
| outputStream | Stream | Le flux de fichiers de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde de la sortie. |
| dataTable | DataTable | Tableau contenant les données à insérer dans les champs de publipostage. Les noms de champs ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |
| mailMergeOptions | MailMergeOptions | Options de publipostage. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images dans le flux spécifié.

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
