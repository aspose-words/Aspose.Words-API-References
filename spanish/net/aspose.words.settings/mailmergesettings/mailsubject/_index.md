---
title: MailMergeSettings.MailSubject
linktitle: MailSubject
articleTitle: MailSubject
second_title: Aspose.Words para .NET
description: Personalice su MailMerge con la propiedad MailSubject para crear líneas de asunto atractivas para correos electrónicos o faxes. Mejore la comunicación con contenido personalizado.
type: docs
weight: 130
url: /es/net/aspose.words.settings/mailmergesettings/mailsubject/
---
## MailMergeSettings.MailSubject property

Especifica el texto que debe aparecer en la línea de asunto de los correos electrónicos o faxes producidos durante la combinación de correspondencia. El valor predeterminado es una cadena vacía.

```csharp
public string MailSubject { get; set; }
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
