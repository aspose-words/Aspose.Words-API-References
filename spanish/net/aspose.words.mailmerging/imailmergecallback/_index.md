---
title: Interface IMailMergeCallback
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.MailMerging.IMailMergeCallback interfaz. Implemente esta interfaz si desea recibir notificaciones mientras se realiza la combinación de correspondencia.
type: docs
weight: 3800
url: /es/net/aspose.words.mailmerging/imailmergecallback/
---
## IMailMergeCallback interface

Implemente esta interfaz si desea recibir notificaciones mientras se realiza la combinación de correspondencia.

```csharp
public interface IMailMergeCallback
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| [TagsReplaced](../../aspose.words.mailmerging/imailmergecallback/tagsreplaced/)() | Se llama cuando las etiquetas de texto "bigote" se reemplazan con campos MERGEFIELD. |

### Ejemplos

Muestra cómo definir una lógica personalizada para manejar eventos durante la combinación de correspondencia.

```csharp
public void Callback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Inserte dos etiquetas de combinación de correspondencia que hagan referencia a dos columnas en una fuente de datos.
    builder.Write("{{FirstName}}");
    builder.Write("{{LastName}}");

    // Cree una fuente de datos que solo contenga una de las columnas a las que hacen referencia nuestras etiquetas de combinación.
    DataTable table = new DataTable("Test");
    table.Columns.Add("FirstName");
    table.Rows.Add("John");
    table.Rows.Add("Jane");

    // Configurar nuestra combinación de correspondencia para utilizar etiquetas de combinación de correspondencia alternativas.
    doc.MailMerge.UseNonMergeFields = true;

    // Luego, asegúrese de que la combinación de correspondencia convierta etiquetas, como nuestra etiqueta "Apellido",
    // en MERGEFIELD en los documentos de combinación.
    doc.MailMerge.PreserveUnusedTags = false;

    MailMergeTagReplacementCounter counter = new MailMergeTagReplacementCounter();
    doc.MailMerge.MailMergeCallback = counter;
    doc.MailMerge.Execute(table);

    Assert.AreEqual(1, counter.TagsReplacedCount);
}

/// <summary>
/// Cuenta el número de veces que una combinación de correspondencia reemplaza etiquetas de combinación de correspondencia que no pudo llenar con datos con MERGEFIELD.
/// </summary>
private class MailMergeTagReplacementCounter : IMailMergeCallback
{
    public void TagsReplaced()
    {
        TagsReplacedCount++;
    }

    public int TagsReplacedCount { get; private set; }
}
```

### Ver también

* espacio de nombres [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../)


