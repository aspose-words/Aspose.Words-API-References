---
title: OdsoRecipientData.Column
second_title: Referencia de API de Aspose.Words para .NET
description: OdsoRecipientData propiedad. Especifica la columna dentro de la fuente de datos que contiene datos únicos para el registro actual. El valor predeterminado es 0.
type: docs
weight: 30
url: /es/net/aspose.words.settings/odsorecipientdata/column/
---
## OdsoRecipientData.Column property

Especifica la columna dentro de la fuente de datos que contiene datos únicos para el registro actual. El valor predeterminado es 0.

```csharp
public int Column { get; set; }
```

### Ejemplos

Muestra cómo acceder a la colección de datos que designa qué registros de origen de datos de combinación excluirá una combinación de correspondencia.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

OdsoRecipientDataCollection dataCollection = doc.MailMergeSettings.Odso.RecipientDatas;

Assert.AreEqual(70, dataCollection.Count);

using (IEnumerator<OdsoRecipientData> enumerator = dataCollection.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine(
            $"Odso recipient data index {index++} will {(enumerator.Current.Active ? "" : "not ")}be imported upon mail merge.");
        Console.WriteLine($"\tColumn #{enumerator.Current.Column}");
        Console.WriteLine($"\tHash code: {enumerator.Current.Hash}");
        Console.WriteLine($"\tContents array length: {enumerator.Current.UniqueTag.Length}");
    }
}

// Podemos clonar los elementos de esta colección.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// También podemos eliminar elementos individualmente o borrar toda la colección a la vez.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Ver también

* class [OdsoRecipientData](../)
* espacio de nombres [Aspose.Words.Settings](../../odsorecipientdata/)
* asamblea [Aspose.Words](../../../)


