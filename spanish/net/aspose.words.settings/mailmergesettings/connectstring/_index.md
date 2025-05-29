---
title: MailMergeSettings.ConnectString
linktitle: ConnectString
articleTitle: ConnectString
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad ConnectString de MailMergeSettings se vincula con fuentes de datos externas. ¡Personalice fácilmente su conexión para una integración de datos fluida!
type: docs
weight: 50
url: /es/net/aspose.words.settings/mailmergesettings/connectstring/
---
## MailMergeSettings.ConnectString property

Especifica la cadena de conexión utilizada para conectarse a una fuente de datos externa. El valor predeterminado es una cadena vacía.

```csharp
public string ConnectString { get; set; }
```

## Ejemplos

Muestra cómo ejecutar una combinación de correspondencia mientras se conecta a una fuente de datos externa.

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

Podemos restablecer esta configuración borrándola. Una vez hecho esto y guardado el documento,
//Microsoft Word ya no ejecutará una combinación de correspondencia cuando lo usemos para cargar el documento.
settings.Clear();

doc.Save(ArtifactsDir + "MailMerge.OdsoEmail.docx");
```

### Ver también

* class [MailMergeSettings](../)
* espacio de nombres [Aspose.Words.Settings](../../../aspose.words.settings/)
* asamblea [Aspose.Words](../../../)
