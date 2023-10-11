---
title: MailMergeSettings.Clear
second_title: Référence de l'API Aspose.Words pour .NET
description: MailMergeSettings méthode. Efface les paramètres de publipostage de telle manière que lorsque le document est enregistré aucun paramètre de publipostage ne sera enregistré et il deviendra un document normal.
type: docs
weight: 180
url: /fr/net/aspose.words.settings/mailmergesettings/clear/
---
## MailMergeSettings.Clear method

Efface les paramètres de publipostage de telle manière que lorsque le document est enregistré, aucun paramètre de publipostage ne sera enregistré et il deviendra un document normal.

```csharp
public void Clear()
```

### Exemples

Montre comment exécuter un publipostage lors de la connexion à une source de données externe.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");
MailMergeSettings settings = doc.MailMergeSettings;

Console.WriteLine($"Connection string:\n\t{settings.ConnectString}");
Console.WriteLine($"Mail merge docs as attachment:\n\t{settings.MailAsAttachment}");
Console.WriteLine($"Mail merge doc e-mail subject:\n\t{settings.MailSubject}");
Console.WriteLine($"Column that contains e-mail addresses:\n\t{settings.AddressFieldName}");
Console.WriteLine($"Active record:\n\t{settings.ActiveRecord}");

Odso odso = settings.Odso;

Console.WriteLine($"File will connect to data source located in:\n\t\"{odso.DataSource}\"");
Console.WriteLine($"Source type:\n\t{odso.DataSourceType}");
Console.WriteLine($"UDL connection string:\n\t{odso.UdlConnectString}");
Console.WriteLine($"Table:\n\t{odso.TableName}");
Console.WriteLine($"Query:\n\t{doc.MailMergeSettings.Query}");

// Nous pouvons réinitialiser ces paramètres en les effaçant. Une fois que nous avons fait cela et enregistré le document,
// Microsoft Word n'exécutera plus de publipostage lorsque nous l'utiliserons pour charger le document.
settings.Clear();

doc.Save(ArtifactsDir + "MailMerge.OdsoEmail.docx");
```

### Voir également

* class [MailMergeSettings](../)
* espace de noms [Aspose.Words.Settings](../../mailmergesettings/)
* Assemblée [Aspose.Words](../../../)


