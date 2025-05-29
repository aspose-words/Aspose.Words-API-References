---
title: MailMergerContext.SetSimpleDataSource
linktitle: SetSimpleDataSource
articleTitle: SetSimpleDataSource
second_title: Aspose.Words para .NET
description: Mejore la eficiencia de la combinación de correspondencia con el método MailMergerContext SetSimpleDataSource, que agiliza la configuración de la fuente de datos para una ejecución perfecta.
type: docs
weight: 40
url: /es/net/aspose.words.lowcode/mailmergercontext/setsimpledatasource/
---
## SetSimpleDataSource(*string[], object[]*) {#setsimpledatasource_2}

Establece la fuente de datos utilizada para ejecutar una combinación de correspondencia simple.

```csharp
public void SetSimpleDataSource(string[] fieldNames, object[] fieldValues)
```

## Observaciones

Si se especifican tanto la fuente de datos de combinación de correspondencia simple como la fuente de datos para la combinación de correspondencia con regiones, se ejecuta primero la combinación de correspondencia con regiones y luego se ejecuta la combinación de correspondencia simple.

## Ejemplos

Muestra cómo realizar una operación de combinación de correspondencia para un solo registro utilizando el contexto.

```csharp
// Hay varias formas de realizar la operación de combinación de correspondencia:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetSimpleDataSource(fieldNames, fieldValues);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContext.docx")
    .Execute();
```

Muestra cómo realizar una operación de combinación de correspondencia para un solo registro de la secuencia usando el contexto.

```csharp
// Hay varias formas de realizar la operación de combinación de correspondencia utilizando documentos del flujo:
string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetSimpleDataSource(fieldNames, fieldValues);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStream.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Ver también

* class [MailMergerContext](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## SetSimpleDataSource(*DataRow*) {#setsimpledatasource}

Establece la fuente de datos utilizada para ejecutar una combinación de correspondencia simple.

```csharp
public void SetSimpleDataSource(DataRow dataRow)
```

## Observaciones

Si se especifican tanto la fuente de datos de combinación de correspondencia simple como la fuente de datos para la combinación de correspondencia con regiones, se ejecuta primero la combinación de correspondencia con regiones y luego se ejecuta la combinación de correspondencia simple.

## Ejemplos

Muestra cómo realizar una operación de combinación de correspondencia desde un DataRow usando el contexto.

```csharp
// Hay varias formas de realizar la operación de combinación de correspondencia desde un DataRow:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetSimpleDataSource(dataRow);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContextDataRow.docx")
    .Execute();
```

Muestra cómo realizar una operación de combinación de correspondencia desde un DataRow utilizando documentos de la secuencia que utiliza el contexto.

```csharp
// Hay varias formas de realizar una operación de combinación de correspondencia desde un DataRow usando documentos del flujo:
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetSimpleDataSource(dataRow);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStreamDataRow.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Ver también

* class [MailMergerContext](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## SetSimpleDataSource(*DataTable*) {#setsimpledatasource_1}

Establece la fuente de datos utilizada para ejecutar una combinación de correspondencia simple.

```csharp
public void SetSimpleDataSource(DataTable dataTable)
```

## Observaciones

Si se especifican tanto la fuente de datos de combinación de correspondencia simple como la fuente de datos para la combinación de correspondencia con regiones, se ejecuta primero la combinación de correspondencia con regiones y luego se ejecuta la combinación de correspondencia simple.

## Ejemplos

Muestra cómo realizar una operación de combinación de correspondencia desde una DataTable utilizando el contexto.

```csharp
// Hay varias formas de realizar la operación de combinación de correspondencia desde una DataTable:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetSimpleDataSource(dataTable);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContextDataTable.docx")
    .Execute();
```

Muestra cómo realizar una operación de combinación de correspondencia desde una DataTable utilizando documentos de la secuencia que utiliza el contexto.

```csharp
// Hay varias formas de realizar la operación de combinación de correspondencia desde una DataTable utilizando documentos del flujo:
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetSimpleDataSource(dataTable);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStreamDataTable.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Ver también

* class [MailMergerContext](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
