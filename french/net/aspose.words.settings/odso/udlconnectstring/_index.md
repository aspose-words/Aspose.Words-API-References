---
title: Odso.UdlConnectString
linktitle: UdlConnectString
articleTitle: UdlConnectString
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Odso UdlConnectString pour des connexions fluides aux sources de données externes grâce à UDL. Intégrez vos données facilement et efficacement !
type: docs
weight: 90
url: /fr/net/aspose.words.settings/odso/udlconnectstring/
---
## Odso.UdlConnectString property

Spécifie la chaîne de connexion Universal Data Link (UDL) utilisée pour se connecter à une source de données externe. La valeur par défaut est une chaîne vide.

```csharp
public string UdlConnectString { get; set; }
```

## Exemples

Montre comment exécuter un publipostage tout en se connectant à une source de données externe.

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

// Nous pouvons réinitialiser ces paramètres en les effaçant. Une fois cette opération effectuée et le document enregistré,
// Microsoft Word n'exécutera plus de publipostage lorsque nous l'utiliserons pour charger le document.
settings.Clear();

doc.Save(ArtifactsDir + "MailMerge.OdsoEmail.docx");
```

### Voir également

* class [Odso](../)
* espace de noms [Aspose.Words.Settings](../../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../../)
