---
title: MailMerger.ExecuteToImages
linktitle: ExecuteToImages
articleTitle: ExecuteToImages
second_title: Aspose.Words pour .NET
description: Effectuez sans effort un publipostage pour des enregistrements individuels et convertissez les résultats en images de haute qualité avec la méthode MailMerger ExecuteToImages.
type: docs
weight: 30
url: /fr/net/aspose.words.lowcode/mailmerger/executetoimages/
---
## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_5}

Effectue une opération de publipostage pour un seul enregistrement et restitue le résultat sous forme d'images.

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| saveOptions | ImageSaveOptions | Les options de sauvegarde de la sortie. |
| fieldNames | String[] | Tableau de noms de champs de fusion. Les noms de champs ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |
| fieldValues | Object[] | Tableau de valeurs à insérer dans les champs de fusion. Le nombre d'éléments de ce tableau doit être identique à celui de fieldNames. |
| mailMergeOptions | MailMergeOptions | Options de publipostage. |

## Exemples

Montre comment effectuer une opération de publipostage pour un seul enregistrement et enregistrer le résultat dans des images.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage :
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues, mailMergeOptions);
```

### Voir également

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_2}

Effectue une opération de publipostage pour un seul enregistrement et restitue le résultat sous forme d'images.

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux du fichier d'entrée. |
| saveOptions | ImageSaveOptions | Les options de sauvegarde de la sortie. |
| fieldNames | String[] | Tableau de noms de champs de fusion. Les noms de champs ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |
| fieldValues | Object[] | Tableau de valeurs à insérer dans les champs de fusion. Le nombre d'éléments de ce tableau doit être identique à celui de fieldNames. |
| mailMergeOptions | MailMergeOptions | Options de publipostage. |

## Exemples

Montre comment effectuer une opération de fusion et de publipostage pour un seul enregistrement du flux et enregistrer le résultat dans des images.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage à l'aide de documents du flux :
string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    Stream[] images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues);

    MailMergeOptions mailMergeOptions = new MailMergeOptions();
    mailMergeOptions.TrimWhitespaces = true;
    images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues, mailMergeOptions);
}
```

### Voir également

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_3}

Effectue un publipostage à partir d'un DataRow dans le document et restitue le résultat sous forme d'images.

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| saveOptions | ImageSaveOptions | Les options de sauvegarde de la sortie. |
| dataRow | DataRow | Ligne contenant les données à insérer dans les champs de publipostage. Les noms de champs ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |
| mailMergeOptions | MailMergeOptions | Options de publipostage. |

## Exemples

Montre comment effectuer une opération de publipostage à partir d'un DataRow et enregistrer le résultat dans des images.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage à partir d'un DataRow :
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataRow);
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataRow, new MailMergeOptions() { TrimWhitespaces = true });
```

### Voir également

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages}

Effectue un publipostage à partir d'un DataRow dans le document et restitue le résultat sous forme d'images.

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux du fichier d'entrée. |
| saveOptions | ImageSaveOptions | Les options de sauvegarde de la sortie. |
| dataRow | DataRow | Ligne contenant les données à insérer dans les champs de publipostage. Les noms de champs ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |
| mailMergeOptions | MailMergeOptions | Options de publipostage. |

## Exemples

Montre comment effectuer une opération de publipostage à partir d'un DataRow à l'aide de documents du flux et enregistrer le résultat dans des images.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage à partir d'un DataRow en utilisant des documents du flux :
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    Stream[] images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataRow);
    images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataRow, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### Voir également

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_4}

Effectue un publipostage à partir d'un DataRow dans le document et restitue le résultat sous forme d'images.

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| saveOptions | ImageSaveOptions | Les options de sauvegarde de la sortie. |
| dataTable | DataTable | Tableau contenant les données à insérer dans les champs de publipostage. Les noms de champs ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |
| mailMergeOptions | MailMergeOptions | Options de publipostage. |

## Exemples

Montre comment effectuer une opération de publipostage à partir d'un DataTable et enregistrer le résultat dans des images.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage à partir d'une table de données :
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable);
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### Voir également

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_1}

Effectue un publipostage à partir d'un DataRow dans le document et restitue le résultat sous forme d'images.

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux du fichier d'entrée. |
| saveOptions | ImageSaveOptions | Les options de sauvegarde de la sortie. |
| dataTable | DataTable | Tableau contenant les données à insérer dans les champs de publipostage. Les noms de champs ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |
| mailMergeOptions | MailMergeOptions | Options de publipostage. |

## Exemples

Montre comment effectuer une opération de publipostage à partir d'un DataTable à l'aide de documents du flux et enregistrer dans des images.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage à partir d'un DataTable en utilisant des documents du flux et en enregistrant le résultat dans des images :
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    Stream[] images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataTable);
    images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataTable, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### Voir également

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
