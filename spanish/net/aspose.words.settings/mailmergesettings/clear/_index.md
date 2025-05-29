---
title: MailMergeSettings.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words para .NET
description: Restablezca sin esfuerzo su configuración de combinación de correspondencia con el método MailMergeSettings Clear, transformando su documento a un formato estándar para un uso sin inconvenientes.
type: docs
weight: 180
url: /es/net/aspose.words.settings/mailmergesettings/clear/
---
## MailMergeSettings.Clear method

Borra la configuración de combinación de correspondencia de tal manera que cuando se guarda el documento, no se guardará ninguna configuración de combinación de correspondencia y se convertirá en un documento normal.

```csharp
public void Clear()
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
