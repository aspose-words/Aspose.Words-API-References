---
title: IMailMergeCallback.TagsReplaced
second_title: Referencia de API de Aspose.Words para .NET
description: IMailMergeCallback método. Llamado cuando las etiquetas de texto bigote se reemplazan con campos MERGEFIELD.
type: docs
weight: 10
url: /es/net/aspose.words.mailmerging/imailmergecallback/tagsreplaced/
---
## IMailMergeCallback.TagsReplaced method

Llamado cuando las etiquetas de texto "bigote" se reemplazan con campos MERGEFIELD.

```csharp
public void TagsReplaced()
```

### Ejemplos

Muestra cómo definir una lógica personalizada para manejar eventos durante la combinación de correspondencia.

```csharp
public void Callback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Insertar dos etiquetas de combinación de correspondencia que hagan referencia a dos columnas en una fuente de datos.
    builder.Write("{{FirstName}}");
    builder.Write("{{LastName}}");

    // Cree una fuente de datos que solo contenga una de las columnas a las que hacen referencia nuestras etiquetas de fusión.
    DataTable table = new DataTable("Test");
    table.Columns.Add("FirstName");
    table.Rows.Add("John");
    table.Rows.Add("Jane");

    // Configure nuestra combinación de correspondencia para usar etiquetas de combinación de correspondencia alternativas.
    doc.MailMerge.UseNonMergeFields = true;

    // Luego, asegúrese de que la combinación de correspondencia convierta etiquetas, como nuestra etiqueta "Apellido",
    // en MERGEFIELDs en los documentos combinados.
    doc.MailMerge.PreserveUnusedTags = false;

    MailMergeTagReplacementCounter counter = new MailMergeTagReplacementCounter();
    doc.MailMerge.MailMergeCallback = counter;
    doc.MailMerge.Execute(table);

    Assert.AreEqual(1, counter.TagsReplacedCount);
}

/// <summary>
/// Cuenta el número de veces que una combinación de correspondencia reemplaza etiquetas de combinación de correspondencia que no pudo llenar con datos con MERGEFIELDs.
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

* property [UseNonMergeFields](../../mailmerge/usenonmergefields/)
* interface [IMailMergeCallback](../)
* espacio de nombres [Aspose.Words.MailMerging](../../imailmergecallback/)
* asamblea [Aspose.Words](../../../)


