---
title: MailMergeSettings.MailAsAttachment
linktitle: MailAsAttachment
articleTitle: MailAsAttachment
second_title: Aspose.Words pour .NET
description: MailMergeSettings MailAsAttachment propriété. Spécifie que les documents produits lors dune opération de fusion et publipostage doivent être envoyés par courrier électronique sous forme de pièce jointe plutôt que et non comme corps de lemail luimême. La valeur par défaut estFAUX  en C#.
type: docs
weight: 120
url: /fr/net/aspose.words.settings/mailmergesettings/mailasattachment/
---
## MailMergeSettings.MailAsAttachment property

Spécifie que les documents produits lors d'une opération de fusion et publipostage doivent être envoyés par courrier électronique sous forme de pièce jointe plutôt que et non comme corps de l'e-mail lui-même. La valeur par défaut est`FAUX` .

```csharp
public bool MailAsAttachment { get; set; }
```

## Exemples

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
* espace de noms [Aspose.Words.Settings](../../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../../)
